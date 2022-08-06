#[AHK] Typora-Evernote 自动复制粘贴脚本

#说明
很简陋的代码，只是把热键串了下，操作方便一些。中间想添加 Typora 无空白文档自动新建一个的功能发现 ```#IfWinNotExist``` 无法精确匹配，还是那句，抛砖引玉

#代码

```
#IfWinActive, Typora
{
	!q::
	send ^a
	send ^c
#IfWinActive, Typora
{
	;在 Typora 窗口 alt+q 会将当前内容全选复制至 Evernote 笔记内
	!q::
	send ^a
	send ^c
	WinActivate, 印象笔记
	Sleep, 200
	; send ^m
	; Sleep, 200
	send ^a
	send ^v
	Return
}

#IfWinActive ahk_class (ENSingleNoteView|ENMainFrame)
{
	;在 Evernote 笔记窗口  alt+q 会将当前内容全选复制至 Untitled - Typora 窗口
	!q::
	send ^a
	send ^c
	#IfWinExist, Untitled - Typora
		{
		WinActivate, Untitled - Typora
		send ^a
		send ^v
		} 
	return
}
```
