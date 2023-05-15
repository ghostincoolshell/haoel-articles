---
layout: post
title: Error handling in Egypt
date: 2011/2/9/ 0:45:3
updated: 2011/2/9/ 0:45:3
status: publish
published: true
type: post
---

以前发布过《[C语言的错误处理](https://coolshell.cn/articles/551.html)》一文，不过今天想说的是Egypt的“错误处理”。埃及的事闹得挺大的，国外和中文twitter上更是炸了锅。不要以为程序员就只会写程序——看看程序员举出来的标语吧。呵呵。


[![](https://coolshell.cn/wp-content/uploads/2011/02/Error-handling-in-Egypt.jpg "Error handling in Egypt")](https://coolshell.cn/wp-content/uploads/2011/02/Error-handling-in-Egypt.jpg)Error handling in Egypt
当然，作为程序员来说，这段代码显然还需要重构：  





```
try{
    elections(free,fare);
} catch(DemocracyNotFoundException){
    System.err.println("Time for Mubarak to leave");
}
```

也有的程序员说，System.err.println不是处理错误的最好方法，正确的方法应该是：



```
try {
    elections(free,fair);
} catch (DemocracyNotFoundException e) {
    throw new MubarakDepartureParty(e);
}
```

最后，我们希望Egypt不要出现：



```
...
finally {
    Security.shootProtesters();
}
```



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![聊聊团队协同和协同工具](https://coolshell.cn/wp-content/uploads/2022/10/communication-150x150.png)](https://coolshell.cn/articles/22298.html)[聊聊团队协同和协同工具](https://coolshell.cn/articles/22298.html)
* [![“一把梭：REST API 全用 POST”](https://coolshell.cn/wp-content/uploads/2022/02/http_method-150x150.png)](https://coolshell.cn/articles/22173.html)[“一把梭：REST API 全用 POST”](https://coolshell.cn/articles/22173.html)
* [![谈谈公司对员工的监控](https://coolshell.cn/wp-content/uploads/2022/02/monitoring-150x150.jpeg)](https://coolshell.cn/articles/22157.html)[谈谈公司对员工的监控](https://coolshell.cn/articles/22157.html)
* [![如何做一个有质量的技术分享](https://coolshell.cn/wp-content/uploads/2021/07/knowledge_sharing-300x169-1-150x150.jpeg)](https://coolshell.cn/articles/21589.html)[如何做一个有质量的技术分享](https://coolshell.cn/articles/21589.html)
* [![程序员如何把控自己的职业](https://coolshell.cn/wp-content/uploads/2020/08/programmer.01-e1596792460687-150x150.png)](https://coolshell.cn/articles/20977.html)[程序员如何把控自己的职业](https://coolshell.cn/articles/20977.html)
* [![MegaEase的远程工作文化](https://coolshell.cn/wp-content/uploads/2020/01/remote-150x150.jpg)](https://coolshell.cn/articles/20765.html)[MegaEase的远程工作文化](https://coolshell.cn/articles/20765.html)
The post [Error handling in Egypt](https://coolshell.cn/articles/3630.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).