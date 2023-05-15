---
layout: post
title: StackOverflow的404错误页
date: 2010/6/25/ 0:35:41
updated: 2010/6/25/ 0:35:41
status: publish
published: true
type: post
---

不知道大家有没有注意到StakeOverflow的[404错误页面](http://stackoverflow.com/404)？其显示了下面的这个图片：


![](http://sstatic.net/stackoverflow/img/polyglot-404.png)


这个是一个很有意思的图片，不知道你看懂了吗？看上去像Python，又像 Ruby，还像 Perl，当然也有 C的影子，还有[Brainfuck](https://coolshell.cn/articles/1142.html)。是的，这是一个杂交程序，杂交了Python，Ruby，Perl，C，还有Brainfuck（注意其中的#号），所有的语句都是输出“404”字符串。


关于这种杂交程序，本站以前也发布过《[C语言和sh脚本的杂交代码](https://coolshell.cn/articles/1824.html)》，大家可以前往一看。这样的有趣的玩法叫“[Polyglot](http://en.wikipedia.org/wiki/Polyglot_%28computing%29)”，也就是说，把N种语言写在一个文件中，然后，该文件在任何编译器下都可以运行，上述的那段代码在Python，Ruby，Perl，Brainfuck下都可以正常运行，也可以被C和的编译器编译通过，并被运行。


下面是这个图片的字符码，以供各位试试。




```
# define v putchar
#   define print(x) main(){v(4+v(v(52)-4));return 0;}/*
#>+++++++4+[>++++++<-]>++++.----.++++.*/
print(202*2);exit();
#define/*>.@*/exit()
```

欢迎你留下你的看法。


（全文完）




**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![编程语言汽车](https://coolshell.cn/wp-content/uploads/2009/11/oscar-meyer-wienermobile-150x150.jpg)](https://coolshell.cn/articles/1839.html)[编程语言汽车](https://coolshell.cn/articles/1839.html)
* [![到处都是Unix的胎记](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/24.jpg)](https://coolshell.cn/articles/1532.html)[到处都是Unix的胎记](https://coolshell.cn/articles/1532.html)
* [![程序员练级攻略（2018)  与我的专栏](https://coolshell.cn/wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![数据即代码：元驱动编程](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/24.jpg)](https://coolshell.cn/articles/10337.html)[数据即代码：元驱动编程](https://coolshell.cn/articles/10337.html)
* [![类型的本质和函数式实现](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/5.jpg)](https://coolshell.cn/articles/10169.html)[类型的本质和函数式实现](https://coolshell.cn/articles/10169.html)
* [![代码执行的效率](https://coolshell.cn/wp-content/uploads/2012/07/muxnt-150x150.jpg)](https://coolshell.cn/articles/7886.html)[代码执行的效率](https://coolshell.cn/articles/7886.html)
The post [StackOverflow的404错误页](https://coolshell.cn/articles/2529.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).