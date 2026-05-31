[中文](README.md) | English

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
