---
author: ccbikai
comments: true
date: 2013-06-25 12:26:55 +0800
layout: post
slug: play-openwrt-1
title: openwrt折腾记(一)
postid: 1582
categories:
- 科技牛逼
tags:
- 路由器
- linux
- openwrt
---
六月十七号，趁着天猫搞活动送的四十块红包，入手了一款迷你路由器TP-WR702N v3，看着挺迷你，不过还能刷openwrt。  
[![WR720N](https://dn-mtimg.qbox.me/large/4eda25f5jw1e60a2pf9elj20et080aa5.jpg)](https://dn-mtimg.qbox.me/large/4eda25f5jw1e60a2pf9elj20et080aa5.jpg "WR720N")  
<!-- more -->
网上有好几个刷机包，有集成软件的，有纯净的，不过我这人有点儿小“洁癖”，就选择了纯净版。刷机很简单，直接升级就好了，刷完机没有什么问题，我就去搞联网，这就遇到了几个问题。  

路由器联网后，路由器可以访问互联网，电脑却不行。问了好几个论坛，有人说是防火墙问题。有人说是DNS问题。不过我在电脑上边ping baidu.com ,可以得到百度的ip地址，明显就不是DNS的问题了。再看看防火墙配置，我把防火墙所有的设置都设置为接受，电脑还是不能联网，改了好多地方都不行。然后实在没有办法了，就去刷了个集成软件的固件，刷好设置一下上网密码，就可以上网了，然后研究了一下他的配置，发现我第一次设置PPPoE 的时候，没有选择防火墙，然后就不能NAT 转发，导致电脑发出去的数据包丢失，自然就不能上网了。  
[![openwrt](https://dn-mtimg.qbox.me/large/4eda25f5jw1e60a5b4skcj211j156jvf.jpg)](https://dn-mtimg.qbox.me/large/4eda25f5jw1e60a5b4skcj211j156jvf.jpg "openwrt")  

上网搞定就折腾文件共享，首先是挂载优盘，这个由于最近在使用linux系统，所以很容易就挂载好了。不过装软件的时候，固件自带的软件源已经不能访问了，只能自己搭建了一个软件源，这个软件源只有wr720n能用的软件，也就200多M，找了个免费的cdn（可以直接FTP上传文件的），上传好，绑定域名，更新软件源，安装samba，一切OK。然后设置共享目录，账户密码，基本也没有遇到什么大问题，小问题谷歌一下就找到了教程。  

samba配置好以后，电脑直接文件管理器打开smb://192.168.1.1 ,输入密码账户就可以访问了。手机我用的是安卓系统，使用es文件浏览器的局域网功能，也可以访问共享文件。不过windows我还没有搞好，暂时不研究了，现在主要用linux系统，以后再说。  

第一次折腾就先到这儿，下次折腾离线下载。
