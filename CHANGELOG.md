# Changelog

All notable changes to this project will be documented in this file.

## 🆕 v1.7.5 (2026-06-15)

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
