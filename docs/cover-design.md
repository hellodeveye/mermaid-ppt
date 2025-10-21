# 封面背景设计说明

## 📸 图片组成

演示文稿的封面使用了三张图片的组合效果：

### 图片文件
- `cover_top.png` - 上半部分背景图（工业设备场景）
- `cover_bottom.png` - 下半部分背景图（盐场储存场景）
- ~~`cover_overlay.png`~~ - 已改用纯CSS蒙层（rgba(26, 32, 44, 0.75)）

### 图片布局

```
┌─────────────────────────────────┐
│                                 │
│   cover_top.png (上半部分)       │  ← 上半部分
│                                 │
├─────────────────────────────────┤
│                                 │
│   cover_bottom.png (下半部分)    │  ← 下半部分
│                                 │
└─────────────────────────────────┘
        ↓ 叠加CSS蒙层
┌─────────────────────────────────┐
│                                 │
│   深蓝灰色半透明 (CSS)           │  ← 纯CSS蒙层，100%覆盖
│   rgba(26, 32, 44, 0.75)        │
│                                 │
└─────────────────────────────────┘
        ↓ 最上层
┌─────────────────────────────────┐
│                                 │
│    AI × Mermaid 文字内容         │  ← z-index: 3
│                                 │
└─────────────────────────────────┘
```

## 🎨 层叠关系 (Z-Index)

1. **Z-Index 1**: 背景图片容器
   - `cover_top.png`：上半部分（0-50%高度）
   - `cover_bottom.png`：下半部分（50%-100%高度）

2. **Z-Index 2**: CSS 蒙层 ✨
   - 纯 CSS 半透明层：`rgba(26, 32, 44, 0.75)`
   - 优势：100% 覆盖，无图片尺寸问题

3. **Z-Index 3**: 文字内容
   - 标题、副标题、元信息

## 🔧 CSS 实现

### 关键样式类

```css
/* 全屏封面容器 */
.cover-slide-with-bg {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;    /* 视口宽度 */
    height: 100vh;   /* 视口高度 */
    margin: 0;
    padding: 0;
    overflow: hidden;
}

.cover-bg-container {
    position: absolute;
    z-index: 1;  /* 最底层 */
}

.cover-overlay {
    position: absolute;
    z-index: 2;  /* 蒙层 */
}

.cover-content {
    position: relative;
    z-index: 3;  /* 文字最上层 */
}

/* 白色标题，增强阴影 */
.cover-title {
    color: #ffffff !important;
    text-shadow: 3px 3px 12px rgba(0,0,0,0.8), 
                 0 0 30px rgba(0,0,0,0.5);
}

.cover-subtitle, .cover-meta {
    color: #ffffff !important;
    text-shadow: 2px 2px 8px rgba(0,0,0,0.8);
}
```

## 📝 HTML 结构

```html
<section>
    <div class="cover-slide-with-bg">
        <!-- 背景图片 -->
        <div class="cover-bg-container">
            <div class="cover-bg-top" style="background-image: url('cover_top.png');"></div>
            <div class="cover-bg-bottom" style="background-image: url('cover_bottom.png');"></div>
            <!-- CSS蒙层，不使用图片 -->
            <div class="cover-overlay"></div>
        </div>
        
        <!-- 文字内容 -->
        <div class="cover-content">
            <h1>AI × Mermaid</h1>
            <p>智能图表生成的革命性突破</p>
        </div>
    </div>
</section>
```

## 🎯 设计特点

### 1. 全屏展示 ✨
- **100vw × 100vh**：完全填充整个视口
- **position: fixed**：固定定位，不受滚动影响
- **无边距无内边距**：真正的全屏效果
- **覆盖RevealJS默认样式**：使用 `!important` 确保全屏

### 2. 分层背景
- **上半部分**：展示工业设备、技术感
- **下半部分**：展示产品储存、规模感
- 两张图片无缝拼接，各占50%高度

### 3. 蒙层效果
- 深蓝色半透明蒙层增强文字可读性
- 统一视觉风格，与主题色协调
- 营造专业、科技的氛围

### 4. 白色文字优化 ✨
- **纯白色** `#ffffff !important` 确保最高对比度
- **双层阴影效果**：
  - 主阴影：`3px 3px 12px rgba(0,0,0,0.8)` - 增强立体感
  - 光晕效果：`0 0 30px rgba(0,0,0,0.5)` - 提升可读性
- **图标也是白色**：统一视觉风格
- **在任何背景上都清晰可见**

## 🔄 更换图片

如需更换封面背景图片，请按以下步骤操作：

### 方法1: 替换文件
1. 准备新的图片文件
2. 重命名为 `cover_top.png`、`cover_bottom.png`
3. 放在与 `index.html` 相同的目录
4. 刷新浏览器即可看到新背景

### 方法2: 修改代码
在 `index.html` 中找到封面部分（约第908行）：

```html
<!-- 修改这些 url() 中的路径 -->
<div class="cover-bg-top" style="background-image: url('your_top_image.png');"></div>
<div class="cover-bg-bottom" style="background-image: url('your_bottom_image.png');"></div>
<!-- 蒙层已改用CSS，不需要图片 -->
```

### 方法3: 修改蒙层颜色
在 `index.html` 中找到 CSS 部分（约第232行）：

```css
.cover-overlay {
    /* 修改颜色和透明度 */
    background: rgba(26, 32, 44, 0.75);
    /* rgba(红, 绿, 蓝, 透明度) */
}
```

## 💡 优化建议

### 图片尺寸建议
- **推荐分辨率**: 1920x1080 (Full HD) 或更高
- **文件格式**: PNG（支持透明度）或 JPG
- **文件大小**: 建议每张图片 < 500KB，优化加载速度

### 图片内容建议
- **上半部分图片**：适合横向构图，重点在画面中上部
- **下半部分图片**：适合横向构图，重点在画面中下部
- **蒙层图片**：纯色或渐变，透明度30-60%为佳

### 响应式考虑
当前配置已支持响应式，在不同屏幕尺寸下：
- 图片自动缩放适配
- 保持宽高比
- 文字始终居中显示

## 🎨 视觉效果

### 当前效果
- ✅ 工业场景 + 产品场景的双重展示
- ✅ 深蓝色蒙层统一色调
- ✅ 白色文字清晰可见
- ✅ 动画效果流畅自然

### 设计理念
通过实景图片展现：
1. **技术实力**：工业设备体现技术能力
2. **业务规模**：产品储存展示规模优势
3. **专业形象**：蒙层和配色营造专业感

## 🚀 使用提示

1. **图片位置**: 确保图片与 `index.html` 文件在同一目录
2. **命名规范**: 使用清晰的文件名（`cover_*.png`）便于管理
3. **路径检查**: 如果图片不显示，检查浏览器控制台是否有路径错误
4. **缓存问题**: 如果更换图片后未生效，清除浏览器缓存或强制刷新 (`Cmd+Shift+R` / `Ctrl+F5`)
5. **性能优化**: 建议压缩图片以提高加载速度

## 📂 文件结构

```
mermaid-ppt/
├── index.html              # 主演示文稿
├── cover_top.png           # 封面上半部分背景
├── cover_bottom.png        # 封面下半部分背景
├── README.md               # 项目说明
└── docs/                   # 详细文档
    ├── cover-design.md     # 封面设计说明（本文件）
    └── color-scheme.md     # 配色方案
```

---

**最后更新**: 2025年10月21日  
**版本**: v2.0

