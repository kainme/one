---
author: ccbikai
comments: true
date: 2014-04-03 20:02:45 +0800
layout: post
slug: a-xiami-music-link
title: 写了个虾米音乐外链工具
postid: 1607
categories:
- 一块分享
tags:
- 音乐
- 工具
---
前两天发现一个虾米手机客户端的一个[接口][1]，可以生成虾米的音乐直链地址，不过后边有一个动态的hash，所以简封装了一下，拿出来共享。

<!-- more -->
先听首歌:
<iframe src="http://miantiao.jd-app.com/xiamiplayer/1772353128" frameborder="0" scrolling="0" width="430" height="200" allowtransparency></iframe>

总是有人问博客音乐外链放哪里，放自己空间怕被搜索引擎抓到，流量超标，网上找的又不稳定，说不定那天就失效了。幸好虾米支持外链，直接获得地址就能调用了。还有个网易云音乐，也可以支持外链调用，可是获取麻烦，我用python写的程序总是抓不到地址，但是别人PHP写的却可以，不知道什么情况。

把我的程序共享出来，需要的可以直接使用（我自己也在用，只要我能用，也就能用），怕不稳定的，我已经开源了代码，你可以自己在SAE，或者BAE/JAE上搭建一个。SAE教程：[利用SAE获得虾米音乐外链][2]

使用方法很简单，获取虾米音乐ID（就是浏览器地址栏那串数字），替换http://miantiao.jd-app.com/xiami/1772353128.mp3中的数字就行了。

其实这个程序也支持百度音乐的，不过不支持外链，只支持下载。


  [1]: http://www.xiami.com/app/iphone/song/id/1772353128
  [2]: http://www.inbiji.com/biji/li-yong-sae-huo-de-xia-mi-yin-le-wai-lian.html
