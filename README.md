# Regex CSS Highlighter

[![release](https://img.shields.io/badge/version-1.5.6-blue)](https://github.com/dlsdgj/obsidian-regex-css-highlighter)

Obsidian 插件：用**正则表达式**匹配文本，再用**自定义 CSS** 实现高亮与样式化。支持实时预览、即时生效，是文本标注与知识管理的利器。

## 核心功能

| 功能 | 说明 | 快捷键 |
|------|------|--------|
| 🎨 **打开主窗口** | 管理所有高亮规则（新建/编辑/删除/搜索） | `Ctrl+Alt+R` |
| 📋 **合并剪贴板到规则** | 将剪贴板内容与选中文本合并为高亮规则 | `Ctrl+Alt+M` |
| 🎲 **随机高亮选中文本** | 为选中的文本随机应用一种高亮样式 | `Ctrl+Alt+H` |
| ❌ **移除高亮样式** | 移除选中文本上的高亮样式 | `Ctrl+Alt+D` |

## 特性一览

### 🖌️ 正则 + CSS 高亮

- 用正则表达式精确匹配文本内容（支持捕获组、前后断言等完整语法）
- 为每条规则绑定一个 CSS 类名，自定义颜色、背景、边框、字号、下划线等
- 规则**实时预览**，保存后**即时生效**

### 🏷️ 样式分类 & 快捷键

- 将高亮规则按**分类**组织管理
- 每个分类可绑定独立快捷键，一键批量应用/切换

### 🎯 格式替换

- 不仅高亮，还可以按正则匹配后执行**文本格式替换**
- 适合统一格式化日期、标点、数字等场景

### 📝 备注标注

- 为高亮文本附加**备注说明**
- 鼠标悬停或点击可查看备注内容，支持阅读模式下展示

### 🔤 拼音注音

- 自动为中文文本生成**拼音标注**（基于 `pinyin-data.json`）
- 支持全局拼音 CSS 和本地拼音 CSS 自定义样式
- 拼音样式实时预览

### 🤖 AI 助手

- 集成 AI 辅助功能，可直接在插件中调用 AI 进行文本处理
- 需要配合 Obsidian 的 AI 能力使用

### 👤 实体提取

- 从选中文本中自动提取**人名、地名**等命名实体
- 提取结果以结构化方式展示，支持自定义样式映射

### 🎈 悬浮球（Floating Ball）

一个始终可用的快捷操作面板，包含：

- **打开主面板** — 快速调出规则管理窗口
- **格式替换** — 当前文档内执行格式替换
- **添加备注** — 为选中区域附加备注
- **移除高亮** — 一键清除当前高亮
- **注音** — 快速切换拼音显示
- **AI回复** — 触发 AI 助手
- **实体提取** — 提取选中文本的命名实体
- **高亮列表** — 展示所有已应用的高亮样式
- **切换字体** — 快速切换阅读字体（需先在设置中启用）
- **模式切换** — 在多种显示模式间切换
- **隐藏按钮** — 临时收起悬浮按钮

悬浮球支持：
- 拖拽定位、跟随选中、固定位置多种模式
- 透明度调节
- 自定义可见选项
- 悬浮样式窗口独立拖拽

### 🌐 全局规则

- 在 `global-rules.json` 中定义**全局高亮规则**
- 在**所有文档**中自动生效，无需逐个设置

### 📱 桌面 + 手机双端兼容

- 桌面端使用 Node.js `fs` 模块，读写快速
- 手机端使用 Obsidian Vault Adapter，兼容性良好
- 手机阅读模式支持**边距和行高**自定义

### 🔠 字体切换

- 启用后读取系统所有已安装字体
- 支持收藏字体列表
- 一键切换阅读/编辑字体（需在设置中启用）

### 🎭 标题样式

- 自定义各级标题（H1-H6）的 CSS 样式
- 可开关标题装饰效果

## 安装

### 手动安装

1. 从 [Releases](https://github.com/dlsdgj/obsidian-regex-css-highlighter/releases) 下载 `main.js` 和 `manifest.json`
2. 放入 Vault 的 `.obsidian/plugins/Regex-Css-Highlighter/` 目录
3. 在 Obsidian 设置 → 社区插件中启用 **Regex Css Highlighter**

### 通过 BRAT

也可以通过 [BRAT](https://github.com/TfTHacker/obsidian42-brat) 插件安装，指向此仓库地址：
```
dlsdgj/obsidian-regex-css-highlighter
```

## 配置说明

插件会在插件目录下生成以下配置文件：

| 文件 | 用途 |
|------|------|
| `data.json` | 主设置文件（规则、分类、UI 偏好等） |
| `global-rules.json` | 全局高亮规则 |
| `style-categories.json` | 样式分类定义 |
| `pinyin-data.json` | 拼音数据 |
| `prompt-templates.json` | AI 提示模板 |
| `floatbutton_data.json` | 悬浮球配置 |

## 兼容性

- 最低 Obsidian 版本：**0.15.0**
- 支持 **桌面端**（Windows / macOS / Linux）和**移动端**（iOS / Android）

## 开发

```bash
# 克隆仓库
git clone https://github.com/dlsdgj/obsidian-regex-css-highlighter.git

# 安装依赖（如果有）
npm install

# 构建
npm run build
```

## 许可证

MIT License

## 作者

nilmarko

---

> 💡 **提示**：安装后按 `Ctrl+Alt+R` 打开主窗口，开始创建你的第一条高亮规则！
