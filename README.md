# Caps4 settings

Syntax highlighting for Caps4 settings file

## Syntax

```caps4
♦️ Caps4 settings special symbols:
♦️ ★ prop name prefix, prop name can not contain spaces, prop name could be empty and has the prefix only
♦️ • space at the beginning or the ending of a prop value
♦️ ¶ end of paragraph
♦️ → tab
♦️ «@» «@:T» «@:L» «@:U» «@:F» placeholder for clipboard text to insert (T: trim, L: to lower, U: to upper, F: fix locale)
♦️
♦️ Typical keyboard action settings:
♦️
♦️ hotkey
♦️     ★action actionName ♦️ if actionName missing, text is assumed
♦️     ★for app ♦️ filter by app (to get app name use currentApp action)
♦️     ★isDialog true ♦️ filter by current window type; values: true or false
♦️     ★caption caption ♦️ filter by current window caption; can be regex
♦️
♦️ by default "equals" comparision is performed;
♦️ to use regex add -REGEX option;
♦️ to ignore case add -CI option
♦️ to negate add -NOT option
♦️
♦️ if no hotkey present, values will be applied to the subsequent hotkeys
♦️
♦️ ★wordLeft ♦️ send Ctrl+Shift+Left before Ctrl+V to select a word to the lreft
♦️ ★showMenuAlways ♦️ show popup menu even there is a single action assigned to a hotkey
♦️ ★centerScreenMenu ♦️ show popup menu in the center of the screen
♦️
♦️ Actions:
♦️
♦️ text
♦️     ★ ♦️ text to insert or replace
♦️     ★pattern ♦️ text to match (can be regex)
♦️     ★from selection | clipboard
♦️     ★external exe-file-name
♦️     ★args app-args
♦️     ★desc description ♦️ for popup menu
♦️     ★prefix prefix ♦️ for popup menu
♦️
♦️ clipboardHistory
♦️ clipboardFormats
♦️ currentApp
♦️ keyboardLayout
♦️ keyboardLayoutRecode
♦️
♦️ runApp
♦️     ★desc description ♦️ for popup menu
♦️
♦️ sendKeys
♦️ smartPaste
♦️ sortLines

Shift+A ★ this text is pasted on shift+a
Shift+B ★ •••three spaces around•••
Shift+B ★ first line¶second line

♦️ replace standart paste keybinds with Caps4
Shift+Ins ★action smartPaste
Ctrl+V ★action smartPaste

♦️ paste selected
Alt+Shift+' ★ console.log(«@»);
Alt+Ctrl+Shift+Down ★ «@:L» ★desc make lower-cased
Alt+Ctrl+Shift+Up ★ «@:U» ★desc make upper-cased

♦️ paste from clipboard
Alt+Shift+' ★ console.log(«@»); ★from clipboard
Ctrl+Shift+V ★ («@:T»)• ★from clipboard ★desc paste trimmed

♦️ utilities
Ins ★action clipboardHistory ★show main,internal
Ctrl+F24 ★action keyboardLayoutRecode ★desc Recode Keyboard Layout
Ctrl+Alt+S ★pattern-REGEX ((?'t'\S+)\s+)?(?'var'\S+)\s*=\s*(?'val'[^;]+)(?'end';?) ★ ${val} = ${var}${end} ★desc Swap Assignments

♦️ keybinds for specific app
Alt+F24 ★action currentApp ★desc copy current app name to clipboard

★for Code, devenv
Ctrl+Alt+P ★ private•

★for-NOT devenv
Ctrl+Alt+P ★ 12345
```