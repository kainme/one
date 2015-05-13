---
author: ccbikai
comments: true
date: 2014-08-09 14:50:23 +0800
layout: post
slug: a-html5-netease-music-player
title: HTML5 版网易云音乐外链播放器
postid: 1625
categories:
- 一块分享
tags:
- 音乐
- 播放器
---
前段时间写了个虾米的外链播放器，有人问有没有网易版的，毕竟网易云音乐 的歌曲也挺多，于是就折腾出来了网易云音乐版的。

<!-- more -->
使用方法和虾米的是一样的，提供音乐外链和播放器外链。音乐外链请使用 http://miantiao.jd-app.com/m163/ID.mp3 ,ID 请替换为网易云音乐的 ID，也就是浏览器地址栏那个数字。如：http://miantiao.jd-app.com/m163/111677.mp3

播放器使用方法也和虾米一样：  
###演示：  
<iframe src="http://miantiao.jd-app.com/m163player/111677" frameborder="0" scrolling="0" width="430" height="200" allowtransparency></iframe>

###使用方法：
使用 iframe 调用（替换里边的数字为虾米音乐ID）：  
`<iframe src="http://miantiao.jd-app.com/m163player/111677" frameborder="0" scrolling="0" width="430" height="200" allowtransparency></iframe>`

###WordPress使用方法：  
直接在functions.php插入下面的代码：  
<iframe width="100%" height="200" src="http://tool.miantiao.me/gist/ccbikai/6b85829db7749cc196ab.pibb" frameborder=0 ></iframe>

然后单独在把虾米音乐地址写在一行就行了。

嗯，代码也是开源的，有问题欢迎帮我解决。  
<iframe src="http://lab.lepture.com/github-cards/cards/medium.html?user=ccbikai&repo=musicplayer" frameborder="0" scrolling="0" width="400" height="300" allowtransparency></iframe>




