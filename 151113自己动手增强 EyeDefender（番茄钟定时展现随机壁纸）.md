#自己动手增强 EyeDefender（番茄钟定时展现随机壁纸）

EyeDefender 是一款很赞的、美观的、可以默默的提示番茄工作法的、保护视力预防近视……的 windows 软件，但美中不足的是它只能固定展示一张图片，对此折腾控显然无法满意，继续祭出批处理神器。

##功能

实现 EyeDefender 定时展现指定文件夹内随机壁纸（对于没有用过 EyeDefender 的同学来说，可以理解为每隔28分钟你的屏幕上会随机显示一张指定文件夹内的图片，持续2分钟，这两分钟你可以退出壁纸继续努力工作，喝水散步伸懒腰扰乱工作秩序，以及盯着壁纸看满时间……）

##代码

**vbs 文件**（静默调用 bat 文件）
```
set ws=wscript.createobject("wscript.shell")
ws.run "helloworld.bat /start",0
```
（如果你和我一样同为代码盲）请将代码中 helloworld 改为你接下来的 bat 文件名称，例如 seeyouwork，并将其复制到记事本中保存退出，将该文本文件改名为 abc.vbs，并建立快捷方式，拖入系统 startup 文件夹。

**bat 文件** （功能实现）
```
@echo off 
:main
setlocal enabledelayedexpansion 
for %%a in (d:\pic\*.jpg) do set/a "n+=1" & set "jpg!n!=%%a" 
set/a "a=%random%%%!n!+1" 
copy /y "!jpg%a%!" "d:\pic\eyedefender\0.jpg" 
ping -n 1800 127.1>nul
goto main
```
（如果你和我一样同为代码盲）记得将代码中的 ```d:\pic\``` 修改为自己的图片文件夹目录，将 ```d:\pic\eyedefender\0.jpg``` 修改为自己的展示图片位置，并在 EyeDefender 中指定。```1800``` 为设定更换图片时间，例如番茄钟设定为 28-2 30分钟的话1800秒刚好。

##其他

说到随机壁纸，个人觉得现在 Chrome 上最赞的是 FlickrTab，看到养眼的风景收下来扔到图片文件夹，改造过的 EyeDefender 没准就会在某个眼痛手酸的时候给你一剂心灵鸡汤了。