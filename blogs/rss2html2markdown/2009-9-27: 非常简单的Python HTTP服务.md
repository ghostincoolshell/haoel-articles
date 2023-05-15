---
layout: post
title: 非常简单的Python HTTP服务
date: 2009/9/27/ 3:34:10
updated: 2009/9/27/ 3:34:10
status: publish
published: true
type: post
---

如果你急需一个简单的Web Server，但你又不想去下载并安装那些复杂的HTTP服务程序，比如：Apache，ISS等。那么， [Python](http://www.python.org/) 可能帮助你。使用Python可以完成一个简单的内建 HTTP 服务器。于是，你可以把你的目录和文件都以HTTP的方式展示出来。佻只需要干一件事情，那就是安装一个Python。


实际上来说，这是一个可以用来共享文件的非常有用的方式。实现一个微型的HTTP服务程序来说是很简单的事情，在Python下，只需要一个命令行。下面是这个命令行：（假设我们需要共享我们的目录 /home/haoel 而IP地址是192.168.1.1）



```

$ cd /home/haoel
$ python -m SimpleHTTPServer

```


这就行了，而我们的HTTP服务在8000号端口上侦听。你会得到下面的信息：



```
Serving HTTP on 0.0.0.0 port 8000 ...
```

你可以打开你的浏览器（IE或Firefox），然后输入下面的URL：



```
http://192.168.1.1:8000
```

如果你的目录下有一个叫 index.html 的文件名的文件，那么这个文件就会成为一个默认页，如果没有这个文件，那么，目录列表就会显示出来。


如果你想改变端口号，你可以使用如下的命令：



```

$ python -m SimpleHTTPServer 8080

```

如果你只想让这个HTTP服务器服务于本地环境，那么，你需要定制一下你的Python的程序，下面是一个示例：


[py]  

import sys  

import BaseHTTPServer  

from SimpleHTTPServer import SimpleHTTPRequestHandler  

HandlerClass = SimpleHTTPRequestHandler  

ServerClass  = BaseHTTPServer.HTTPServer  

Protocol     = "HTTP/1.0"


if sys.argv[1:]:  

    port = int(sys.argv[1])  

else:  

    port = 8000  

server\_address = (‘127.0.0.1’, port)


HandlerClass.protocol\_version = Protocol  

httpd = ServerClass(server\_address, HandlerClass)


sa = httpd.socket.getsockname()  

print "Serving HTTP on", sa[0], "port", sa[1], "…"  

httpd.serve\_forever()  

[/py]


注意：所有的这些东西都可以在 Windows 或 [Cygwin](http://www.cygwin.com/) 下工作。



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![“一把梭：REST API 全用 POST”](https://coolshell.cn/wp-content/uploads/2022/02/http_method-150x150.png)](https://coolshell.cn/articles/22173.html)[“一把梭：REST API 全用 POST”](https://coolshell.cn/articles/22173.html)
* [![HTTP的前世今生](https://coolshell.cn/wp-content/uploads/2019/10/HTTP-770x513-300x200-1-150x150.jpg)](https://coolshell.cn/articles/19840.html)[HTTP的前世今生](https://coolshell.cn/articles/19840.html)
* [![程序员练级攻略（2018)  与我的专栏](https://coolshell.cn/wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![如何免费的让网站启用HTTPS](https://coolshell.cn/wp-content/uploads/2017/08/enable-https-banner-150x150.png)](https://coolshell.cn/articles/18094.html)[如何免费的让网站启用HTTPS](https://coolshell.cn/articles/18094.html)
* [![Python修饰器的函数式编程](https://coolshell.cn/wp-content/uploads/2014/03/snake-hat-new-year-schedule-800x960-150x150.jpg)](https://coolshell.cn/articles/11265.html)[Python修饰器的函数式编程](https://coolshell.cn/articles/11265.html)
* [![函数式编程](https://coolshell.cn/wp-content/uploads/2013/12/yoda-lambda-150x150.png)](https://coolshell.cn/articles/10822.html)[函数式编程](https://coolshell.cn/articles/10822.html)
The post [非常简单的Python HTTP服务](https://coolshell.cn/articles/1480.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).