---
author: ccbikai
comments: true
date: 2014-05-11 18:13:15 +0800
layout: post
slug: weibo-like-for-dear
title: 新浪微博"为女神点赞"脚本
postid: 1613
categories:
- 一块分享
tags:
- 微博
- 代码
---
前两天发现了[新浪微博点赞](http://tool.miantiao.me/url/1safNHI)的接口，于是就写了这个脚本。

<!-- more -->
需要的马上去部署，暂时没有女神的，先Star一下，然后去找女神。

全自动点赞版本：[https://github.com/ccbikai/likefordear/releases/tag/v0.1](http://tool.miantiao.me/url/1nF0iaM)
<iframe src="http://lab.lepture.com/github-cards/cards/medium.html?user=ccbikai&repo=likefordear" frameborder="0" scrolling="0" width="400" height="300" allowtransparency></iframe>

这是一个自动给女神微博点赞的脚本，三分钟检查一次女神微博更新，如果有新微博，就立马点赞。(全自动版)  
如果女神发了悲伤的微博，攒了就惨了，所以有了半自动版。半自动版：如果有新微博，邮件通知，邮件里边包含**一键点赞**链接。然后自己判断

部署在SAE，一个Python 脚本。

###搭建方法：
1.在SAE新建一个应用，**初始化KVDB**。

2.编辑源代码index.wsgi，修改女神微博ID和授权码。  
>微博ID获取方法：打开女神的任意一条微博的如:`http://weibo.com/1649913047/B3FVInUPr` , 这里边的数字就是微博ID。  
授权码获取方法：打开`https://api.weibo.com/2/oauth2/authorize?client_id=82966982&response_type=token&display=js&redirect_uri=https://api.weibo.com/oauth2/default.html` ，授权后出现一个空白页面，不要关闭，按 Ctrl+U 查看源代码，找到"access_token":"2.00tlp********"。嗯，授权码就找到了。

>SECRET: 自己设置的验证密钥，防止赞微博接口被乱用（随便写几位字母就行了）  
TOMAIL: 接收提醒的邮箱  
smtp相关的是邮件发送服务器，配置方法见各邮箱帮助页 
    
3.编辑config.yaml，加入下边的代码：  

 
```
    cron:
    - description: like
      url: /like
      timezone: Beijing
      schedule: "*/3 * * * *"
```

4.打开 `http://<appname>.sinaapp.com/like` 出现'get again'，再刷新一次出现'liked'，好了，女神以后发的微博都会在三分钟内邮件通知你。  
5.收到邮件以后，自己判断下需不需要点赞，如果需要，点击邮件里边的链接，看到'liked',就是赞成功了。
###注意事项：
 1.授权有效期如果不使用Weico.apple微博客户端一般是90天，到时记得续期。如果使用Weico苹果客户端。建议替换Weico苹果的APPKEY为Weico安卓的'211160679 '。代码和授权页面都改一下。
   
 2.每三分钟抓取一次，每次抓取最新20条微博。这参数可以在源码里边改，三分钟在config.yaml,20条在wsgi.py，注意每次最多100条。
 
####有些未公开的接口，新浪微博开发平台的同志看到不要封，大家找个女朋友不容易。
