---
author: ccbikai
comments: true
date: 2014-05-10 19:16:37 +0800
layout: post
slug: a-random-image-tool
title: 随机图片链接生成工具
postid: 1612
categories:
- 一块分享
tags:
- 图片
- 工具
---
以前看到过国外的一个随机图片生成服务（Placeimg.com），可以为博客配图。不过速度实在不咋地，就想着自己写一个，现在写好了，那个网站的功能全有，不过没有介绍页面。

<!-- more -->
其实这个程序主要是需要一个好的图片源，我现在找到图片源还算可以，速度也很快（图片在[七牛]()，肯定快）。目前支持"people","car","digital","fashion","food","pet","toy","city"八个分类，如果不在意分类的话，可以使用"Any"分类。大小可以使用"300x200"这个格式，也可以只限制宽度，设置"300",就可以了。更多尺寸参数和七牛一样的，见下图：  
[![图片尺寸](https://dn-mtimg.qbox.me/large/005ygACVjw1eg9dh5hm83j30e00lb41c.jpg)](http://tool.miantiao.me/url/1j60QH4)

地址格式：http://randomimg.jd-app.com/分类/尺寸

演示：   
任意： http://randomimg.jd-app.com/any/500x300  
![任意](http://randomimg.jd-app.com/any/500)
人物： http://randomimg.jd-app.com/people/500
![人物](http://randomimg.jd-app.com/people/500)  
汽车： http://randomimg.jd-app.com/car/500
![汽车](http://randomimg.jd-app.com/car/500)  
数码： http://randomimg.jd-app.com/digital/500
![数码](http://randomimg.jd-app.com/digital/500)  
时尚： http://randomimg.jd-app.com/fashion/500
![时尚](http://randomimg.jd-app.com/fashion/500)  
食物： http://randomimg.jd-app.com/food/500
![食物](http://randomimg.jd-app.com/food/500)  
宠物： http://randomimg.jd-app.com/pet/500
![宠物](http://randomimg.jd-app.com/pet/500)  
玩具： http://randomimg.jd-app.com/toy/500
![玩具](http://randomimg.jd-app.com/toy/500)  
城市： http://randomimg.jd-app.com/city/500
![城市](http://randomimg.jd-app.com/city/500) 

还有功能，比如旋转，剪裁，高斯模糊，格式转换。需要的同学可以去看[七牛的文档](http://tool.miantiao.me/url/1fWAF58)。  
这是一个旋转了45度加了高斯模糊格式为webp的图片。
![高级](http://randomimg.jd-app.com/digital/500/blur/3x5/rotate/45/format/webp)
