---
author: ccbikai
comments: true
date: 2014-05-20 11:26:55 +0800
layout: post
slug: zhihuzhuanlan-rss
title: 知乎专栏RSS
postid: 1614
categories:
- 一块分享
tags:
- 知乎
- RSS
---
昨晚看到一些知乎专栏挺好，想订阅到Feedly，用Press阅读，却没有发现RSS，于是就自己写了一个。

<!-- more -->
现在已经有了知乎日报的 RSS ，需要的请点击[知乎日报 RSS](/zhihu-daily-rss.html)。

本来以为需要写爬虫，正好可以练习一下BeautiSoup，没想到知乎专栏有开放的API，直接调用就好了。全当练习Flask和Requests了。

程序没有缓存，直接读知乎的内容，一般来说feed基本都不需要缓存。框架用的Flask，抓数据用Requests，顺便加了图片防盗链处理，阅读无障碍。代码很快就写好了，然后就调试，除Bug。不过最麻烦的是在JAE部署，老是失败（不是程序的问题）。

使用很简单，替换下面的 `$username` 为专栏ID就行了。  
> http://zhihurss.miantiao.me/zhihuzhuanlan/$username

如[http://zhihurss.miantiao.me/zhihuzhuanlan/taosay](http://zhihurss.miantiao.me/zhihuzhuanlan/taosay)

程序支持限制读取数量，参数是limit，默认是10，最大是多少也没有测试，反正1000是可以的。  
带参数使用方法：[http://zhihurss.miantiao.me/zhihuzhuanlan/taosay?limit=20](http://zhihurss.miantiao.me/zhihuzhuanlan/taosay?limit=20) 。
