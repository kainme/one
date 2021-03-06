---
author: ccbikai
comments: true
date: 2014-01-18 16:23:45 +0800
layout: post
slug: qiniu-feel
title: 七牛云存储使用感受
postid: 1598
categories:
- 科技牛逼
tags:
- 网站
- 云存储
---
[in笔记](http://www.inbiji.com)使用七牛云存储也已经将近三个月了，期间一直很稳定，图片加载速度很快，而且我也把网站备份放在上边。现在讲讲使用感受。

<!-- more -->
最开始使用七牛是为了给博客图片加速，原来用的是Inscapdns，但是速度不怎么样，受不了等待就切换到了七牛。切换过程基本上没有遇到问题，用的主要是七牛后台的源站加速，后台设置一下，然后在博客替换一下图片地址就好了，具体过程见《[无痛使用七牛为你的WORDPRESS博客图床加速](http://www.inbiji.com/biji/using-seven-cattle-painless-wordpress-blog-for-your-bed-acceleration-diagram.html)》。由于我经常修改博客模板就没有给css,js文件加速，只给图片加速。这样做有个好处，就是可以给博客图片在七牛做个备份，如果源站图片丢失（概率不大），可以去七牛找回来。七牛的图片只要你不删除，就一直在的，别担心七牛会出问题，他们的工程师也不是吃软饭的。

文章内图片加速搞定，加载速度很快，但是首页和分类等页面的缩略图还是原来的地址，这个也用七牛解决了。七牛不仅能存储图片，而且还可以在云端处理图片，使用方法也很简单，只需要在图片URL后边加入一些参数即可，可以生成缩略图，也可以加水印，还可以直接返回exif信息，具体使用方法看看官方文档，很简单。修改模板的图片地址，把缩略图的生成交给了七牛，给自己博客的小VPS（只用128M）节省点内存。七牛不仅可以处理图片，还可以音频，视频。而且比处理图片的功能还要强大，不过我暂时还用不到，有兴趣的同学可以去看官方文档。

以前的博客是备份到Dropbox的，但是Dropbox的空间太小，只有2G，用几天就满了。我把网站的备份也放在了七牛，用的是七牛的python SDK，不得不说七牛的SDK也做得不错，我只用了几行shell脚本，然后python调用七牛上传，加入cron定时，博客备份就搞定了，这样大概一个月七牛删除一下比较早的备份就行了。具体的实现过程我在[in笔记](http://www.inbiji.com)写了教程，需要的朋友去看看《[备份vps数据到七牛云存储](http://www.inbiji.com/biji/vps-backup-data-to-cloud-storage-seven-cattle.html)》，脚本在[github](https://github.com/ccbikai/backuptoqiniu)上边有开源。

<iframe src="http://lab.lepture.com/github-cards/cards/medium.html?user=ccbikai&repo=backuptoqiniu" frameborder="0" scrolling="0" width="400" height="300" allowtransparency></iframe>

目前用到的七牛的功能主要就这三个，不过我还准备做个小实验，就是用七牛统计博客订阅人数。准备在rss里边添加一张存储在七牛的图片，然后给存储仓库开启访问日志（图片单独存储在一个仓库），过段时间下载日志，用日志宝分析一下，就可以推算出大约有多少人在订阅我博客（嗯，我知道订阅的人肯定很少，要不您[订阅](http://feed.miantiao.me)一下?）。不过七牛的日志是按日分割生成的，要是能按大小分割生成就好了，貌似我的需求有点儿变态。

七牛每个账户也有一定的免费额度，够小博客使用，反正我是够用了。如果流量不够用，记得先去设置一下防盗链白名单。邀请其他人也是可以增加免费额度的，如果你要注册七牛，用我的邀请链接吧[http://126.am/qiniuyun](http://126.am/qiniuyun)。

忘了说了，七牛还有一个公益CDN项目—— http://www.staticfile.org，里边的js,css库很全。
