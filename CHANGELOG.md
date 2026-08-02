# Changelog

All notable changes to this project will be documented in this file.

## 🆕 v2.0.4 (2026-08-03)

- **AI Prompt Panel Rewrite / AI提示词面板重写** — Multi-select chips with combined prompts, removed reply length setting (users set length in prompt text directly) / 多选chip组合提示词，移除回复长度设定（用户直接在提示词中写长度）
- **Preset Prompts in Settings / 预设提示词移至设置** — 4 preset prompts moved to info settings under custom prompts, fully editable/deletable / 4个预设提示词移到info设置自定义提示词下，可编辑删除
- **Preset Prompt i18n / 预设提示词国际化** — Preset prompts auto-translate on language switch via _isPreset flag; editing a preset converts it to custom / 预设提示词语言切换时自动翻译；编辑后变为自定义提示词
- **New Install Defaults / 新装默认值** — showInfoSection defaults to true; floating notes include consultation info preset (hidden by default) / 显示Info板块默认开启；悬浮笔记包含咨询信息预设（默认隐藏）

## v2.0.3 (2026-08-03)

- **GridStack 24-Col CSS Fix / GridStack 24列CSS修复** — Injected dynamic `.gs-24` CSS rules for widget width/left positioning (gridstack.min.css only had `.gs-12` rules, causing widgets to collapse to 0 width) / 注入24列CSS规则修复卡片宽度坍缩（gridstack.min.css仅有12列规则，导致卡片宽度为0）
- **Drag Handle SVG / 拖动手柄SVG** — Replaced text character with 6-dot SVG icon, unified desktop/mobile appearance / 用6点SVG图标替换文字字符，桌面/手机统一样式
- **Info Color Scheme / Info配色方案** — Replaced preset palettes with custom color pickers (section bg + card bg) + 6 preset schemes, card header set transparent / 自定义颜色选择器替换预设调色板（板块+卡片背景）+6组预设，卡片标题栏透明
- **Info Section Grid / Info板块网格** — Toggleable grid background on info section matching gridstack cell size for visual snapping guide / Info板块可切换网格背景，尺寸与gridstack吸附步长一致
- **Card Drag Fix / 卡片拖动修复** — Drag limited to drag handle only, card content/header don't trigger drag, fixes mobile scroll issue / 拖动仅通过手柄，卡片内容/标题栏不触发拖动，修复手机滚动问题
- **Floating Ball Style Edit / 悬浮球样式编辑** — Right-click shows options menu (edit class name + display text, or custom CSS), removes conflicting inline styles when applying class / 右键弹选项菜单（编辑类名+显示文字或自定义CSS），应用类名时移除冲突内联样式
- **Multi-line Remark Edit / 多行备注编辑** — Inline remark editing changed to textarea, Esc key saves content / 内联备注改为多行textarea，Esc键保存
- **New Install Defaults / 新装默认值** — showRuleSourceBadge, showRemarkBadge, chipHoverMode default to false; moved remark badge setting to display group above rule source badge / 规则来源标记、备注提示符、悬停模式默认关闭；备注提示符设置移至显示组规则来源标记上方

## v2.0.2.2 (2026-08-02)

- **GridStack.js Integration / GridStack.js集成** — Replaced masonry CSS columns with GridStack.js for free drag-and-drop resizable card layout / 用GridStack.js替换masonry布局，实现自由拖拽调整大小的卡片布局
- **Inline Resource Loading / 内联资源加载** — GridStack JS/CSS loaded via adapter.read() and injected inline to bypass CSP restrictions / 通过adapter.read()读取并内联注入GridStack JS/CSS，绕过CSP限制
- **GridStack Layout Persistence / GridStack布局持久化** — Layout saved as {x,y,w,h} per card in infoGridLayout, replacing old height-only infoCardLayout / 每张卡片布局保存为{x,y,w,h}到infoGridLayout，替换仅高度的infoCardLayout
- **GridStack Resize Freedom / GridStack自由调整** — disableOneColumnMode, all 8 resize handles, alwaysShowResizeHandle, minW=1 for full resize freedom / 禁用单列模式，8方向resize手柄，始终显示手柄，最小宽度1列
- **Hover Popup Info at Top / 悬停弹窗info置顶** — Info section moved to top of hover popup content instead of bottom / Info板块移至悬停弹窗内容顶部
- **Sidebar Info Restoration / 侧边栏info恢复** — Modal info section recreated after hover popup closes, fixing addInfoSection closure overwriting / 悬停弹窗关闭后重建面板info板块，修复闭包覆盖问题
- **Non-Keyword Info Hiding / 非关键词info隐藏** — Info section hidden when selecting non-keyword text, shown when selecting keyword / 选中非关键词时隐藏info板块，选中关键词时显示
- **Non-Keyword Style Chip Hiding / 非关键词样式chip隐藏** — Editing chip hidden when selecting non-keyword text via _refreshUpdateChip / 选中非关键词时通过_refreshUpdateChip隐藏样式chip
- **English Translation Fix / 英文翻译修复** — Replaced "关键词" with "keyword" in 3 English translation strings / 3处英文翻译中"关键词"改为"keyword"

## v2.0.2.1 (2026-08-01)

- **Hover Mode Translation / 悬停模式翻译** — Added missing English translation for "桌面端鼠标悬停模式" setting label / 补充"桌面端鼠标悬停模式"设置的英文翻译
- **CSS Tab Context Menu: Copy Full Style / CSS tab右键菜单：复制完整样式** — Replaced "Add as Global Rule" option with "Copy Full Style" in style button right-click menu / 样式按钮右键菜单中"添加为全局规则"替换为"复制完整样式"
- **Keyword Group Toggle Inline / 关键词分组toggle内联** — Group collapse/expand toggle button placed inside groupGrid (same line as rules), hidden when collapsed, dynamically moved to visible grid on group switch / 分组折叠/展开按钮放入groupGrid内（与规则同行），折叠时隐藏，切换分组时动态移动到可见grid
- **Keyword Group Count Badge / 关键词分组计数** — Added count badge at end of each group showing keyword count / 每个分组末尾添加关键词数量计数badge
- **Remark Settings Button / 备注设置按钮** — Added settings button (font size/line height sliders) next to keyword remarks title, inline expand like related highlights; removed font/line-height from popup settings panel / 关键词备注标题旁添加设置按钮（字体/行距slider），内联展开；移除弹窗设置中的字体/行间距项
- **Related Keywords SVG Fix / 关联词SVG修复** — Changed textContent to innerHTML for related keywords title so SVG icon renders correctly / 关联词标题改用innerHTML使SVG图标正确渲染
- **Emoji to SVG in English / 英文翻译emoji替换SVG** — Replaced 📝🔗🤖 emojis in English translations with SVG icons matching Chinese version / 英文翻译中emoji替换为与中文一致的SVG图标
- **Hover Popup Without Remark / 无备注时悬停弹窗** — Hover popup now shows when rule regex exists (has related highlights/documents) even without remark content / 有规则regex（相关高亮/文档）时即使无备注也显示悬停弹窗

## v2.0.2 (2026-08-01)

