# Changelog

All notable changes to this project will be documented in this file.

## 🆕 v1.9.3 (2026-07-07)

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
