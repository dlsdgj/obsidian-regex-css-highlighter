中文 | [English](#english)

# Regex CSS Highlighter

一个 Obsidian 插件，通过正则表达式匹配文本并应用自定义 CSS 样式高亮显示。

## 功能特性

### 🎨 样式高亮

- **正则匹配 + CSS 样式** — 使用正则表达式匹配文本，为匹配内容应用自定义 CSS 样式
- **样式分类管理** — 样式按分组分类，支持添加、编辑、删除样式
- **样式即时生效** — 添加/编辑/删除样式后无需重启，立即在笔记中生效
- **样式悬浮按钮** — 右键样式按钮可创建可拖动的悬浮按钮，支持调整大小和透明度
- **样式按钮右键菜单** — 复制类名、复制完整样式、悬浮显示等快捷操作

### 📝 规则管理

- **当前文件规则 / 全局规则** — 支持文件级和全局级两种规则范围
- **规则来源标记** — 鼠标悬停匹配文本时显示规则来源（g=全局/l=局部），点击可跳转
- **高亮列表** — 查看当前文件中所有匹配的高亮规则，支持按列搜索、筛选
- **合并剪贴板** — 将剪贴板内容与选中文本合并添加为高亮规则

### 🔮 悬浮球

- **快速访问** — 悬浮球提供样式快速应用入口，左键应用当前文件规则，中键应用全局规则
- **分组子菜单** — 悬停分组选项展开子菜单，显示该分组所有样式
- **悬浮选项按钮** — 菜单选项可创建独立的悬浮按钮，随时可用
- **显示/隐藏文本样式** — 一键切换所有文本样式的显示与隐藏

### 🌐 国际化

- **中英文切换** — 主面板左上角 CN/EN 切换按钮，界面文本全面国际化
- **双语翻译** — 设置项、悬浮球选项、分组样式按钮等所有界面文本均支持中英文

### 📱 移动端适配

- **触摸拖动** — 悬浮球和悬浮按钮支持触摸拖动调整位置
- **独立排版设置** — 手机版阅读模式行距、边距独立于桌面版设置
- **面板透明度** — 手机版主面板和按钮面板支持透明度调整
- **折叠式筛选** — 高亮列表筛选区域默认收起，节省屏幕空间

### ✏️ 排版与字体

- **系统字体切换** — 直接读取系统已安装字体，无需放入字体文件
- **字体收藏** — 星标收藏常用字体，收藏字体置顶显示
- **行间距与边距** — 支持行间距、左边距、右边距设置，编辑和阅读模式均生效
- **滚轮微调** — 数值输入框支持鼠标滚轮快速调整

### 📌 备注功能

- **文本备注** — 为高亮文本添加备注，支持 Markdown 渲染
- **图片支持** — 备注弹窗支持上传图片和粘贴剪贴板图片
- **表格渲染** — 备注支持 Markdown 表格，带边框和斑马纹样式

### 🤖 AI 集成

- **多 AI 配置** — 支持配置多个 AI 服务（OpenAI、DeepSeek 等），自定义 API 地址和模型
- **AI 实体提取** — 使用 AI 自动识别文本中的实体并批量添加高亮规则

### ⌨️ 快捷键

| 快捷键 | 功能 |
|--------|------|
| `Ctrl+Alt+R` | 打开主窗口 |
| `Ctrl+Alt+H` | 随机高亮选中文本 |
| `Ctrl+Alt+M` | 合并剪贴板与选中文本到高亮规则 |
| `Ctrl+Alt+D` | 移除选中文本的高亮样式 |
| `Alt+滚轮` | 调整悬浮按钮/主面板大小 |
| `Ctrl+滚轮` | 调整悬浮按钮/主面板透明度 |

## 安装

1. 下载 `main.js`、`manifest.json`
2. 在 Obsidian 库的 `.obsidian/plugins/` 目录下创建 `Regex-Css-Highlighter` 文件夹
3. 将下载的文件放入该文件夹
4. 在 Obsidian 设置 → 社区插件中启用 "Regex Css Highlighter"

## 更新日志

### 🆕 v1.5.8 (2026-06-01)

- **移除"关于"部分** - 移除主面板底部"关于"section，版本更新日志统一迁移至readme.md
- **清理捐赠功能代码** - 移除showDonateImage类方法和独立函数、setupDonateText函数、捐赠按钮CSS样式及相关翻译键
- **清理无用翻译键** - 移除main.tab.about、settings.about、settings.updateHistory、settings.viewUpdates等不再使用的翻译键
- **清理DONATE_QR_CODE常量** - 移除base64编码的捐赠二维码图片常量

### v1.5.7 (2026-05-31)

- **国际化支持** - 主面板添加 CN/EN 语言切换按钮，支持中英文界面切换
- **全面国际化** - 设置项标题、悬浮球选项、分组样式按钮等所有界面文本国际化
- **管理悬浮球选项新增"隐藏/显示文本样式"** - 可在设置中控制该选项是否在悬浮球菜单中显示
- **修复分组子菜单中键点击触发自动滚动** - 中键点击添加全局规则时不再进入自动滚动状态
- **高亮列表样式名列** - 高亮列表添加样式名列，有显示文字时分行显示，支持显示/隐藏切换
- **高亮列表表头搜索** - 每个表头添加搜索框，placeholder显示表头文字，支持按列实时搜索过滤
- **移除"加入展示"功能** - 移除样式按钮右键"加入展示"选项及高亮列表filter的show style name、by style name
- **min count始终显示** - 移除mode下拉框，min count输入框始终显示，中文标签改为"样式最少被应用[X]次"

### v1.5.6 (2026-05-31)

- **悬浮子菜单右键选项** - 悬浮按钮子菜单样式右键添加"修改显示文字"、"复制类名"、"复制完整样式"选项
- **子菜单右键体验修复** - 修复鼠标移动到右键选项时子菜单会隐藏的问题
- **中键添加全局规则** - 中键点击悬浮分组子菜单样式可将选中文字添加为全局规则
- **规则来源标记(g/l)** - 鼠标悬停匹配规则文本时显示全局/局部标记"g/l"，点击可跳转到对应规则，支持字数阈值设置
- **编辑模式标记修复** - 修复编辑模式下"g/l"标记被添加为文本内容的问题
- **悬浮子菜单类名提示** - 悬浮分组子菜单样式项悬停时显示类名提示
- **文本样式显示/隐藏** - 悬浮球悬停菜单添加"显示文本样式"/"隐藏文本样式"选项，隐藏时所有文本中匹配的规则样式都禁止显示

### v1.5.5 (2026-05-29)

- **隐藏保留位置数据** - 隐藏悬浮样式按钮时保存位置数据，下次显示时自动恢复到原位置
- **主面板悬浮显示按钮** - 主面板样式按钮hover时显示📌按钮，点击即可悬浮显示该样式

### v1.5.4 (2026-05-28)

- **清理不存在样式** - 设置-显示下新增"清理分类文件中不存在样式"功能，可扫描并一键清除 style-categories.json 中有但 styles.css 中没有的样式
- **分组子菜单滚动条** - 悬浮球菜单和悬浮选项按钮的分组样式子菜单添加滚动条，样式过多时不再超出软件界面
- **设置标题淡蓝背景** - 主面板设置中各级标题添加淡蓝色背景，占满整行，层级更清晰

### v1.5.3 (2026-05-27)

- **手机版阅读模式行距** - 手机版"显示"设置中新增行距设定，与边距设置合并为"手机版阅读模式行、边距"
- **手机版面板透明度** - 手机版"显示"设置中新增主面板和按钮面板透明度设置
- **手机版排版设置分离** - 手机端不再应用桌面版的行间距和边距设置，由手机版独立设置控制
- **手机版自动展开修复** - 修复手机端自动展开模式下分组展开时第一个样式被误应用到文字的bug
- **标题设置分类** - 将"标题层级标签"和"禁用标题样式"移至新建的"标题"设置分类下
- **计数信息修复** - 修复"样式类别"和"计数文件"计数不在同一行显示的bug，移除链接样式
- **悬浮球菜单透明度** - 悬浮球菜单支持Ctrl+滚轮调整透明度，设置重启后保留
- **右键菜单改进** - 右键另一个样式时自动关闭之前的菜单；普通模式右键菜单新增"移动到分组"选项

### v1.5.2 (2026-05-26)

- **设置大纲式重组** - 将设置区域从扁平分隔线形式改为大纲笔记缩进折叠形式，层级更清晰
- **折叠时显示最近规则** - 新增设置选项，控制未选中文字打开主面板且高亮规则折叠时是否显示最近添加的规则
- **手机端隐藏字体切换** - 手机端隐藏设置中的字体切换功能区域
- **手机端隐藏打开文件链接** - 手机端隐藏"设置"标题旁的打开data.json文件链接

### v1.5.1 (2026-05-25)

- **排版设置** - 在"切换正文字体"弹窗中新增行间距、左边距、右边距设置，编辑和阅读模式均生效
- **滚轮调整数值** - 行间距和边距输入框支持鼠标滚轮快速调整数值
- **编辑模式边距修复** - 修复编辑模式下左右边距不生效的问题

### v1.5.0 (2026-05-25)

- **禁用标题样式** - 设置中新增"禁用标题样式"开关，禁用后不应用自定义标题样式，但保留标题层级标签；禁用时主面板隐藏"标题样式"区域
- **层级标签兼容渐变文字** - 修复使用渐变文字CSS片段时层级标签不可见的问题，在伪元素中重置继承的透明文字和背景裁剪属性
- **移除使用方法** - 移除主面板中"使用方法"相关内容，精简界面

### v1.4.9 (2026-05-25)

- **添加样式即时生效** - 修复添加/编辑/删除样式后需要重启Obsidian才能显示的问题，新样式现在立即生效
- **样式刷新机制优化** - 移除破坏性的forceStyleRefresh调用，避免新注入的CSS被清空；写入CSS文件后直接更新动态样式元素，无需重新读取文件
- **CSS读写一致性修复** - injectCSSContent改用vault.adapter.read，与写入API保持一致，避免缓存不同步
- **模态框刷新加速** - 移除添加样式后的多层setTimeout延迟（500ms+200ms），弹窗即时刷新
- **删除样式即时刷新** - 删除样式后移除1秒延迟，立即重新注入CSS并刷新视图

### v1.4.7 (2026-05-24)

- **系统字体切换** - 字体切换改为直接读取系统已安装字体，无需放入字体文件，告别CSP/OTS兼容问题
- **字体收藏功能** - 字体列表支持星标收藏，收藏字体置顶显示，方便快速切换常用字体
- **字体搜索** - 字体选择弹窗新增搜索框，快速过滤定位字体
- **字体列表美化** - 卡片式布局、SVG星标图标、使用中标签、hover交互优化

### v1.4.6 (2026-05-22)

- **DeepSeek默认配置更新** - 新装插件时DeepSeek默认base_url改为https://api.deepseek.com/chat/completions，模型改为deepseek-v4-flash
- **样式类名提示** - 编辑悬浮选项窗口的样式类名输入框添加提示"主面板样式按钮长按/右键→复制类名"

### v1.4.5 (2026-05-22)

- **悬浮球移除高亮** - 悬浮球选项新增"移除高亮"，选中高亮文本后点击即可移除对应规则，支持多部分规则智能拆分
- **规则右键菜单增强** - 当前文件规则和全局规则按钮右键新增"删除规则"和"移动到全局/当前文件规则"选项
- **阅读模式选中文本修复** - 修复阅读模式下选中文本后打开主面板无法获取选中文本的问题，在模态框打开前提前保存选区
- **悬浮选项箭头修复** - 修复编辑样式后悬浮选项出现两个箭头的问题，箭头移入样式内部节省空间
- **手机端主面板优化** - 手机端隐藏透明度/宽度控件和标题后提示消息与链接，正则表达式标签单独一行显示
- **移除添加备注按钮** - 主面板移除"添加备注"按钮，备注功能仍可通过右键菜单和悬浮球使用

### v1.4.4 (2026-05-22)

- **悬浮按钮缩放偏移修复** - 修复Alt+滚轮缩放悬浮样式按钮后，点击时按钮会左右移动的bug
- **关于面板高度修复** - 展开"关于"区域高度从固定300px改为70vh自适应窗口高度
- **复制类名功能** - 样式按钮右键菜单添加"复制类名"选项，一键复制CSS类名到剪贴板

### v1.4.3 (2026-05-22)

- **阅读模式跨元素高亮** - 重写高亮匹配逻辑，支持跨DOM元素边界匹配长文本，解决阅读模式下含已有高亮或全局规则修饰的文本无法应用新样式的问题
- **右键菜单溢出修复** - 悬浮选项按钮和悬浮样式按钮的右键菜单在屏幕右侧/底部时自动调整位置，不再溢出屏幕

### v1.4.2 (2026-05-21)

- **手机端悬浮样式按钮拖动** - 修复恢复的悬浮样式按钮在手机端无法拖动调整位置的问题
- **触摸拖动防误触** - 悬浮样式按钮触摸拖动后不再误触发样式应用

### v1.4.1 (2026-05-21)

- **悬浮选项右键菜单** - 悬浮选项按钮右键改为弹出菜单（编辑/关闭），不再直接关闭
- **悬浮选项编辑功能** - 右键"编辑"可修改显示文字和样式类名，样式类名支持伪元素完整渲染
- **悬浮选项滚轮调整** - Alt+滚轮调整大小，Ctrl+滚轮调整透明度，设置重启后保留
- **悬浮样式按钮编辑名称** - 悬浮样式按钮右键菜单添加"编辑名称"选项，可修改显示文字
- **样式类名渲染优化** - 设置样式类名后移除默认线框，完整注入CSS规则含伪元素，支持复杂样式

### v1.4.0 (2026-05-21)

- **手机端悬浮球适配** - 增大悬浮球尺寸至36px，调整默认位置，添加位置安全检查确保可见
- **手机端悬浮球菜单** - 点击悬浮球弹出选项菜单而非直接高亮，与电脑端行为区分
- **手机端悬浮按钮拖动** - 悬浮样式按钮和悬浮选项按钮添加触摸事件支持，可拖动调整位置
- **手机版阅读模式行、边距** - 新增手机版阅读模式行距和左右边距设置，移至"显示"分类下，与桌面版排版设置分开
- **手机端折叠筛选面板** - 高亮列表筛选区域改为折叠式面板，默认收起，点击展开
- **手机端列表式高亮显示** - 高亮列表改为卡片式布局，备注折叠进高亮文本中，点击展开
- **高亮列表性能优化** - 文件读取并行化、内存缓存优先、省去冗余exists调用、全局规则Map索引
- **加载状态提示** - 高亮列表打开和筛选切换时显示"加载中..."提示，先渲染UI再加载数据

### v1.3.9 (2026-05-20)

- **手机端兼容** - 封装跨平台文件操作工具类，桌面端用Node.js fs模块（高性能），手机端用Vault Adapter（兼容）
- **阅读模式滚动高亮** - 修复滚动后高亮丢失的问题，监听滚动事件自动补刷视口内高亮
- **延迟处理竞态修复** - 修复PostProcessor延迟分批处理的定时器竞态问题

### v1.3.8 (2026-05-14)

- **阅读模式高亮修复** - 修复阅读模式下部分匹配文本不显示样式的问题，递归处理嵌套行内元素中的文本节点
- **悬浮按钮跟随边框** - 悬浮选项按钮和悬浮样式按钮在屏幕右侧时改用right定位，窗口边框拖动时自动跟随移动
- **禁用规则过滤** - 高亮处理时自动过滤已禁用的规则，避免无效匹配

### v1.3.7 (2026-05-13)

- **备注支持图片** - 备注弹窗支持上传图片和粘贴剪贴板图片，图片自动保存到附件目录
- **备注支持表格** - 备注弹窗支持Markdown表格渲染，带边框、表头高亮和斑马纹样式
- **备注弹窗自适应** - 弹窗根据图片实际大小自动调整尺寸，箭头指示位置同步更新
- **表格和Callout高亮** - 修复高亮规则在表格和Callout中不显示样式的问题

### v1.3.6 (2026-05-09)

- **悬浮按钮边界约束** - 悬浮球、悬浮选项按钮、悬浮样式按钮在窗口缩小时自动向内缩进，拖动时限制在视口范围内
- **二级子菜单溢出修复** - 悬浮选项的二级子菜单在右侧边缘时自动翻转方向，避免超出窗口边界
- **窗口调整内容随动** - 拖动右下角手柄调整主面板大小时，内部按钮即时随动重排

### v1.3.5 (2026-05-08)

- **高亮列表按应用次数模式** - 新增"按应用次数"显示模式，可设置最小次数阈值，自动显示应用次数≥该值的所有样式高亮
- **窗口调整手柄** - 主面板和实体提取弹窗右下角添加可拖拽调整窗口大小的手柄
- **跳转功能修复** - 修复高亮列表双击跳转时报错的问题
- **性能优化** - CSS样式加载改用Node.js fs模块直接读取，提升加载速度

### v1.3.4 (2026-05-06)

- **默认拼音样式优化** - 新安装插件时默认拼音样式更美观（红色字体、方正书宋字体）
- **AI设置链接修复** - 修复编辑AI配置时"获取API Key"链接始终显示OpenAI地址的问题

### v1.3.3 (2026-05-03)

- **悬浮球中键点击** - 鼠标中键点击悬浮球可随机应用样式到全局规则（左键单击为当前文件规则）

### v1.3.2 (2026-05-01)

- **悬浮按钮伪元素修复** - 修复重启后悬浮按钮的伪元素样式不显示的问题

### v1.3.1 (2026-04-28)

- **悬浮选项功能** - 悬浮球菜单所有选项添加"悬浮显示"按钮，点击后创建悬浮按钮
- **注音悬浮按钮** - 注音选项支持悬浮显示，鼠标悬停显示子菜单（局部/全局注音、编辑、删除）
- **分组悬浮按钮** - 分组选项支持悬浮显示，鼠标悬停显示该分组所有样式
- **样式快速悬浮** - 样式子菜单中每个样式按钮右上角有📌按钮，可单独悬浮显示该样式
- **设置分离优化** - 分组菜单显示和悬浮显示使用独立设置，互不影响

### v1.3.0.0 (2026-04-21)

- **悬浮显示功能** - 右键样式按钮添加"悬浮显示"选项，创建可拖动的样式悬浮按钮
- **多悬浮窗口** - 支持同时显示多个悬浮按钮，位置、透明度和大小会在重启后保留
- **主面板交互优化** - 添加Alt+鼠标滚轮调整主面板宽度，Ctrl+滚轮调整透明度
- **输入框提示** - 鼠标悬浮在透明度/宽度输入框上时显示操作提示

### v1.2.9.9 (2026-04-21)

- **悬浮按钮交互优化** - 修复拖动时误触发高亮的问题，添加移动阈值判断
- **光标显示优化** - 悬浮按钮默认显示手型指针，拖动时显示抓手指针
- **拖动逻辑修复** - 修复按钮一直跟随鼠标移动的问题，只在按下鼠标时响应拖动

### v1.2.9.8 (2026-04-21)

- **悬浮显示功能** - 右键样式按钮添加"悬浮显示"选项，创建可拖动的样式悬浮按钮
- **多悬浮窗口** - 支持同时显示多个悬浮按钮，每次点击"悬浮显示"会创建新的窗口
- **位置记忆** - 悬浮按钮位置、透明度和大小会在重启插件后保留
- **交互功能** - 按住拖动位置，左键点击应用样式到选中文本，Ctrl+滚轮调整透明度，Alt+滚轮调整大小
- **右键菜单** - 悬浮按钮右键菜单添加"关闭悬浮显示"选项

---

<a id="english"></a>

[中文](#中文) | English

# Regex CSS Highlighter

An Obsidian plugin that matches text via regular expressions and applies custom CSS styles for highlighting.

## Features

### 🎨 Style Highlighting

- **Regex Matching + CSS Styles** — Match text using regular expressions and apply custom CSS styles to matched content
- **Style Category Management** — Styles organized by groups, with support for adding, editing, and deleting
- **Instant Style Application** — Styles take effect immediately after adding/editing/deleting, no restart required
- **Floating Style Buttons** — Right-click a style button to create a draggable floating button with adjustable size and opacity
- **Style Button Context Menu** — Copy class name, copy full style, float display, and other quick actions

### 📝 Rule Management

- **Current File / Global Rules** — Support for both file-level and global rule scopes
- **Rule Source Markers** — Hover over matched text to see rule source (g=global/l=local), click to jump to the rule
- **Highlight List** — View all matched highlight rules in the current file, with per-column search and filtering
- **Clipboard Merge** — Merge clipboard content with selected text to add as a highlight rule

### 🔮 Floating Ball

- **Quick Access** — Floating ball provides quick style application: left-click for current file rules, middle-click for global rules
- **Group Submenu** — Hover over a group option to expand a submenu showing all styles in that group
- **Floating Option Buttons** — Menu options can be pinned as independent floating buttons for instant access
- **Show/Hide Text Styles** — One-click toggle to show or hide all text style highlights

### 🌐 Internationalization

- **CN/EN Language Switch** — Language toggle button at the top-left of the main panel, full i18n support
- **Bilingual Translation** — All UI text including settings, floating ball options, and group style buttons support both Chinese and English

### 📱 Mobile Adaptation

- **Touch Dragging** — Floating ball and floating buttons support touch dragging to adjust position
- **Independent Layout Settings** — Mobile reading mode line height and margins are independent from desktop settings
- **Panel Opacity** — Mobile main panel and button panel support opacity adjustment
- **Collapsible Filters** — Highlight list filter area defaults to collapsed to save screen space

### ✏️ Typography & Fonts

- **System Font Switching** — Directly read system-installed fonts, no need to place font files
- **Font Favorites** — Star favorite fonts, favorited fonts displayed at the top
- **Line Height & Margins** — Support for line height, left margin, and right margin settings, effective in both edit and reading modes
- **Scroll Wheel Fine-tuning** — Numeric input fields support mouse scroll wheel for quick adjustments

### 📌 Notes

- **Text Notes** — Add notes to highlighted text with Markdown rendering support
- **Image Support** — Note popup supports uploading images and pasting clipboard images
- **Table Rendering** — Notes support Markdown tables with borders and zebra stripe styling

### 🤖 AI Integration

- **Multiple AI Configs** — Support configuring multiple AI services (OpenAI, DeepSeek, etc.) with custom API URLs and models
- **AI Entity Extraction** — Use AI to automatically identify entities in text and batch-add highlight rules

### ⌨️ Keyboard Shortcuts

| Shortcut | Function |
|----------|----------|
| `Ctrl+Alt+R` | Open main window |
| `Ctrl+Alt+H` | Random highlight selected text |
| `Ctrl+Alt+M` | Merge clipboard with selected text into highlight rule |
| `Ctrl+Alt+D` | Remove highlight style from selected text |
| `Alt+Scroll` | Adjust floating button / main panel size |
| `Ctrl+Scroll` | Adjust floating button / main panel opacity |

## Installation

1. Download `main.js` and `manifest.json`
2. Create a `Regex-Css-Highlighter` folder in your Obsidian vault's `.obsidian/plugins/` directory
3. Place the downloaded files into that folder
4. Enable "Regex Css Highlighter" in Obsidian Settings → Community Plugins

## Changelog

### 🆕 v1.5.8 (2026-06-01)

- **Remove "About" section** - Removed the "About" section from the main panel bottom, version changelog unified to readme.md
- **Clean up donate code** - Removed showDonateImage class method and standalone function, setupDonateText function, donate button CSS styles and related translation keys
- **Clean up unused translation keys** - Removed main.tab.about, settings.about, settings.updateHistory, settings.viewUpdates and other unused translation keys
- **Clean up DONATE_QR_CODE constant** - Removed base64-encoded donation QR code image constant

### v1.5.7 (2026-05-31)

- **Internationalization support** - Added CN/EN language toggle button to the main panel, supporting Chinese/English UI switching
- **Full i18n** - Settings titles, floating ball options, group style buttons and all UI text internationalized
- **Manage floating ball options: add "Hide/Show text styles"** - Can control whether this option appears in the floating ball menu
- **Fix middle-click in group submenu triggering auto-scroll** - Middle-click to add global rule no longer enters auto-scroll state
- **Highlight list style name column** - Added style name column to highlight list, displayed on separate line when display text exists, with show/hide toggle
- **Highlight list header search** - Added search box to each column header, placeholder shows header text, supports real-time per-column search filtering
- **Remove "Add to Highlight" feature** - Removed style button right-click "Add to Highlight" option and highlight list filter's show style name, by style name
- **Min count always visible** - Removed mode dropdown, min count input always visible, Chinese label changed to "样式最少被应用[X]次"

### v1.5.6 (2026-05-31)

- **Floating submenu right-click options** - Added "Edit display text", "Copy class name", "Copy full style" to floating button submenu style right-click
- **Submenu right-click UX fix** - Fixed submenu hiding when mouse moves to right-click option
- **Middle-click add global rule** - Middle-click floating group submenu style to add selected text as global rule
- **Rule source markers (g/l)** - Hover over matched rule text to show global/local marker "g/l", click to jump to the rule, with character threshold setting
- **Edit mode marker fix** - Fixed "g/l" markers being added as text content in edit mode
- **Floating submenu class name tooltip** - Hover over floating group submenu style item to show class name tooltip
- **Show/Hide text styles** - Added "Show text styles"/"Hide text styles" option to floating ball hover menu, hiding disables all matched rule styles in text

### v1.5.5 (2026-05-29)

- **Preserve position data on hide** - Save position data when hiding floating style button, auto-restore on next show
- **Main panel float display button** - Main panel style button hover shows 📌 button, click to float display that style

### v1.5.4 (2026-05-28)

- **Clean up non-existent styles** - Added "Clean up non-existent styles in category file" under Display settings, scan and one-click remove styles in style-categories.json but not in styles.css
- **Group submenu scrollbar** - Added scrollbar to floating ball menu and floating option button group style submenus, no longer exceeds app interface with many styles
- **Settings title light blue background** - Added light blue background to main panel settings headers, full-width, clearer hierarchy

### v1.5.3 (2026-05-27)

- **Mobile reading mode line height** - Added line height setting to mobile Display settings, merged with margins as "Mobile reading mode line height & margins"
- **Mobile panel opacity** - Added main panel and button panel opacity settings to mobile Display settings
- **Mobile layout settings separation** - Mobile no longer applies desktop line height and margin settings, controlled by independent mobile settings
- **Mobile auto-expand fix** - Fixed bug where first style was mistakenly applied to text when group expanded in mobile auto-expand mode
- **Heading settings category** - Moved "Heading level labels" and "Disable heading styles" to new "Heading" settings category
- **Count info fix** - Fixed "Style categories" and "Count files" not displaying on the same line, removed link styles
- **Floating ball menu opacity** - Floating ball menu supports Ctrl+scroll to adjust opacity, persisted after restart
- **Context menu improvements** - Right-clicking another style auto-closes previous menu; normal mode right-click menu adds "Move to group" option

### v1.5.2 (2026-05-26)

- **Settings outline restructure** - Changed settings area from flat dividers to outline-style indented folding, clearer hierarchy
- **Show recent rules when collapsed** - New setting option to control whether recently added rules are shown when main panel opens with no text selected and highlight rules collapsed
- **Mobile hide font switch** - Mobile hides font switch function area in settings
- **Mobile hide open file link** - Mobile hides "Open data.json" link next to Settings title

### v1.5.1 (2026-05-25)

- **Typography settings** - Added line height, left margin, right margin settings in "Switch body font" popup, effective in both edit and reading modes
- **Scroll wheel adjust values** - Line height and margin input fields support mouse scroll wheel for quick value adjustment
- **Edit mode margin fix** - Fixed left/right margins not working in edit mode

### v1.5.0 (2026-05-25)

- **Disable heading styles** - Added "Disable heading styles" toggle in settings, when disabled custom heading styles are not applied but heading level labels are preserved; "Heading styles" area hidden in main panel when disabled
- **Level labels compatible with gradient text** - Fixed level labels invisible when using gradient text CSS snippet, reset inherited transparent text and background-clip properties in pseudo-elements
- **Remove usage instructions** - Removed "Usage" related content from main panel, simplified interface

### v1.4.9 (2026-05-25)

- **Instant style application** - Fixed styles requiring Obsidian restart after add/edit/delete, styles now take effect immediately
- **Style refresh optimization** - Removed destructive forceStyleRefresh calls, avoid newly injected CSS being cleared; directly update dynamic style elements after writing CSS file
- **CSS read/write consistency fix** - injectCSSContent now uses vault.adapter.read, consistent with write API, avoiding cache desync
- **Modal refresh acceleration** - Removed multi-layer setTimeout delays after adding styles (500ms+200ms), instant modal refresh
- **Delete style instant refresh** - Removed 1-second delay after deleting style, immediately re-inject CSS and refresh view

### v1.4.7 (2026-05-24)

- **System font switching** - Font switching now directly reads system-installed fonts, no need to place font files, goodbye CSP/OTS compatibility issues
- **Font favorites** - Font list supports star favorites, favorited fonts displayed at top for quick switching
- **Font search** - Added search box to font selection popup for quick filtering
- **Font list beautification** - Card layout, SVG star icons, in-use labels, hover interaction optimization

### v1.4.6 (2026-05-22)

- **DeepSeek default config update** - New install DeepSeek default base_url changed to https://api.deepseek.com/chat/completions, model changed to deepseek-v4-flash
- **Style class name tooltip** - Added tooltip to style class name input in edit floating option window

### v1.4.5 (2026-05-22)

- **Floating ball remove highlight** - Added "Remove highlight" to floating ball options, click after selecting highlighted text to remove corresponding rule
- **Rule right-click menu enhancement** - Current file and global rule buttons right-click add "Delete rule" and "Move to global/current file rule" options
- **Reading mode selected text fix** - Fixed unable to get selected text after opening main panel in reading mode, save selection before modal opens
- **Floating option arrow fix** - Fixed two arrows appearing after editing style, arrow moved inside style to save space
- **Mobile main panel optimization** - Mobile hides opacity/width controls and post-title messages/links, regex label on separate line
- **Remove add note button** - Removed "Add note" button from main panel, note function still available via right-click menu and floating ball

### v1.4.4 (2026-05-22)

- **Floating button scale offset fix** - Fixed floating style button shifting left/right when clicked after Alt+scroll scaling
- **About panel height fix** - Changed "About" section height from fixed 300px to 70vh adaptive window height
- **Copy class name** - Added "Copy class name" option to style button right-click menu

### v1.4.3 (2026-05-22)

- **Reading mode cross-element highlighting** - Rewrote highlight matching logic, supports matching long text across DOM element boundaries
- **Right-click menu overflow fix** - Floating option and style button right-click menus auto-adjust position when near screen edges

### v1.4.2 (2026-05-21)

- **Mobile floating style button drag** - Fixed restored floating style buttons unable to be dragged on mobile
- **Touch drag anti-mistouch** - Floating style buttons no longer mistakenly trigger style application after touch dragging

### v1.4.1 (2026-05-21)

- **Floating option right-click menu** - Changed floating option button right-click to popup menu (edit/close) instead of direct close
- **Floating option edit** - Right-click "Edit" to modify display text and style class name, style class name supports pseudo-element full rendering
- **Floating option scroll adjust** - Alt+scroll for size, Ctrl+scroll for opacity, persisted after restart
- **Floating style button edit name** - Added "Edit name" option to floating style button right-click menu
- **Style class name rendering optimization** - Removed default wireframe after setting class name, fully inject CSS rules including pseudo-elements

### v1.4.0 (2026-05-21)

- **Mobile floating ball adaptation** - Increased floating ball size to 36px, adjusted default position, added position safety check
- **Mobile floating ball menu** - Click floating ball to show options menu instead of direct highlight, differentiated from desktop behavior
- **Mobile floating button drag** - Added touch event support to floating style and option buttons for drag position adjustment
- **Mobile reading mode line height & margins** - Added mobile reading mode line height and margin settings under "Display" category
- **Mobile collapsible filter panel** - Highlight list filter area changed to collapsible panel, default collapsed
- **Mobile card-style highlight display** - Highlight list changed to card layout, notes collapsed into highlight text
- **Highlight list performance optimization** - Parallel file reads, memory cache priority, eliminate redundant exists calls, global rule Map index
- **Loading state indicator** - Show "Loading..." prompt when opening highlight list and switching filters

### v1.3.9 (2026-05-20)

- **Mobile compatibility** - Encapsulated cross-platform file operation utility, desktop uses Node.js fs module, mobile uses Vault Adapter
- **Reading mode scroll highlighting** - Fixed highlights lost after scrolling, listen to scroll events to auto-refresh viewport highlights
- **Delayed processing race condition fix** - Fixed timer race condition in PostProcessor delayed batch processing

### v1.3.8 (2026-05-14)

- **Reading mode highlight fix** - Fixed some matched text not showing styles in reading mode, recursively process text nodes in nested inline elements
- **Floating button follow window border** - Floating option and style buttons use right positioning when on screen right side, auto-follow window border drag
- **Disabled rule filtering** - Automatically filter disabled rules during highlight processing

### v1.3.7 (2026-05-13)

- **Notes image support** - Note popup supports uploading images and pasting clipboard images, auto-save to attachments directory
- **Notes table support** - Note popup supports Markdown table rendering with borders, header highlighting, and zebra stripe styling
- **Note popup auto-sizing** - Popup auto-adjusts size based on actual image dimensions, arrow position syncs
- **Table and Callout highlighting** - Fixed highlight rules not showing styles in tables and Callouts

### v1.3.6 (2026-05-09)

- **Floating button boundary constraints** - Floating ball, option buttons, and style buttons auto-retract when window shrinks, drag constrained to viewport
- **Secondary submenu overflow fix** - Floating option secondary submenu auto-flips direction at right edge
- **Window resize content reflow** - Internal buttons instantly reflow when dragging resize handle

### v1.3.5 (2026-05-08)

- **Highlight list by application count mode** - Added "By application count" display mode with minimum count threshold
- **Window resize handle** - Added draggable resize handle to main panel and entity extraction popup bottom-right corner
- **Jump function fix** - Fixed error when double-clicking to jump in highlight list
- **Performance optimization** - CSS style loading uses Node.js fs module for direct reading

### v1.3.4 (2026-05-06)

- **Default pinyin style optimization** - More aesthetic default pinyin style for new installations
- **AI settings link fix** - Fixed "Get API Key" link always showing OpenAI address when editing AI config

### v1.3.3 (2026-05-03)

- **Floating ball middle-click** - Middle-click floating ball to randomly apply style to global rules (left-click for current file rules)

### v1.3.2 (2026-05-01)

- **Floating button pseudo-element fix** - Fixed pseudo-element styles not showing on floating buttons after restart

### v1.3.1 (2026-04-28)

- **Floating option feature** - All floating ball menu options have "Float display" button to create floating buttons
- **Ruby floating button** - Ruby option supports floating display with hover submenu
- **Group floating button** - Group option supports floating display with hover submenu showing all group styles
- **Quick style float** - Each style button in submenu has 📌 button for individual floating display
- **Settings separation** - Group menu display and floating display use independent settings

### v1.3.0.0 (2026-04-21)

- **Floating display feature** - Right-click style button to add "Float display" option, creating draggable floating style buttons
- **Multiple floating windows** - Support simultaneous display of multiple floating buttons, position/opacity/size persisted after restart
- **Main panel interaction optimization** - Alt+scroll to adjust main panel width, Ctrl+scroll for opacity
- **Input field tooltips** - Hover over opacity/width input fields to show operation tips

### v1.2.9.9 (2026-04-21)

- **Floating button interaction optimization** - Fixed mistouch highlighting during drag, added movement threshold
- **Cursor display optimization** - Floating buttons show pointer cursor by default, grab cursor during drag
- **Drag logic fix** - Fixed button always following mouse, only respond to drag when mouse pressed

### v1.2.9.8 (2026-04-21)

- **Floating display feature** - Right-click style button to add "Float display" option, creating draggable floating style buttons
- **Multiple floating windows** - Support multiple floating buttons, each click creates a new window
- **Position memory** - Floating button position, opacity, and size persisted after plugin restart
- **Interaction** - Hold to drag position, left-click to apply style to selected text, Ctrl+scroll for opacity, Alt+scroll for size
- **Right-click menu** - Added "Close floating display" option to floating button right-click menu
