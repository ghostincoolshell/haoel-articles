---
layout: post
title: 在Javascript里写Python
date: 2010/7/21/ 0:17:39
updated: 2010/7/21/ 0:17:39
status: publish
published: true
type: post
---

以前，本站介绍过去一种[写HTML和CSS的新方法](https://coolshell.cn/articles/2406.html)，以[一种杂交式的代码](https://coolshell.cn/articles/2529.html)，昨天给大家介绍了[.NET代码和Python及Ruby代码的互相转换工具](https://coolshell.cn/articles/2672.html)，但是这个世界可能比我们想像的还疯狂。[IronPython](http://ironpython.net/) 是一个在.NET平台上运行Python的东西，就像那些在[JVM上运行其它语言的东东](https://coolshell.cn/articles/2631.html)一样。当然，IronPython最邪恶的事情并不是在.NET上运行Python，而是在Javascript里写Python的语法。这个畸形混血儿的网址在[这里](http://ironpython.net/browser/)（请注意翻墙）。


使用这个玩意很简单，下面，让我们看看这个混血儿长啥样？


首先，你需要链接一个js文件：



```

<script src="http://gestalt.ironpython.net/dlr-latest.js" type="text/javascript"></script>
```

然后，让我们看看如何写一个按钮事件：



```

<input id="button" type="button" value="Say, Hello!" />
<script type="text/python">
  def button_onclick(s, e):
      window.Alert("Hello from Python!")
  document.button.events.onclick += button_onclick
</script>

```

你对此事怎么看？欢迎留下你的看法。



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![程序员练级攻略（2018)  与我的专栏](../wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![函数式编程](../wp-content/uploads/2013/12/yoda-lambda-150x150.png)](https://coolshell.cn/articles/10822.html)[函数式编程](https://coolshell.cn/articles/10822.html)
* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/5.jpg](https://coolshell.cn/articles/10169.html)[类型的本质和函数式实现](https://coolshell.cn/articles/10169.html)
* [![Chrome开发者工具的小技巧](../wp-content/uploads/2017/01/pretty-code-150x150.gif)](https://coolshell.cn/articles/17634.html)[Chrome开发者工具的小技巧](https://coolshell.cn/articles/17634.html)
* [![如何读懂并写出装逼的函数式代码](../wp-content/uploads/2016/10/drawing-recursive-150x150.jpg)](https://coolshell.cn/articles/17524.html)[如何读懂并写出装逼的函数式代码](https://coolshell.cn/articles/17524.html)
* [![Python修饰器的函数式编程](../wp-content/uploads/2014/03/snake-hat-new-year-schedule-800x960-150x150.jpg)](https://coolshell.cn/articles/11265.html)[Python修饰器的函数式编程](https://coolshell.cn/articles/11265.html)
The post [在Javascript里写Python](https://coolshell.cn/articles/2688.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).