- **Tooltip Disabled State / Tooltip禁用状态** — "Add as Global Rule" and "Add as File Rule" options in style button tooltip now appear grayed out and non-clickable when no text is selected, instead of silently doing nothing / 未选中文字时样式按钮tooltip中"添加为全局规则"和"添加为文件规则"选项显示为灰色不可点击，而非静默无反馈
- **Floating Ball Action Buttons Redesign / 悬浮球操作按钮重设计** — c/i/g/l buttons redesigned as circular icons that expand to pill shape on hover with label text, using purple accent color (#7c6cf0) matching the floating ball gradient / c/i/g/l按钮改为圆形图标，悬停展开药丸形显示文字标签，使用紫色accent配色呼应悬浮球渐变
- **Right-Side Expansion / 右侧展开方向** — When floating ball is on the right side of screen, action buttons expand text to the left instead of right / 悬浮球在右侧时按钮文字向左展开
- **g/l Toggle Capsule / g/l胶囊切换** — g/l button changed from single text to capsule toggle with circular sub-items, active item highlighted with purple background / g/l按钮改为胶囊toggle，圆形子项，激活项紫底紫字

## v2.0.1.3 (2026-08-01)

- **EditingChip Click Opens CSS Editor / 样式Ghip点击打开CSS编辑器** — Clicking the editingChip now opens CSSEditorModal instead of canceling edit / 点击editingChip现在打开CSS编辑器而非取消编辑
- **Switch Style No Longer Collapses CSS Tab / 切换样式不再折叠CSS tab** — "Switch style" action only opens the style chip if not already pinned, preventing unintended collapse / 切换样式时仅在未展开时才点击styleChip，避免意外折叠
- **Style Button Hover Tooltip / 样式按钮悬停提示** — Added interactive tooltip on style buttons with primary options (Edit, Add as Global Rule, Add as File Rule, Delete Style) and expandable secondary options / 样式按钮添加悬停交互式tooltip，主要选项始终可见，次要选项可展开
- **Tooltip Expand Button / 提示展开按钮** — Bar-shaped expand button at tooltip bottom reveals secondary options (Copy Full Style, Float Display, Format5 Format Replace, Move to Group, Add as Heading Style) / 底部条形展开按钮显示次要选项
- **Remove Update Rule Button / 移除更新规则按钮** — Removed the "Update Rule" button from input area as it's no longer needed / 移除输入框中的"更新规则"按钮
- **EditingChip Hidden for Non-Rule Text / 非规则文本时隐藏editingChip** — editingChip only shows when input text matches the current editing rule's regex / 输入文本不匹配当前编辑规则时隐藏editingChip
- **Global Rule Duplicate Prevention / 全局规则重复防护** — Clicking style button when a global rule already exists for the same regex now shows a notice instead of adding a duplicate file rule / 全局规则已存在时点击样式按钮仅提示，不再添加重复文件规则
- **Dynamic Rule Existence Check / 动态规则存在检查** — Style button click handler now dynamically checks rule existence instead of using stale closure variables / 样式按钮click处理器改为动态检查规则存在性，不再使用过期闭包变量
- **Highlight Dedup Safety Net / 高亮去重安全网** — allRules merged from file+global rules now deduplicates by regex+cssClass to prevent double highlighting / 合并fileRules和globalRules时按regex+cssClass去重，防止双重高亮
- **Sentence Rule Global Rule Guard / 长句全局规则防护** — addGlobalRule now rejects regex exceeding sentence threshold (CN≥8 chars / EN≥3 words) with notice / addGlobalRule拒绝超过句子长度阈值的regex并提示
- **addGlobalRule Returns Boolean / addGlobalRule返回布尔值** — Returns false on rejection (sentence rule), true on success; callers only show success notice on true / 拒绝时返回false，成功时返回true；调用方仅true时显示成功提示
- **Remove Duplicate Middle-Click Handlers / 移除重复中键处理器** — Removed redundant mousedown middle-click handlers (keeping auxclick only), eliminating double Notice issue / 移除冗余mousedown中键处理器（仅保留auxclick），消除双重Notice问题
- **Direct globalRules.push Replaced / 直接push替换为addGlobalRule** — All 3 places that bypassed addGlobal1Rule with direct globalRules.push now use addGlobalRule for consistent sentence rule checking / 3处绕过addGlobalRule的直接push改为调用addGlobalRule
- **Style Button Tooltip Guard / 样式按钮tooltip防遮挡** — Tooltip positioned below button with guard: skips creation if existing tooltip is being hovered / tooltip定位在按钮下方，若当前tooltip正被悬停则不创建新tooltip
- **Complex Regex Keyword Highlighting / 复杂正则关键词高亮** — _buildKeywordRanges now supports complex regex (lookbehind, non-capturing groups) via RegExp matching instead of skipping all / _buildKeywordRanges支持复杂正则（lookbehind、非捕获组）通过RegExp匹配而非跳过
- **_extractPlainText Non-Capturing Group / _extractPlainText非捕获组** — Added (?:...) removal in _extractPlainText for proper plain text extraction / _extractPlainText添加(?:...)移除以正确提取纯文本
- **Click-Show Remark Dblclick Edit Fix / 点击显示评论双击编辑修复** — Row click handler now excludes remarkSpan.contains(e.target), allowing dblclick on remark to trigger edit / row click排除remarkSpan上的点击，使dblclick编辑正常触发
- **Remark Display Mode Instant Refresh / 评论显示方式即时刷新** — Changing display mode now immediately updates all visible remark elements via cloneNode + _SG_APPLY_REMARK_DISPLAY rebind / 切换显示方式时用cloneNode+重新绑定立即更新所有可见评论元素
- **Always Mode Remark Display Fix / 常显模式评论显示修复** — _SG_APPLY_REMARK_DISPLAY now sets remarkSpan.style.display='' for 'always' mode instead of returning silently / 常显模式现在设置display=''而非静默返回
- **Remark Keyword Matching / 评论关键词匹配** — Keywords in highlight comments now display with their CSS class styles and are clickable to open keyword window / 高亮评论中的关键词现在以CSS类样式显示，可点击打开关键词窗口
- **Float Button Data Empty JSON Fix / 悬浮按钮数据空JSON修复** — JSON.parse now checks for empty content before parsing, preventing "Unexpected end of JSON input" error / JSON.parse前检查空内容，防止解析空文件报错

## v2.0.1.2 (2026-07-29)

- **Prompt Dialog Fix / prompt()对话框修复** — Replaced browser `prompt()` with custom InputModal in Electron environment, fixing "prompt is not defined" error / Electron环境中用自定义InputModal替代prompt()，修复未定义错误
- **Collapsed Note Disappear Fix / 折叠笔记消失修复** — `renderGlobalNotesArea()` now removes both `.global-note-card` and `.global-note-mini` to prevent stale DOM references from mini restoreCard / 渲染时同时移除card和mini，防止mini的restoreCard引用已删除DOM
- **Drag Auto-Expand Fix / 拖动自动展开修复** — Added drag state guard in mini click handler; mouseup uses requestAnimationFrame to reset drag flag after event processing / mini click添加拖动状态守卫，mouseup延迟重置拖动标志
- **Drag Position Save / 拖动位置保存** — Collapsed mini drag now saves position to `_collapsedPos` and persists via saveGlobalNotes / 折叠mini拖动后保存位置到_collapsedPos并持久化
- **Window Size Loss Fix / 窗口大小丢失修复** — 5-layer protection: ResizeObserver skips hidden/small sizes; collapseToMini saves pre-collapse rect; restoreCard restores size; saveGlobalNotes/onunload clean 0px data / 5层防护：ResizeObserver跳过隐藏/小尺寸，折叠前保存尺寸，展开时恢复，保存/卸载时清理0px
- **Mobile Chip First-Click Fix / 手机chip首次点击修复** — Used capture-phase handler with `_chipsRevealTime` timestamp guard (400ms) to prevent chip activation during reveal animation / 用capture-phase handler加时间戳守卫，防止reveal动画期间激活chip
- **Mobile Settings Bar Drag / 手机设置栏拖动** — Added touchstart/touchmove/touchend drag support on settings bar for floating panel position adjustment / 设置栏添加触摸拖动支持，可调整悬浮面板位置
- **Panel Dblclick Scroll Fix / 面板双击跳顶修复** — Removed dblclick handlers on remarkContainer and kw-chip that called showInlineRemarkForRegex (causing DOM rebuild and scrollTop reset); dblclick now only prevents text selection / 移除remarkContainer和kw-chip的dblclick handler（调用showInlineRemarkForRegex导致DOM重建和scrollTop重置），dblclick仅阻止文本选择
- **Related Keyword Chip Click Fix / 关联词chip点击修复** — Changed related keyword chip click from showInlineRemarkForRegex to openKeywordWindow, preventing panel content rebuild and scroll reset / 关联词chip点击改为openKeywordWindow，不再重建面板内容导致滚动重置
- **ScrollTop Preservation / scrollTop保持** — showInlineRemarkForRegex uses `_preservedScrollTop` instance property to pass scroll position through refreshModalContent chain; _showInlineRemarkForRules uses setTimeout(0) instead of rAF for reliable restore / 用_preservedScrollTop实例属性在refreshModalContent链路中传递scrollTop，用setTimeout(0)替代rAF确保可靠恢复
- **Mini Note Touch/Click Fix / 迷你笔记触摸点击修复** — Unified touch and click handling: touchstart no longer preventDefault (allows native click); touchend calls restoreCard with vibrate feedback; click handler checks _touchRestored flag to prevent double invocation / 统一touch/click处理：touchstart不再preventDefault，touchend调restoreCard并震动反馈，click检查_touchRestored防止双重调用
- **Mobile Haptic Feedback / 手机震动反馈** — Collapsed mini note tap now triggers navigator.vibrate(30) for tactile confirmation / 点击折叠mini笔记时触发navigator.vibrate(30)提供触觉反馈
- **Card Touchstart Skip Action Bar / 卡片touchstart跳过操作栏** — Card touchstart drag handler now skips .note-action-bar, .note-collapse-btn, .note-copy-btn, .note-palette-btn and interactive elements / 卡片touchstart拖拽handler跳过操作栏和交互元素，不再干扰按钮点击
- **Floating Ball Toggle as Checkbox / 悬浮球开关改复选框** — Replaced "Show/Hide Floating Ball" chip with native checkbox in settings chips row, avoiding touch/click event competition on mobile / 将"显示/隐藏悬浮球"chip替换为原生checkbox放在设置chip行，避开手机端touch/click事件竞争
- **Settings Bar Click Exclusion / 设置栏click排除** — Settings bar click/touchstart/mousedown handlers now exclude .floating-ball-toggle-chip, .settings-popup-window, and interactive elements (input, button, select, a, .setting-item, .clickable-icon) / 设置栏click/touchstart/mousedown排除复选框、弹窗内和交互元素
- **Dblclick Debug Logs Cleanup / 双击调试日志清理** — Removed console.log debug statements from remarkContainer dblclick and chip-click handlers / 移除remarkContainer dblclick和chip-click中的console.log调试语句

## v2.0.1.1 (2026-07-28)

- **Update Rule Button Redesign / 更新规则按钮重设计** — Moved "Update Rule" button inside regex input as a compact pill, hidden by default, only shown after clicking a rule button / "更新规则"按钮移入输入框内部药丸形，默认隐藏，仅点击规则按钮后显示
- **Update Rule Logic Fix / 更新规则逻辑修复** — `currentEditingRule` only set when user clicks a rule button, reset on input change; prevents false activation when selecting non-rule text / 仅点击规则按钮时设置currentEditingRule，输入变化时重置，防止选中非规则文本时误激活
- **Color Scheme Save as New / 配色方案保存为新方案** — "Save as New" now adds a new preset instead of replacing the original; auto-renames on ID conflict / "保存为新方案"现在新增而非替换原方案，ID冲突时自动重命名
- **Related Highlights Settings / 相关高亮设置** — Added gear icon with settings popup for both "Non-Keyword Related Highlights" and "Keyword Related Highlights": font size, line height, uniform keyword style, click-to-show remarks / 两种相关高亮均添加齿轮设置按钮：字体大小、行距、关键词样式统一、高亮评论点击显示
- **Related Highlights Renamed / 相关高亮改名** — Distinguished two types: "Non-Keyword Related Highlights" (shown when selecting non-rule text) and "Keyword Related Highlights" (shown when clicking a keyword) / 区分两种相关高亮："非关键词相关高亮"和"关键词相关高亮"
- **Uniform Keyword Style / 关键词样式统一** — New setting to unify all keyword highlight styles to a single CSS class, fallback to original style when empty / 新增设置统一所有关键词高亮样式为指定CSS类名，空值时用原样式
- **Click-to-Show Remarks / 高亮评论点击显示** — New toggle to hide remark bubbles by default and show on click, reducing space when many highlights have comments / 新增开关默认隐藏评论气泡，点击显示，减少多高亮时的空间占用
- **Chip Hover Mode for Groups / 分组悬停模式** — Keyword group chips now respect "Desktop Hover Mode" setting; unchecking disables hover-expand for groups / 关键词分组chip现在受"桌面端鼠标悬停模式"控制
- **Float Note Width Fix / 悬浮笔记宽度修复** — Removed maxWidth lock from saved width; 0px values skipped; restored max-width:480px / 移除maxWidth锁定，0px值跳过，恢复max-width:480px
- **Panel Card Height Fix / 面板笔记高度修复** — Removed `_panelCardHeight` mechanism=that locked minHeight causing blank space; height now auto-adapts to content / 移除_panelCardHeight机制，高度由内容自适应，不再有底部空白
- **Dblclick Edit Fix / 双击编辑修复** — Removed `span[style]` guard that blocked dblclick on note text; double-click now works on text directly / 移除span[style]守卫条件，双击文字可直接进入编辑
- **chipBar Position Fix / chipBar位置修复** — Fixed chipBar being moved out of chipContentSection by `_showInlineRemarkForRules` / 修复chipBar被_showInlineRemarkForRules移出chipContentSection
- **Keyword Click Fix / 关键词点击修复** — Clicking keywords in related highlights now opens independent keyword window (openKeywordWindow) instead of inline panel / 点击相关高亮中的关键词现在打开独立窗口而非面板内显示
- **saveSettings Error Fix / saveSettings错误修复** — Fixed `this.plugin.saveSettings is not a function` error, changed to `this.plugin.saveData()` / 修复saveSettings未定义错误

## v2.0.1.1 (2026-07-26)

- **Mobile Floating Note Toolbar / 手机悬浮笔记操作栏** — Toolbar now hidden by default on mobile, tap card content to toggle show/hide instead of always blocking text / 手机端操作栏默认隐藏，点击卡片内容切换显示，不再遮挡文字
- **Collapsed Note Drag Fix / 折叠笔记拖动修复** — Desktop: dragging mini no longer triggers expand on mouse release; collapsed state persisted via `_collapsed`/`_miniPos` so notes stay collapsed across re-renders, restarts, and view switches / 桌面端拖动mini释放鼠标不再展开；折叠状态持久化，重启/切换视图/重新渲染后保持折叠
- **Collapsed Note Drag Fix / 折叠笔记拖动修复** — Desktop: dragging mini no longer triggers expand on mouse release; collapsed state persisted via `_collapsed`/`_miniPos` so notes stay collapsed across re-renders, restarts, and view switches / 桌面端拖动mini释放鼠标不再展开；折叠状态持久化，重启/切换视图/重新渲染后保持折叠
- **Mobile History Keywords Always Visible / 手机端历史关键词常显** — History keyword section always visible on mobile; clear button only clears chips, not the section itself; mobile keyword clicks now add to history / 手机端历史关键词区块常显，清空仅清chip，手机端点击关键词添加历史
- **Mobile Del Button / 手机端删除按钮** — Added "del" button below c/i/g/l buttons near floating ball for quick rule deletion on mobile / 悬浮球旁c/i/g/l按钮下方添加del按钮，手机端快速删除规则
- **Mobile Main Panel Scroll / 手机端主面板滚动** — Content area now allows vertical scroll (pan-y) instead of requiring tap on blank area / 内容区域允许垂直滚动，无需在空白区域下手
- **Mobile Main Panel Drag / 手机端主面板拖动** — Settings bar bottom supports touch drag (floating panel only, not sidebar); resize handle follows panel position during drag / 设置栏底部支持触摸拖动（仅悬浮面板不含右侧面板）；拖动时resize handle跟随
- **Mobile Sidebar Match Fix / 手机端侧边栏匹配修复** — After closing and reopening main panel, clicking keywords now correctly shows matches in sidebar / 关闭主面板后再点击关键词，右侧面板正确显示匹配
- **Floating Note Edit Style / 悬浮笔记编辑样式** — Removed border and border-radius from edit textarea; edit area fills note window size / 编辑框去掉边框和圆角，编辑区域自适应窗口大小
- **Related Highlights for Rule Keywords / 规则关键词相关高亮** — Keywords with matching rules (e.g. "昆德拉", "马克思") now show related highlights and backlinks in main panel, previously only shown when no matching rule existed / 有匹配规则的关键词（如"昆德拉"、"马克思"）现在也显示相关高亮和反向引用

## v2.0.1 (2026-07-26)

- **SG Sentence Keyword Non-clickable / SG句子关键词不可点击** — Removed click handler from SG sentence keywords in related highlights (both main panel and keyword popup) to avoid redundant popup showing the same sentence / 移除相关高亮中SG句子规则关键词的点击事件，避免打开弹窗重复显示相同句子

## v2.0.0 (2026-07-26)

- **Related Highlights Tooltip Bilingual / 相关高亮提示双语** — Fully translated Related Highlights help tooltip to bilingual format (Display logic, Suggested usage, Remark style, etc.) / 相关高亮帮助提示完整双语翻译（显示逻辑、建议用法、备注样式等）
- **Modal Initial Position Fix / 主面板初始位置修复** — Fixed main panel briefly appearing at top-left corner on first open by adding centered transform in constructor / 修复首次打开主面板时短暂出现在左上角，构造时添加居中transform
- **Dark Theme Cursor Fix / 深色主题光标修复** — Added caret-color matching text color for floating notes in editing mode, fixing invisible cursor on dark color schemes / 添加与文本颜色匹配的caret-color，修复深色配色方案下光标不可见
- **Note Undo Delete / 笔记误删恢复** — Deleted notes now show a 5-second pulse countdown button near the floating ball for undo recovery / 删除笔记后在悬浮球附近显示5秒脉冲倒计时按钮可恢复
- **Sidebar Transform Fix / 侧边栏transform修复** — Properly clear transform CSS when moving modal to sidebar to prevent layout issues / 模态框移入侧边栏时正确清除transform防止布局异常

## v1.9.9.17.5 (2026-07-26)

- **Section Toggle Buttons / 区块折叠按钮** — Added ▽/▷ collapse toggle to Related Notes, Related Highlights, Keyword Remarks, Related Keywords, and AI Questions section headers; right-click to remember expand/collapse state / 在相关文档、相关高亮、关键词备注、关联词、AI提问标题前添加折叠按钮，右键可记住展开/折叠状态
- **Related Highlights Help Icon / 相关高亮问号图标** — Added ❓ icon after "Related Highlights" header showing tips on display logic, usage suggestions, and remark style switching / "相关高亮"标题后添加问号图标，点击显示显示逻辑、建议用法、备注样式切换提示
- **Related Highlights Match Remarks / 相关高亮匹配备注** — Search terms appearing in highlight comments/remarks now also trigger related highlights display / 搜索词出现在高亮备注中时也会显示相关高亮
- **Keyword Window for No-Remark Keywords / 无备注关键词弹窗** — Clicking keywords without remarks now opens popup window showing related notes and highlights / 点击无备注关键词也能打开弹窗显示相关文档和相关高亮
- **History Keywords Filter / 历史关键词过滤** — History keywords now only show rules-based keywords, default 10 items with expand button for more / 历史关键词仅显示规则中的关键词，默认10个，更多需展开
- **AI Questions "+" Button Position / AI提问按钮位置** — Moved "+" button to title bar right side, consistent with Related Keywords layout / "+"按钮移至标题栏右侧，与关联词布局一致
- **rule.links Safety Fix / rule.links安全修复** — Fixed TypeError when iterating rule.links that was undefined after delete operation / 修复rule.links被delete后迭代报错

## v1.9.9.17.3 (2026-07-26)

- **Related Highlight Keyword Style Fix / 相关高亮关键词样式修复** — Fixed keyword CSS style being applied to entire highlight entry instead of only matched keyword segments; created `_buildKeywordRanges` helper for precise text segmentation / 修复关键词CSS样式被应用到整段高亮条目而非仅匹配的关键词片段；新增_buildKeywordRanges辅助函数进行精确文本分段
- **Related Highlight Unified Background / 相关高亮统一背景** — Added consistent `rgba(255,235,100,0.12)` background to all related highlight entries (both SG sentences and OB highlights) / 所有相关高亮条目（SG句子和OB高亮）统一添加淡黄色背景
- **Mobile Panel Resize Fix / 手机端面板resize修复** — Fixed duplicate resize handles by removing independent mobile handle and adding touchstart/touchmove/touchend support to existing `setupModalResizeHandle`; enlarged handle to 28px on mobile / 修复重复resize按钮问题，删除独立手机端handle，在setupModalResizeHandle中添加touch支持，手机端handle放大到28px
- **Mobile Sidebar Resize Handle Removal / 手机端侧边栏resize按钮移除** — Sidebar onOpen now removes modal-resize-handle from modalEl when panel enters sidebar / 侧边栏打开时移除面板中的resize handle
- **Mobile Mini Note Click Fix / 手机端迷你笔记点击修复** — Fixed touchstart preventDefault blocking click event on mini notes; touchend now directly calls restoreCard when no drag detected / 修复touchstart的preventDefault阻止迷你笔记click事件，touchend中未拖动时直接调用restoreCard展开
- **Mobile Inline Note Custom Resize / 手机端内嵌笔记自定义resize** — Replaced native CSS resize:both with custom 20px touch resize handle for better mobile usability / 替代原生CSS resize:both为20px自定义触摸resize handle，提升手机端操作体验
- **Mobile Inline Note Collapse Button / 手机端内嵌笔记折叠按钮** — Added SVG collapse/mini button to inline note toolbar on mobile (equivalent to desktop middle-click) / 手机端内嵌笔记操作栏添加SVG折叠按钮（等同桌面端中键点击）
- **Panel Lock State Fix / 面板锁定状态修复** — Removed desktop-only check from outside-click handler; locked panels now can only be closed via close button on all platforms / 移除外部点击handler的桌面端限制，锁定状态面板在所有平台只能通过关闭按钮关闭
- **Middle-Click Link Fix / 中键链接修复** — Fixed middle-click on file links opening new window but not navigating to document; added metadataCache.getFirstLinkpathDest with fallback / 修复中键点击文件链接打开新窗口但未导航到文档的问题，添加metadataCache解析和fallback

## v1.9.9.17 (2026-07-25)

- **AI Graph Button Position Fix / AI关系图按钮位置修复** — Moved ⬡ button back to related keywords block header instead of AI question block / 将⬡按钮移回关联词标题栏，不再显示在AI提问块
- **AI Question Block Collapse / AI提问块折叠** — Added ▽/▷ collapse toggle button in AI question block header / 在AI提问块标题栏添加折叠按钮，可折叠/展开内容
- **No-Title Chip Removal / 无标题chip移除** — Removed residual no-title chip at bottom of keyword remarks block for AI-only groups / 移除关键词备注底部AI提问分组残留的无标题chip

## v1.9.9.16 (2026-07-24)

- **Masonry Mode Button in Remark Block / 瀑布流按钮移至备注块内** — Moved masonry toggle button from window header to inside the keyword remarks block; button only affects remarks content, not related notes/highlights / 瀑布流切换按钮从窗口标题栏移至关键词备注块内，仅作用于备注内容
- **Auto Masonry Mode / 自动瀑布流模式** — New remarkMasonryAuto setting (default on): 1 remark → list, multiple → masonry; manual override via button / 新增自动瀑布流设置，1条备注→列表，多条→瀑布流，可通过按钮手动覆盖
- **Remark & Keywords as Independent Blocks / 备注与关联词独立块** — Remark content wrapped as "关键词备注" block, keyword chips wrapped as "关联词" block, consistent with related notes/highlights style / 备注内容包裹为"关键词备注"独立块，关联词chips包裹为"关联词"独立块，与相关笔记/高亮样式一致
- **AI Relation Graph in Keywords Block / AI关系图移入关联词块** — Graph section rendered inside keyword-chips-block below chips, collapsed by default with ▸/▾ toggle / 关系图渲染在关联词块内部chips下方，默认折叠，点击▸/▾展开
- **AI Graph Persistence Fix / AI关系图持久化修复** — Fixed loadFileRulesFromPath dropping _mermaidGraph; existing graph now renders in kwBlock after switching keywords / 修复文件规则加载时丢失_mermaidGraph，切换关键词后已有关系图正确渲染
- **AI Graph Max Tokens Setting / AI关系图Max Tokens设置** — New aiGraphMaxTokens setting (default 4096) in AI settings panel / AI设置面板新增Max Tokens设置项
- **Exclude Related Highlights / 排除相关高亮** — excludedRelatedNotesCategories now also excludes related highlights, not just related notes / 排除相关笔记分组设置同时排除相关高亮
- **Scroll Position Restore / 滚动位置恢复** — Panel preserves scroll position when toggling masonry mode / 面板切换瀑布流模式时保持滚动位置
- **Unified aiBtnContainer Sticky / 统一?+按钮粘底** — Both keyword-detail-window and remark-custom-popup use position:sticky for aiBtnContainer; kwBlock inserted before aiBtnContainer / 两种弹窗统一使用sticky粘底，kwBlock插入在aiBtnContainer之前
- **CodeMirror Import Fix / CodeMirror导入修复** — Added require('@codemirror/state') and require('@codemirror/view') for StateEffect, StateField, EditorView, Decoration / 添加CodeMirror 6依赖导入

## v1.9.9.15 (2026-07-24)

- **Related Keywords Chip Fix / 关联词chip修复** — Sentence length threshold no longer applies to related keywords in remark popup; all related keywords now display as compact keyword-chips instead of full-width sentence-chips / 句子长度阈值不再作用于备注弹窗底部的关联词，统一渲染为关键词chip
- **Inline Note Action Bar Drag / 内嵌笔记操作栏拖动** — Action bar blank area now supports drag to move the note card; button clicks unaffected / 操作栏空白区域可拖动移动卡片，按钮点击不受影响
- **Color Scheme Sync Fix / 配色方案同步修复** — Fixed `_syncNoteTheme` using wrong selectors (`.fn-text`→`.global-note-text`), color scheme changes in panel now correctly sync to inline notes / 修复配色方案切换时内嵌笔记颜色不同步的问题
- **Related Notes → Related Files / 相关笔记改为相关文档** — Renamed "相关笔记" to "相关文档" (Related Files) with document count displayed after the title / "相关笔记"更名为"相关文档"，标题后显示文档数量
- **Related File Name Truncation / 相关文档名称截断** — Long file names auto-truncate with ellipsis; no horizontal scrollbar in related files section / 长文件名自动截断显示省略号，不出现横向滚动条
- **Settings Panel Drag / 设置面板拖拽** — Settings popup blank area supports drag to move position on both desktop and mobile; drag position preserved after MutationObserver reposition / 设置面板空白区域支持拖拽移动，拖动后位置不被重置
- **Lookahead/Lookbehind Highlight Fix / lookahead规则高亮修复** — Removed `includes(_extractPlainText(term))` fallback in related highlights matching; regex like `意识(?!到|不)` no longer incorrectly matches "意识到"/"意识不" / 移除纯文本包含匹配fallback，lookahead规则不再错误匹配排除文本
- **Regex Rule Chip Display / 正则词chip显示修复** — Added `_regexMatch` matching condition for selected text; regex rules like `bc|d` and `意识(?!到|不)` now correctly show chips when text is selected / 添加正则匹配条件，正则词关键词选中后正确显示chip
- **Chinese Class Name Scheme Fix / 中文类名配色方案修复** — Class name regex changed from `[a-zA-Z0-9_-]+` to `[\w\u4e00-\u9fff-]+`; Chinese class names like `.蓝眼泪` now correctly show "Update" button instead of "Save as New" / 类名正则支持中文，中文类名配色方案按钮正确显示"更新"
- **Inline Note Scroll Fix / 内嵌笔记滚动修复** — Card uses `overflow:hidden` with text area scrolling independently; timestamp fixed at bottom; no double scrollbar in edit mode / 卡片overflow:hidden，文本区域独立滚动，时间戳固定底部，编辑时无双滚动条
- **Inline Note Edit Height Fix / 内嵌笔记编辑高度修复** — Card height locked before entering edit mode; `_floatSize` saves actual height instead of `'auto'`; height restored after restart / 编辑前锁定卡片高度，保存实际高度而非'auto'，重启后恢复正常高度

## v1.9.9.14 (2026-07-23)

- **Sentence Length Threshold / 句子长度阈值** — Added settings for Chinese character count (default 8) and English word count (default 3) to distinguish keyword rules from sentence rules; sentences displayed differently in panel / 新增中文字数（默认8）和英文词数（默认3）阈值设置，区分关键词与句子规则，句子在面板中以不同方式显示
- **Remark Keyword Chips / 备注区域关键词chips** — Replaced pipe-separated keyword display with clickable chips; default shows first keyword, click to switch; related highlights follow active chip / 替代"|"分隔显示为可点击chips，默认显示第一个关键词，点击切换，相关高亮跟随当前chip
- **SG Sentence Related Highlights / SG句子相关高亮** — Sentence rules shown as related highlights with source file name and jump-to-position; merged with OB highlights in same section, no separate display / 句子规则以相关高亮形式显示，带源文件名和跳转定位，与OB高亮合并在同一区域
- **g/l Button / g/l按钮** — Added g/l button to floating ball action buttons for switching rules between global and file scope / 悬浮球操作按钮新增g/l按钮，在全局与文件规则间切换
- **Unified c/i/g/l Buttons / 统一c/i/g/l按钮** — Simplified to plain text without border/background, vertically displayed below floating ball; unified desktop and mobile style / 简化为纯文本无背景边框，纵向挂在悬浮球下方，桌面端与手机端统一
- **Desktop Click-to-Show Buttons / 桌面端点击显示按钮** — Click highlighted keyword directly shows c/i/g/l buttons without selecting text first / 点击高亮关键词直接显示按钮，无需先选中文本
- **Mobile Button Display / 手机端按钮显示** — c/i/g/l buttons now shown on mobile when tapping highlighted keywords; removed desktop-only restriction / 手机端点击高亮关键词也显示c/i/g/l按钮，移除桌面端限制
- **Cross-File Rule Matching / 跨文件规则匹配** — Selecting text now searches other files' rules via `_fileRulesData`, matching long sentences defined in different files / 选中文本时跨文件搜索规则，匹配其他文件中定义的长句
- **i Button Keyword Support / i按钮关键词支持** — i button passes clicked keyword text to interlinear note input instead of requiring text selection / i按钮将点击的关键词文本传入行间注释输入，不再要求先选中文本
- **Button Flash Fix / 按钮闪现修复** — Added `_keepRuleActionButtons` flag to prevent `selectionchange` from removing buttons immediately after click / 添加标记防止selectionchange在点击后立即移除按钮
- **global-notes.json Auto-Repair / global-notes.json自动修复** — JSON parse failure now auto-truncates to longest valid prefix and saves; fixed `onunload` missing `defaultFnGroup` field causing concurrent write corruption / JSON解析失败时自动截断到最长合法前缀并保存；修复onunload缺少defaultFnGroup导致并发写入损坏

## v1.9.9.13 (2026-07-22)

- **Palette Button Scroll Switch / 调色盘按钮滚轮切换** — Scroll wheel on the color scheme palette button in inline notes and panel now directly switches color scheme with scheme name tooltip / 内嵌笔记和面板的调色盘按钮上滚轮可直接切换配色方案，显示方案名提示
- **Shift+Scroll Theme Sync Fix / Shift+滚轮切换同步修复** — Fixed box-shadow, backdrop-filter, and texture layer not updating when switching color scheme via Shift+scroll on inline notes / 修复内嵌笔记Shift+滚轮切换方案时box-shadow、backdrop-filter、纹理层未更新的问题
- **Exclude Related Notes Fix / 排除相关笔记功能修复** — Fixed `excludedRelatedNotesCategories` being stored but never consumed; related notes now correctly skip rules from excluded groups / 修复排除相关笔记分组只存不消费的bug，被排除分组的规则不再显示相关笔记
- **Smart Save Button Logic / 保存按钮智能逻辑** — Save button shows "Update" when only class name or only property values changed; shows "Add as New Scheme" when both class name and values differ / 仅改类名或仅改属性值显示"更新"，类名和属性值都改显示"添加为新方案"
- **i18n Translation / 国际化翻译** — Replaced ~90+ hardcoded Chinese strings with t() calls; added 70+ new translation keys (fn.*, kw.*, cmd.*, other.*, font.*); removed 25+ Chinese fallbacks / 替换约90+处硬编码中文为t()调用，新增70+翻译key，移除25+处中文fallback
- **Cross-View Theme Sync / 跨视图配色同步** — Color scheme changes in panel/inline/popout now instantly sync to all other views via `_syncNoteTheme` / 面板/内嵌/独立窗口配色切换后即时同步到其他视图
- **Panel Note Card Attributes / 面板笔记卡片属性** — Added `fn-panel-card` class and `data-note-id` attribute to panel note cards for reliable cross-view identification / 面板笔记卡片添加类名和data属性，确保跨视图识别
- **Inline Right-Click Panel Sync / 内嵌右键面板同步** — Delete note, show/hide floating, move to group operations in inline right-click menu now instantly refresh panel / 内嵌笔记右键菜单中删除/显隐/移动分组操作后即时刷新面板

## v1.9.9.12 (2026-07-22)

- **Panel Remark Double-Click Fix / 面板备注双击编辑修复** — Added container-level dblclick event delegation in `renderRemarkContent` so all remark elements (including AI question entries and non-masonry remarks) respond to double-click editing, not just masonry card remarks / 在`renderRemarkContent`中添加container级dblclick事件委托，所有备注元素（含AI问题条目和非masonry备注）均可双击编辑
- **Color Scheme Name Tooltip / 配色方案名提示** — Shift+scroll on floating notes now shows the scheme id as a temporary tooltip; works in both inline cards and popout windows / 悬浮笔记Shift+滚轮切换配色时显示方案名提示；内嵌卡片和独立窗口均支持
- **Inline Note Tooltip Position Fix / 内嵌笔记tooltip定位修复** — Tooltip changed to `position:fixed` on `document.body` with `getBoundingClientRect` positioning, preventing accidental change of card `position:fixed` to `relative` which caused the note window to disappear / tooltip改为fixed定位挂载到body，避免误将卡片position改为relative导致窗口消失
- **Inline Note Tooltip Cleanup / 内嵌笔记tooltip清理** — Tooltip stored on `card._schemeTip` to prevent duplicate creation on continuous scrolling; `card.remove()` overridden to auto-cleanup tooltip and timer when note closes / tip存储在card属性上避免连续滚动重复创建；覆写remove方法在关闭时自动清理tip和定时器

## v1.9.9.11 (2026-07-22)

- **Custom Schemes Migration / 自定义方案迁移** — Moved `customColorSchemes` from `global-notes.json` to `color-schemes.json`; old `{bg,text}` format converted to CSS rules; `sg-float-` prefix trimmed / 自定义配色从`global-notes.json`迁移到`color-schemes.json`；旧格式转为CSS规则；修剪`sg-float-`前缀
- **Smart Save Button / 智能保存按钮** — Save button hidden when no changes; shows "更新" when editing existing scheme, "保存为新方案" when creating new; class name changes correctly update instead of creating duplicates / 无变化时隐藏；编辑已有方案显示"更新"，新建显示"保存为新方案"；类名变更时正确更新而非新增
- **Unified Color Schemes / 统一配色方案** — New notes cycle through `colorSchemePresets` instead of hardcoded themes; removed `_panelThemes`, `_floatNoteThemes`, and popout `themes` arrays; all theme derivation now uses `schemeToTheme` from `colorSchemePresets` / 新建笔记循环使用配色方案预设；移除硬编码主题数组；所有主题推导统一使用`schemeToTheme`
- **Close Button Enhancement / 关闭按钮增强** — Tooltip shows "单击关闭/中键点击删除"; middle-click deletes note from `globalNotes`; works in both inline and popout windows / tooltip显示操作提示；中键从globalNotes删除笔记；内嵌和独立窗口均支持
- **Mobile Fixes / 手机端修复** — Color scheme popup now draggable via touch events; inline display button visible on mobile (previously desktop-only) / 配色弹窗支持触摸拖动；内嵌显示按钮在手机端可见
- **Related Keywords Per-Section / 相关词按分组显示** — Related keyword chips now render per-rule section (before 3 buttons) instead of all merged at bottom / 相关词按关键词分组渲染在各自3按钮上方，而非全部堆在底部
- **Remove + Button / 移除+按钮** — Removed "+" button from color scheme popup header / 移除配色弹窗右上角+按钮
- **Bug Fixes / 错误修复** — Fixed `inputValue is not defined` in `applyZoom`; fixed `insertBefore` error when section not in DOM; middle-click delete no longer closes panel / 修复`applyZoom`中未定义变量；修复`insertBefore`错误；中键删除不再关闭面板

## v1.9.9.10 (2026-07-21)

- **Color Scheme CSS Format / 配色方案CSS格式** — Scheme data refactored from custom JSON (`{bg,text,glow,glass,texture}`) to standard CSS rules (`.scheme-id { background:...; color:...; box-shadow:...; }`); id extracted from class name; no class name = invalid / 配色方案数据从自定义JSON重构为标准CSS规则格式；id从类名提取；无类名视为无效
- **Remove Scheme Grouping / 移除分组** — Removed `cat` field and grouped rendering; all 25 presets now display in a flat 5-column grid / 移除cat字段和分组渲染，25个预设平铺5列网格显示
- **Trim Class Names / 修剪类名** — Shortened CSS class names from `.sg-float-vintage-01` to `.vintage-01` for cleaner editing / CSS类名从`.sg-float-vintage-01`修剪为`.vintage-01`
- **Editable Scheme Code / 可编辑方案代码** — Read-only `<pre>` replaced with shared textarea; edits preview in real-time via `parseSchemeCss`; clicking a swatch shows its CSS rule / 只读`<pre>`替换为共用textarea；编辑时通过parseSchemeCss实时预览；点击色卡显示CSS规则
- **Add Scheme Button / 添加方案按钮** — "CSS" toggle replaced with "+" button; clears textarea for new scheme input; "Save" button parses CSS and adds to grid / "CSS"切换按钮替换为"+"按钮；清空textarea等待输入；"保存"按钮解析CSS并添加到网格
- **Middle-Click Delete / 中键删除方案** — Middle-click a swatch to delete its scheme; confirmation dialog with "don't ask again" checkbox (stored in localStorage) / 中键点击色卡删除方案；确认弹窗含"不再询问"复选框（存localStorage）
- **Swatch Selection Border Fix / 色卡选中边框修复** — Used `selectedSwatch` variable to track selection instead of unreliable style attribute matching / 用selectedSwatch变量追踪选中状态，替代不可靠的style属性匹配
- **Popout Palette Button Removed / 移除独立窗口配色按钮** — Removed non-functional palette button from popout window titlebar / 移除独立窗口标题栏中不工作的配色按钮
- **Popout Texture z-index Fix / 独立窗口纹理z-index修复** — Changed texture layer z-index from -1 to 1; added z-index:2 to titlebar/content/timestamp for interaction / 纹理层z-index从-1改为1；titlebar/content/timestamp加z-index:2确保可交互
- **Legacy Format Compatibility / 旧格式兼容** — `schemeToTheme` now handles both new CSS format and legacy `{bg,text}` format for backward compatibility / schemeToTheme兼容新CSS格式和旧{bg,text}格式
- **Custom Schemes Migration / 自定义方案迁移** — 6 existing custom schemes auto-migrated from `{bg,text}` to CSS rule format / 6个现有自定义方案自动从{bg,text}迁移为CSS规则格式

## v1.9.9.9 (2026-07-20)

- **SVG Action Buttons / SVG操作按钮** — Replaced emoji (📌📋✕) with SVG vector icons for inline notes, panel notes, and popout windows; consistent 24px touch targets; hover highlight with subtle background; auto-adapts icon color to note theme (light/dark) / 内嵌笔记、面板笔记、独立窗口的emoji按钮替换为SVG矢量图标；统一24px点击区域；悬浮微妙高亮；图标颜色自适应笔记主题深浅
- **Inline Note Action Bar / 内嵌笔记操作栏** — Top-positioned floating action bar with semi-transparent background and backdrop blur; hidden during editing; double-click anywhere on card to enter edit mode; min-height increased to 80px / 顶部悬浮操作栏，半透明背景+模糊；编辑时隐藏；双击卡片任意位置进入编辑；最小高度增至80px
- **Panel Note Action Bar / 面板笔记操作栏** — Same SVG icon style as inline notes; top-positioned with theme-adaptive colors; added timestamp at bottom of each card / 与内嵌笔记一致的SVG图标样式；顶部悬浮，颜色自适应主题；每张卡片底部添加时间戳
- **Popout Window Buttons / 独立窗口按钮** — SVG icons replace emoji in titlebar; always visible with theme-color background; removed blur effect for cleaner drag area / 标题栏SVG图标替代emoji；始终可见，使用主题色背景；移除模糊效果保持拖动区域清晰
- **Default Group Display / 默认分组显示** — Right-click "全部"/"未分组"/custom groups to set as default; persisted via `defaultFnGroup`; auto-selects on panel open / 右键"全部"/"未分组"/自定义分组可设为默认显示；通过`defaultFnGroup`持久化；打开面板时自动选中
- **Dynamic Masonry Columns / 动态瀑布流列数** — Panel note masonry layout now dynamically adjusts column count based on panel width (1 column per 160px); ResizeObserver for real-time updates / 面板笔记瀑布流根据面板宽度动态调整列数（每160px一列）；ResizeObserver实时更新
- **JSON Data Safety / JSON数据安全** — Fixed global-notes.json corruption from double closing braces; auto-restore from backup on parse failure / 修复global-notes.json双重闭合花括号损坏；解析失败时自动从备份恢复

- **Floating Note Data Safety / 悬浮笔记数据安全** — Added sync save on plugin unload, snapshot-based write to prevent race condition overwriting, backup to `.bak.json` before each write, auto-restore from backup when main file is empty / 插件卸载时同步保存数据，写入时使用快照防止竞态覆盖，每次写入前备份到`.bak.json`，主文件为空时自动从备份恢复
- **Floating Note Inline Display / 悬浮笔记内嵌显示** — Inline notes auto-adjust height to show full text; min-width 200px, max-width 480px; scrollable when content overflows; timestamp hidden during editing / 内嵌笔记高度自适应显示全文；最小宽度200px，最大宽度480px；内容超出可滚动；编辑时隐藏时间戳
- **Floating Note Preview / 悬浮笔记预览** — Switched from Markdown rendering to plain text to eliminate unwanted paragraph margins and properly display blank lines / 预览改用纯文本替代Markdown渲染，消除非手动添加的段落边距，空行正常显示
- **Floating Note Edit Height / 悬浮笔记编辑高度** — Edit textarea auto-resizes based on content line count with minimum 80px height, fixing single-line-only issue after restart / 编辑textarea根据内容行数自适应高度（最低80px），修复重启后编辑高度仅一行的问题
- **Panel Floating Notes Layout / 面板悬浮笔记布局** — Changed from fixed 2-column to 3-column masonry layout; action buttons (📌📋) shown on hover only, hidden on mouse leave; added copy button / 从固定两栏改为三栏瀑布流；操作按钮（📌📋）悬浮时显示、离开隐藏；添加复制按钮

## v1.9.9.7 (2026-07-20)

- **Floating Note Inline Display / 悬浮笔记内嵌显示** — Inline floating notes now support Ctrl+Shift+Alt+scroll wheel adjustments (opacity/theme/font size), matching popout window functionality / 内嵌悬浮笔记支持Ctrl/Shift/Alt+滚轮调整（透明度/主题/字号），与独立窗口一致
- **Floating Note Popout Window / 悬浮笔记独立窗口** — Popout windows are always-on-top, no longer use parent window relationship to avoid activating Obsidian on focus; close button hides note (preserves data) instead of deleting; back button (↩) returns to inline display with preserved window size / 独立窗口始终置顶，移除父窗口关系避免聚焦时激活Obsidian；关闭按钮改为隐藏而非删除；返回按钮切回内嵌并保持窗口大小
- **Floating Note Themes / 悬浮笔记配色** — Added 5 new color schemes (steel blue, crimson, gold, teal, mauve); increased background opacity for better readability; inline notes now use same theme colors as popout; custom color editor via right-click menu (replaces prompt() which is unsupported in Electron) / 新增5组配色（钢蓝/赤红/金黄/青绿/紫粉）；提高背景不透明度改善可读性；内嵌笔记使用与独立窗口相同的配色；右键菜单添加自定义配色编辑器（替代Electron不支持的prompt()）
- **Floating Note Editing / 悬浮笔记编辑** — Double-click to edit places cursor at end of text instead of selecting all; edit area expands to fill card edges; popout window uses textarea overlay instead of contentEditable for reliable re-editing / 双击编辑时光标放在文本末尾而非选中全文；编辑区扩展到卡片边缘；独立窗口改用textarea覆盖替代contentEditable，修复再次双击无法编辑
- **Floating Note Resize Fix / 悬浮笔记调整大小修复** — Card mousedown no longer intercepts browser native resize handle (bottom-right 16px zone) / 卡片mousedown不再拦截浏览器原生resize手柄（右下角16px区域）
- **Floating Note Pin Button / 悬浮笔记📌按钮** — Panel notes have 📌 icon: left-click for inline display, middle-click for popout window; inline notes have 📌 button to switch to popout / 面板笔记📌图标：左键内嵌显示、中键独立窗口；内嵌笔记📌按钮切换到独立窗口
- **Floating Note Copy Button / 悬浮笔记复制按钮** — Added copy button (📋) to inline notes (hover to show) and popout window bar / 内嵌笔记添加复制按钮（悬浮显示），独立窗口bar添加复制按钮
- **Floating Note Timestamp / 悬浮笔记时间戳** — Each note shows creation timestamp at bottom (year/month/day hour:minute) / 每条笔记底部显示创建时间戳（年/月/日 时:分）
- **Floating Note Markdown / 悬浮笔记Markdown** — Inline notes render text as Markdown using Obsidian's MarkdownRenderer / 内嵌笔记使用Obsidian的MarkdownRenderer渲染Markdown文本
- **Floating Note Groups / 悬浮笔记分组** — Added note grouping in panel with default "归档/Archive" group; add/rename/delete groups via right-click; "Move to group" in note right-click menu; group chips use rounded style / 面板添加笔记分组功能，默认"归档"分组；右键添加/重命名/删除分组；笔记右键"移动到分组"；分组chip使用圆角样式
- **Panel Right-Click Fix / 面板右键修复** — Right-clicking elements under keywords/css/floating notes chips now pins the chip to prevent auto-hide; mouseleave/mouseout excludes .menu targets / 右键点击keywords/css/悬浮笔记chip下的元素时固定chip防止自动隐藏；mouseleave/mouseout排除.menu目标
- **New Note Defaults / 新笔记默认值** — New notes default to 180×140px size and cycle through color schemes / 新笔记默认180×140px大小，循环使用配色方案

## v1.9.9.6 (2026-07-20)

- **Floating Notes Chip Close Fix / 悬浮笔记Chip关闭修复** — Moved fnContainer from inside chipBar to after chipBar (`chipBar.after`), fixing mouseout event being intercepted by `.rch-top-chip-bar` check when leaving from bottom / 将fnContainer从chipBar内部移到chipBar外部，修复从下方离开时mouseout事件被chipBar检查拦截导致不自动关闭
- **Floating Notes Chip Position Fix / 悬浮笔记Chip位置修复** — Added `chipBar.after(fnContainer)` position correction in updateDisplay, ensuring fnContainer always stays directly below chipBar after DOM rebuilds / 在updateDisplay中添加位置修正，确保DOM重建后fnContainer始终紧跟chipBar

## v1.9.9.5 (2026-07-20)

- **Keyword Bar Position & Visibility / 关键词栏位置与可见性** — keywordBar moved inside chipBar with `flex-basis:100%` for correct positioning below chips; only visible when style chip is active (checked via `data-active` attribute) / keywordBar移入chipBar内部用flex-basis:100%换行定位；仅在style chip激活时显示
- **Chip Bar Background Removed / 移除chipBar背景** — Removed background from chipBar, keywordBar, and rules section for cleaner look / 移除chipBar、keywordBar、rules区域的背景色
- **Chip Event Delegation Fix / Chip事件委托修复** — Added `e.target.closest('.rch-top-chip-bar')` guard in `mouseover`/`mouseout` handlers to prevent keywordBar button events from triggering `scheduleHide()` / 在事件委托中排除chipBar内部事件，防止关键词按钮触发收起
- **Chip mouseleave Fix / Chip离开事件修复** — `mouseleave` on chip now checks `e.relatedTarget` — if mouse moves to another element inside chipBar (keywordBar, other chip), `scheduleHide()` is not triggered / chip的mouseleave检查relatedTarget，鼠标在chipBar内移动时不触发收起

## v1.9.9.4 (2026-07-20)

- **Keyword Switch Bar / 关键词切换栏** — Added keyword button bar below CSS chip bar when multiple rules match; default shows exact-match keyword's styles, click to switch other keywords' styles / 多规则匹配时在CSS chip bar下方显示关键词切换按钮，默认显示精确匹配关键词的样式，点击切换其他关键词样式
- **Current Editing Rule Priority / 当前编辑规则优先级** — `currentEditingRule` now prioritizes exact match over first-in-array, then longest match / `currentEditingRule`优先精确匹配，其次最长匹配，不再取数组第一个
- **Style Click State Update / 样式点击状态更新** — After clicking a style, `currentEditingRule` and `highlightMatchingRuleButtons` are now updated in all three branches (existing rule / global rule / new rule), fixing file rule group not appearing after applying style to global rule keyword / 样式点击后三个分支都更新`currentEditingRule`并调用`highlightMatchingRuleButtons`，修复全局规则点击其他样式后文件规则分组不显示
- **Chip Event Delegation / Chip事件委托** — Changed `bindChip` from direct `mouseenter`/`mouseleave` to event delegation via `mouseover`/`mouseout` + `closest(selector)`, fixing collapsed groups after DOM rebuild from section clear/re-add / 改用事件委托替代直接绑定，修复DOM重建后鼠标移入内容区导致展开分组收起

## v1.9.9.3 (2026-07-20)

- **Regex Pipe Split Fix / 正则管道符分割修复** — Added `_splitRegexPipes()` function with bracket-depth awareness; replaced 31 occurrences of `regex.split('|')` to correctly handle `|` inside lookbehind/lookahead/capturing groups (e.g., `(?<!拉|欧)美国|United States` no longer splits incorrectly) / 新增`_splitRegexPipes()`括号深度感知分割函数，替换31处`regex.split('|')`，修复lookbehind等括号内含`|`时被错误拆分的问题
- **Remove Group Double-Click / 移除分组双击操作** — Removed double-click on style group title (move to single-display) and double-click on collapsed tab (pin back to normal display) / 移除双击样式分组标题移动到单显区、双击标签钉回常显的操作
- **Remove PinToNormalDisplay Menu / 移除钉回常显右键选项** — Removed "Pin to normal display" context menu option from collapsed category tabs / 移除折叠标签右键菜单中的"钉回常显区"选项

## v1.9.9.2 (2026-07-20)

- **Sidebar Panel Drag Fix / 侧边栏面板拖动修复** — Fixed title bar cursor and drag not being disabled when panel is in sidebar; changed `_inSidebar` from static const to dynamic `isInSidebar()` check using `_sidebarView.isVisible()`, and update cursor on sidebar open/close / 修复面板移入侧边栏后标题栏仍显示抓手指针且可拖动的问题，将静态_inSidebar改为动态isInSidebar()检测，侧边栏开关时更新cursor
- **Keyword Click Group Auto-Switch / 关键词点击分组自动切换** — Removed `activeGlobalGroup` and `activeTabCategory` "don't override" logic; clicking a new keyword now automatically switches to the matching rule/style group instead of staying on the manually selected group / 移除activeGlobalGroup和activeTabCategory的"不覆盖"逻辑，点击新关键词时自动切换到匹配的规则/样式分组
- **Panel Scroll Position Fix / 面板滚动位置修复** — Removed `scrollIntoView` after showing inline remarks; now preserves scroll position so top chip bar stays visible when keyword remarks are displayed / 移除备注显示后的scrollIntoView，改为保存恢复滚动位置，确保顶部chip栏不被滚出视口
- **Global Notes Concurrent Write Fix / 全局笔记并发写入修复** — Added write lock to `saveGlobalNotes()` to prevent file corruption from overlapping async writes / 为saveGlobalNotes添加写入锁，防止并发异步写入导致文件损坏

## v1.9.9.1 (2026-07-19)

- **Ungrouped i18n Fix / 未分组国际化修复** — Keywords chip area "未分组" now uses `t()` function, correctly displaying "Ungrouped" in English mode / 关键词chip区域的"未分组"改用t()函数，英文模式下正确显示"Ungrouped"
- **Keywords Group Default Name / 关键词分组默认名称** — English default name changed from "New Styles" to "new keywords group" for semantic accuracy / 英文默认名称从"New Styles"改为"new keywords group"，语义更准确
- **CSS Group Default Name / CSS分组默认名称** — CSS chip "+" button now presets "new Styles group" as default group name / CSS chip"+"按钮添加分组时预设名称改为"new Styles group"
- **Sidebar SG Icon Auto-Show / 侧边栏SG图标自动显示** — New install now automatically shows SG icon in right sidebar via `ensureSidebarView()` on layout ready / 新装插件时通过`ensureSidebarView()`自动在右侧面板显示SG图标
- **Main Panel Default Size / 主面板默认尺寸** — Default main panel size changed from 1000×80vh to 800×500 for better initial display / 主面板默认尺寸从1000×80vh改为800×500
- **Ribbon Icon SG / 左侧功能区图标SG** — Left ribbon icon changed from highlighter to swiftglossa-icon displaying "SG" text / 左侧功能区图标从highlighter改为swiftglossa-icon显示"SG"文字

## v1.9.9 (2026-07-19)

- **Floating Note Mobile Drag / 悬浮笔记手机拖动** — Added touchstart/touchmove/touchend handlers to global-note-card, enabling drag-to-move on mobile devices / 为global-note-card添加触摸事件处理，手机端可拖动悬浮笔记位置
- **Remark Buttons Size Reduction / 备注按钮缩小** — Reduced remark popup action buttons (?、+、⬡) diameter from 36px to 26px on desktop for more compact layout / 桌面版备注弹窗操作按钮(?、+、⬡)直径从36px减至26px，布局更紧凑

## v1.9.8.4 (2026-07-19)

- **Popout Note Ctrl+Scroll Opacity Fix / 独立窗口Ctrl+滚轮透明度修复** — Fixed ipc-message args parsing (off-by-one) and note.id type mismatch (number vs string) that prevented Ctrl+scroll from adjusting popout window opacity / 修复ipc-message参数解析偏移和note.id类型不匹配（数字vs字符串）导致Ctrl+滚轮无法调整独立窗口透明度
- **Popout Note Restore on Startup / 启动恢复独立窗口修复** — Popout windows now correctly restore on Obsidian startup; removed `_hidden` filter from restore, fixed `@electron/remote` require order, and ensured `renderGlobalNotesArea` runs after `_restoreNotePopouts` / 启动时独立窗口正确恢复，移除恢复时的_hidden过滤，修复@electron/remote获取顺序，确保render在restore之后执行
- **Popout Note Empty Lines Fix / 独立窗口空行压缩修复** — Changed `content.textContent` to `content.innerText` in popout blur handler to preserve line breaks when syncing text back to chip panel / 独立窗口blur处理中用innerText替代textContent，保留换行符同步到chip面板
- **Chip-to-Popout Sync Fix / Chip编辑同步到独立窗口修复** — Editing a note in the chip panel now correctly syncs to the popout window; fixed `_syncNoteToPopout` key type mismatch and switched to `innerText` for proper newline rendering / chip面板编辑笔记现在正确同步到独立窗口，修复_syncNoteToPopout键类型不匹配，改用innerText保留换行
- **Popout Note Frosted Glass Style / 独立窗口毛玻璃样式** — Popout windows now use semi-transparent dark background (`rgba(30,30,30,0.72)`) simulating frosted glass effect with rounded corners and subtle borders / 独立窗口使用半透明深色背景模拟毛玻璃效果，圆角和细边框
- **Popout Note Theme Switching / 独立窗口配色切换** — Shift+scroll now cycles through 5 color themes (dark, light, green, purple, brown) with smooth transitions; theme index saved to `_popoutTheme` / Shift+滚轮循环切换5套配色（深色、浅色、绿调、紫调、棕调），带过渡动画，保存到_popoutTheme
- **Popout Note Font Size Zoom / 独立窗口文本缩放** — Alt+scroll now adjusts popout note text size (9-28px); font size saved to `_popoutFontSize` / Alt+滚轮调整独立窗口文本字号（9-28px），保存到_popoutFontSize
- **Startup Performance Optimization / 启动性能优化** — Pinyin and interlinear note data loading moved out of critical `Promise.all` path; CSS file reading unified via `crossFS.read` + `_cachedCssContent` (eliminated 3x redundant reads); CSS parsing merged between `syncStylesToCategories` and `loadPluginCssStyles`; `loadGlobalRules` migration save deferred with `setTimeout` to avoid blocking `refreshCurrentView` during startup / 拼音和行间注释数据加载移出关键Promise.all路径；CSS文件读取统一走crossFS.read+_cachedCssContent（消除3次重复读取）；CSS解析在syncStylesToCategories和loadPluginCssStyles间合并；loadGlobalRules迁移回写延迟执行避免启动时阻塞refreshCurrentView

## v1.9.8.3 (2026-07-18)

- **Rule Group Buttons Visibility Fix / 规则分组按钮可见性修复** — When manually switching to a different rule group via chip hover, all buttons in that group now remain visible when moving the mouse downward; previously `highlightMatchingRuleButtons` filtered non-matching buttons to `display:none` even in the user's active group / 手动通过chip悬浮切换到其他规则分组后，鼠标下移时该分组内所有按钮保持可见，此前`highlightMatchingRuleButtons`会过滤掉用户活动分组中的非匹配按钮
- **Rule Group Auto-Activate Guard / 规则分组自动激活守卫** — `_activateGlobalGroup` and collapsed-mode grid display logic now skip when user has manually selected a different group, preventing chip jump-back and button disappearance / `_activateGlobalGroup`和折叠模式grid显示逻辑在用户已手动选择其他分组时跳过，防止chip跳回和按钮消失
- **Rule Group Chip Hover Cooldown / 规则分组Chip悬浮冷却** — Added cooldown and hover-verification after rule group chip hover-triggered activation, same as CSS group chip / 规则分组chip悬浮触发激活后添加冷却期和hover验证，与CSS分组chip一致

## v1.9.8.2 (2026-07-18)

- **Style Group Switch Fix / 样式分组切换修复** — Switching to a different style group via hover no longer jumps back to the original group; `highlightMatchingRuleButtons` now respects user's manual group selection and won't auto-expand the matched group when another group is active / 悬浮切换到其他样式分组时不再跳回原分组，`highlightMatchingRuleButtons`现在尊重用户手动选择的分组，不会在用户已切换分组时自动展开匹配分组
- **Group Chip Hover Cooldown / 分组Chip悬浮冷却** — Added cooldown after group chip hover-triggered click to prevent DOM re-layout from causing cascading mouseenter events that repeatedly toggle groups / 分组chip悬浮触发click后添加冷却期，防止DOM重新布局导致连锁mouseenter事件反复切换分组

## v1.9.8.1 (2026-07-18)

- **Mobile Chip Toggle Fix / 手机端Chip切换修复** — Tapping an expanded top chip (CSS/KEY WORDS) now correctly collapses it on mobile; previously `hoveredChip` wasn't cleared on unpin, preventing toggle / 手机端点击已展开的顶部chip（CSS/KEY WORDS）现在能正确收起，此前取消pin时未清除hoveredChip导致无法切换
- **No-Remark Keyword Window Fix / 无备注关键词窗口修复** — Keywords without remarks now correctly open the keyword detail window showing related notes and highlights; previously `openKeywordWindow` returned early when `links` was empty / 无备注关键词现在能正确打开关键词详情窗口显示相关笔记和高亮，此前links为空时函数提前返回
- **Related Links Click Fix / 相关链接点击修复** — Related notes and highlights links now work on mobile; replaced `<a class="internal-link">` with `<span>` to avoid Obsidian intercepting click events, and fixed `innerHTML +=` destroying event listeners when `linksByFile` is empty / 相关笔记和高亮链接在手机端现在可正常点击，用`<span>`替代`<a class="internal-link">`避免Obsidian拦截click事件，修复`innerHTML +=`在linksByFile为空时销毁事件监听器的问题

## v1.9.8 (2026-07-18)

- **Panel Chip Bar Position Fix / 面板ChipBar位置修复** — Fixed rule group chips moving below remark section after updating rules; `addGlobalRulesSection`/`addHeadingStylesSection` now correctly insert before `.inline-remark-section` / 修复更新规则后规则分组chips移到备注下方的问题，插入逻辑增加inline-remark-section参考
- **Rule Click Input Restore / 规则点击输入框恢复** — After panel auto-refresh, clicking a rule button now correctly fills the regex into the top input box and restores `currentEditingRule` / 面板自动刷新后点击规则按钮正确填入关键词到输入框并恢复编辑状态
- **Local Chip Name Translation Fix / 文件规则Chip名称修复** — Fixed file rule chip showing raw translation key "main.currentFile" instead of "当前文件" when active view is unavailable / 修复文件规则chip显示未解析翻译键"main.currentFile"的问题
- **File Rules Load on First Open / 首次打开加载文件规则** — Right panel now loads current file rules on first open, ensuring the file-name chip group appears immediately / 右侧面板首次打开时加载当前文件规则，文件名chip分组立即可见
- **Collapse Setting Persistence / 折叠设置持久化修复** — Activating a rule group chip no longer overwrites the "默认折叠规则分组" setting; the preference is only changed via the toggle button / 激活规则分组chip不再覆盖"默认折叠规则分组"设置，仅通过折叠按钮修改
- **Chip Hover After Rule Delete / 删除规则后Chip悬浮修复** — Top chip bar (CSS/KEY WORDS) hover behavior no longer breaks after deleting rules; switched to `mouseover`/`mouseout` event delegation with `relatedTarget` checks, and added display state sync after section rebuild / 删除规则后顶部chip悬浮触发不再失效，改用mouseover/mouseout事件委托并添加重建后显示状态同步
- **Rule Group Activation Fix / 规则分组激活修复** — Clicking a global rule button no longer jumps to the file-rules group; `highlightMatchingRuleButtons` now only activates the group matching `currentEditingRule` / 点击全局规则按钮不再跳到文件规则分组，仅激活与当前编辑规则匹配的分组

## v1.9.7 (2026-07-18)

- **Regex Pattern Matching for Related Content / 正则模式匹配相关内容** — Related notes and highlights now support regex patterns (e.g. `(?<!发展)中国`); auto-extracts plain text fallback when full regex matching fails / 相关笔记和高亮现在支持正则模式关键词，正则匹配失败时自动提取纯文本回退匹配
- **Panel Content Preserve on Navigation / 跳转后保持面板内容** — Clicking related notes/highlights links no longer refreshes the right panel; current keyword display is preserved after navigation / 点击相关笔记/高亮跳转后右侧面板不再刷新，保持当前关键词显示
- **clearHighlights Memory Fix / clearHighlights内存修复** — Replaced array accumulation with DocumentFragment in `clearHighlights` to prevent RangeError on large documents / `clearHighlights`中用DocumentFragment替代数组累积，防止大文档RangeError
- **Enter to Search / 输入框Enter搜索** — Pressing Enter in the panel input field now searches for matching keywords and displays related notes and highlights / 面板输入框按Enter键直接搜索匹配关键词并显示相关笔记和高亮

## v1.9.6.2 (2026-07-18)

- **Related Notes Middle-Click Fix / 相关笔记中键点击修复** — Middle-click on related note links now opens in background tab (previously opened in foreground); added `mousedown` `preventDefault()` to block browser auto-scroll on middle-click / 相关笔记链接中键点击改为后台新标签页打开（此前为前台），添加mousedown阻止默认自动滚动行为
- **Related Notes Expand All / 相关笔记展开全部** — The "+n" tag after related notes is now clickable; clicking it expands all remaining note links instead of just showing a count / 相关笔记数量超过10时"+n"标签可点击，点击后展开所有剩余链接

## v1.9.6 (2026-07-17)

- **Panel Auto-Refresh / 面板自动刷新** — Right panel now listens to `rulesUpdateEmitter`; clicking l/g button or adding rules via floating ball/group/style buttons instantly updates the panel without manual refresh / 右侧面板监听`rulesUpdateEmitter`事件，点击l/g按钮或通过悬浮球/分组/样式按钮添加规则后面板即时刷新
- **Mobile Sidebar Remark / 手机端侧边栏备注** — New "Mobile Remark in Sidebar" setting; when enabled, clicking a keyword on mobile shows remarks in the sidebar background instead of a popup, with haptic feedback; swipe left to view / 新增"手机端备注在侧边栏显示"设置，开启后手机端点击关键词在侧边栏后台显示备注而非弹窗，带震动反馈，手动滑动查看
- **Mobile Sidebar Fix / 手机端侧边栏修复** — Fixed mobile `contextmenu` event (long-press/select text) incorrectly closing the sidebar panel; added sidebar mode check matching `_outsideClickHandler` / 修复手机端`contextmenu`事件（长按/选中文本）误关闭侧边栏面板，添加侧边栏模式检查
- **Remark Text Selectable / 备注文字可选** — `inline-remark-section` now has `user-select:text`; mobile CSS excludes remark area from `user-select:none`, enabling text selection and drag-to-search / 备注区域添加`user-select:text`，手机端CSS排除备注区域，支持文字选中拖放搜索

## v1.9.5 (2026-07-16)

- **Related Notes / 显示相关笔记** — New setting "Show Related Notes"; when selecting or clicking a keyword, notes whose filenames contain the keyword are shown above the remark area; left-click opens in new tab, middle-click opens in background tab; also works for non-rule selected text / 新增"显示相关笔记"设置选项，选中或点击关键词时在备注区域上方显示文件名包含该关键词的笔记链接，左键新标签页打开，中键后台打开；非规则选中文本也支持
- **Underline Count Support / 下划线样式计数支持** — Removed 3 exclusion points that prevented underline-style keywords (e.g. `.underline-solid-1`) from displaying match counts; underline keywords now show counts normally / 移除3处下划线样式排除逻辑，下划线类关键词现在可正常显示计数
- **Remark Add Button Fix / 备注添加按钮修复** — Rewrote "+" button save logic to use `ruleSource === 'global'` (matching n-button pattern) instead of unreliable reference comparison; fixed first-time remark addition failing for local rules in sidebar / 重写"+"按钮保存逻辑，改用`ruleSource`判断全局/局部规则，修复侧边栏中局部规则首次添加备注失败的问题
- **Sidebar Panel Group Collapse / 侧边栏分组折叠** — When no keyword matches, all style groups are now collapsed by default to reduce visual clutter; previously all groups expanded when clicking empty area / 无关键词匹配时所有样式分组默认折叠，减少视觉干扰
- **Sidebar Button Hide / 侧边栏按钮隐藏** — "Move to Sidebar" and "Close" buttons are now hidden in sidebar mode and won't reappear after language switch / 侧边栏模式下隐藏"移至侧边栏"和"关闭"按钮，切换语言后不再闪现
- **Remark Filename Edit / 备注文件名编辑** — Double-click on remark file name tag (both normal and masonry mode) to edit the filePath; Enter/blur saves, Escape cancels / 双击备注文件名标签可编辑filePath，回车/失焦保存，Esc取消
- **AI Button Shape / AI按钮圆形化** — AI Ask, AI Graph, and Add (+) buttons now display as 36px circles on desktop (previously elliptical) / AI提问、AI关系图、添加(+)按钮桌面端统一为36px圆形
- **Status Bar Hide / 状态栏隐藏** — Settings popup now uses `display:none` instead of `transform:translateY(100%)` to hide the status bar / 设置弹窗改用`display:none`隐藏状态栏
- **Debug Logs Removed / 调试日志移除** — Removed all 14 `[SG-DEBUG]` console.log statements / 移除全部14条`[SG-DEBUG]`调试日志

## v1.9.4.3 (2026-07-15)

- **Popup Mouse Tracking Fix / 弹窗鼠标追踪修复** — Replaced unreliable `relatedTarget`-based `handleMouseOut` with `mousemove` bounds-box detection; added `popup.contains(el)` check in `isInBounds` for fixed-position badges that extend outside bounding rect / 将不可靠的`relatedTarget`依赖改为`mousemove`包围盒检测；`isInBounds`增加`popup.contains`检测以覆盖fixed定位的badge元素
- **Dynamic Z-Index / 动态Z层级** — Added `bringToFront` with static `_topZ` counter (starting at 1200); all popup-like windows raise z-index on mousedown, preventing chip preview from appearing behind other windows / 新增`bringToFront`动态提升z-index（初始1200），所有弹窗类窗口mousedown时提升层级，修复chip预览显示在窗口下方的问题
- **AI Graph Height Fix / AI关系图高度修复** — `applyZoom` sets SVG width/height directly instead of `transform:scale()`; `tryFit` waits for actual SVG content elements (g/path/rect) with size >50px via `requestAnimationFrame`; viewport height synced with content height / `applyZoom`直接设SVG宽高而非`transform:scale()`；`tryFit`通过`requestAnimationFrame`等待实际图形元素且尺寸>50px；viewport高度与内容同步
- **SVG className Fix / SVG className修复** — Fixed crash when accessing SVG element `className` (which is `SVGAnimatedString` not a string) by checking type before calling `.substring()` / 修复SVG元素className为`SVGAnimatedString`时调用`.substring()`崩溃的问题
- **Scroll Position Preserve / 滚动位置保留** — `renderRemarkContent` now preserves `scrollTop` across content re-renders using `requestAnimationFrame` / `renderRemarkContent`重渲染时通过`requestAnimationFrame`保留滚动位置
- **Image Hover Skip / 图片悬浮预览跳过** — Masonry card image hover preview no longer appears when image is already displayed at ≥95% of its natural size / 瀑布流卡片图片已100%显示时不再弹出悬浮预览
- **Debug Logs Removed / 调试日志移除** — Removed all `console.log('[RemarkPopup]')` debug messages / 移除所有`[RemarkPopup]`调试日志

## v1.9.4.2 (2026-07-14)

- **AI Graph Async Render Fix / AI关系图异步渲染修复** — Fixed remark popup showing incomplete AI relationship graph on open; mermaid SVG renders asynchronously but `autoFitZoom` ran before SVG was ready, leaving graph height unset; added MutationObserver to detect SVG appearance and re-apply zoom, plus `onReposition` callback to recalculate popup position after graph is fully rendered / 修复备注弹窗打开时AI关系图显示不全的问题；mermaid SVG异步渲染但autoFitZoom在SVG就绪前执行导致高度未设置，新增MutationObserver监听SVG出现后重新应用缩放，并添加onReposition回调在图形渲染完成后重新计算弹窗位置

## v1.9.4.1 (2026-07-14)

- **Interlinear Note Regex Key Fix / 行间注释正则Key修复** — Fixed interlinear note using matched text as key instead of full regex (e.g., only storing "Geoffery Hinton" instead of "Geoffery Hinton|Hinton|杰弗里·辛顿"); remark popup now uses ruleRegex as key / 修复行间注释以匹配文本而非完整正则作为key的问题，备注弹窗现在使用ruleRegex作为key
- **Interlinear Note Regex Rendering / 行间注释正则渲染** — Rendering now splits regex keys by `|` to match each alternative separately, supporting multi-branch regex patterns / 渲染时按`|`分割正则key分别匹配，支持多分支正则模式
- **Interlinear Note Auto-Migration / 行间注释自动迁移** — Added `findInterlinearNote` and `migrateInterlinearNoteKey` methods; when rule regex changes (e.g., "戴宗"→"戴宗|戴院长"), old key is automatically found and migrated to new key / 新增回退查找和自动迁移方法，规则正则变更后自动查找旧key并迁移到新key
- **List Mode Title Size Fix / 列表模式标题大小修复** — Adjusted remark popup list mode file title from 12px to 10px to match masonry mode, reducing vertical space usage / 备注弹窗列表模式文档标题从12px调整为与瀑布流一致的10px，减少纵向空间占用

## v1.9.4 (2026-07-12)

- **Mermaid Parser Rewrite / Mermaid解析器重写** — Rewrote `_sanitizeMermaid` line parser: removed conflicting pre-processing regexes, added cross-line node tracking (`lastNodeId`/`lastNodeDef`), `_parseBracketDef`/`_parseEdgeTail` helpers; correctly handles chained edges (`A -->|label| B -->|label2| C`) and bracket node definitions (`A["text"] --> B["text2"]`) / 重写`_sanitizeMermaid`行解析器：移除冲突的预处理正则，新增跨行节点追踪和辅助函数，正确处理链式边和带括号定义的节点
- **AI Graph Anti-Weak-Relation / AI关系图防牵强关系** — Added `_extractSnippet` to show context snippets for each related keyword in the prompt; new prompt rule #14 explicitly forbids creating edges for incidental word usage (e.g. "chose" as a verb ≠ "choice/decision" concept) / 新增`_extractSnippet`在Prompt中展示关联依据上下文片段，第14条规则严禁为偶然用词建边
- **AI Graph Bilingual Prompt / AI关系图双语Prompt** — Auto-detects remark language (Chinese vs non-Chinese, excluding Japanese/Korean from Chinese detection) and selects Chinese or English prompt and context labels accordingly / 自动检测备注语言，中文用中文Prompt，日语韩语及其他语言用英文Prompt
- **Graph Zoom Height Fix / 关系图缩放高度修复** — `applyZoom` now calculates height from SVG viewBox intrinsic dimensions instead of `getBoundingClientRect()`, ensuring correct height on initial render without manual zoom / `applyZoom`改用SVG viewBox固有尺寸计算高度，初始渲染即正确适配，无需手动缩放
- **Graph Scrollbar Fix / 关系图滚动条修复** — Changed viewport overflow from `auto` to `overflow-x:auto;overflow-y:hidden`, removing unnecessary vertical scrollbar / viewport溢出改为水平自动垂直隐藏，移除不必要的垂直滚动条
- **Masonry Mode i18n / 瀑布流模式国际化** — Replaced hardcoded "瀑布流模式" with `t('remark.masonryMode')` i18n key; added Chinese and English translations / 硬编码"瀑布流模式"改为i18n调用，中英文翻译表均已添加

## v1.9.3.4 (2026-07-11)

- **Random Group All Styles / 随机分组全部样式** — Fixed floating ball random highlight with group filter showing "no unused styles"; now randomly picks from all styles in the group regardless of usage / 修复悬浮球随机分组高亮提示"没有可用的未使用样式"的问题，现在从分组内所有样式中随机选取
- **Open Doc Button Style / 打开文档按钮样式** — Changed open document button icon to document+🔍 style matching SwiftMatch plugin / 打开文档按钮图标改为与SwiftMatch插件一致的文档+🔍样式
- **Paste Remark Button / 粘贴备注按钮** — Added paste button between open document and copy buttons; appends to existing remark content / 在打开文档与复制按钮之间新增粘贴按钮，备注已有内容时执行追加
- **Paste in Edit Mode / 编辑状态粘贴修复** — Fixed paste button losing textarea focus in edit mode; now inserts clipboard text at cursor position / 修复编辑状态下点击粘贴按钮导致textarea失焦的问题，现在直接在光标位置插入剪贴板文本

## v1.9.3.3 (2026-07-09)

- **Remark Badge Wrong Target Fix / 备注n按钮错位修复** — Fixed bug where clicking "n" badge to add remark would add it to an already-open popup of a different keyword instead of the clicked one; now correctly identifies target by ruleRegex/ruleSource / 修复点击"n"按钮添加备注时，若其他关键词的备注弹窗已打开，备注会错误添加到已打开弹窗而非点击的关键词的问题
- **Multiple Remark Popups / 多备注弹窗共存** — Different keywords' remark popups can now stay open simultaneously instead of closing each other / 不同关键词的备注弹窗现在可以同时打开，不再互相关闭

## v1.9.3.2 (2026-07-09)

- **Floating Group Middle-Click Global / 悬浮分组随机模式中键全局** — Middle-click on floating group button with random mode enabled now applies as global rule, consistent with floating ball behavior / 开启随机模式的悬浮分组按钮中键点击可应用为全局规则，与悬浮球操作一致
- **Mobile Main Panel Drag / 手机端主面板拖动** — Added touch event support to main panel title bar, enabling drag-to-move on mobile / 主面板标题栏添加触摸事件支持，手机端可拖动标题栏移动面板位置
- **Shortcut Delete Global Rule / 快捷键删除全局规则** — Remove style shortcut now also deletes global rules; confirmation dialog shown when rule has remarks / 移除样式快捷键现在也支持删除全局规则，含备注时弹出确认窗口
- **Remark Popup Long-Press Close Bug / 备注弹窗长按关闭修复** — Fixed bug where long-pressing close button on remark popup prevented subsequent remark popups from triggering until another keyword's popup was shown / 修复长按关闭按钮关闭备注弹窗后，再次悬浮无法触发备注弹窗的问题

## v1.9.3.1 (2026-07-09)

- **Rename to SwiftGlossa / 更名为SwiftGlossa** — Renamed plugin from SwiftGloss to SwiftGlossa for uniqueness; plugin ID remains `regex-css-highlighter` for compatibility / 插件从SwiftGloss更名为SwiftGlossa以保唯一性；插件ID保持`regex-css-highlighter`不变以兼容升级

## v1.9.3 (2026-07-07)

- **Desktop Chips Drag / 桌面端chips区拖动窗口** — Click empty area in bottom chips bar to drag remark popup and keyword detail window on desktop (previously mobile-only) / 桌面端点击备注弹窗和关键词窗口底部chips区空白处可拖动窗口位置（此前仅手机端支持）
- **n Badge Position / n按钮位置上移** — Moved "n" remark badge upward to align with g/l badge when hovering highlighted text / 鼠标悬浮高亮文本时"n"按钮上移至与g/l按钮平行位置
- **Interlinear Note Key Fix / 行间注释key修复** — Fixed remark popup interlinear note using ruleRegex as key instead of plain text, causing data mismatch and duplicate notes with floating ball's interlinear note feature / 修复备注弹窗行间注释使用ruleRegex而非纯文本作为key，导致与悬浮球行间注释功能数据不一致、出现重复注释
- **Popup Close Button / 弹窗关闭按钮优化** — Close button hidden initially, shown after dragging popup; color changed to red for visibility / 关闭按钮初始隐藏，拖动弹窗后显示；颜色改为红色

## v1.9.2 (2026-07-07)

- **Desktop c/i Button Style / 桌面端c/i按钮样式优化** — Enlarged c/i buttons (28×28px, 14px font, 2px border), hover keeps visible, auto-hide timer pauses on hover / 增大c/i按钮尺寸（28×28px, 14px字号, 2px边框），鼠标悬浮时保持显示，自动隐藏计时器暂停
- **Desktop c/i Button Right-click Edit / 桌面端c/i按钮右键编辑** — Right-click c/i buttons to edit display text, CSS class name, or inline CSS; style persists across restarts / 右键c/i按钮可编辑显示文字、CSS类名、内联CSS，样式重启后保留
- **Masonry Remark Edit & Paste / 瀑布流备注编辑与粘贴** — Double-click remark content in masonry mode to edit (previously only toolbar dblclick worked); added clipboard image paste support in masonry edit textarea / 瀑布流模式下双击备注内容即可编辑（此前仅工具栏双击有效）；编辑框支持Ctrl+V粘贴剪贴板图片
- **Keyword Detail Image Render / 关键词详情图片渲染** — Fixed images not displaying in keyword detail window opened from bottom chips, only filenames shown / 修复从底部chip打开的关键词详情窗口中图片不显示、只显示文件名的问题

## v1.9.1.4 (2026-07-06)

- **Mobile c/i Buttons / 手机端c/i按钮** — Added "c" (add/remove count) and "i" (add/edit interlinear note) buttons to mobile highlight action buttons alongside existing l/g and n buttons / 手机端点击高亮关键词时，在l/g和n按钮旁新增"c"（添加/移除计数）和"i"（添加/编辑行间注释）按钮
- **Desktop Rule Action Buttons / 桌面端规则操作按钮** — Desktop: selecting rule text now auto-shows c/i buttons next to floating ball in both always and followSelection modes / 桌面端选中文本为规则文本时，自动在悬浮球旁显示c、i按钮（常显和跟随选中模式均支持）
- **Per-Platform Floating Ball Visibility / 悬浮球可见性按平台独立** — Split floatingBallHidden into floatingBallHiddenDesktop/floatingBallHiddenMobile so hiding on mobile doesn't affect desktop after sync, with auto-migration from old setting / 悬浮球隐藏设置按平台独立存储，手机端隐藏不影响桌面端，自动迁移旧数据

## v1.9.1.3 (2026-07-06)

- **Fix AI Question Remark Lost / 修复AI问题备注丢失** — Fixed bug where edited AI question remarks disappeared after closing and reopening the popup: `doHide` pre-save condition treated empty `filePath` as falsy, now uses `!== undefined` check / 修复备注弹窗中编辑AI问题后退出再双击编辑时内容消失的bug：`doHide`预保存条件将空`filePath`当作falsy跳过，改为`!== undefined`检查

## v1.9.1.2 (2026-07-06)

- **Fix Add/AI Button in Remark Popup / 修复备注弹窗添加/AI按钮** — Fixed "+" and "?" buttons not working in hover remark popup: rule was null, now auto-finds from rule list; links array was stale closure, now re-reads from DOM / 修复鼠标悬浮备注弹窗中"+"和"?"按钮无效：rule为null时自动从规则列表查找；links闭包数据过期改为从DOM重新读取
- **Masonry Toolbar Fix / 瀑布流工具栏修复** — Restored hover-to-show toolbar with pointer-events control; added dblclick on toolbar to enter edit mode, dblclick on search chip to edit search text / 恢复悬浮显示工具栏并控制pointer-events；双击toolbar进入编辑，双击搜索词chip编辑搜索词
- **Button Order Swap / 按钮顺序对调** — Swapped "Open Document" and "Copy" button positions in remark toolbars / 备注工具栏中"打开文档"和"复制"按钮位置对调
- **Masonry Mode Persistence / 瀑布流模式持久化** — Masonry mode state now saved to settings and persists across restarts / 瀑布流模式状态保存到设置中，重启后不丢失

## v1.9.1.1 (2026-07-05)

- **Frosted Glass Popups / 毛玻璃弹窗** — All popups (remark, keyword-detail, chip preview, main panel) now use frosted glass effect with `backdrop-filter:blur(16px) saturate(180%)` + semi-transparent background, replacing solid backgrounds / 所有弹窗（备注、关键词详情、chip预览、主面板）统一使用毛玻璃效果，替换原有的实心背景
- **Remove Popup Borders / 移除弹窗边框** — Removed all popup borders and border width/color settings, unified border-radius to 12px / 移除所有弹窗边框及边框宽度/颜色设置项，统一圆角为12px
- **Transparent Inner Elements / 内部元素透明化** — Title bars, content containers, chips bars, masonry cards, dividers all use transparent/semi-transparent backgrounds to show blur effect / 标题栏、内容容器、chips区域、瀑布流卡片、分隔线全部改为透明/半透明背景以透出模糊效果
- **Ribbon Icon Rename / 侧边栏按钮更名** — Changed sidebar ribbon icon tooltip from "Regex-Css-Highlighter" to "SwiftGloss" / 侧边栏功能区按钮提示文字从"Regex-Css-Highlighter"改为"SwiftGloss"

## v1.9.1 (2026-07-05)

- **Count Styles Hardcoded / 计数样式硬编码** — Hardcoded count badge CSS styles into main.js, fixing count badges not displaying on fresh installations where styles.css lacked the counter rules / 将计数标记CSS样式硬编码到main.js中，修复新装插件时styles.css缺少计数样式导致计数标记不显示的问题

## v1.9.0 (2026-07-05)

- **Masonry Layout Mode / 瀑布流模式** — New masonry/waterfall layout for remark popups: all remark entries mixed as cards with file name tags, color bar at top replacing dots, hover-to-show toolbar, search keyword placeholder + drag-drop support, dynamic column count via ResizeObserver
- **Remark Popup Code Reuse / 备注弹窗代码复用** — Extracted `renderRemarkContent` shared function, both `remark-custom-popup` and `keyword-detail-window` now share content rendering logic, reducing ~774 lines of duplicate code
- **Remark Link Fix After File Rename / 文件改名后备注链接修复** — Fixed remark links not updating after file rename: moved links update logic outside the conditional guard, replaced `fileRules` Map iteration with `_fileRulesData` traversal

## v1.8.9.7 (2026-07-05)

- **文件改名后备注链接修复** — 修复文件改名后备注弹窗中引用的文件路径未更新的bug：将 links 更新逻辑移出条件守卫，改用 `_fileRulesData` 遍历替代 `fileRules` Map 遍历，确保无论被重命名文件是否有自身规则、其他文件规则是否已加载，所有 links.filePath 都能正确更新 / Fixed remark links not updating after file rename — moved links update logic outside the conditional guard, replaced `fileRules` Map iteration with `_fileRulesData` traversal, ensuring all links.filePath are correctly updated regardless of whether the renamed file has its own rules or other file rules are loaded

## v1.8.9.6 (2026-07-04)

- **移除手机版阅读模式行、边距设置** — 移除"手机版阅读模式行、边距"设置项及 applyMobilePreviewMargins 方法，已改用其他插件实现 / Removed "Mobile Reading Mode Line & Margin" setting and applyMobilePreviewMargins method — now handled by another plugin
- **悬浮球隐藏/显示功能** — 点击"隐藏悬浮按钮"时同步隐藏悬浮球，添加左侧功能区按钮打开主面板，主面板设置-悬浮球选项顶部添加"显示/隐藏悬浮球"chip / Floating ball now hides when "Hide Floating Buttons" is clicked; added left ribbon icon to open main panel; added "Show/Hide Floating Ball" chip at top of floating ball settings
- **移除手机版注音📌按钮** — 手机端悬浮球菜单中"注音"选项后的📌按钮已隐藏 / Hidden the 📌 pin button after the "Pinyin" option in mobile floating ball menu
- **悬浮球显示修复** — 修复悬浮球重新显示时"SG"文本未居中的问题，恢复 display 为 flex / Fixed "SG" text not centered when floating ball is re-shown — restored display to flex

## v1.8.9.5 (2026-07-04)

- **手机端主面板交互修复** — 修复手机端长按样式/规则按钮后浏览器进入选择模式导致面板无法关闭的严重bug，通过在交互元素 touchstart 上 preventDefault 阻止浏览器长按检测，并手动处理 tap 触发 click / Fixed critical mobile bug where long-pressing style/rule buttons caused browser selection mode, making the panel impossible to close — resolved by calling preventDefault on touchstart for interactive elements and manually handling tap-to-click
- **手机端关闭按钮修复** — 关闭按钮添加 rch-close-btn 类名，contextmenu 事件作为长按后的备用关闭通道 / Close button now has rch-close-btn class, contextmenu event serves as fallback close channel after long-press
- **手机端外部点击关闭** — document 级别 contextmenu 监听作为面板外部点击的备用关闭通道 / Document-level contextmenu listener as fallback outside-click close channel on mobile
- **拖拽监听器泄漏修复** — 将匿名 mousemove/mouseup 监听器改为具名引用，在 onClose/onOpen 中正确清理，防止 refreshModalContent 调用时累积 / Fixed anonymous mousemove/mouseup listener leak — converted to named references, properly cleaned up in onClose/onOpen to prevent accumulation during refreshModalContent
- **_activeContextMenuCleanup 清理** — onClose 中清理残留的右键菜单 document 事件监听器 / Clean up residual context menu document event listeners in onClose
- **close() 死锁修复** — 移除 close() 中的 _locked 检查，手机端 outsideClickHandler 忽略 _locked 状态 / Removed _locked check in close(), mobile outsideClickHandler ignores _locked state
- **i18n key 补全** — 添加 main.localRule、main.globalRule、main.clickToEdit、main.clickToApply、main.clickToGlobal、main.empty、main.preview、main.status、main.globalRuleDeleted、main.ruleDeleted、main.ruleToggled、main.movedToLocalRule 到中英文字典 / Added missing i18n keys for main panel UI elements
- **手机端长按菜单屏蔽** — 样式按钮和规则按钮的 contextmenu 注册用 _isDesktop 包裹，手机端仅 preventDefault / Desktop-only contextmenu registration for style/rule buttons, mobile only prevents default
- **手机端备注选项隐藏** — 规则按钮右键菜单的"编辑备注"和备注悬浮在手机端隐藏 / Hide "Edit Remark" option and remark hover on mobile
- **菜单项顺序调整** — "移动到分组"移到菜单顶部，"移动到当前文件规则"放入其子菜单 / "Move to Group" moved to top of menu, "Move to Local Rule" placed in its submenu
- **二级菜单溢出修复** — 桌面端子菜单添加底部溢出检查，手机端子菜单改为向下展开+maxHeight / Desktop submenu bottom overflow check, mobile submenu expands downward with maxHeight

## v1.8.9.4 (2026-07-03)

- **文件规则路径前缀斜杠修复** — 启动时自动检测并移除库根文件夹下文件规则 key 的前缀 `/`（如 `/犬儒主义.md` → `犬儒主义.md`），修复根目录文件规则无法加载的问题，一次性迁移 / Auto-detects and removes leading `/` from file rule keys on startup (e.g. `/犬儒主义.md` → `犬儒主义.md`), fixing root-level file rules not loading — one-time migration

## v1.8.9.3 (2026-07-03)

- **旧版备注自动迁移** — 启动时自动将旧版 `rule.remark` 迁移为 `link` 条目（`filePath: ""`），迁移后清空旧字段并持久化，无需用户手动操作 / Automatically migrates legacy `rule.remark` to `link` entries (`filePath: ""`) on startup, clears the old field and persists changes — no manual user action required
- **全局规则弹窗显示文件规则备注** — 全局规则备注弹窗中追加显示同 regex 的所有文件规则备注，文件名后标注"l"标记以区分来源 / Global rule remark popup now also shows file rule remarks for the same regex from all files, with an "l" badge after the file name to distinguish the source
- **文件规则引用备注只读保护** — 来自文件规则的引用备注不显示编辑/删除工具栏，避免误操作 / File rule reference remarks are read-only in the global popup — no edit/delete toolbar shown to prevent accidental modifications

## v1.8.9.2 (2026-07-02)

- **行间注释字体大小持久化修复** — 修复 `injectInterlinearNoteStyles` 始终使用默认CSS而非用户自定义CSS，导致重启后行间注释字体大小等样式恢复默认的bug / Fixed `injectInterlinearNoteStyles` always using default CSS instead of user-customized CSS, causing interlinear note font size and other styles to revert to defaults after restart
- **行间注释与计数共存** — 当关键词同时有行间注释和计数时，行间注释自动移至关键词下方、计数保持在上方，创建时即添加 `has-counter` 类避免时序问题 / When a keyword has both interlinear note and count, the note automatically moves below the keyword while count stays above; `has-counter` class added at creation time to avoid timing issues

## v1.8.9.1 (2026-07-02)

- **计数功能** — 备注弹窗标题栏添加"c"按钮，悬浮球菜单添加"添加计数"选项，点击后为匹配文本添加毛玻璃计数标记（显示"位置/总数"），再次点击移除计数 / Added "c" count button to remark popup title bar and "Add Count" option to floating ball menu; clicking adds frosted-glass count badges (showing "position/total") to matched text, clicking again removes count
- **计数持久化** — 计数状态保存到settings，重启Obsidian后自动恢复 / Count state persisted to settings, automatically restored after Obsidian restart
- **阅读模式计数修复** — 阅读模式总数从文件内容计算（非DOM），用段落文本定位确定全局序号，解决懒渲染下计数不准和滚动变化问题 / Fixed reading mode count: total computed from file content (not DOM), global index determined by paragraph text positioning, resolving inaccurate counts and scroll-dependent changes under lazy rendering
- **翻译补全** — 补全 `floating.openMainPanel`、`floating.addRemark`、`floating.removeHighlight`、`floating.pinyin`、`floating.formatReplace`、`settings.heading`、`settings.popup` 等缺失的中英文翻译 / Completed missing Chinese/English translations for `floating.openMainPanel`, `floating.addRemark`, `floating.removeHighlight`, `floating.pinyin`, `floating.formatReplace`, `settings.heading`, `settings.popup`
- **随机模式样式叠加修复** — 修复悬浮分组随机模式第二次点击时新增规则而非替换旧规则，导致同一文本叠加两种样式的bug / Fixed floating group random mode adding new rule instead of replacing old one on second click, which caused two styles stacking on the same text

## v1.8.9 (2026-07-01)

- **悬浮分组随机模式** — 悬浮样式分组右键菜单新增"随机模式"，开启后点击分组直接随机应用组内样式到选中文本，移除箭头、鼠标悬浮不展开子菜单 / Added "Random Mode" to floating style group right-click menu; when enabled, clicking the group directly applies a random style from the group to selected text, arrow removed, hover does not expand submenu
- **移除打开文件链接设置** — 移除主面板设置-显示中的"不显示标题后面的打开文件链接"选项及⚙️后的"打开data.json"链接 / Removed "Hide open file link after title" setting option and "Open data.json" link next to ⚙️ in main panel
- **移除折叠时显示最近规则设置** — 移除主面板设置-显示中的"折叠时显示最近规则"选项 / Removed "Show recent rules when collapsed" setting option from main panel display settings
- **默认不启用标题样式** — 新装插件默认禁用标题样式和标题层级标签显示 / New installations now default to disabling heading styles and heading level labels
- **默认分组显示在切换标签区域** — 自动生成的"新分组"默认显示在切换标签区域（"+"按钮前），而非常显区域 / Auto-generated "New Group" now defaults to switchable tab area (before "+" button) instead of always-visible area
- **英文预览文本改为gloss** — 默认英文预览文本从"Preview"改为"gloss" / Default English preview text changed from "Preview" to "gloss"

## v1.8.8.5 (2026-07-01)

- **移除样式使用次数(count)功能** — 完全移除 `_count.json` 计数文件生成机制及相关代码，包括 `updateStyleCountFile`、`loadStyleCountFile`、`loadAngle0Styles` 等函数，以及所有 16 处调用点和 6 条 i18n 条目 / Completely removed `_count.json` count file generation mechanism and related code, including `updateStyleCountFile`, `loadStyleCountFile`, `loadAngle0Styles` functions, all 16 call sites and 6 i18n entries
- **随机高亮改为内存计算** — `getUnusedStyles` 不再依赖 count 文件，改为从内存中的 `fileRules` 和 `globalRules` 实时统计未使用样式 / `getUnusedStyles` no longer depends on count files; now computes unused styles from in-memory `fileRules` and `globalRules` in real-time
- **文件规则合并为单JSON** — 所有文件高亮规则从 `data/{编码文件名}.json` 合并到 `data/file-rules.json`，key 使用原始文件路径，消除路径编码歧义 / Merged all file highlight rules from individual `data/{encoded_name}.json` files into single `data/file-rules.json`, using original file paths as keys to eliminate path encoding ambiguity
- **内存缓存+Debounce写入** — `saveFileRules` 先写入内存缓存 `_fileRulesData`，500ms debounce 后批量写磁盘，`loadFileRules` 从内存读取零IO / `saveFileRules` writes to in-memory cache `_fileRulesData` first, flushes to disk with 500ms debounce; `loadFileRules` reads from memory with zero IO
- **自动迁移旧数据** — 首次启动时自动将零散规则文件迁移到 `file-rules.json`，同时清理所有 `_count.json` 文件，迁移完成后设置标志位不再重复执行 / Auto-migrates scattered rule files to `file-rules.json` on first launch, cleans up all `_count.json` files, sets flag to avoid re-running
- **文件重命名简化** — 重命名/移动文件时直接操作内存缓存 key，不再涉及文件系统级 rename / File rename/move now operates on in-memory cache keys directly, no more filesystem-level rename operations

## v1.8.8.4 (2026-06-30)

- **禁用规则移至右键菜单** — 移除Shift+右键禁用规则操作，将禁用/启用规则选项添加到规则右键菜单中 / Moved disable/enable rule from Shift+right-click to right-click context menu
- **修复禁用规则不生效** — 修复因浅拷贝导致修改副本而非原始规则对象，禁用规则提示成功但实际未生效的bug / Fixed rule disable not working due to shallow copy modifying clone instead of original rule object
- **备注弹窗按文件分组显示** — 悬浮备注弹窗优先显示links中的备注（按文件分组、带文件名标签和色点），无link备注时回退显示外部remark / Remark hover popup now groups remarks by source file with filename labels and color dots; falls back to external remark
- **设置栏底部固定改造** — 移除折叠式设置面板，改为⚙️图标+chip常驻面板底部，hover显示chips，点击chip弹出悬浮窗口 / Replaced collapsible settings panel with fixed bottom bar (⚙️ icon + chips); hover to show chips, click to open floating popup
- **设置chip悬浮窗口** — 点击chip弹出悬浮设置窗口，chip间划过自动切换内容，鼠标离开延迟关闭 / Settings chip opens floating popup; auto-switch on hover between chips; delayed close on mouse leave
- **设置栏固定在面板底部** — 设置栏从contentEl移至modalEl，始终固定在面板底部不随内容滚动 / Settings bar moved from contentEl to modalEl, always fixed at panel bottom
- **修复点击设置弹窗退出主面板** — 在outsideClickHandler排除列表中添加设置弹窗，避免点击弹窗关闭主面板 / Fixed clicking settings popup closing main panel by adding popup to outsideClickHandler exclusion list
- **设置弹窗自适应高度** — 移除max-height滚动限制，弹窗自适应内容高度，内容展开时MutationObserver自动重新定位 / Removed max-height scroll limit; popup auto-sizes to content; MutationObserver repositions on content changes
- **拼音/行间注释弹窗加宽** — 拼音样式和行间注释样式的设置弹窗使用更宽尺寸（460~700px）以容纳textarea / Wider popup (460~700px) for Pinyin and Interlinear Note settings to accommodate textareas

## v1.8.8.3 (2026-06-30)

- **移除Ctrl+Enter更新规则** — 移除无效的Ctrl+Enter快捷键（Obsidian全局快捷键拦截），改用输入框右侧"更新规则"chip按钮 / Removed non-functional Ctrl+Enter shortcut (intercepted by Obsidian global hotkeys); replaced with "Update Rule" chip button next to input field
- **更新规则Chip按钮** — 输入框右侧新增"更新规则"chip按钮，点击规则按钮后高亮可用，无选中规则时灰色禁用 / Added "Update Rule" chip button next to input; highlighted when a rule is selected, grayed out when no rule is selected
- **showErrorMessage调用修复** — 修复`showErrorMessage`单参数调用导致styleOption.appendChild抛出TypeError的问题 / Fixed TypeError from calling showErrorMessage with wrong number of arguments
- **editRule/editGlobalRule返回布尔值** — 规则编辑失败时返回false，`updateCurrentRule`检查返回值避免误报成功 / editRule/editGlobalRule now return boolean; updateCurrentRule checks return value to avoid false success messages
- **规则按钮高亮边框修复** — 清除高亮时同时清除全局规则按钮边框；移除蓝色/橙色固定边框改为透明 / Fixed highlight border not clearing on global rule buttons; removed blue/orange fixed borders in favor of transparent
- **匹配高亮统一为主题色粗边框** — 规则按钮和样式按钮的匹配高亮统一为`2px solid var(--interactive-accent)`，移除scale/发光效果 / Unified matching highlight to `2px solid var(--interactive-accent)` for both rule and style buttons; removed scale/glow effects
- **规则按钮hover备注弹窗** — 全局规则按钮和history按钮添加备注hover弹窗，复用编辑区备注弹窗样式 / Added remark hover popup to global rule and history buttons, reusing editor remark popup styles
- **选中文本自动展开规则分组** — 匹配规则按钮时自动展开其所在规则分组chip，确保高亮可见 / Auto-expand rule group chip when matching rule button is found, ensuring highlight is visible
- **样式按钮缺少data-class属性** — 修复样式按钮未设置`data-class`属性导致样式chip不自动激活、样式按钮不高亮的根本问题 / Fixed style buttons missing `data-class` attribute, which was the root cause of style chips not auto-activating and style buttons not being highlighted

## v1.8.8.2 (2026-06-29)

- **Chip激活后规则按钮不显示** — 修复高亮规则区域点击分组chip后规则按钮消失的问题；激活分组时清除maxHeight限制并恢复按钮display / Fixed rule buttons disappearing after clicking group chip in highlight rules section; clear maxHeight restriction and restore button display on activation
- **删除规则index错误** — 修复右键/中键删除规则时使用allRules索引而非globalRules索引导致删除失败或删错规则的问题 / Fixed wrong index used when deleting rules via right-click/middle-click; use globalRules index instead of allRules index
- **全局规则移到当前文件后原规则未删除** — 修复移动全局规则到当前文件时原全局规则仍保留的问题（复制而非移动） / Fixed global rule not removed after moving to current file (was copying instead of moving)
- **删除文件规则提示"全局规则已删除"** — 修复删除文件规则时显示全局规则删除提示的问题，现在区分文件/全局规则显示不同提示 / Fixed file rule deletion showing "global rule deleted" message; now shows correct message based on rule type
- **deleteRuleById调用错误** — 修复`this.plugin.deleteRuleById`应为`this.deleteRuleById`导致的TypeError / Fixed TypeError from calling deleteRuleById on plugin instead of modal instance
- **文件规则移到分组后刷新又出现** — 修复文件规则移到分组后刷新页面规则重新出现的问题；移到分组时先转为全局规则再从文件规则中删除 / Fixed file rule reappearing after moving to group; convert to global rule and remove from file rules before assigning to group

## v1.8.8 (2026-06-24)

- **Remark Popup Save Button** — Added "s" button in popup title bar for saving remark as file; removed right-click context menu "Save as File" option / 备注弹窗标题栏新增"s"保存文件按钮；移除右键菜单的"保存为文件"选项
- **Remark Popup Interlinear Note Field** — Replaced "i" button with always-visible text field in title bar for interlinear note; supports double-click to edit and drag-drop text to set note; shows existing note content / 备注弹窗标题栏新增常显行间注释文本框，替代原"i"按钮；支持双击编辑和拖放文本设置行间注释；显示已有注释内容
- **Remark Popup Title Bar Layout** — Buttons (g/l, s, inNote) now grouped tightly on the left side of title bar; keyword name stays centered with original width / 标题栏按钮（g/l、s、行间注释）左侧紧凑排列；关键词名居中保持原宽度
- **Remark Popup Resize Handle** — Added resize handle at bottom-right corner of remark popup; supports both mouse drag and mobile touch to adjust height / 备注弹窗右下角新增resize手柄，支持鼠标和手机触摸调整高度
- **Chip Window Touch Resize** — Added touchstart event to chip window resize handle; onTouchMove now handles both drag and resize; fixed onTouchEnd not resetting isResizing state / Chip弹窗resize手柄支持触摸事件；修复touchEnd未重置isResizing导致调整后点击弹窗会移动右下角
- **Chips Bar Touch Drag** — Bottom chips area in both remark popup and chip window now supports touch drag to move the popup/window / 备注弹窗和chip弹窗底部chips区域支持触摸拖动移动弹窗位置

## v1.8.7 (2026-06-23)

- **Chip Window Max Height** — Added max-height limit to keyword-detail-window; long remarks scroll inside content area instead of expanding the window infinitely, preventing mobile freeze and bottom buttons being pushed off-screen
- **Chip Window "+" and "?" Buttons** — Added floating "add remark" and "AI question" buttons at bottom of chip window, matching remark popup style with gradient text and animations
- **Chip Window Double-click Edit** — Double-clicking remark content in chip window now enters edit mode with textarea; blur saves and replaces in-place without rebuilding the window
- **Chip Window AI Question Buttons** — Added "?" (break down question) and "delete" buttons to askedbyAi entries in chip window, matching remark popup behavior
- **Chip Window Empty Remark Hint** — Empty remark entries now show "(双击编辑备注)" placeholder text in both regular and AI question entries
- **Chip Window Resize Beyond Default** — Drag-resizing chip window now syncs max-height, allowing users to expand height beyond the default limit
- **Chip Window Size Preservation** — After editing or adding remarks via AI/"+" buttons, chip window preserves user-adjusted size and position instead of resetting to defaults
- **Remark Popup Width Fix** — Fixed remark popup width unable to shrink after exiting edit mode; renderAllRemarks now resets minWidth lock

## v1.8.6 (2026-06-23)

- **AI Question Feature** — Added "?" button next to "+" in remark popup; AI generates targeted questions based on keyword and related keyword remarks to help deepen understanding
- **AI Conversation Thread** — Each AI question supports multi-turn dialog: "?" button asks AI to break down the question, "↗" button sends user's answer back to AI for feedback; thread persisted in `_aiThread` array
- **AI Question Text Wrapping** — Fixed long AI question text not wrapping in title bar; replaced `white-space:nowrap` with `overflow-wrap:break-word`
- **AI Question Persistence** — Fixed AI question entries being deleted on popup close when user hasn't answered; `doHide` cleanup now preserves links with `_aiQuestion`
- **DeepSeek Model Validation** — Removed outdated hardcoded model whitelist that caused false warnings during API test; API test success itself validates the model
- **Preview Language Switch Fix** — Fixed English mode reverting "Preview" to Chinese "示例" after canceling style edit; replaced hardcoded Chinese with `t('entity.preview')`
- **Floating Group Arrow Duplication Fix** — Fixed default-style floating group buttons appending duplicate arrows on each drag; now uses reusable `<span>` element instead of `innerHTML` concatenation

## v1.8.5 (2026-06-22)

- **Random Highlight Group Filter i18n** — Fixed hardcoded Chinese strings in "Random Highlight Group Filter" settings (title, description, empty hint) not translating in English mode; added missing i18n keys and English translations; updated description to include usage hint about selecting text and clicking the floating ball
- **Style Usage Count Badge Default Off** — Changed default value of "Style Usage Count Badge" from enabled to disabled for new installations; added warning hint that enabling this feature generates many count files in the data folder
- **Panel Title Rename** — Changed main panel title from "regex css highlighter" to "SwiftGloss"

## v1.8.4 (2026-06-22)

- **Interlinear Note + Style Coexistence Fix** — Reading mode now applies interlinear notes first, then style highlights; `clearHighlights` preserves `in-note-wrapper` structure instead of destroying it; notes with styles now display correctly without scrolling
- **Mobile Pin Button Removal** — Removed 📌 float buttons from group/style buttons in main panel on mobile to prevent accidental taps
- **SwiftSwitch Hint** — Added hint in CSS Snippets settings: "Desktop only, restart required, recommend SwiftSwitch" with `obsidian://show-plugin?id=swift-snippets` link
- **Rule Edit Input Width** — Double-click to edit rule name now enforces minimum 80px width so short rules remain readable

## v1.8.3 (2026-06-21)

- **Remark Popup Improvements** — Pinned popup no longer closes on outside click; scroll/resize no longer resets position; custom resize handle replaces CSS resize; "+" button for adding remarks
- **Keyword Detail Window Unification** — Chip popup window style unified with remark popup; content uses flex layout; entries show bullet+search tag+copy/open buttons; bottom chips with hover preview and color extraction
- **Chip Color Fix** — Keywords using `color:transparent` + `background-clip:text` now extract gradient color for chip text
- **Jump Highlight** — Jump-to-document highlights search text (marshmallow style); CM6 Decoration in edit mode, Range.surroundContents in read mode; 1250ms delay for plugin compatibility
- **Random Highlight Group Filter** — Floating ball settings now have chips selector to limit random styles to specific groups
- **Interlinear Notes** — New feature: select text → floating input box → `::before` pseudo-element / CM6 Decoration display; independent storage in `interlinear-note-data.json`; 6 presets + alignment setting + custom CSS
- **Chip Popup Refinements** — Smaller bullets (6px), compressed margins, user-select:text, drag-to-pin close behavior, long-press ✕ closes all, editable search text and rule name, mobile width limit and touch drag
- **Piped Regex Matching** — Rules with `|` (e.g. "犬儒派|犬儒主义") now correctly matched in chips backlinks via `plainTexts` array
- **Interlinear Notes Refactor** — `in-note-wrapper` replaces per-character spans; `!important` reset on `::before`; inherits parent gradient styles; alignment setting; simplified to dropdown + CSS textarea
- **Remark Popup Interaction** — No popup on text selection (`e.buttons>0`); delayed refresh after close when text selected; new "Hide popup on selection" setting
- **Mobile Fixes** — Short tap closes current / long press closes all; prefer live selection over cache; mousedown excludes INPUT elements

## v1.8.2 (2026-06-19)

- **Floating Ball Label** — Changed floating ball text from "rch" to "SG"
- **Pinyin Submenu Pin Buttons** — Added 📌 pin buttons to all pinyin submenu items (Add Pinyin Local/Global, Edit Pinyin File, Remove Pinyin) for floating display
- **Font Switch Hover Submenu** — Changed "Font Switch" option from click-to-open to hover-to-open submenu, consistent with other submenu options; added 📌 pin buttons to font switch submenu items
- **Submenu Pin Button Fix** — Fixed pinned submenu items showing raw option IDs instead of localized labels, and fixed click handlers not working when pinned as floating buttons
- **Global Rules Scroll Fix** — Removed the independent scrollbar in the global rules section; now uses the main panel scrollbar for unified smooth scrolling

## v1.8.1 (2026-06-19)

- **Single-Display Group Fix** — Fixed single-display groups being incorrectly moved to always-display area when highlighting matched styles; single-display groups now stay in their tab area with proper style button highlighting
- **Single-Display Style Buttons Fix** — Fixed style buttons always appearing collapsed when reopening the main panel with an active single-display group; buttons now correctly display as expanded
- **Single-Display Tab Arrow** — Changed the active single-display tab indicator from a triangle arrow to a red horizontal line for clearer visual identification
- **Snippet Manager Disable** — When "Enable Snippet Manager" is unchecked, the snippets list and status bar option are now hidden in settings, fully disabling the feature

## v1.7.7 (2026-06-19)

- **Snippet Manager** — New CSS Snippets management feature with a frosted-glass popup window: toggle snippets on/off via chips, add/edit/delete/copy snippets, edit with external program, drag chips to reorder
- **Snippet Groups** — Organize snippets into collapsible groups; right-click to add/rename/delete groups; drag chips between groups; "Ungrouped" section for unassigned snippets
- **Status Bar Button** — Optional "CSS" button in the status bar for quick access to the snippet manager
- **Enable Heading Styles** — Reversed "Disable Heading Styles" setting to "Enable Heading Styles" with inverted logic; heading styles are now enabled by default
- **Snippet Manager Toggle** — Added master switch to enable/disable the entire snippet manager feature
- **Custom Input Dialog** — Replaced unsupported Electron `prompt()` with a custom frosted-glass input dialog for group naming

## v1.7.6 (2026-06-17)

- **Plugin Startup Performance Optimization** — Cached `require('fs')`/`require('path')` at module level to eliminate repeated `require` calls; cached `styles.css` content to reduce 5 disk reads to 1; batched all `saveData()` calls in `onload()` from 10+ async writes to at most 1; parallelized independent async operations (`loadStyleCategories`, `loadGlobalRules`, `_preloadPinyinData`) with `Promise.all`; eliminated duplicate `style-categories.json` reads in `syncStylesToCategories`; deferred `cacheHoverStyles()` to lazy-load on first use instead of blocking startup; fixed `_preloadPinyinData()` being called twice

## v1.7.5 (2026-06-15)

- **Remark Popup File Name Sync Fix** — Fixed file name in remark popup not updating after renaming a note; `handleFileRenameOrMove` now updates `links[].filePath` in all rules (current file, global, and other files) and persists changes to disk

## v1.7.4 (2026-06-14)

- **Dark Mode Title Visibility Fix** — Removed hardcoded `#555` color from "Single Display" and "Always Display" section titles, now uses default theme text color for proper visibility in dark mode
- **Single-display Tab Arrow Indicator** — Added a downward-pointing triangle arrow below the active single-display tab, visually connecting the tab to the content panel below

## v1.7.3.1 (2026-06-14)

- **Release Asset Fix** — Fixed missing main.js and manifest.json in GitHub release assets

## v1.7.3 (2026-06-14)

- **Release Asset Fix** — Fixed missing main.js and manifest.json in v1.7.2 GitHub release assets

## v1.7.2 (2026-06-14)

- **Group Button Default Style** — Changed group button default style from blue background with white text to white background with black text; custom styles now properly override the default
- **Single-display Tab Element Fix** — Changed single-display tab from `<button>` to `<h4>` element, fixing custom styles (gradient backgrounds, custom colors) not applying correctly
- **Single-display Active State Persistence** — Single-display group active state is now saved and restored when reopening the main panel

## v1.7.1 (2026-06-14)

- **Remark Badge Click Popup Fix** — Fixed remark popup not appearing immediately when clicking the "n" badge to add a remark while hover delay is non-zero; popup now shows instantly and is protected from accidental mouseout cancellation
- **Default Settings for New Install** — New installs now default to: showRemarkBadge=true, remarkBadgeThreshold=2, popupLineHeight=1.5, popupBorderWidth=2, popupBorderColor=#ffffff

## v1.7.0 (2026-06-10)

- **Mobile Context Menu Fix** — Fixed long-press style button options freezing, clicks not responding, and options remaining visible after closing the main panel on mobile
- **Mobile Submenu Removal** — Removed "Add as Heading Style" and "Move to Group" submenus on mobile (they rely on mouse hover events which don't work on touch devices)
- **Remark Popup Hover Delay** — Added setting to control how long the mouse must hover over matched text before the remark popup appears; moving the mouse away before the delay cancels the popup, preventing accidental triggers
- **Add Group Instant Refresh** — Fixed new groups not appearing in the main panel after adding; panel now refreshes immediately

## v1.6.9 (2026-06-09)

- **Single-display Group Pin Button Fix** — Changed single-display tab 📌 button from inline to absolute positioning (matching always-visible groups), removed overflow:hidden that was clipping the button
- **Main Panel Dark Background Fix** — Injected !important CSS rule (.rch-transparent-bg) to forcefully override Obsidian's default modal-bg background, combined with MutationObserver for triple-layer protection
- **Main Panel Lock Improvement** — Lock button now directly sets pointer-events on modal-bg and modal-container to allow editor interaction when locked; fixed previously ineffective CSS class approach
- **Lock Focus Stealing Fix** — When locked, focusin events not triggered by user clicks on the panel are intercepted and focus is returned to the editor, preventing the panel from stealing focus
- **Resize Handle Follows Panel** — Right-bottom resize handle now updates position in real-time when dragging the main panel

## v1.6.8 (2026-06-08)

- **Popup z-index Improvement** — Sub-modals (add group, rename, CSS editor, etc.) now appear above the main panel by raising their own z-index instead of lowering the main panel's, preventing Obsidian's sidebar divider from overlapping the panel

## v1.6.7 (2026-06-08)

- **Sticky Title Bar** — Main panel title bar now stays fixed at the top when scrolling content
- **Scrollbar Position Fix** — Resizing the main panel no longer causes the scrollbar to jump to the left of the close button
- **Removed Display Settings** — Removed "Main Panel Opacity" and "Main Panel Width" settings from Display section; Ctrl+scroll and Alt+scroll shortcuts still work
- **Instant Group Toggle** — Toggling "Hide All Groups by Default" now immediately refreshes the panel instead of waiting for next open
- **Popup z-index Fix** — CSS editor and remark editor popups now correctly appear above the main panel
- **Cancel Button Optimization** — Clicking "Cancel" in CSS editor no longer triggers unnecessary UI refresh
- **Toggle Collapse Performance** — Expand/collapse operations no longer wait for file save, eliminating 1.7s delay after CSS editor closes
- **Main Panel Open Speed** — Deferred rendering of rules/settings sections, removed forced reflows, and batched font fixes for faster panel opening

## v1.6.6 (2026-06-07)

- **Rule Conversion Merge** — When converting a rule between global and local, if a rule with the same regex already exists in the target, the cssClass is overwritten and remark/links are merged instead of blocking the conversion
- **Popup Rule Source Badge** — Added l/g (local/global) badge at the top-right corner of remark popup, always visible and clickable to convert rule source
- **Remark Popup i18n** — Translated hardcoded Chinese strings in remark popup (double-click to edit, no search text, no title, copy/open/delete remark) for English mode support
- **Updated Remark Demo GIF** — Replaced addremark.gif with new demo animation

## v1.6.5 (2026-06-03)

- **Pseudo-element Style Support** — Add Style dialog now correctly previews and saves CSS rules with pseudo-elements (::before, ::after); pseudo-element rules are associated with their parent class
- **@keyframes Animation Support** — Add Style dialog now correctly previews and saves CSS rules with @keyframes animations; animation rules are placed below the main style rules; @keyframes blocks are stripped before class parsing to prevent false matches from decimal values inside keyframe definitions
- **Remove Highlight Regex Matching Fix** — Fixed bug where rules containing regex escape characters (e.g. `\\.`) could not be matched when removing highlights by selecting text; replaced direct string comparison with regex matching via `textMatchesRegex()` helper function
- **Remove Preview Checkboxes** — Removed checkboxes from style preview in Add Style dialog; clicking "Add Style" now adds all parsed styles by default
- **README Add Style Demo** — Added "Add Style" and "AI Create Style" demo GIFs to README in both English and Chinese sections

## v1.6.4 (2026-06-03)

- **Main Panel Group Button Style Customization** — Added right-click context menu option to edit group button style class; supports custom CSS class preview and application
- **Dark Mode Title Text Visibility Fix** — Removed custom text colors from panel titles, style list/group labels, and settings text; now uses default theme colors for proper dark mode support
- **Pin Submenu Button Repositioned** — Moved "Pin Submenu" button to top-left corner of submenus to avoid blocking style buttons
- **Submenu Direction Adaptation** — Floating group submenus now open to the left when the group is on the right side of the screen, preventing overlap with group buttons on mobile
- **Mobile Horizontal Scroll Fix** — Mobile now limits modal width to screen width even when desktop saved a larger modalWidth value; prevents horizontal overflow caused by cross-device settings sync

## v1.6.3 (2026-06-02)

- **Fixed Callout Highlight Not Showing in Edit Mode** — Added `applyHighlightsToLivePreviewCallouts` method to apply DOM-based highlighting to callout widgets in live preview mode; ViewPlugin's update now schedules callout highlight via debounced `requestAnimationFrame`; scroll and layout-change events also trigger callout highlighting in source mode
- **Fixed Overlapping Decoration Ranges** — Improved range sorting with secondary `to` key; added validation filter for invalid ranges; switched to `Decoration.set(validRanges, true)` to enable CodeMirror's internal sorting for safer handling of overlapping decorations from multiple rules
- **Added Remark Demo GIF** — Added `addremark.gif` to assets folder and referenced it in both English and Chinese Notes/备注功能 sections of README.md

## v1.6.2 (2026-06-02)

- **Custom Default Preview Text** - Added "Default Preview Text" setting in Display section with separate Chinese/English input fields; when no text is selected, style buttons show custom text instead of default "示例"/"Preview"
- **Fixed Clickable Title Text for Rules Sections** - Clicking "Current File Rules" and "Global Rules" title text now correctly triggers expand/collapse; added pointer-events:none to h3 and description elements to ensure click events bubble properly
- **Highlight List Search No Data Fix** - When column filters match no results, table header with search inputs is now preserved instead of being cleared; "No data" message appears in tbody while search remains functional
- **Visible Column Resizer** - Column resize handles in highlight list are now always visible with a subtle border color; hover highlights in accent color
- **Fixed Column Resize Affecting Other Columns** - Dragging a column resizer now only adjusts the current column and its right neighbor (one grows, one shrinks); other columns remain unaffected
- **Smooth Column Resizing** - Cached table width on mousedown instead of reading DOM on every mousemove; eliminated layout thrashing for smooth drag experience
- **Highlight List Performance Optimization** - Used DocumentFragment for batch DOM construction; replaced per-row event listeners with event delegation on tbody; eliminated duplicate filter computation in stats display

## v1.6.1 (2026-06-02)

- **Remark Badge Indicator** - Added "Show remark indicator at top-right of highlighted text" setting under Remark Popup section; hovering highlighted text shows a small "n" badge, clicking it opens the Add Remark modal; includes character threshold option
- **Long Phrase Priority Matching** - When merging rules (e.g. "视角主义" + "视角主义真理观"), longer phrases now match first; added sortRegexByLength utility function applied to all regex matching logic
- **Fixed Remark Popup in Edit Mode Callouts** - Remark popup now works correctly in CodeMirror edit mode for text inside callouts; changed from classList.contains to closest() for upward DOM traversal
- **Remark Popup Setting Name Fix** - Renamed "确认后不自动关闭" to "鼠标离开不自动关闭"; remark popup now auto-closes after clicking confirm
- **Global Highlight Rules Scrollbar** - Added scrollbar to global highlight rules section when content exceeds viewport height
- **Hide Open File Links Setting** - Added "Don't show open file links after panel titles" setting in Display section; controls visibility of "Open styles.css", "Open group file", "Open data.json" links
- **Localized Default Group Name** - Default group name for new styles now follows plugin language (e.g. "New Group" in English mode)
- **Floating Element Initial Position** - First-time hover on options/groups/style buttons now positions near the mouse cursor
- **Language Switch Instant Refresh** - Switching language now immediately refreshes the panel without needing to reopen
- **Fixed Arrow Position After Style Edit** - Arrow indicator now stays inside the group style area after editing custom styles
- **Floating Group Button Positioning** - Each floating group button appears near the mouse cursor with top-right corner aligned to mouse position; position info cleared on close
- **Full-Width Clickable Panel Titles** - "Settings", "Current File Rules", "Global Rules" titles now have full-width clickable area and background shading for expand/collapse

## v1.6.0 (2026-06-01)

- **Floating Group No Longer Auto-Added to Floating Ball Menu** - Floating a group via main panel group title hover button or right-click "Float This Group" now only creates floating buttons without automatically adding the group to the floating ball menu; users can manually add groups in the floating ball menu settings

## v1.5.9 (2026-06-01)

- **Default Language Changed to English** - New installations now default to English; Chinese users can switch via CN/EN button
- **Floating Ball Options Simplified** - Format Replace, Ruby, AI Reply, Entity Extract, Font Switch, Mode Switch, Hide Floating Buttons, Show/Hide Text Styles are unchecked by default for new installations
- **Heading Styles Disabled by Default** - New installations have heading styles disabled to reduce visual clutter
- **Floating Ball Menu Position Fix** - Menu now appears on the left side when floating ball is on the right half of the screen, avoiding overlap
- **English Menu Text Wrapping Fix** - Increased menu width and added nowrap to prevent English option text from wrapping to two lines
- **Plugin Market Support** - Added versions.json for Obsidian plugin market compatibility; install directly by searching "Regex Css Highlighter"
- **README Updated** - Added demo GIFs, plugin market install instructions, removed keyboard shortcuts section, manual install moved to collapsible section
- **Changelog Migrated to CHANGELOG.md** - Version history moved from README.md to standalone CHANGELOG.md file

## v1.5.8 (2026-06-01)

- **Removed "About" Section** - Removed "About" section from bottom of main panel; version changelog migrated to CHANGELOG.md
- **Cleaned Up Donation Code** - Removed showDonateImage class methods and standalone functions, setupDonateText function, donation button CSS styles, and related translation keys
- **Cleaned Up Unused Translation Keys** - Removed main.tab.about, settings.about, settings.updateHistory, settings.viewUpdates and other unused translation keys
- **Removed DONATE_QR_CODE Constant** - Removed base64-encoded donation QR code image constant

## v1.5.7 (2026-05-31)

- **Internationalization Support** - Added CN/EN language switch button in main panel, supports switching between Chinese and English interfaces
- **Full i18n Coverage** - All UI text including settings titles, floating ball options, and group style buttons fully internationalized
- **"Show/Hide Text Styles" in Floating Ball Management** - Added option to control whether this feature appears in floating ball menu
- **Fixed Auto-Scroll on Middle-Click in Group Submenu** - Middle-click to add global rules no longer triggers auto-scroll state
- **Style Name Column in Highlight List** - Added style name column to highlight list; display text shown on separate line when present; toggleable visibility
- **Per-Column Header Search** - Added search box to each table header with placeholder showing header text, supports real-time per-column filtering
- **Removed "Add to Highlight List" Feature** - Removed style button right-click "Add to Highlight List" option and highlight list filters: show style name, by style name
- **Min Count Always Visible** - Removed mode dropdown; min count input always visible; Chinese label changed to "样式最少被应用 [X] 次"

## v1.5.6 (2026-05-31)

- **Floating Submenu Right-Click Options** - Added "Modify Display Text", "Copy Class Name", "Copy Full Style" options to floating group submenu style right-click menu
- **Submenu Right-Click UX Fix** - Fixed issue where submenu would hide when mouse moved to right-click menu options
- **Middle-Click for Global Rules** - Middle-click on floating group submenu style adds selected text as global rule
- **Rule Source Markers (g/l)** - Hover over matched rule text to show global/local marker "g/l", click to jump to corresponding rule; supports character count threshold setting
- **Edit Mode Marker Fix** - Fixed bug where "g/l" markers were added as text content in edit mode
- **Floating Submenu Class Name Hint** - Hover over floating group submenu style items to display class name hint
- **Text Style Show/Hide** - Added "Show Text Styles"/"Hide Text Styles" options to floating ball hover menu; hides all text style matches when hidden

## v1.5.5 (2026-05-29)

- **Hidden Position Data Preservation** - Saves position data when hiding floating style buttons; automatically restores to original position on next show
- **Floating Display Button in Main Panel** - Added 📌 button that appears on hover over style buttons in main panel; click to float display that style

## v1.5.4 (2026-05-28)

- **Clean Up Non-Existent Styles** - Added "Clean Up Non-Existent Styles in Category Files" feature under Settings → Display; scans and removes styles present in style-categories.json but missing from styles.css
- **Scrollbar for Group Submenus** - Added scrollbars to floating ball menu and floating option button group style submenus; prevents overflow when many styles exist
- **Light Blue Background for Settings Headers** - Added light blue background to all level headers in main panel settings for better visual hierarchy

## v1.5.3 (2026-05-27)

- **Mobile Reading Mode Line Height** - Added line height setting in mobile "Display" settings; merged with margin settings into "Mobile Reading Mode Line/Margin"
- **Mobile Panel Opacity** - Added main panel and button panel opacity settings in mobile "Display" settings
- **Mobile Typography Settings Separated** - Mobile no longer applies desktop line height and margin settings; controlled by mobile-specific settings
- **Mobile Auto-Expand Fix** - Fixed bug where first style was incorrectly applied to text when group expanded in mobile auto-expand mode
- **Header Settings Category** - Moved "Header Level Tags" and "Disable Header Styles" to newly created "Headers" settings category
- **Count Info Fix** - Fixed bug where "Style Categories" and "Count Files" count info not displayed on same line; removed link styling
- **Floating Ball Menu Opacity** - Floating ball menu supports Ctrl+scroll to adjust opacity; preserved after restart
- **Right-Click Menu Improvements** - Auto-closes previous menu when right-clicking another style; added "Move to Group" option in normal mode right-click menu

## v1.5.2 (2026-05-26)

- **Settings Outline Reorganization** - Changed settings from flat separator line format to outline-style indentation with collapse/expand, better visual hierarchy
- **Show Recent Rules When Collapsed** - Added setting to control whether to show recently added rules when main panel opened with no text selected and highlight rules collapsed
- **Hide Font Switch on Mobile** - Hidden font switching feature area on mobile devices
- **Hide Open File Link on Mobile** - Hidden open data.json file link next to "Settings" header on mobile

## v1.5.1 (2026-05-25)

- **Typography Settings** - Added line height, left margin, and right margin settings in "Switch Body Font" popup; works in both edit and reading mode
- **Scroll Wheel Value Adjustment** - Line height and margin input fields support mouse wheel for quick value adjustment
- **Edit Mode Margin Fix** - Fixed issue where left/right margins not working in edit mode

## v1.5.0 (2026-05-25)

- **Disable Header Styles** - Added "Disable Header Styles" toggle in settings; when disabled, custom header styles not applied but header level tags preserved; "Header Styles" area hidden in main panel when disabled
- **Level Tags Compatible with Gradient Text** - Fixed issue where level tags invisible when using gradient text CSS snippet; reset inherited transparent text and background-clip properties in pseudo-element
- **Removed Usage Instructions** - Removed "Usage Instructions" content from main panel for cleaner UI

## v1.4.9 (2026-05-25)

- **Instant Style Application** - Fixed issue where adding/editing/deleting styles required Obsidian restart to display; new styles now take effect immediately
- **Style Refresh Mechanism Optimized** - Removed destructive forceStyleRefresh call to avoid clearing newly injected CSS; directly update dynamic style elements after writing CSS file, no re-read needed
- **CSS Read/Write Consistency Fix** - Changed injectCSSContent to use vault.adapter.read for consistency with write API, avoiding cache desynchronization
- **Modal Refresh Acceleration** - Removed multi-layer setTimeout delays (500ms+200ms) after adding styles; popup refreshes instantly
- **Delete Style Instant Refresh** - Removed 1-second delay after deleting styles; immediately re-inject CSS and refresh view

## v1.4.7 (2026-05-24)

- **System Font Switching** - Font switching now directly reads installed system fonts, no font files needed; eliminates CSP/OTS compatibility issues
- **Font Favorites Feature** - Font list supports starring to favorite; favorited fonts pinned to top for easy access
- **Font Search** - Added search box to font selection popup for quick font filtering and positioning
- **Font List Styling** - Card-style layout, SVG star icons, "In Use" label, hover interaction optimizations

## v1.4.6 (2026-05-22)

- **DeepSeek Default Config Update** - For new plugin installations, DeepSeek default base_url changed to https://api.deepseek.com/chat/completions, model changed to deepseek-v4-flash
- **Style Class Name Hint** - Added hint to style class name input field in edit floating option window: "Long-press/right-click main panel style button → Copy Class Name"

## v1.4.5 (2026-05-22)

- **Floating Ball Remove Highlight** - Added "Remove Highlight" option to floating ball; click after selecting highlighted text to remove corresponding rule; supports intelligent multi-part rule splitting
- **Rule Right-Click Menu Enhanced** - Current file rule and global rule buttons right-click menu added "Delete Rule" and "Move to Global/Current File Rule" options
- **Reading Mode Selected Text Fix** - Fixed issue where selecting text in reading mode then opening main panel couldn't get selected text; save selection before modal opens
- **Floating Option Arrow Fix** - Fixed issue with two arrows appearing on floating option button after editing style; arrow moved inside style area to save space
- **Mobile Main Panel Optimization** - Hidden opacity/width controls and title hint message/link on mobile; regular expression label displayed on separate line
- **Removed Add Note Button** - Removed "Add Note" button from main panel; note feature still accessible via right-click menu and floating ball

## v1.4.4 (2026-05-22)

- **Floating Button Zoom Offset Fix** - Fixed bug where floating style button would move left/right when clicked after Alt+scroll zoom adjustment
- **About Panel Height Fix** - Changed "About" section height from fixed 300px to 70vh adaptive to window height
- **Copy Class Name Feature** - Added "Copy Class Name" option to style button right-click menu; one-click copy CSS class name to clipboard

## v1.4.3 (2026-05-22)

- **Reading Mode Cross-Element Highlighting** - Rewrote highlight matching logic to support matching long text across DOM element boundaries; solves issue where text with existing highlights or global rule modifiers couldn't apply new styles in reading mode
- **Right-Click Menu Overflow Fix** - Floating option button and floating style button right-click menus automatically adjust position when at screen right/bottom edges; no longer overflow screen

## v1.4.2 (2026-05-21)

- **Mobile Floating Style Button Dragging** - Fixed issue where restored floating style buttons couldn't be dragged to adjust position on mobile
- **Touch Drag Anti-Misoperation** - Floating style button touch drag no longer accidentally triggers style application

## v1.4.1 (2026-05-21)

- **Floating Option Right-Click Menu** - Changed floating option button right-click to popup menu (Edit/Close); no longer closes directly
- **Floating Option Edit Feature** - Right-click "Edit" allows modifying display text and style class name; style class name supports full pseudo-element rendering
- **Floating Option Scroll Wheel Adjustment** - Alt+scroll adjusts size, Ctrl+scroll adjusts opacity; preserved after restart
- **Floating Style Button Edit Name** - Added "Edit Name" option to floating style button right-click menu; allows modifying display text
- **Style Class Name Rendering Optimization** - Removed default border frame after setting style class name; fully injects CSS rules including pseudo-elements; supports complex styles

## v1.4.0 (2026-05-21)

- **Mobile Floating Ball Adaptation** - Increased floating ball size to 36px, adjusted default position, added position safety check to ensure visibility
- **Mobile Floating Ball Menu** - Clicking floating ball pops up option menu instead of direct highlighting; differentiated from desktop behavior
- **Mobile Floating Button Dragging** - Added touch event support to floating style buttons and floating option buttons; draggable to adjust position
- **Mobile Reading Mode Line/Margin** - Added mobile reading mode line height and left/right margin settings; moved to "Display" category; separated from desktop typography settings
- **Mobile Collapsible Filter Panel** - Changed highlight list filter area to collapsible panel; collapsed by default, click to expand
- **Mobile List-Style Highlight Display** - Changed highlight list to card-style layout on mobile; notes collapsed into highlight text, click to expand
- **Highlight List Performance Optimization** - Parallelized file reading, memory cache priority, eliminated redundant exists calls, global rule Map indexing
- **Loading State Indicator** - Shows "Loading..." indicator when highlight list opens and when filter switches; renders UI first then loads data

## v1.3.9 (2026-05-20)

- **Mobile Compatibility** - Encapsulated cross-platform file operation utility class; desktop uses Node.js fs module (high performance), mobile uses Vault Adapter (compatibility)
- **Reading Mode Scroll Highlighting** - Fixed issue where highlights lost after scrolling; added scroll event listener to automatically re-apply highlights in viewport
- **Delay Handling Race Condition Fix** - Fixed timer race condition in PostProcessor delayed batch processing

## v1.3.8 (2026-05-14)

- **Reading Mode Highlight Fix** - Fixed issue where some matched text didn't display styles in reading mode; recursively processes text nodes in nested inline elements
- **Floating Button Border Following** - Floating option buttons and floating style buttons use right positioning when at screen right edge; automatically follow movement when window border dragged
- **Disabled Rule Filtering** - Automatically filters out disabled rules during highlight processing to avoid invalid matches

## v1.3.7 (2026-05-13)

- **Image Support in Notes** - Note popup supports uploading images and pasting from clipboard; images automatically saved to attachments directory
- **Table Support in Notes** - Note popup supports Markdown table rendering with borders, header highlighting, and zebra striping
- **Note Popup Auto-Resize** - Popup automatically adjusts size based on actual image dimensions; arrow indicator position synchronized
- **Table and Callout Highlighting** - Fixed issue where highlight rules didn't display styles in tables and callouts

## v1.3.6 (2026-05-09)

- **Floating Button Boundary Constraints** - Floating ball, floating option buttons, and floating style buttons automatically inset inward when window shrinks; constrained to viewport range during dragging
- **Level-2 Submenu Overflow Fix** - Floating option level-2 submenus automatically flip direction when at right screen edge; no longer overflow window boundary
- **Window Resize Content Following** - When resizing main panel via bottom-right corner handle, internal buttons immediately re-arrange to follow

## v1.3.5 (2026-05-08)

- **Highlight List by Application Count Mode** - Added "By Application Count" display mode; allows setting minimum count threshold; automatically displays all style highlights with application count ≥ threshold
- **Window Resize Handle** - Added draggable window resize handle to bottom-right corner of main panel and entity extraction popup
- **Jump Function Fix** - Fixed error when double-clicking to jump in highlight list
- **Performance Optimization** - CSS style loading switched to Node.js fs module direct reading for improved speed

## v1.3.4 (2026-05-06)

- **Default Pinyin Style Optimization** - Default pinyin style more aesthetically pleasing for new plugin installations (red text, FangZheng ShuSong font)
- **AI Settings Link Fix** - Fixed issue where "Get API Key" link always showed OpenAI address when editing AI config

## v1.3.3 (2026-05-03)

- **Floating Ball Middle-Click** - Mouse middle-click on floating ball randomly applies style to global rules (left-click for current file rules)

## v1.3.2 (2026-05-01)

- **Floating Button Pseudo-Element Fix** - Fixed issue where floating button pseudo-element styles didn't display after restart

## v1.3.1 (2026-04-28)

- **Floating Options Feature** - Added "Float Display" button to all floating ball menu options; click to create floating button
- **Phonetic Notation Floating Button** - Phonetic notation options support float display; hover to show submenu (local/global notation, edit, delete)
- **Group Floating Button** - Group options support float display; hover to show all styles in that group
- **Style Quick Float** - Each style button in style submenu has 📌 button in top-right corner to float display that style individually
- **Settings Separation Optimization** - Group menu display and float display use independent settings; don't interfere with each other

## v1.3.0.0 (2026-04-21)

- **Float Display Feature** - Added "Float Display" option to style button right-click menu; creates draggable floating style button
- **Multiple Floating Windows** - Supports displaying multiple floating buttons simultaneously; position, opacity, and size preserved after restart
- **Main Panel Interaction Optimization** - Added Alt+mouse wheel to adjust main panel width, Ctrl+scroll to adjust opacity
- **Input Field Hints** - Shows operation hints when hovering over opacity/width input fields

## v1.2.9.9 (2026-04-21)

- **Floating Button Interaction Optimization** - Fixed issue where highlighting accidentally triggered during dragging; added movement threshold check
- **Cursor Display Optimization** - Floating buttons display hand pointer by default; displays grabbing cursor during dragging
- **Drag Logic Fix** - Fixed issue where button continuously followed mouse movement; now only responds to dragging when mouse is pressed

## v1.2.9.8 (2026-04-21)

- **Float Display Feature** - Added "Float Display" option to style button right-click menu; creates draggable floating style button
- **Multiple Floating Windows** - Supports displaying multiple floating buttons simultaneously; each click of "Float Display" creates a new window
- **Position Memory** - Floating button position, opacity, and size preserved after plugin restart
- **Interaction Features** - Hold to drag position, left-click to apply style to selected text, Ctrl+scroll to adjust opacity, Alt+scroll to adjust size
- **Right-Click Menu** - Added "Close Floating Display" option to floating button right-click menu
