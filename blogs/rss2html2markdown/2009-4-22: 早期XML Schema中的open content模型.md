---
layout: post
title: 早期XML Schema中的open content模型
date: 2009/4/22/ 5:4:41
updated: 2009/4/22/ 5:4:41
status: publish
published: true
type: post
---

**摘要**：在看SDO的一些规范文档，可能会出现open content这样的词组，上网查了相关资料，发现这是一种XML Schema的模型，本文就描述了XML Schema的Open Content模型的含义，在最新的XML Schema规范中，好像已经没有Open模型，它的等价物是any模型。


早期发布的XML Schema规范中支持一种新的element定义，在这个定义中，你可以将XML的Element的内容定义为开放的。下面我们将会介绍一下XML的Open Content 模型。


在Open Content模型中，如果一个XML的元素在XML Schema中被声明为开放的，那么这个Schema对应的XML文档的实例就可以包含一个没有在Schema中罗列的子元素。例如，一个包含着如下的XML Schema的Schema文件




```

      <element name=&quot;Book&quot;>
           <type>
               <element name=&quot;Title&quot; type=&quot;string&quot;/>
               <element name=&quot;Author&quot; type=&quot;string&quot;/>
               <element name=&quot;Date&quot; type=&quot;string&quot;/>
               <element name=&quot;ISBN&quot; type=&quot;string&quot;/>
               <element name=&quot;Publisher&quot; type=&quot;string&quot;/>
           </type>
      </element>
```

这个book element的声明意味着这个Schema的实例XML文件必须包含5个元素 – Title,Author，Date，ISBN，Pbulish。例如：



```

     <Book>
         <Title>Illusions The Adventures of a Reluctant Messiah</Title>
         <Author>Richard Bach</Author>
         <Date>1977</Date>
         <ISBN>0-440-34319-4</ISBN>
         <Publisher>Dell Publishing Co.</Publisher>
     </Book>


```

假设，在实例XML文件，你希望增加book的另外一个子元素，比如，你希望增加一个到某一个网页的连接：



```

     <Book>
         <Title>Illusions The Adventures of a Reluctant Messiah</Title>
         <Author>Richard Bach</Author>
         <Date>1977</Date>
         <ISBN>0-440-34319-4</ISBN>
         <Publisher>Dell Publishing Co.</Publisher>
         <AuthorsWebPage xlink:href=&quot;<a href=&quot;http://www.rbach.com&quot;/&quot;>http://www.rbach.com&quot;/</a>>
    </Book>


```

对于上面这个XML文件，XML Schema分析器将会认为这个XML文件是无效的XML，因为上面的文件的包含了Scheme中没有定义的元素。但是在我们的应用场景中，我们可能会希望XML Schema分析器不要报错，因为，应用程序自己知道如何处理<AuthorsWebPage>这个元素。为了达到这个目的，我们就可以将Book声明为开放的。



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![PFIF网上寻人协议](https://coolshell.cn/wp-content/uploads/2013/04/Google-Person-Finder-150x150.png)](https://coolshell.cn/articles/9508.html)[PFIF网上寻人协议](https://coolshell.cn/articles/9508.html)
* [![语言的数据亲和力](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/3.jpg)](https://coolshell.cn/articles/4905.html)[语言的数据亲和力](https://coolshell.cn/articles/4905.html)
* [![Web开发人员速查卡](https://coolshell.cn/wp-content/uploads/2011/02/1128-150x150.jpg)](https://coolshell.cn/articles/3684.html)[Web开发人员速查卡](https://coolshell.cn/articles/3684.html)
* [![那些炒作过度的技术和概念](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/2.jpg)](https://coolshell.cn/articles/3609.html)[那些炒作过度的技术和概念](https://coolshell.cn/articles/3609.html)
* [![SOAP的S是Simple](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/6.jpg)](https://coolshell.cn/articles/3585.html)[SOAP的S是Simple](https://coolshell.cn/articles/3585.html)
* [![信XML，得自信](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/9.jpg)](https://coolshell.cn/articles/3498.html)[信XML，得自信](https://coolshell.cn/articles/3498.html)
The post [早期XML Schema中的open content模型](https://coolshell.cn/articles/604.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).