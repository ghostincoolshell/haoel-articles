---
layout: post
title: Javascripts加密库
date: 2009/8/10/ 10:16:29
updated: 2009/8/10/ 10:16:29
status: publish
published: true
type: post
---

一般说来，使用HTTP协议是不加密的，所有的数据都是以纯文本方式提交的，就算是你提交数据时，也是使用纯文本的方式发送。只有HTTPS协议会有SSL加密数据，但一般来说，HTTPS需要服务器端进行SSL设置，并有些麻烦。而jCryption这个jQuery插件能够加密由Forms提交的POST/GET数据。jCryption使用RSA公钥密码算法加密，另外，该项目还提供一个PHP文件来处理数据的解密。


[![](http://www.webresourcesdepot.com/wp-content/uploads/image/javascript-encyrption.jpg "JCryption")](http://www.jcryption.org/)



这个库是一个开源库，也是一个同时使用MIT和GPL协议的项目。


你需要注意的是，这个库无法取代SSL，使用这个库，你依然可能受到[MITM攻击](http://en.wikipedia.org/wiki/Man-in-the-middle_attack)（中间人攻击 Man-in-the-middle-attacks）


主页：<http://www.jcryption.org/>  

下载：<http://code.google.com/p/jcryption/downloads/list>  

示例：<http://www.jcryption.org/demo/>



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![深入浅出单实例Singleton设计模式](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/29.jpg)](https://coolshell.cn/articles/265.html)[深入浅出单实例Singleton设计模式](https://coolshell.cn/articles/265.html)
* [![我做系统架构的一些原则](https://coolshell.cn/wp-content/uploads/2021/12/bachelor-mechanical-eng-icon@72x-150x150.png)](https://coolshell.cn/articles/21672.html)[我做系统架构的一些原则](https://coolshell.cn/articles/21672.html)
* [![Unix考古记：一个“遗失”的shell](https://coolshell.cn/wp-content/uploads/2013/04/figure1-150x150.gif)](https://coolshell.cn/articles/9410.html)[Unix考古记：一个“遗失”的shell](https://coolshell.cn/articles/9410.html)
* [![如何学好C语言](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/25.jpg)](https://coolshell.cn/articles/4102.html)[如何学好C语言](https://coolshell.cn/articles/4102.html)
* [![ C++11 中值得关注的几大变化（详解）](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/27.jpg)](https://coolshell.cn/articles/5265.html) [C++11 中值得关注的几大变化（详解）](https://coolshell.cn/articles/5265.html)
* [![2009年脚本语言排名](https://coolshell.cn/wp-content/uploads/2009/04/overall-150x150.jpg)](https://coolshell.cn/articles/325.html)[2009年脚本语言排名](https://coolshell.cn/articles/325.html)
The post [Javascripts加密库](https://coolshell.cn/articles/1231.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).