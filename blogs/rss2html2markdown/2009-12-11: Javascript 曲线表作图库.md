---
layout: post
title: Javascript 曲线表作图库
date: 2009/12/11/ 5:44:45
updated: 2009/12/11/ 5:44:45
status: publish
published: true
type: post
---

[dygraphs](http://www.danvk.org/dygraphs/) 是一个开源的Javascript库，它可以产生一个可交互式的，可缩放的的曲线表。其可以用来显示大密度的数据集（比如股票，气温，等等），并且可以让用户来浏览和解释这个曲线图。在它的主页（<http://www.danvk.org/dygraphs/>），你可以看到一些示例和用法。


[![dygraphs Javascript 曲线图库](https://coolshell.cn/wp-content/uploads/2009/12/dygraphs.jpg "dygraphs Javascript 曲线图库")](https://coolshell.cn/wp-content/uploads/2009/12/dygraphs.jpg)


要使用这个库，很简单，只需要包括`[dygraph-combined.js](http://github.com/danvk/dygraphs/downloads/)`文件，其文件尺寸很经济，也就45K。



```
<script type="text/javascript"
  src="dygraph-combined.js"></script>
```

下面两个示例，你可以把数据写在javascript中，也可以设置一个csv文件。



**示例一，你可以在代码中指定数据**



```

<div id="graphdiv"></div>
<script type="text/javascript">
  g = new Dygraph(

    // containing div
    document.getElementById("graphdiv"),

    // CSV or path to a CSV file.
    "Date,Temperature\n" +
    "2008-05-07,75\n" +
    "2008-05-08,70\n" +
    "2008-05-09,80\n"

  );
</script>

```

**示例二、你可以引入外部的CSV文件**。(`[temperatures.csv](https://coolshell.cn/wp-admin/temperatures.csv))`



```
<div id="graphdiv2"
  style="width:500px; height:300px;"></div>
<script type="text/javascript">
  g2 = new Dygraph(
    document.getElementById("graphdiv2"),
    "temperatures.csv", // path to CSV file
    {}          // options
  );
</script>
```



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![程序员练级攻略（2018)  与我的专栏](https://coolshell.cn/wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![Chrome开发者工具的小技巧](https://coolshell.cn/wp-content/uploads/2017/01/pretty-code-150x150.gif)](https://coolshell.cn/articles/17634.html)[Chrome开发者工具的小技巧](https://coolshell.cn/articles/17634.html)
* [![如何读懂并写出装逼的函数式代码](https://coolshell.cn/wp-content/uploads/2016/10/drawing-recursive-150x150.jpg)](https://coolshell.cn/articles/17524.html)[如何读懂并写出装逼的函数式代码](https://coolshell.cn/articles/17524.html)
* [![函数式编程](https://coolshell.cn/wp-content/uploads/2013/12/yoda-lambda-150x150.png)](https://coolshell.cn/articles/10822.html)[函数式编程](https://coolshell.cn/articles/10822.html)
* [![Lua简明教程](https://coolshell.cn/wp-content/uploads/2013/12/lua-150x150.gif)](https://coolshell.cn/articles/10739.html)[Lua简明教程](https://coolshell.cn/articles/10739.html)
* [![数据即代码：元驱动编程](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/24.jpg)](https://coolshell.cn/articles/10337.html)[数据即代码：元驱动编程](https://coolshell.cn/articles/10337.html)
The post [Javascript 曲线表作图库](https://coolshell.cn/articles/1924.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).