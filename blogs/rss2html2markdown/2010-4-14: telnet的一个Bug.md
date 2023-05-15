---
layout: post
title: telnet的一个Bug
date: 2010/4/14/ 1:10:20
updated: 2010/4/14/ 1:10:20
status: publish
published: true
type: post
---

下面这个链接是Linux分发包Ubuntu的关于Telnet命令的Man Page，


<http://manpages.ubuntu.com/manpages/karmic/man1/telnet-ssl.1.html>


打开这个Man Page，把页面拉到最后一行，你会看到下面这个BUG（“BUGS：源代码不易读！”）



```
     The source code is not comprehensible.
```

Telnet的源代码在这里：<http://packages.ubuntu.com/source/dapper/netkit-telnet>，下载下来一看，还真是不易读，简单地看了一下代码，发现至少有这样一些问题：


* 空格和Tab键混用的缩进，导致很多代码在没有缩进。
* 大量的#if #else以及大量的各种预编译宏。以及一些怪异的宏。如：


#ifndef B19200  

#define B19200 B9600  

#endif


#ifndef B38400  

#define B38400 B19200  

#endif


* 什么叫在C中写C++，第一次见。（在terminal.cc中间居然出现了几个class）
* 变量命名很不直观，大量的old, tmp, c1, c2, s1, s2, s3 等学校里用的变量名，只有作者自己知道是什么意思。函数命令的风格也不一致，编程风格也很不一致，基本没有编程规范。


的确很不易读。不管怎么样，很欣赏在man page中把源码的易读性列为BUG的这种作法。



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![GNU/Linux下有多少是GNU的？](https://coolshell.cn/wp-content/uploads/2011/06/GNUTotalSplit-150x150.png)](https://coolshell.cn/articles/4826.html)[GNU/Linux下有多少是GNU的？](https://coolshell.cn/articles/4826.html)
* [![装完Ubuntu 9.10后要干的事](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/10.jpg)](https://coolshell.cn/articles/1644.html)[装完Ubuntu 9.10后要干的事](https://coolshell.cn/articles/1644.html)
* [![Ksplice Uptrack — Ubuntu更新不用重启](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/24.jpg)](https://coolshell.cn/articles/1097.html)[Ksplice Uptrack — Ubuntu更新不用重启](https://coolshell.cn/articles/1097.html)
* [![Ubuntu的并行启动](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/30.jpg)](https://coolshell.cn/articles/501.html)[Ubuntu的并行启动](https://coolshell.cn/articles/501.html)
* [![Java书籍Top 10](https://coolshell.cn/wp-content/uploads/2009/03/zcover-150x150.jpg)](https://coolshell.cn/articles/14.html)[Java书籍Top 10](https://coolshell.cn/articles/14.html)
* [![你确信你了解时间吗？](https://coolshell.cn/wp-content/uploads/2011/07/Time-changes-in-year-1927-for-China-–-ShanghaiS-150x150.png)](https://coolshell.cn/articles/5075.html)[你确信你了解时间吗？](https://coolshell.cn/articles/5075.html)
The post [telnet的一个Bug](https://coolshell.cn/articles/2352.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).