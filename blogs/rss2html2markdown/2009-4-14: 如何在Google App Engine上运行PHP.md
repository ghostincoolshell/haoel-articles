---
layout: post
title: 如何在Google App Engine上运行PHP
date: 2009/4/14/ 15:0:30
updated: 2009/4/14/ 15:0:30
status: publish
published: true
type: post
---

Google 在一年前发布了[Google App Engine](http://code.google.com/appengine/) (GAE) 。这是一个免费的 App Engine 主机，可以让你的每个Application（免费的最多有10个）有1GB的磁盘空间和43.6个CPU小时与10GB的上传和10GB的下载带宽，以及2000个电子邮件。如果你需要地更多，那就是付钱了。


GAE 最近发布了正式[支持Java](http://googleappengine.blogspot.com/2009/04/seriously-this-time-new-language-on-app.html)的通知。于是，互联网上开始有了各种各样的BLOG评论文章，还有一些人居然在Google App Engine 中运行PHP程序，这个太不可思议了。因为GAE目前并不支持PHP。


其实，他们使用了一个叫做 [Quercus](http://www.caucho.com/resin-3.0/quercus/)的东东， Quercus 本质上是一个 100% 的用Java 实现的一个 PHP 引擎 (需要 JDK 1.5)，所以，只要你把Quercus集成到你的GAE中，你自然也可以运行PHP脚本了。



下面是大体步骤：


1) 注删一个 [免费的帐号](http://appengine.google.com/)。  

2) 下载[这个文件](http://www.webdigi.co.uk/fun/php-appengine/phpwithjava.zip) 到你本机。  

3) 在 war\WEB-INF\appengine-web.xml 编辑应用的XML tag，把其名字改成你所注册的名字。  

4) 最后，[上传你的应用](http://code.google.com/appengine/docs/java/gettingstarted/uploading.html)。


更多细节请参看：


* [http://phpwithjava.appspot.com/webdigi.php](http://phpwithjava.appspot.com/webdigi.phphttp://phpwithjava.appspot.com/info.php)
* <http://phpwithjava.appspot.com/info.php>




**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![一些文章和各种资源](https://coolshell.cn/wp-content/uploads/2011/09/image008-150x150.jpg)](https://coolshell.cn/articles/5224.html)[一些文章和各种资源](https://coolshell.cn/articles/5224.html)
* [![我看ChatGPT: 为啥谷歌掉了千亿美金](https://coolshell.cn/wp-content/uploads/2023/02/chatgpt-150x150.jpg)](https://coolshell.cn/articles/22398.html)[我看ChatGPT: 为啥谷歌掉了千亿美金](https://coolshell.cn/articles/22398.html)
* [![Google Inbox如何跨平台重用代码？](https://coolshell.cn/wp-content/uploads/2014/11/inbox2-640x264-150x150.jpg)](https://coolshell.cn/articles/12136.html)[Google Inbox如何跨平台重用代码？](https://coolshell.cn/articles/12136.html)
* [![PFIF网上寻人协议](https://coolshell.cn/wp-content/uploads/2013/04/Google-Person-Finder-150x150.png)](https://coolshell.cn/articles/9508.html)[PFIF网上寻人协议](https://coolshell.cn/articles/9508.html)
* [![代码执行的效率](https://coolshell.cn/wp-content/uploads/2012/07/muxnt-150x150.jpg)](https://coolshell.cn/articles/7886.html)[代码执行的效率](https://coolshell.cn/articles/7886.html)
* [![来信， 创业 和 移动互联网](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/2.jpg)](https://coolshell.cn/articles/5815.html)[来信， 创业 和 移动互联网](https://coolshell.cn/articles/5815.html)
The post [如何在Google App Engine上运行PHP](https://coolshell.cn/articles/531.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).