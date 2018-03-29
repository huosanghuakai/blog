# 以 GTD 模式使用 Workflowy

## 背景

Workflowy 是一款自由度极高的层级式笔记应用，重度用户甚至仅用 Workflowy 构建整个 GTD 或者 PKM 系统，但这种操作实在非常人所能，这里仅讨论以 GTD 模式使用 Workflowy （辅助式的，配合其他软件建立的 GTD 或 PKM 系统）。

以 Workflowy 和 Evernote 的组合为例，前者长于处理高度结构化的信息，如思路整理、操作记录、长文创作、复杂任务的规划，后者则在全平台的剪辑查阅、海量信息的组织管理方面更占优势（参见 [为什么选择 Evernote](https://cloudlet.info/t/366)）。

那么，是否有一种方式能够衔接 Workflowy 和 Evernote，使其各展所长呢？遗憾的是，目前两者虽然能够进行一定的衔接------Workflowy 的节点和 Evernote 的笔记都拥有独立的地址，可以相互链接。Workflowy 的每日内容变更可以自动转发至 Evernote。Workflowy 的导出面板内容可以完美剪辑至 Evernote。包括最近 @locktionc  发布的「同步 Workflowy 大纲到印象笔记」的脚本------但效果都不大理想，Workflowy 的强大在于其灵活的视角和独特的动态版面，搬到 Evernote 会大失神韵，反之 Evernote 强悍的信息组织能力到了 Workflowy 也英雄无用武之地。

在反复衡量增加一个收集篮带来的精力损耗和增加一套强大的复杂任务处理系统带来的系统加成之后，我最终选择了在 Workflowy 中建立一套和 Evernote 类似但相对独立的 GTD 系统（参见[使用 Evernote 建立桌面 GTD 系统](https://cloudlet.info/t/284)）。

## 实现

而一旦决定在 Workflowy 中建立 GTD 系统，曾经在 Evernote 碰到的问题会再次出现------一款无限层级的大纲式笔记应用，绝大多数用户会近乎本能的使用节点来作为内容分类，然后这种内容分类会干扰 GTD 的清单系统。

所以，第一个改变是在 Workflowy 中放弃使用节点来体现内容分类，将每个根节点视作一则独立的笔记/任务（这样的额外好处是不需要再为节点归类和调整层级花费精力了）。

之后的变动就顺理成章了，使用 \# 标签建立清单系统，使用 @ 标签 建立场景系统（在节点标题后放置标签，基于美观的考虑，可以把标签放在 note 位置 ）。

接下来在 Home 页面顶部建立索引面板（Workflowy 的原生功能，标签筛选器，通过 点击相应 标签可以方便的在各个清单/场景中切换）

> \#1actions \| \#2project \| \#3review \| \#5waitting \| \#6someday \| \#7probe \| \#8thinking
>
> @1work \| @2office \| @3home \| ...

和主 GTD 系统不同，基于取长补短的原则，Workflowy 的清单系统不设置收集篮、日程清单（0.stuff、\#4schedule 在 Evernote 里，毕竟材料剪辑、快捷输入和日程提醒都是 Evernote 的主场），增加一个符合 Workflowy 用途的 \#8thinking 清单。 场景系统和 Evernote 一样采用场景和内容分类的混合系统，可酌情设置。

## 扩展

继续使用可能会碰到一个小问题，不在 Home 页面时，虽然 Esc 能激活搜索框，但只能搜索当前节点中的内容。原生功能上，需要首先点击 Logo 或者通过浏览器的「后退」动作回到 Home 页面（因为每个节点都有独立的链接，在 Workflowy 中灵活使用「前进」和「后退」也可以带来极大的便利），再次激活搜索框才能全局搜索。。

WorkFindy for Workflowy 这个原理简单（实际上只是调用了 Workflowy 原生的搜索功能）但效果出色的扩展的出现解决了这种尴尬。

任意浏览器页面（包括 Workflowy 任意节点）：选中文本，热键激活，在 Workflowy 中搜索该字符串。未选中文本，热键激活，弹出搜索面板。输入字符串确认，在 Workflowy 中搜索，不输入字符串确认，打开 Workflowy。

通过该扩展可以实现如下 GTD 功能：在任意页面（包括 Workflowy 内），热键激活：直接回车，打开（或跳转）至 Home 页面；输入 \#1 回车，跳转至 \#1actions 清单。

## 相关

### Moo.do

和 Workflowy 类似而又最有特色的笔记软件应该就是 Moo.do 了。其中最实用的是贴心的多面板功能（面板之间可以无缝拖拽，但是使用 GTD 模式的话，Workflowy 不大需要这种拖拽功能了）和看上去还不错的节点索引功能。日历面板看上去也很赞，但里面的节点不能跳转缩放导致只能起到简单的标示功能，另外个人很不习惯这种非清单筛选而是仅仅添加标签分组（把所有任务堆在一起陡增焦虑）的任务组织形式。当然，Moo.do 最致命的问题是没有 Workflowy 标签的筛选器功能。这个缺陷足以秒杀以其他一切亮点。最后，Moo.do 也许看上去功能丰富，但是界面相对太累赘了，远远不如 Workflowy 的简约而不简单。

### MyLifeOrganized

在同类笔记应用以外，和 Workflowy 也很相似的还有传说中大能的 MyLifeOrganized（MLO）。不过遗憾的是，习惯了原始 GTD 系统的轻便灵活（但又不失强大）之后，个人有些排斥 MLO 这类重型武器。在 MLO 中，似乎任何任务的添加都需要一系列的设置，最后也只是提供一个类似上面说的添加标签分组的任务组织形式，而在 Evernote 中，仅仅通过清单和场景的组合就可以轻松应付绝大多数任务和使用情景，并且这种组合筛选的设置和实现都很方便。而在引入 Workflowy 之后，Evernote 对复杂任务的组织乏力的问题也得到完满的解决，所以...... 

## 小技巧

### 展开/折叠所有节点

之前因故被开发者取消，17年11月在 alpha 版中以按钮形式回归，目前可以通过 [加入 alpha ](https://workflowy.com/features/alpha)开启该功能

### 显示 note 全文

stylus 添加 css 

```css
.notes .content {
    height: auto !important; 
    overflow: visible !important;
    display: block !important; 
}
```

### OPML 的导入

直接在 Workflowy 复制 opml 文件的文本内容即可

### 应用模式

需要一个极简的 Workflowy 界面？Chrome App 并不好用，既受限于 Chrome 应用机制，又不能享受 Chome 强大的扩展加成。而在 chrome 快捷方式的「目标」一栏添加 --app=https://www.workflowy.com，点击即可开启一个独立的不带标签栏地址栏的纯粹 Workflowy 窗口（并且享受对应扩展效果，但不支持热键激活扩展）。这样一个在工作过程中可以实时记录和规划的迷你笔记本就完成了（对界面不满意还可以祭出 Stylus 针对小窗口设置独立样式）。

### 文档的导出

Workflowy 原生支持导出 OPML 格式，之后通过加成了 Pandoc 的 Typroa 可以方便的转换为任意格式的文档。

### 多面板 （伪）

开两个浏览器窗口......


