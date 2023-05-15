---
layout: post
title: McAfee误杀svchost.exe
date: 2010/4/23/ 0:45:21
updated: 2010/4/23/ 0:45:21
status: publish
published: true
type: post
---

这两天，杀毒软件又出事了。还记得2007年5月，那次是Norton把简体中文Windows下的netapi32.dll 和 lsasrv.dll。最近的一次是，2008年11月，AVG把user32.dll给干掉了。


这次是McAfee的5958版病毒库，导致McAfee误杀了Windows XP SP3下的svchost.exe，这最终导致了Windows不断地重复启动，据说有数十万PC成了小白鼠。简单地到Twitter和各国外技术社区看看，真是受灾严重啊。


下面是出错信息：



```
The file C:WINDOWS\system32\svchost.exe contains the W32/Wecorl.a Virus.
Undetermined clean error, OAS denied access and continued.
Detected using Scan engine version 5400.1158 DAT version 5958.0000.
```

其实，可能大家都误解了，McAfee把svchost.exe识别为一个恶意程序，我觉得这是一种“实事求是”的态度啊，svchost.exe难道不是Windows下的万恶之源吗？多少年来，svchost.exe成为了多少病毒，木马和流氓程序的温床，这么多年过去了，Windows用户们默默地承受着svchost.exe所带来的痛苦，经过这么长的时间，只有McAfee不惧M$的淫威第一个站出来把svchost.exe揪出来办了，这是一种什么样的精神啊……



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![图片搜索引擎优化Checklist](../wp-content/uploads/2009/10/seo-cartoon-150x150.jpg)](https://coolshell.cn/articles/1528.html)[图片搜索引擎优化Checklist](https://coolshell.cn/articles/1528.html)
* [![Amazon的书为什么卖到了$2000万](../wp-content/uploads/2011/04/lawrence_1-150x150.png)](https://coolshell.cn/articles/4605.html)[Amazon的书为什么卖到了$2000万](https://coolshell.cn/articles/4605.html)
* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/24.jpg](https://coolshell.cn/articles/2606.html)[五个方法成为更好的程序员](https://coolshell.cn/articles/2606.html)
* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/5.jpg](https://coolshell.cn/articles/2785.html)[JS1K 演示](https://coolshell.cn/articles/2785.html)
* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/19.jpg](https://coolshell.cn/articles/290.html)[雷人的程序注释](https://coolshell.cn/articles/290.html)
* [![在线作图编辑服务](../wp-content/uploads/2010/10/Photo-editor-150x150.jpg)](https://coolshell.cn/articles/3244.html)[在线作图编辑服务](https://coolshell.cn/articles/3244.html)
The post [McAfee误杀svchost.exe](https://coolshell.cn/articles/2376.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).