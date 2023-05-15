---
layout: post
title: Unix Pipes 管道原稿
date: 2009/8/24/ 16:17:11
updated: 2009/8/24/ 16:17:11
status: publish
published: true
type: post
---

![Douglas McIlroy](https://coolshell.cn/wp-content/uploads/2009/08/Douglas-McIlroy.jpg "Douglas McIlroy")


40年前，Unix操作系统横空出世，Unix不仅仅带来了一个操作系统，还创造C语言，Socket，开源，黑客等等文化，这些文化影响着整个计算机世界的文明，直到今天。


如果说Unix是计算机文明中最伟大的发明，那么，Unix下的Pipe管道就是跟随Unix所带来的另一个伟大的发明。管道的出现，解决的就是让不同功能的程序可以互相连通通讯，从而可以让软件开发，程序开发更加的“高内聚，低耦合”，从而可以让程序“Do one thing, Do it well”，从而可以让程序“Keep it Simple Stupid”等等，这一哲学引影了一代又一代的软件架构，直到今天的云计算。


管道的发名者叫，[**Malcolm Douglas McIlroy**](http://en.wikipedia.org/wiki/Douglas_McIlroy)，他也是Unix的创建者，是Unix文化的缔造者之一。他归纳的Unix哲学如下：



> 程序应该只关注一个目标，并尽可能把它做好。让程序能够互相协同工作。应该让程序处理文本数据流，因为这是一个通用的接口。
> 
> 



下面是管道在1964年10月11日，出现的第一个打印稿，下面是扫描件。



![Unix Pipes](https://coolshell.cn/wp-content/uploads/2009/08/pipe.png "Unix Pipes")


全文如下：



```
                        - 10 -
            Summary--what's most important.
    To put my strongest concerns into a nutshell:
1. We should have some ways of connecting programs like
garden hose--screw in another segment when it becomes when
it becomes necessary to massage data in another way.
This is the way of IO also.
2. Our loader should be able to do link-loading and
controlled establishment.
3. Our library filing scheme should allow for rather
general indexing, responsibility, generations, data path
switching.
4. It should be possible to get private system components
(all routines are system components) for buggering around with.

                                                M. D. McIlroy
                                                October 11, 1964

```

我就不翻译了，因为这段文字足够的简单，就像连接花园中浇花用的软管一样，相信你不但能够读懂它，还能从中收益。


（全文完）



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![Unix 50 年：Ken Thompson 的密码](https://coolshell.cn/wp-content/uploads/2019/11/ken.dennis-300x186-1-150x150.jpeg)](https://coolshell.cn/articles/19996.html)[Unix 50 年：Ken Thompson 的密码](https://coolshell.cn/articles/19996.html)
* [![程序员练级攻略（2018)  与我的专栏](https://coolshell.cn/wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![Linux PID 1 和 Systemd](https://coolshell.cn/wp-content/uploads/2017/07/systemd-1-150x150.jpeg)](https://coolshell.cn/articles/17998.html)[Linux PID 1 和 Systemd](https://coolshell.cn/articles/17998.html)
* [![vfork 挂掉的一个问题](https://coolshell.cn/wp-content/uploads/2014/11/tux-fork-150x150.gif)](https://coolshell.cn/articles/12103.html)[vfork 挂掉的一个问题](https://coolshell.cn/articles/12103.html)
* [![谜题的答案和活动的心得体会](https://coolshell.cn/wp-content/uploads/2014/08/puzzle-150x150.png)](https://coolshell.cn/articles/11847.html)[谜题的答案和活动的心得体会](https://coolshell.cn/articles/11847.html)
* [![Unix考古记：一个“遗失”的shell](https://coolshell.cn/wp-content/uploads/2013/04/figure1-150x150.gif)](https://coolshell.cn/articles/9410.html)[Unix考古记：一个“遗失”的shell](https://coolshell.cn/articles/9410.html)
The post [Unix Pipes 管道原稿](https://coolshell.cn/articles/1351.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).