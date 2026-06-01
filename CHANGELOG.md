# Changelog

All notable changes to this project will be documented in this file.

## 🆕 v1.6.0 (2026-06-01)

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
