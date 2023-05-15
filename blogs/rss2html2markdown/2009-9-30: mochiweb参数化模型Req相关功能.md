---
layout: post
title: mochiweb参数化模型Req相关功能
date: 2009/9/30/ 12:0:34
updated: 2009/9/30/ 12:0:34
status: publish
published: true
type: post
---

本文的笔记讲述如何从client请求中获取各种参数,如method, request path, headers, cookie等。


Mochiweb是Erlang实现的一个开源Web服务器，它设计的一个亮点就是他本身的Http请求的参数化模型。因此我们可以用OO的方式来理解它的相关用法。  

它的实现在mochiweb\_request模块.在mochiweb中,每个client请求其构造一个 Req 对象(注：这个“对象“只是便于理解的提法), Req 可以理解成 mochiweb\_request 的一个参数化或实例化.  




1.**Req:get(method)**-> ‘OPTIONS’ | ‘GET’ | ‘HEAD’ | ‘POST’ | ‘PUT’ | ‘DELETE’ | ‘TRACE’.  

获取Http请求的方式.


2.**Req:get(raw\_path)** -> String().  

获取raw\_path.比如 http://www.nextim.cn/session/login?username=test#p,那/session/login?username=test#p就是这个raw\_path.


3.**Req:get(path)**-> String().  

获取path.比如 http://www.nextim.cn/session/login?username=test#p,那/session/login就是这个raw\_path.


4.**Req:parse\_qs()** -> [{strng(), string()}].  

获取get参数.比如 http://www.nextim.cn/session/login?username=test#p,则返回[{“username”,”test”}].


5.**Req:parse\_post()** -> [{strng(), string()}].  

确保post数据类型为: application/x-www-form-urlencoded, 否则不要调用(其内部会调用Req:recv\_body),返回值类似Req:parse\_qs().


6.**Req:get(peer)**-> string().  

返回值为client的ip


7.**Req:get\_header\_value(Key)** -> undefined | string().  

获取某个header,比如Key为”User-Agent”时，返回”Mozila…….”


8.**Req:get\_primary\_header\_value(Key)** -> undefined | string().  

获取http headers中某个key对应的主值(value以分号分割).  

举例: 假设 Content-Type 为 application/x-www-form-urlencoded; charset=utf8,则  

Req:get\_header\_value(“content-type”) 返回 application/x-www-form-urlencoded


9.**Req:get(headers)** -> dict().  

获取所有headers  

说明: 返回结果为stdlib/dict 数据结构,可以通过mochiweb\_headers模块进行操作.  

举例: 下面代码显示请求中所有headers:  

Headers = Req:get(headers),  

lists:foreach(fun(Key, Value) ->  

io:format(“~p : ~p ~n”, [Key, Value])  

end,  

mochiweb\_headers:to\_list(Headers)).


10.**Req:parse\_cookie()** -> [{string(), string()}].  

解析Cookie


11.**R****eq:get\_cookie\_value(Key)**-> string().  

类似Req:get\_header\_value(Key)


最近搜了下，发现用mochiweb的挺多的。但自己用的时候发现来不少疑难。以上文档皆由litaocheng总结提供。感谢所带来的帮助。希望这个对国内使用mochiweb的朋友们带来帮助。


**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![erlang打包独立环境](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/28.jpg)](https://coolshell.cn/articles/2111.html)[erlang打包独立环境](https://coolshell.cn/articles/2111.html)
* [![编程语言汽车](https://coolshell.cn/wp-content/uploads/2009/11/oscar-meyer-wienermobile-150x150.jpg)](https://coolshell.cn/articles/1839.html)[编程语言汽车](https://coolshell.cn/articles/1839.html)
* [![Erlang和Python互通](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/2.jpg)](https://coolshell.cn/articles/1313.html)[Erlang和Python互通](https://coolshell.cn/articles/1313.html)
* [![一张关于操作系统的图](https://coolshell.cn/wp-content/uploads/2009/10/operating-systems-150x150.jpg)](https://coolshell.cn/articles/1579.html)[一张关于操作系统的图](https://coolshell.cn/articles/1579.html)
* [![sed 简明教程](https://coolshell.cn/wp-content/uploads/2013/02/sed-superman-150x150.png)](https://coolshell.cn/articles/9104.html)[sed 简明教程](https://coolshell.cn/articles/9104.html)
* [![消费者的消费观](https://coolshell.cn/wp-content/uploads/2010/09/1-150x150.png)](https://coolshell.cn/articles/2913.html)[消费者的消费观](https://coolshell.cn/articles/2913.html)
The post [mochiweb参数化模型Req相关功能](https://coolshell.cn/articles/1516.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).