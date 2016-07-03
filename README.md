#Sublime-configuration

在Sublime Console中输入`sublime.log_commands(True)` 可以显示按键的参数及命令（用来写快捷键有用）

配置了NodeJS的运行环境和Python的运行环境

- 在配置Python的时候，因为Python的输出是采用cp936编码格式，所以我们要配置一下Build文件：

```json
{
    "cmd": ["python", "-u", "$file"],
    "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
    "selector": "source.python",
    "env": {"LANG": "utf-8"},
    "encoding":"cp936",
}
```

- 在配置NodeJS的时候，运行下一个程序会占用一个端口去监听，没有及时的去销毁，用这样的Build可以解决问题：

```json
{
  "shell_cmd": "taskkill /F /IM node.exe & node \"$file\"",
  "selector": "source.js",
}
```

# 包列表

```json
{
	"bootstrapped": true,
	"in_process_packages":
	[
	],
	"installed_packages":
	[
		"Alignment",
		"BracketHighlighter",
		"Clickable URLs",
		"Clipboard Manager",
		"ConvertToUTF8",
		"CSScomb",
		"Emmet",
		"FileHeader",
		"Git",
		"Gitignore",
		"HTML-CSS-JS Prettify",
		"HTML5",
		"jQuery",
		"JsFormat",
		"JSLint",
		"LiveReload",
		"Markdown Preview",
		"MarkdownEditing",
		"Material Theme - White Panels",
		"Package Control",
		"SideBarEnhancements",
		"SublimeCodeIntel",
		"SublimeLinter",
		"SublimeREPL",
		"SyncedSidebarBg",
		"Theme - Soda",
		"Themr",
		"TrailingSpaces"
	]
}

```
