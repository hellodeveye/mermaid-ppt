# AI × Mermaid 演示文稿

一个现代化的 HTML 演示文稿，展示 AI 与 Mermaid 图表的完美结合。

![Version](https://img.shields.io/badge/version-2.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ 特性

- 🎨 **现代设计** - 精美的渐变色彩和卡片式布局
- 📊 **丰富图表** - 内置 30+ Mermaid 图表示例
- 🎬 **流畅动画** - 精心设计的过渡效果
- 📱 **完全响应式** - 适配各种屏幕尺寸
- 🚀 **开箱即用** - 单一 HTML 文件，无需构建

## 🚀 快速开始

### 方法 1: 直接打开
```bash
# 在浏览器中打开
open index.html
```

### 方法 2: 本地服务器
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (需要安装 http-server)
npx http-server
```

然后访问 `http://localhost:8000`

## ⌨️ 快捷键

| 按键 | 功能 |
|------|------|
| `→` `Space` | 下一页 |
| `←` | 上一页 |
| `Esc` `O` | 总览模式 |
| `S` | 演讲者视图 |
| `F` | 全屏模式 |
| `?` | 帮助 |

## 📁 项目结构

```
mermaid-ppt/
├── index.html              # 主演示文稿 ⭐
├── cover_top.png           # 封面上半部分背景
├── cover_bottom.png        # 封面下半部分背景
├── README.md               # 项目说明（本文件）
└── docs/                   # 详细文档
    ├── cover-design.md     # 封面设计说明
    └── color-scheme.md     # 配色方案
```

## 🎨 主题色

| 颜色 | 色值 | 用途 |
|------|------|------|
| 主色调 | `#257FD5` | 标题、按钮、重要元素 |
| 强调色 | `#FF6B35` | 重点提示、对比元素 |
| 辅助色 | `#2EC4B6` | 技术内容、清新风格 |

详细配色说明请查看 [color-scheme.md](docs/color-scheme.md)

## 🎯 内容概览

演示文稿包含 **50+ 幻灯片**，分为以下章节：

1. **📋 议程** - 内容概览
2. **📊 Mermaid 基础** - 介绍与图表类型（10+ 页）
3. **🤖 AI 的力量** - AI 增强图表创建（8+ 页）
4. **🚀 实际应用** - 真实场景案例（8+ 页）
5. **🛠️ 技术实现** - 架构与集成（3 页）
6. **⭐ 最佳实践** - 使用技巧（4 页）
7. **✨ 高级技巧** - Mermaid 进阶（7 页）
8. **🔮 未来展望** - 发展趋势（3 页）

## 🛠️ 技术栈

- **RevealJS 4.3.1** - 演示文稿框架
- **Tailwind CSS** - 样式框架
- **Mermaid.js** - 图表渲染引擎
- **Font Awesome 6.4.0** - 图标库
- **Google Fonts** - Noto Sans/Serif SC

## 🎓 使用场景

适用于以下场景：
- 💼 技术分享会
- 🎤 产品演示
- 📚 培训教学
- 🏢 企业汇报
- 🎨 设计提案

## 📝 自定义修改

### 修改主题色
在 `index.html` 中编辑 CSS 变量（约第 25-60 行）：
```css
:root {
    --primary-color: #257FD5;    /* 修改主色 */
    --accent-color: #FF6B35;     /* 修改强调色 */
    /* ... 更多变量 */
}
```

### 更换封面图片
替换以下文件即可：
- `cover_top.png` - 上半部分
- `cover_bottom.png` - 下半部分

封面使用纯 CSS 蒙层（`rgba(26, 32, 44, 0.75)`），无需图片

### 添加新页面
在 `index.html` 中复制任意 `<section>` 标签，修改内容即可

## 🌐 浏览器兼容性

| 浏览器 | 支持 |
|--------|------|
| Chrome / Edge | ✅ 推荐 |
| Firefox | ✅ |
| Safari | ✅ |
| IE11 及以下 | ❌ |

## 💡 提示

1. **总览模式**: 按 `O` 快速浏览所有幻灯片
2. **演讲者视图**: 按 `S` 查看备注和下一页预览
3. **导出 PDF**: URL 后加 `?print-pdf` 然后打印
4. **移动设备**: 左右滑动切换幻灯片

## 🔧 常见问题

### 图片不显示？
检查 `cover_top.png` 和 `cover_bottom.png` 是否与 `index.html` 在同一目录。

### Mermaid 图表渲染错误？
1. 清除浏览器缓存（`Cmd+Shift+R` 或 `Ctrl+Shift+R`）
2. 检查控制台（F12）是否有错误信息
3. 确保可以访问 Mermaid CDN

### 如何导出为 PDF？
访问 `index.html?print-pdf`，然后使用浏览器打印功能保存为 PDF。

## 📞 支持

如有问题或建议，欢迎：
- 📧 提交 Issue
- 💬 参与讨论
- 🌟 给项目点星

## 📄 许可证

MIT License - 可自由使用和修改

---

**预祝演讲成功！** 🎉

*Created: 2025年10月 | Version: 2.0*
