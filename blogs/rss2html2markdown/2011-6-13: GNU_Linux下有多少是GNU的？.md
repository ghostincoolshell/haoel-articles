---
layout: post
title: GNU/Linux下有多少是GNU的？
date: 2011/6/13/ 0:25:42
updated: 2011/6/13/ 0:25:42
status: publish
published: true
type: post
---

一个葡萄牙的学生写了一篇文章 《[How much GNU is there in GNU/Linux?](http://pedrocr.net/text/how-much-gnu-in-gnu-linux)》 – GNU/Linux下有多少是GNU的。他的这篇文章主要分布了今年4月份的Ubuntu Natty的Linux分发包。其主要是用代码行来做的分析，其给了两个饼图。


第一个饼图如下，其指明了各种主流的开源项目组的分布情况。可见GNU只占了8%，当然，GNome也是GNU的，加起来也只有13%，只占整个分发包很少的比重。


http://pedrocr.net/images/GNUTotalSplit.png


第二个图，作者把GNU的部分拿了出来，再进行了分析：



在下面这个图中，我们可以看到主要是四大块——gcc, gdb, binutils 和 glibc，所以，作者说，这些东西都不是最终用户需要的，不是每一个用户都是需要搞开发的。所以，如果去除这些，再去除Gnome（这个桌面UI也不是很力），那么GNU的东西几乎没有了。


http://pedrocr.net/images/GNUSplit.png


所以，作者以此来挑战Richard Stallman提到的 GNU/Linux的这个说法。好像更为好的说法应该叫——


**GNU/KDE/java/xorg/Linux**


我对这篇文章有下述一些感觉：


* 以代码行来衡量重要性，非常的不准确。比尔盖茨说过——“用代码行数来衡量编程的进度，就如同用航空器零件的重量来衡量航空飞机的制造进度一样”（参看《[最佳编程语录](https://coolshell.cn/articles/2753.html "最佳编程语录")》），所以，用这个数据来并不一定正确。如果用Linux的各种包的依赖性可能会更好一点。
* 至少我知道，离开了glibc，可能整个操作系统都会不举。Linux下，绝大多数软件都是gcc/gdb编程和调试出来的（当然，LLVM和Clang正在挑战着gcc编译器），而且大多数软件都在用着GPL的许可证（[虽然开源世界的许可证是如此的混乱](https://coolshell.cn/articles/4657.html "狗日的开源软件许可证")）
* 辩证地，我们不能否定GNU的历史价值，同时我们似乎也在看到GNU好像有点萎靡。


老实说，其实叫什么不重要，是GNU/Linux也好，是Ubuntu 也好，还是Android也好，无所谓。Linux的各种分发包中都存在着全世界黑客文化的和开源文化的结晶，每当我看到这样的分布图时（例如：[是谁写的Linux?](https://coolshell.cn/articles/1360.html "谁写了Linux")），我心中都有一种说不出来的豪情，这难道不真是一种壮举吗？（[Unix黑客文化的真正延伸](https://coolshell.cn/articles/2322.html "Unix传奇(上篇)")）。


不管这种方式的软件有没有市场，能不能得到“最终用户”的认可，但这已成为了软件开发的一种精神——那种不分彼此，相互协作的精神，不是吗？


（全文完）



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/24.jpg](https://coolshell.cn/articles/1097.html)[Ksplice Uptrack — Ubuntu更新不用重启](https://coolshell.cn/articles/1097.html)
* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/30.jpg](https://coolshell.cn/articles/501.html)[Ubuntu的并行启动](https://coolshell.cn/articles/501.html)
* [![eBPF 介绍](../wp-content/uploads/2022/12/eBPF-150x150.jpeg)](https://coolshell.cn/articles/22320.html)[eBPF 介绍](https://coolshell.cn/articles/22320.html)
* [![打造高效的工作环境 – Shell 篇](../wp-content/uploads/2019/03/linux.ninja_-150x150.png)](https://coolshell.cn/articles/19219.html)[打造高效的工作环境 – Shell 篇](https://coolshell.cn/articles/19219.html)
* [![记一次Kubernetes/Docker网络排障](../wp-content/uploads/2018/12/docker-networking-1-150x150.png)](https://coolshell.cn/articles/18654.html)[记一次Kubernetes/Docker网络排障](https://coolshell.cn/articles/18654.html)
* [![程序员练级攻略（2018)  与我的专栏](../wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
The post [GNU/Linux下有多少是GNU的？](https://coolshell.cn/articles/4826.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).