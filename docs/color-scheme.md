# 演示文稿配色方案

## 🎨 主题色

### 主色调
- **Primary Blue**: `RGB(37, 127, 213)` / `#257FD5`
  - 专业、可信赖的蓝色
  - 用于：主标题、主按钮、重要节点

### 次要色
- **Deep Blue**: `RGB(26, 95, 166)` / `#1a5fa6`
  - 深蓝色，与主色形成层次
  - 用于：渐变、边框、副标题

### 强调色
- **Vibrant Orange**: `RGB(255, 107, 53)` / `#FF6B35`
  - 活力橙色，与蓝色形成对比
  - 用于：重要提示、警告、次要节点

- **Light Coral**: `RGB(255, 160, 122)` / `#FFA07A`
  - 柔和的珊瑚色
  - 用于：渐变结束、辅助元素

### 辅助色
- **Teal**: `RGB(46, 196, 182)` / `#2EC4B6`
  - 青绿色，清新现代
  - 用于：特殊节点、信息提示

- **Bright Cyan**: `RGB(0, 212, 255)` / `#00D4FF`
  - 明亮的青色
  - 用于：渐变、连接线

## 🌈 渐变方案

### 主渐变
```css
linear-gradient(135deg, #257FD5 0%, #1a5fa6 100%)
```
**用途**: 封面背景、章节标题背景、主按钮

### 强调渐变
```css
linear-gradient(135deg, #FF6B35 0%, #FFA07A 100%)
```
**用途**: 重要提示卡片、强调背景

### 清爽渐变
```css
linear-gradient(135deg, #2EC4B6 0%, #00D4FF 100%)
```
**用途**: 技术内容背景、代码示例区域

## 📊 Mermaid 图表配色

### 主题变量
```javascript
{
  primaryColor: '#257FD5',        // 主色
  primaryTextColor: '#fff',       // 白色文字
  primaryBorderColor: '#1a5fa6',  // 深蓝边框
  lineColor: '#257FD5',           // 连接线
  secondaryColor: '#FF6B35',      // 次要色
  tertiaryColor: '#2EC4B6'        // 第三色
}
```

### 节点样式建议

#### 开始/重要节点
```
style A fill:#257FD5,stroke:#1a5fa6,stroke-width:3px,color:#fff
```

#### 结束/完成节点
```
style Z fill:#FF6B35,stroke:#FFA07A,stroke-width:3px,color:#fff
```

#### 特殊/技术节点
```
style N fill:#2EC4B6,stroke:#00D4FF,stroke-width:2px,color:#fff
```

#### 成功状态
```
style S fill:#48bb78,color:#fff
```

#### 错误状态
```
style E fill:#f56565,color:#fff
```

## 🎯 使用场景

### 专业场景
主要使用蓝色系（#257FD5, #1a5fa6），营造专业、可信的氛围：
- 企业汇报
- 技术分享
- 产品介绍

### 创新场景
结合蓝色和青色（#2EC4B6），展现创新和活力：
- 技术创新
- 产品发布
- 团队协作

### 强调重点
使用橙色（#FF6B35）突出关键信息：
- 重要数据
- 行动号召
- 警告提示

## 💡 设计原则

### 1. 对比度
- 蓝色背景 + 白色文字：优秀的可读性
- 橙色点缀：在蓝色中形成强烈视觉焦点

### 2. 层次感
- 主色（#257FD5）→ 次要色（#1a5fa6）形成深浅层次
- 渐变增强立体感

### 3. 和谐度
- 蓝色系为主：80%
- 橙色强调：15%
- 其他辅助色：5%

### 4. 情感传达
- **蓝色**：专业、可靠、科技
- **橙色**：活力、创新、热情
- **青色**：清新、现代、友好

## 🔧 自定义修改

如需更改配色，请修改 `presentation.html` 中的 CSS 变量：

```css
:root {
    --primary-color: #257FD5;
    --secondary-color: #1a5fa6;
    --accent-color: #FF6B35;
    --gradient-primary: linear-gradient(135deg, #257FD5 0%, #1a5fa6 100%);
    --gradient-accent: linear-gradient(135deg, #FF6B35 0%, #FFA07A 100%);
    --gradient-cool: linear-gradient(135deg, #2EC4B6 0%, #00D4FF 100%);
}
```

## 📱 响应性

所有颜色在以下场景中都经过测试：
- ✅ 大屏投影
- ✅ 笔记本屏幕
- ✅ 平板设备
- ✅ 深色模式下的对比度

## 🌟 配色灵感

这套配色方案灵感来源于：
- 科技公司的品牌色（蓝色代表信任）
- 现代UI设计趋势（橙蓝对比）
- 数字海洋与日出的视觉意象

---

**创建日期**: 2025年10月21日  
**版本**: v1.0  
**主题**: AI × Mermaid 专业版

