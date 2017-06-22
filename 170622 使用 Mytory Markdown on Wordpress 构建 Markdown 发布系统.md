# 使用 Mytory Markdown on Wordpress 构建 Markdown 发布系统

之前考虑重选 blog 系统，Jekyll on Github 方案某些方面堪称完美，但基于各方面的考虑，最终还是选择了 Mytory Markdown on WordPress 方案，记录如下

## Jekyll on Github 

依托 Github 及其原生支持的静态 blog 系统，在静态 blog 各种优点的基础上还有 Github 的强势 buff ，但同时也不可避免的继承静态 blog 和 Github 带来的短板，主要特点：

- **文件管理简单** 只需处理 markdown 文件，相关的修改更新较为方便


- **没有数据库带来的性能瓶颈**



- **但也没有数据库带来的内容管理系统** 这里说的内容管理系统包括文章的分类、标签、状态等内容，这点对于普通用户来还是很重要的，例如 WordPress ，因为有数据库的存在可以通过各类转换工具方便的转换和提取


- **需要服务器搭建特殊环境** Jekyll 可以托管在 Github，这个比较特殊，一方面省去了服务器端的要求，比较省心；另一方面，这种公共的内容提供商面对的河蟹手段措施都够呛，比较闹心


- **渲染需要时间，文件越多处理时间越长** 站点通过渲染 markdown 文件生成，文章越多展示前的渲染时间越多（据说，未实际体验）


- **站点功能有限，扩展困难**


## Mytory Markdown on WordPress

依托 Wordpress 成熟的程序生态，当然主要还是 Mytory Markdown 的强悍功能，MW 方案几乎可以实现 JG 方案的亮点功能，除了某些环节要麻烦一点

### 功能实现

-   MW 方案首先需要将 markdown 文件推送至 github（这步工作两者差不多）
-   获得文件在 github 中 raw 的链接地址（这步略麻烦）
-   在 WordPress 中新建 blog，设置分类、标签等需要的参数（这步比较麻烦）
-   填入 文件链接地址，发布
-   如果仅止于此，那么 Mytory Markdown 只不过是又一款中规中矩的 Markdown 插件而已，但实际上……修改 markdown 文件推送后，刷新你的 blog 页面，没错，Wordpress 中的内容自动更新了

### 方案缺点

-   **发文略繁琐** 缺点主要就是发布新日志中新建 blog 比较繁琐的步骤了
-   **不够省心** 动态 blog 系统虽然各方面都友好得多，但需要服务器支持和一定维护，无法像 JG 方案那么省心

### 方案优点

-   **便于写作** 原生 markdown 支持，静态 blog 的最大亮点
-   **便于编辑** 修改 markdown 文件推送，blog 内容即可同步更新
-   **便于管理** Wordpress 内容管理系统完备，且可随时向其他 blog 系统转换
-   **便于扩展** Wordpress 插件生态成熟，方便 blog 扩展功能
-   **便于控制版本** github 副产品，静态 blog 的亮点之二

## Workflowy to Typroa

上面介绍的都是展示端，而输出端个人采用的方案同样是两大神器的组合：

 ——Workflowy，梳理思路、整理结构化信息的笔记神器

 ——Typroa，简约、强大、养眼的单窗口 markdown 编辑神器

 而最赞的，Workflowy export - OPML - Typora import，一篇原生 markdown blog 出炉

## 趟坑相关

当前方案实现较为理想，但也非一蹴而就，中间历经：

- Octopress、Hexo、Hugo 各类静态 blog 系统（缺点前文已述） 


- WordPress 内部也考虑过 markdown 类编辑器实现的 WP-Markdown、PrettyPress（缺点显而易见） 


- WordPress 外部考虑过邮件远程发文、python 程序 Markpress（发文实现相对完美，但无法编辑修改，放弃……）、python 程序 PyPoster（功能描述不错，但是安装之后报错无法使用，放弃……） 

记录于此，供有相关需求同学参考