---
layout: post
title: [推荐]基于Mac的Port工具Fink
date: 2009/10/19/ 11:6:41
updated: 2009/10/19/ 11:6:41
status: publish
published: true
type: post
---

看到标题，读者朋友们肯定第一时间想到的MacPort 。


恩，那是一款非常棒的工具。 不过我更愿意推荐各位使用另外一款工具 Fink(http://www.finkproject.org/).



> Fink 项目希望把 Unix 上各种[开放源码](http://www.opensource.org/)软件带到 [Darwin](http://www.opensource.apple.com/) 和 [Mac OS X](http://www.apple.com/macosx/) 平台上。 我们通过修改 Unix 软件使得它可以在 Mac OS X 上编译和运行（“移植”）,并提供一个方便的分发系统使得每个人都可以下载和使用它。 Fink 使用 [Debian](http://www.debian.org/) 中的象 dpkg 和 apt-get 等工具来提供强大的二进制软件包管理。 你可以随意选择是下载预编译好的二进制安装包或从源代码自己构建一切。
> 
> 


关于 Fink的安装 ，大部分用户可参见http://www.finkproject.org/download/index.php?phpLang=zh。  

不过后面我主要想介绍我的安装方式，因为我的Mac 版本是10.6 64bit.所以还是有些差别。也许上述普通方法有效，但是我并未尝试。


安装步骤如下（感谢 <http://sage.ucsc.edu/~wgscott/xtal/wiki/index.php/64-bit_Fink_for_10.6>）




```

cvs -d:pserver:anonymous@fink.cvs.sourceforge.net:/cvsroot/fink login
 #just hit return when prompted for password
cvs -z3 -d:pserver:anonymous@fink.cvs.sourceforge.net:/cvsroot/fink co -P fink
cd fink
./bootstrap /sw

```

以上最后一步可能会花80%的时间，因为它会执行下载及编译这些很核心的工作。


完成之后编辑 /sw/etc/fink.conf 第4行为：


**Trees: local/main stable/main stable/crypto unstable/main unstable/crypto**


接下来就可以使用fink了。 fink的启动 我加了如下代码



```
source /sw/bin/init.sh
fink selfupdate-cvs
fink -y update-all
fink scanpackages

```

我建议 再执行一条


`echo "source /sw/bin/init.sh" >> ~/.bash_profile`


这样新开终端进程的时候 就不用重新初始化fint了,完成以上步骤，就能使用fink了。


我之所以抛弃了macport 是因为他目前出现的和新版10.6的冲突问题，导致系统gcc库环境出现错误，而macport又与系统架构上不兼容 ，导致Port不能用 gcc 也不能用，而我又准备拿光盘重装developer环境的时候，光驱坏了 DVD盘一律不能读 :shame goodness…!  

fink的出现完全让我避开了以上问题，或许上述问题的出现有我个人原因。 但是fink有很重要的一点，就是它的源很快。他会自动推荐最适合我们的镜像。如果我们要随时更换fink的配置， 可以执行 fink configure.


我相信读到这里，会有不少习惯Port的朋友使用 Fink， Just do it, Fink和MacPort 同时存在并不是什么坏事，虽然我已经把MacPort彻底删了。



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/2.jpg](https://coolshell.cn/articles/2719.html)[苹果开发工具Xcode 4 第二预览版](https://coolshell.cn/articles/2719.html)
* [![操作系统航空公司](../wp-content/uploads/2009/08/linux_airline-150x150.jpg)](https://coolshell.cn/articles/1272.html)[操作系统航空公司](https://coolshell.cn/articles/1272.html)
* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/1.jpg](https://coolshell.cn/articles/559.html)[菜鸟学PHP之Smarty入门](https://coolshell.cn/articles/559.html)
* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/10.jpg](https://coolshell.cn/articles/3433.html)[6个有用的MySQL语句](https://coolshell.cn/articles/3433.html)
* [![一个人脸识别的Javascript](../wp-content/uploads/2010/11/jpDEK-150x150.jpg)](https://coolshell.cn/articles/3254.html)[一个人脸识别的Javascript](https://coolshell.cn/articles/3254.html)
* [https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/15.jpg](https://coolshell.cn/articles/4261.html)[JavaMail使用](https://coolshell.cn/articles/4261.html)
The post [[推荐]基于Mac的Port工具Fink](https://coolshell.cn/articles/1592.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).