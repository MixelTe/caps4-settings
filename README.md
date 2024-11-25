# Caps4 settings

Syntax highlighting for Caps4 settings file

## Syntax

```caps4
♦️ this is a comment
♦️ • - space in start or end of pasted text
♦️ ¶ - line break in pasted text
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