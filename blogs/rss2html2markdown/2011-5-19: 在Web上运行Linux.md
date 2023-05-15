---
layout: post
title: 在Web上运行Linux
date: 2011/5/19/ 0:35:8
updated: 2011/5/19/ 0:35:8
status: publish
published: true
type: post
---

一个叫Fabrice Bellard的程序员写了一段Javascript在Web浏览器中启动Linux（[原网页](http://bellard.org/jslinux/)，我把这个网页iframe在了下面），目前，你只能使用Firefox 4和Chrome 11运行这个Linux。这不是什么假的模仿Linux的东西，这是实实在在的运行一个Linux。这一举动还引起了很多很牛人的关注，包括Javascript的创建者[Brendan Eich](http://twitter.com/#!/BrendanEich/status/70393502328045568)。


清除启动开始启动




随后，Fabrice Bellard发布了相关的技术说明：<http://bellard.org/jslinux/tech.html>，从这份文档中我们可以看到：


* 这个模似器完全由Javascript写成
* CPU仿真器使用的是[QEMU](http://qemu.org/)（接近于原古的486），为了装上Linux，其做了一些改动。
* Javascript的终端本来可以使用[termlib](http://www.masswerk.at/termlib/)，但他还是自己写了一个，因为OS的按键和Web浏览器不一样（[here](http://unixpapa.com/js/key.html)）
* Linux  使用了2.6.20内核，编译配置在[这里](http://bellard.org/jslinux/config_linux-2.6.20)，并做了一些[小改动](http://bellard.org/jslinux/patch_linux-2.6.20)。
* 磁盘用的是Ram Disk，在启动的时候装载。其文件系统由[Buildroot](http://buildroot.uclibc.org/) 和[BusyBox](http://www.busybox.net/)产生。
* 在Home目录下有一个hello.c的程序，你可以使用[TinyCC](http://bellard.org/tcc)编译（tcc，参看酷壳的[这篇文章](https://coolshell.cn/articles/786.html "用TCC可以干些什么？")）


从这个事我有这些感触，


1. 在Web上运行一个Linux的操作系统不是问题。那么在Web上还有什么不能做的吗？
2. Linux真是性能很高，在Javascript下运行感觉也不慢啊。
3. 真是Techno-Geek。


 



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![程序员练级攻略（2018)  与我的专栏](https://coolshell.cn/wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![eBPF 介绍](https://coolshell.cn/wp-content/uploads/2022/12/eBPF-150x150.jpeg)](https://coolshell.cn/articles/22320.html)[eBPF 介绍](https://coolshell.cn/articles/22320.html)
* [![打造高效的工作环境 – Shell 篇](https://coolshell.cn/wp-content/uploads/2019/03/linux.ninja_-150x150.png)](https://coolshell.cn/articles/19219.html)[打造高效的工作环境 – Shell 篇](https://coolshell.cn/articles/19219.html)
* [![记一次Kubernetes/Docker网络排障](https://coolshell.cn/wp-content/uploads/2018/12/docker-networking-1-150x150.png)](https://coolshell.cn/articles/18654.html)[记一次Kubernetes/Docker网络排障](https://coolshell.cn/articles/18654.html)
* [![Linux PID 1 和 Systemd](https://coolshell.cn/wp-content/uploads/2017/07/systemd-1-150x150.jpeg)](https://coolshell.cn/articles/17998.html)[Linux PID 1 和 Systemd](https://coolshell.cn/articles/17998.html)
* [![Chrome开发者工具的小技巧](https://coolshell.cn/wp-content/uploads/2017/01/pretty-code-150x150.gif)](https://coolshell.cn/articles/17634.html)[Chrome开发者工具的小技巧](https://coolshell.cn/articles/17634.html)
The post [在Web上运行Linux](https://coolshell.cn/articles/4722.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).