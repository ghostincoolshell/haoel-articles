---
layout: post
title: WTF Javascript
date: 2010/6/2/ 1:51:49
updated: 2010/6/2/ 1:51:49
status: publish
published: true
type: post
---

请先看一下下面的这段Javascript程序以及其结果。


[javascript]  

1 + + 1              // => 2  

1 + – + 1            // => 0  

1 + – + – + 1        // => 2  

1 + – + – + – + 1    // => 0  

1 + – + + + – + 1    // => 2  

1 + / + + + / + 1    // => 1/ + + + /1  

[/javascript]


提示一下，1++1等价于1 + (+1)，也就是1加上一个正数1，如果你能搞懂其它的表达式的话，请看看下面的这段程序，你能说出其结果吗？


[javascript]  

1 + / + / + / + 1 // => ?  

[/javascript]


如果不知道的话，你可以到这个[网页上去讨论讨论](http://mir.aculo.us/2010/05/28/valid-javascript-or-not/)。当然，如果你不懂也没有什么关系，因为Javascript本身就是一个很怪异的语言，再加上浏览器的种种不是，所以，[Javascript程序员也是很郁闷的](https://coolshell.cn/articles/1850.html)。在以前的“[最为奇怪的程序语言的特性](https://coolshell.cn/articles/2053.html)”中也说过一些。Javascript最怪异的特性导致了[wtfjs.com](http://wtfjs.com/)这样的一个网站，还有一个[WTF JS的开源站点](http://github.com/brianleroux/wtfjs)。呵呵。



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![程序员练级攻略（2018)  与我的专栏](https://coolshell.cn/wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![Chrome开发者工具的小技巧](https://coolshell.cn/wp-content/uploads/2017/01/pretty-code-150x150.gif)](https://coolshell.cn/articles/17634.html)[Chrome开发者工具的小技巧](https://coolshell.cn/articles/17634.html)
* [![如何读懂并写出装逼的函数式代码](https://coolshell.cn/wp-content/uploads/2016/10/drawing-recursive-150x150.jpg)](https://coolshell.cn/articles/17524.html)[如何读懂并写出装逼的函数式代码](https://coolshell.cn/articles/17524.html)
* [![函数式编程](https://coolshell.cn/wp-content/uploads/2013/12/yoda-lambda-150x150.png)](https://coolshell.cn/articles/10822.html)[函数式编程](https://coolshell.cn/articles/10822.html)
* [![Lua简明教程](https://coolshell.cn/wp-content/uploads/2013/12/lua-150x150.gif)](https://coolshell.cn/articles/10739.html)[Lua简明教程](https://coolshell.cn/articles/10739.html)
* [![数据即代码：元驱动编程](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/24.jpg)](https://coolshell.cn/articles/10337.html)[数据即代码：元驱动编程](https://coolshell.cn/articles/10337.html)
The post [WTF Javascript](https://coolshell.cn/articles/2492.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).