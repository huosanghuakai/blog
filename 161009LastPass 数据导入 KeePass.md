#LastPass 数据导入 KeePass

（虽然相对来说 KeePass 更安全，但 LastPass 的自动填表和默认云同步显然更为便利，还是那句，安全和便利自行权衡）。

同时使用两者的情况下，在某些不方便使用 LastPass 的场景单独建立一个 LastPass 的 KeePass 数据库，即方便使用，又可以在其他场景保持两者独立，还能兼做 LastPass 备份。

LastPass （Chrome） 导出位置在 更多选项-高级-导出-“LastPass CSV 文件”，导出数据是一个 html 页面，需要将其复制至记事本，另存为 *.csv（注意编码选择 UTF-8，否则中文部分会变成乱码）。然后 KeePass 新建数据库，导入格式选择 LastPass CSV 即可。