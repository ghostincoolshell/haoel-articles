---
layout: post
title: 谷歌Chrome取消”http://”
date: 2010/4/22/ 3:12:24
updated: 2010/4/22/ 3:12:24
status: publish
published: true
type: post
---

谷歌下一个版本的Chrome浏览器软件将缺少一个在近20年来一直是浏览器的一个特点的功能：在地址栏中的“http://”。目前开发人员版本的Chrome浏览器已经做了这种改变。这个变化虽然看起来很小，但是，已经在Chrome网站引起了程序员们很大的争议。


[![](https://coolshell.cn/wp-content/uploads/2010/04/URL-BAR.png "Google Chrome 取消 http://")](https://coolshell.cn/wp-content/uploads/2010/04/URL-BAR.png)


在Google Chrome的开发站点上，又有了一个很热的BUG——[Issue  41467](http://code.google.com/p/chromium/issues/detail?id=41467)（上一次的一热议的BUG是的《[Go语言更名Issue 9](https://coolshell.cn/articles/1781.html)》），这个BUG目前已被关闭。不过在其它地方还在热议中，如：[Reddit.com](http://www.reddit.com/r/programming/comments/bt0oh/issue_41467_url_bar_no_longer_shows_http/)。基本上来说，90%以上的程序员反对的，他们希望Google的Chrome可以给一个设置关闭或打开这一功能。


一些程序员觉得这是违反了RFC，并且觉得这是在向End User传播一种很不好的东西，那就是网址可以不用http://，这样一来会给程序员增加很多麻烦，比如：他们的程序无法使用http://这一关键字来检查用户的输出，等等。


iPhone浏览器的也是这样的， 不过当你把光标放到地址栏中，其会显示http://，广大程序员希望Chrome也实现这一方案。然而，[Issue  41467](http://code.google.com/p/chromium/issues/detail?id=41467)目前的状态是“WontFix”，呵呵。


有人说，如果你在地址栏中直接输入网址，没有协议前缀，默认就是http://，Google用的就是这个特性，然后，你可以试试在地址栏中输入“[ftp.gnu.org/gnu](ftp://ftp.gnu.org/gnu)”，你会发现，自动加入的不是http://而是ftp://，呵呵。


有人说，既然你要省，不如也把www.和后面的.com加上/也省了，因为这些都是默认的嘛。直接打google就OK了。Chrome开发团队说，没有www.和.com/只能算是一个主机名，不能算是DNS域名。呵呵。


还有人说，搞这种隐藏的最恶心的就是Windows，隐藏文件后缀名，隐藏系统文件，太扯了，于是，像sexy\_girls.jpg.exe，huge-tits.jpg.src这样玩意儿让某些电脑知识薄弱意志不坚定的人深受其害。


如果有空，请留下你的观点。



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![我看ChatGPT: 为啥谷歌掉了千亿美金](https://coolshell.cn/wp-content/uploads/2023/02/chatgpt-150x150.jpg)](https://coolshell.cn/articles/22398.html)[我看ChatGPT: 为啥谷歌掉了千亿美金](https://coolshell.cn/articles/22398.html)
* [![“一把梭：REST API 全用 POST”](https://coolshell.cn/wp-content/uploads/2022/02/http_method-150x150.png)](https://coolshell.cn/articles/22173.html)[“一把梭：REST API 全用 POST”](https://coolshell.cn/articles/22173.html)
* [![HTTP的前世今生](https://coolshell.cn/wp-content/uploads/2019/10/HTTP-770x513-300x200-1-150x150.jpg)](https://coolshell.cn/articles/19840.html)[HTTP的前世今生](https://coolshell.cn/articles/19840.html)
* [![如何免费的让网站启用HTTPS](https://coolshell.cn/wp-content/uploads/2017/08/enable-https-banner-150x150.png)](https://coolshell.cn/articles/18094.html)[如何免费的让网站启用HTTPS](https://coolshell.cn/articles/18094.html)
* [![Chrome开发者工具的小技巧](https://coolshell.cn/wp-content/uploads/2017/01/pretty-code-150x150.gif)](https://coolshell.cn/articles/17634.html)[Chrome开发者工具的小技巧](https://coolshell.cn/articles/17634.html)
* [![Google Inbox如何跨平台重用代码？](https://coolshell.cn/wp-content/uploads/2014/11/inbox2-640x264-150x150.jpg)](https://coolshell.cn/articles/12136.html)[Google Inbox如何跨平台重用代码？](https://coolshell.cn/articles/12136.html)
The post [谷歌Chrome取消”http://”](https://coolshell.cn/articles/2367.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).