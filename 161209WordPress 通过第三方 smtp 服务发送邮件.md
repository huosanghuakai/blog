#WordPress 通过第三方 smtp 服务发送邮件

最近碰到 500 问题才发现定期数据库备份的邮件断了大半年了，试了网上说的比较多的 phpinfo 和 mail.php 检测方法似乎 mail() 功能正常，再问主机商……果然禁掉了邮件功能……最后选了 **WP-Mail-SMTP** 插件来解决问题，记录如下：

- **SMTP Host**：smtp.gmail.com（通过 Google 的 smtp 服务）


- **SMTP Port**：465（注意 587 测试失败）


- **Encryption**：Use SSL encryption （这里开始以为 ssl 需要服务器支持，实际不需要）


- **Authentication**：Yes: Use SMTP authentication.（不验证选择情况不详……）


- Username、Password：为了安全起见，使用的独立的邮箱

设置完成后，可以通过 Send Test 来检测，设置好后之前无辜背锅的 **WordPress Database Backup** 沉冤昭雪（btw：BackWPup 不好用，界面复杂，定期似乎还要设置 API）