---
layout: post
title: Erlang和Python互通
date: 2009/8/24/ 14:30:49
updated: 2009/8/24/ 14:30:49
status: publish
published: true
type: post
---

最近开发 Erlang ,对其字符串处理能力无言至极,于是决定把它和python联合起来,打造一个强力的分布式系统,等将来需要系统级开发时,我再把 C++/C组合进来.


首先参考了 Erlang 官方文档和 [http://blog.developers.api.sina.com.cn/?tag=**erlang**](http://www.zend2.com/DoIt.php?u=Oi8vd3d3LmJsb2dnZXIuY29tL2Jsb2cuZGV2ZWxvcGVycy5hcGkuc2luYS5jb20uY24vP3RhZz1lcmxhbmc%3D&b=5) 以及 [http://kazmier.net/computer/port-howto/](http://www.zend2.com/DoIt.php?u=Oi8va2F6bWllci5uZXQvY29tcHV0ZXIvcG9ydC1ob3d0by8%3D&b=5) .


研读了将近24个小时, 才终于完全把问题解决.  起名为town，town在英文里表示集市，也就是代表各种语言在这里的交流与互动。) )  

  

[erl]-module(town).  

-behaviour(gen\_server).


%% API  

-export([start/0,combine/1]).


%% gen\_server callbacks  

-export([init/1, handle\_call/3, handle\_cast/2, handle\_info/2,  

terminate/2, code\_change/3]).  

-record(state, {port}).


start() -&gt;  

 gen\_server:start\_link({global, ?MODULE}, ?MODULE, [], []).  

stop() -&gt;  

 gen\_server:cast(?SERVER, stop).  

init([]) -&gt;  

 process\_flag(trap\_exit, true),  

 Port = open\_port({spawn, "python -u /home/freefis/Desktop/town.py"},[stream,{line, 1024}]),  

 {ok, #state{port = Port}}.


handle\_call({combine,String}, \_From, #state{port = Port} = State) -&gt;  

 port\_command(Port,String),  

 receive  

 {Port,{data,{\_Flag,Data}}} -&gt;  

 io:format("receiving:~p~n",[Data]),  

 sleep(2000),  

 {reply, Data, Port}  

 end.  

handle\_cast(stop, State) -&gt;  

 {stop, normal, State};  

handle\_cast(\_Msg, State) -&gt;  

 {noreply, State}.


handle\_info(Info, State) -&gt;  

 {noreply,State}.


terminate(\_Reason, Port) -&gt;  

 ok.


code\_change(\_OldVsn, State, \_Extra) -&gt;  

 {ok, State}.


%%——————————————————————–  

%%% Internal ———————————————————  

combine(\_String) -&gt;  

 start(),  

 String = list\_to\_binary("combine|"++\_String++"\n"),  

 gen\_server:call(?SERVER,{combine,String},infinity),  

 stop().[/erl]  

这段是Python的脚本 当erlang中town:combine(“sentence1+sentence2”)执行时，会在后台启动python的脚本，处理完毕后返回给Erlang结果:sentence1sentence2，然后退出。 



```

import sys
def handle(_string):
    if _string.startswith("combine|"):
        string = "".join( _string[8:].split(","))
        return string

"""waiting for input """
while 1:
    # Recv. Binary Stream as Standard IN
    _stream = sys.stdin.readline()

if not _stream: break
    # Scheme, Turn into  Formal String
    inString  = _stream.strip("\r\n")
    # handle String
    outString = handle(inString)
    # send to port as Standart OUT
    sys.stdout.write("%s\n" % (outString,))
    sys.exit(0)
```



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![编程语言汽车](https://coolshell.cn/wp-content/uploads/2009/11/oscar-meyer-wienermobile-150x150.jpg)](https://coolshell.cn/articles/1839.html)[编程语言汽车](https://coolshell.cn/articles/1839.html)
* [![程序员练级攻略（2018)  与我的专栏](https://coolshell.cn/wp-content/uploads/2018/05/300x262-150x150.jpg)](https://coolshell.cn/articles/18360.html)[程序员练级攻略（2018) 与我的专栏](https://coolshell.cn/articles/18360.html)
* [![Python修饰器的函数式编程](https://coolshell.cn/wp-content/uploads/2014/03/snake-hat-new-year-schedule-800x960-150x150.jpg)](https://coolshell.cn/articles/11265.html)[Python修饰器的函数式编程](https://coolshell.cn/articles/11265.html)
* [![函数式编程](https://coolshell.cn/wp-content/uploads/2013/12/yoda-lambda-150x150.png)](https://coolshell.cn/articles/10822.html)[函数式编程](https://coolshell.cn/articles/10822.html)
* [![类型的本质和函数式实现](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/5.jpg)](https://coolshell.cn/articles/10169.html)[类型的本质和函数式实现](https://coolshell.cn/articles/10169.html)
* [![代码执行的效率](https://coolshell.cn/wp-content/uploads/2012/07/muxnt-150x150.jpg)](https://coolshell.cn/articles/7886.html)[代码执行的效率](https://coolshell.cn/articles/7886.html)
The post [Erlang和Python互通](https://coolshell.cn/articles/1313.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).