---
layout: post
title: google的免费dns服务器
date: 2009/12/28/ 11:3:34
updated: 2009/12/28/ 11:3:34
status: publish
published: true
type: post
---

google推出了自己的免费dns服务器，以供公众使用。服务器地址是：


dns1: 8.8.8.8


dns2: 8.8.4.4


我在我的机器上测试了一下：



$ host -a g.cn 8.8.8.8
Trying “g.cn”
Using domain server:
Name: 8.8.8.8
Address: 8.8.8.8#53
Aliases:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 33253
;; flags: qr rd ra; QUERY: 1, ANSWER: 11, AUTHORITY: 0, ADDITIONAL: 0
;; QUESTION SECTION:
;g.cn. IN ANY
;; ANSWER SECTION:
g.cn. 300 IN A 72.14.203.160
g.cn. 259200 IN NS ns3.google.com.
g.cn. 10800 IN MX 10 google.com.s9b2.psmtp.com.
g.cn. 259200 IN NS ns1.google.cn.
g.cn. 259200 IN NS ns2.google.com.
g.cn. 86400 IN SOA ns1.google.com. dns-admin.google.com. 1402219 21600 3600 1209600 300
g.cn. 10800 IN MX 10 google.com.s9b1.psmtp.com.
g.cn. 10800 IN MX 10 google.com.s9a2.psmtp.com.
g.cn. 10800 IN MX 10 google.com.s9a1.psmtp.com.
g.cn. 259200 IN NS ns1.google.com.
g.cn. 259200 IN NS ns4.google.com.
Received 325 bytes from **8.8.8.8#53 in 217 ms**




$ host -a g.cn 8.8.4.4
Trying “g.cn”
Using domain server:
Name: 8.8.4.4
Address: 8.8.4.4#53
Aliases:

;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 40871
;; flags: qr rd ra; QUERY: 1, ANSWER: 11, AUTHORITY: 0, ADDITIONAL: 0

;; QUESTION SECTION:
;g.cn. IN ANY

;; ANSWER SECTION:
g.cn. 227 IN A 72.14.203.160
g.cn. 259127 IN NS ns3.google.com.
g.cn. 10727 IN MX 10 google.com.s9b2.psmtp.com.
g.cn. 259127 IN NS ns1.google.cn.
g.cn. 259127 IN NS ns2.google.com.
g.cn. 86327 IN SOA ns1.google.com. dns-admin.google.com. 1402219 21600 3600 1209600 300
g.cn. 10727 IN MX 10 google.com.s9b1.psmtp.com.
g.cn. 10727 IN MX 10 google.com.s9a2.psmtp.com.
g.cn. 10727 IN MX 10 google.com.s9a1.psmtp.com.
g.cn. 259127 IN NS ns1.google.com.
g.cn. 259127 IN NS ns4.google.com.

Received 325 bytes from **8.8.4.4#53 in 196 ms**



好记又免费，爽哉！！ :)



**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**



### 相关文章

* [![我看ChatGPT: 为啥谷歌掉了千亿美金](https://coolshell.cn/wp-content/uploads/2023/02/chatgpt-150x150.jpg)](https://coolshell.cn/articles/22398.html)[我看ChatGPT: 为啥谷歌掉了千亿美金](https://coolshell.cn/articles/22398.html)
* [![Google Inbox如何跨平台重用代码？](https://coolshell.cn/wp-content/uploads/2014/11/inbox2-640x264-150x150.jpg)](https://coolshell.cn/articles/12136.html)[Google Inbox如何跨平台重用代码？](https://coolshell.cn/articles/12136.html)
* [![PFIF网上寻人协议](https://coolshell.cn/wp-content/uploads/2013/04/Google-Person-Finder-150x150.png)](https://coolshell.cn/articles/9508.html)[PFIF网上寻人协议](https://coolshell.cn/articles/9508.html)
* [![来信， 创业 和 移动互联网](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/2.jpg)](https://coolshell.cn/articles/5815.html)[来信， 创业 和 移动互联网](https://coolshell.cn/articles/5815.html)
* [![SteveY对Amazon和Google平台的吐槽](https://coolshell.cn/wp-content/plugins/wordpress-23-related-posts-plugin/static/thumbs/24.jpg)](https://coolshell.cn/articles/5701.html)[SteveY对Amazon和Google平台的吐槽](https://coolshell.cn/articles/5701.html)
* [![一些文章和各种资源](https://coolshell.cn/wp-content/uploads/2011/09/image008-150x150.jpg)](https://coolshell.cn/articles/5224.html)[一些文章和各种资源](https://coolshell.cn/articles/5224.html)
The post [google的免费dns服务器](https://coolshell.cn/articles/2015.html) first appeared on [酷 壳 - CoolShell](https://coolshell.cn).