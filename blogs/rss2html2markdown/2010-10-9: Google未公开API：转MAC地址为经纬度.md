---
layout: post
title: Google未公开API：转MAC地址为经纬度
date: 2010/10/9/ 7:28:13
updated: 2010/10/9/ 7:28:13
status: publish
published: true
type: post
---

这里有一个POC（Proof of Concept）可以通过你Web浏览器后面的路由器XSS攻击得到一个准确的GPS坐标。注意：路由器和Web浏览器以及IP地址并不包含任和地理信息。其方法是使用了一个Google未公开的API。大约方法如下：


1. 访问一个网页，这个网页隐藏了一个基于你WiFi路由器的XSS（ 参见： [XSS  Verizon FiOS router](http://samy.pl/vzwfios/)）
2. 通过这个XSS 可以获得路由器的MAC 地址。
3. 然后通过 Google Location Services我们可以把这个MAC地址映射到GPS坐标。Googel的这个服务是基于HTTP的服务。这并不是一个Google正式发布的API，而是通过 [Firefox’s Location-Aware Browsing](http://www.mozilla.com/en-US/firefox/geolocation/) 发现的。


演示地点在这里：<http://samy.pl/mapxss/>


我试了一下，无论无线和有线都可以准确定位我的位置。很强大，你也试试看。



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![我看ChatGPT: 为啥谷歌掉了千亿美金](../wp-content/uploads/2023/02/chatgpt-150x150.jpg)](https://coolshell.cn/articles/22398.html)[我看ChatGPT: 为啥谷歌掉了千亿美金](https://coolshell.cn/articles/22398.html)
* [![API设计原则 – Qt官网的设计实践总结](../wp-content/uploads/2017/07/api-design-300x278-2-150x150.jpg)](https://coolshell.cn/articles/18024.html)[API设计原则 – Qt官网的设计实践总结](https://coolshell.cn/articles/18024.html)
* [![Google Inbox如何跨平台重用代码？](../wp-content/uploads/2014/11/inbox2-640x264-150x150.jpg)](https://coolshell.cn/articles/12136.html)[Google Inbox如何跨平台重用代码？](https://coolshell.cn/articles/12136.html)
* [![PFIF网上寻人协议](../wp-content/uploads/2013/04/Google-Person-Finder-150x150.png)](https://coolshell.cn/articles/9508.html)[PFIF网上寻人协议](https://coolshell.cn/articles/9508.html)
* [![程序员疫苗：代码注入](../wp-content/uploads/2012/12/200906020837401710-150x150.jpg)](https://coolshell.cn/articles/8711.html)[程序员疫苗：代码注入](https://coolshell.cn/articles/8711.html)
* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/2.jpg](https://coolshell.cn/articles/5815.html)[来信， 创业 和 移动互联网](https://coolshell.cn/articles/5815.html)
The post [Google未公开API：转MAC地址为经纬度](https://coolshell.cn/articles/3089.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).