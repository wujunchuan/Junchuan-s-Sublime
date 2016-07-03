# sublime-config
我的Sublime配置

##小笔记
在Sublime Console中输入`sublime.log_commands(True)` 可以显示按键的参数及命令（用来写快捷键有用）

因为Python输出的结果是采用cp936编码格式的，所以我们需要修改 `Python.sublime-build` 的配置，为了不麻烦，我新建了一个 `ChinesePython.sublime-build` 文件来存放配置文件
```json
{
    "cmd": ["python", "-u", "$file"],
    "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
    "selector": "source.python",
    "env": {"LANG": "utf-8"},
    "encoding":"cp936",
}
```

##包列表
```json
{
	"in_process_packages":
	[
	],
	"installed_packages":
	[
		"Alignment",
		"AutoFileName",
		"Clipboard Manager",
		"ConvertToUTF8",
		"CSS Format",
		"Emmet",
		"FileHeader",
		"Git",
		"HTML5",
		"HTMLBeautify",
		"JavaScript Completions",
		"jQuery",
		"JsFormat",
		"JSLint",
		"LiveStyle",
		"Markdown Preview",
		"MarkdownEditing",
		"MySQL Snippets",
		"Package Control",
		"SideBarEnhancements",
		"SublimeCodeIntel",
		"SublimeREPL",
		"Theme - Soda",
		"Themr"
	]
}

```
