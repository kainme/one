---
author: ccbikai
comments: true
date: 2014-03-14  18:46:18 +0800
layout: post
slug: google-doc-website-monitor
title: 使用谷歌文档监控网站状态
postid: 1604
categories:
- 科技牛逼
tags:
- 网站
- 谷歌
---
今天在找[Twitter RSS工具](http://www.inbiji.com/biji/ji-ge-twitter-rss-sheng-cheng-gong-ju.html)的时候，发现一个google script可以生成。然后在作者的博客看了看，发现一个监控网站状态的脚本，感觉挺好玩，就分享一下。

<!-- more -->
原本是英文的，顺便汉化了一下，给比我英语还差的人，首先你需要给我的 [网站监控](https://docs.google.com/spreadsheet/ccc?key=0Am75G25Lf4GOdFZWZ1NKamM0U1lCSWxZdG1KalVsVkE&usp=drive_web#gid=0) 文档创建一个副本。
[![创建副本](https://dn-mtimg.qbox.me/large/793f2bffgw1eeffyrkupfj20ct078q3c.jpg)](https://dn-mtimg.qbox.me/large/793f2bffgw1eeffyrkupfj20ct078q3c.jpg)

然后在你创建的副本中配置里边的选项，多个网址需要用**英文逗号**隔开，邮箱填一个你的。  就这么简单，配置完毕。  
[![配置](https://dn-mtimg.qbox.me/large/793f2bffgw1eefg27ic1fj20dk078aam.jpg)](https://dn-mtimg.qbox.me/large/793f2bffgw1eefg27ic1fj20dk078aam.jpg)

然后开始“安装”，点击菜单栏**网站监控**，进行第一步，需要谷歌授权，在弹出小窗口里边确定。然后第二步，点击开始监控。  现在程序就开始工作了，如果网站宕机，就会用你的谷歌邮箱发邮件到你设置的邮箱提醒。短信通知我正在测试中。
短信现在也能通知了，需要谷歌绑定手机号。
[![短信](https://dn-mtimg.qbox.me/large/6257acd7gw1eepixkyn3qj20f00qodi6.jpg)](https://dn-mtimg.qbox.me/large/6257acd7gw1eepixkyn3qj20f00qodi6.jpg)

故意弄了一个宕机，测试一下邮件通知。
[![通知](https://dn-mtimg.qbox.me/large/793f2bffgw1eefg658l8tj209c04bglu.jpg)](https://dn-mtimg.qbox.me/large/793f2bffgw1eefg658l8tj209c04bglu.jpg)

原作者地址：http://www.labnol.org/internet/website-uptime-monitor/21060/
