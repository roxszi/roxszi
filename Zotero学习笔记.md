# Zotero学习笔记

含Zotero安装及基本使用入门，以及WebDAV网盘同步的方法

## 1. Zotero安装及使用指导

1. 去Zotero官网下载Zotero并安装。链接：[https://www.zotero.org/download/](https://www.zotero.org/download/)
    
    > Zotero介绍：
    > 
    > Zotero是开源免费的文献管理软件，不需要破解，免去了破解工具带病毒、破解版版本过旧等问题。
    > 
    > 其可以较为方便的一键生成参考文献等信息，且可自定义参考文献格式，以满足各期刊要求；同时，其“一键/自动同步文献笔记”也是我们组常用的重要功能。
    > 
    > 其最大的短板就是免费的共享空间太小了（只有300MB），十多篇大综述就占满了。
    > 
    > 所以Zotero共享空间只用来同步笔记，至于文献原文pdf文件，则建议用本文的[WebDAV同步方法](#_2-个人文献的webdav同步方法)。
    > 
    > 综上所述，团队使用的话，**请务必认真阅读下面的操作设置，**以免300MB的群组免费空间因为你一个人的不小心而被占满，影响所有人都笔记同步。

2. 下载Zotero插件市场。链接：[https://zotero-chinese.com/plugins/#search=插件市场](https://zotero-chinese.com/plugins/#search=插件市场)

    Zotero插件市场的安装方法：打开Zotero后依次点击左上角`工具`-`插件`-`右上角齿轮`-`Install Add-on From File...`，然后选择刚才下载的“Zotero插件市场”文件，安装即可。

3. 进入Zotero插件市场安装一些趁手的插件。依次点击Zotero左上角`工具`-`插件市场`进入。

    建议安装的插件有：

    1. Translate for Zotero。一款文献翻译插件。

    2. Jasminum。中文文献插件。

    3. Ethereal Reference。能为文献的参考文献生成快速索引链接。
    
    4. Sci-PDF。自动从Sci-Hub下载文献。
    
    > 有些插件会有一些可供自定义设置的选项，依次点击Zotero左上角`编辑`-`设置`就能找到。

4. 一些小技巧

    Zotero里的文献，可以尝试点击右侧`网址`栏快捷键。很多文献已可在期刊网站全文阅览，字大，图清晰，且可用浏览器的各类翻译插件一键翻译。没法在线阅读的，再考虑pdf阅读。

    > 浏览器翻译插件建议选用中英双语同显的插件。推荐如下：
    > 
    > 1. 有道灵动翻译：[https://magicfanyi.youdao.com/](https://magicfanyi.youdao.com/)。有道是国内学术圈的老牌翻译软件了，一般不翻墙的话就选有道。当然这个插件好像只能翻译“正文”，有时候不太方便。
    > 
    > 2. 沉浸式翻译：[https://immersivetranslate.com/](https://immersivetranslate.com/)。这个是第三方翻译，自身不带翻译功能，而是可在设置里选择具体的翻译引擎（如微软、谷歌、SiliconCloud、Yandex的翻译服务引擎等）。
    > 
    > 3. 沙拉查词：[https://saladict.crimx.com/](https://saladict.crimx.com/)。划词翻译。

## 2. 个人文献的WebDAV同步方法

> Zotero关于“同步”的设置那里，除群组文献库以外，还有一个`“我的文献”附件同步方式`设置，可选`WebDAV`。
> 
> WebDAV即“Web-based Distributed Authoring and Versioning”，基于网络的分布式创作和版本控制，简而言之就是“网盘”，且必须得是“支持另外一款软件直接对接”的网盘。
> 
> WebDAV网盘意味着你可以用另外一款软件（如Zotero）实现对网盘的操作，而不用再去下载网盘app了，因此国内大多数网盘不支持WebDAV。我查到的一家支持免费WebDAV服务的网盘厂商（其也是国内最早的网盘厂商）——坚果云。
> 
> 通过注册坚果云账号，可以获得免费1GB的WebDAV存储空间。

以“坚果云”为例，实现WebDAV的方法如下：

1. 注册坚果云账号：[https://www.jianguoyun.com/](https://www.jianguoyun.com/)

2. 进入坚果云网盘，在主界面点击`创建`-`个人同步文件夹`，命名为“Zotero”。

3. 坚果云网盘界面右上角依次点击`账户信息`-`安全选项`-`第三方应用管理`，然后点击`添加应用`，应用名称可以为“zotero”，然后即可得到WebDAV服务的`服务器地址`、`账户`、`密码`。

4. 在zotero的“文献同步”界面，`“我的文献”附件同步方式`选择`WebDAV`，然后输入上一步获得的`服务器地址`、`账户`、`密码`，即可实现1GB空间的WebDAV同步。

> 坚果云设置Zotero的WebDAV服务的官方操作指导：[https://help.jianguoyun.com/?p=3168](https://help.jianguoyun.com/?p=3168)
