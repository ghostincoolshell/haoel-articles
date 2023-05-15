---
layout: post
title: Python处理encoding的小技巧
date: 2010/2/8/ 14:6:0
updated: 2010/2/8/ 14:6:0
status: publish
published: true
type: post
---

用Python写过处理文本经常会遇到需要decoding或者encoding, 尤其是处理中文的时候。


encoding的问题处理起来是个脏活儿，报错不太容易看懂，网上相关资料不太好查。有同感？请继续读下去。


常规做法是读取文件的时候立刻decode, 所有的处理工作都用unicode，写会文件的时候encode. 但是等到读取的时候在处理的代码读/写起来都很别扭，感觉像穿上鞋以后袜子滑下来了…Python 3.1.1以上的版本解决了该问题。在Python 3.1.1中，打开文件可以加入encoding的参数：



```
file = open(filename, encoding='xxx')
```

啊，这样看起来终于舒坦了。 不同写如下的code了



```
file = open(filename)
for line in file:
    decoded\_line = line.decode('xxx')
    do something else
提倡使用utf8
```



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![程序员练级攻略（2018)  与我的专栏](https://coolshell.cn/wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![Python修饰器的函数式编程](https://coolshell.cn/wp-content/uploads/2014/03/snake-hat-new-year-schedule-800x960-150x150.jpg)](https://coolshell.cn/articles/11265.html)[Python修饰器的函数式编程](https://coolshell.cn/articles/11265.html)
* [![函数式编程](https://coolshell.cn/wp-content/uploads/2013/12/yoda-lambda-150x150.png)](https://coolshell.cn/articles/10822.html)[函数式编程](https://coolshell.cn/articles/10822.html)
* [![类型的本质和函数式实现](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/5.jpg)](https://coolshell.cn/articles/10169.html)[类型的本质和函数式实现](https://coolshell.cn/articles/10169.html)
* [![代码执行的效率](https://coolshell.cn/wp-content/uploads/2012/07/muxnt-150x150.jpg)](https://coolshell.cn/articles/7886.html)[代码执行的效率](https://coolshell.cn/articles/7886.html)
* [![Quora使用到的技术](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/29.jpg)](https://coolshell.cn/articles/4939.html)[Quora使用到的技术](https://coolshell.cn/articles/4939.html)
The post [Python处理encoding的小技巧](https://coolshell.cn/articles/2109.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).