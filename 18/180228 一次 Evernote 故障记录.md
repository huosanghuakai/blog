# 一次 Evernote 故障记录

**环境** Evernote 5.8.13  Windows 7

## 故障

开机自动弹出重建索引提示，笔记同步后角标不消失（看上去仍未同步，实际上已经同步成功），无法清空废纸篓。

按住 Ctrl 点击「帮助」后，使用「修复全部笔记」和「重建全文搜索索引」等命令无效，在 Web 端清空废纸篓无效。

点击「活动日志」会发现日志不停的弹

```
Finished reindexing, 1 items still in queue
Reindexing 1 items
Failed to remove item 18481 from reindex queue, error: LINK_ATTR_NOT_FOUND
```

## 解决

清除原数据库（将 Databases 文件夹改名最简单稳妥），重新同步全部笔记。（同步时间还好，4000 条笔记近 1G 大小的数据库用时 13 分钟）