---
layout: post
title: 我有一个Hello World的C++程序编译不过
date: 2011/4/2/ 6:33:57
updated: 2011/4/2/ 6:33:57
status: publish
published: true
type: post
---

在StackOverflow上有这样[一个贴子](http://stackoverflow.com/questions/5508110/why-is-this-program-erroneously-rejected-by-three-c-compilers)，楼主说，我有下面这样的一个C++程序，为什么编译不通过啊。其让我想起了以前的这两个帖子《[编程真难啊](https://coolshell.cn/articles/1391.html "编程真难啊")》和《[给我一个序列号](https://coolshell.cn/articles/1693.html "给我一个序列号")》。**仅以此篇文章祝大家假期快乐吧**。


![hello world 程序](http://i.stack.imgur.com/JQXWL.png "hello world 程序")hello world 程序
楼主还给出了相关的编译出错的信息（相信你一看就明白问题在哪里了，你应该还会发出一声“靠”！！！）


先是用Visual C++ 2010编译



```
c:\dev>cl /nologo helloworld.png
cl : Command line warning D9024 : unrecognized source file type 'helloworld.png', object file assumed
helloworld.png : fatal error LNK1107: invalid or corrupt file: cannot read at 0x5172
```

再用G++ 4.5.2编译




```
c:\dev>g++ helloworld.png
helloworld.png: file not recognized: File format not recognized
collect2: ld returned 1 exit status
```

再用clang编译



```
c:\dev>clang++ helloworld.png
helloworld.png: file not recognized: File format not recognized
collect2: ld returned 1 exit status
clang++: error: linker (via gcc) command failed with exit code 1 (use -v to see invocation)
```

不过，最强大的，有人居然给出了一个fix，靠！  

（下面的图片是一个4M大的gif动画，演示了整个过程，下载可能需要一定的时间。）


[![hello world 的解决方案](http://i.imgur.com/QlGpd.gif "hello world 的解决方案")](http://i.imgur.com/QlGpd.gif)hello world 的解决方案 （图片有点大4M，请耐心等待下载）
真是BT啊，呵呵。**仅以此篇文章祝大家假期快乐吧**。



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![Rust语言的编程范式](https://coolshell.cn/wp-content/uploads/2020/03/rust-social-wide-150x150.jpg)](https://coolshell.cn/articles/20845.html)[Rust语言的编程范式](https://coolshell.cn/articles/20845.html)
* [![程序员练级攻略（2018)  与我的专栏](https://coolshell.cn/wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![API设计原则 – Qt官网的设计实践总结](https://coolshell.cn/wp-content/uploads/2017/07/api-design-300x278-2-150x150.jpg)](https://coolshell.cn/articles/18024.html)[API设计原则 – Qt官网的设计实践总结](https://coolshell.cn/articles/18024.html)
* [![Leetcode 编程训练](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/29.jpg)](https://coolshell.cn/articles/12052.html)[Leetcode 编程训练](https://coolshell.cn/articles/12052.html)
* [![State Threads 回调终结者](https://coolshell.cn/wp-content/uploads/2014/10/edsm-150x150.gif)](https://coolshell.cn/articles/12012.html)[State Threads 回调终结者](https://coolshell.cn/articles/12012.html)
* [![C语言的整型溢出问题](https://coolshell.cn/wp-content/uploads/2014/04/c99-150x150.jpg)](https://coolshell.cn/articles/11466.html)[C语言的整型溢出问题](https://coolshell.cn/articles/11466.html)
The post [我有一个Hello World的C++程序编译不过](https://coolshell.cn/articles/4170.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).