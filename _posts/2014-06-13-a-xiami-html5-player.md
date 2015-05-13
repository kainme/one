---
author: ccbikai
comments: true
date: 2014-06-13 12:09:06 +0800
layout: post
slug: a-xiami-html5-player
title: HTML5版虾米音乐外链播放器
postid: 1619
categories:
- 一块分享
tags:
- 虾米
- 音乐
- 播放器
- 代码
---
虾米原来的外链播放器是Flash的，手机上不能播放，于是折腾了一个HTML5的播放器。而且比官方的强大，支持封面图，支持同步歌词。还有下载，分享到微博功能（带“虾米音乐”尾巴）。

<!-- more -->
服务端还是用Python读取[虾米的API](http://miantiao.me/a-xiami-music-link.html)，然后渲染一下模板就行了。客户端网页项目太小，就没有用 jQuery，直接用原生 JavaScript 控制 audio 的播放暂停就行了。

###演示：  
<iframe src="http://miantiao.jd-app.com/xiamiplayer/45819" frameborder="0" scrolling="0" width="430" height="200" allowtransparency></iframe>

###使用方法：
使用 iframe 调用（替换里边的数字为虾米音乐ID）：  
`<iframe src="http://miantiao.jd-app.com/xiamiplayer/45819" frameborder="0" scrolling="0" width="430" height="200" allowtransparency></iframe>`

###WordPress使用方法：  
直接在functions.php插入下面的代码：  
<iframe width="100%" height="200" src="http://tool.miantiao.me/gist/ccbikai/00f810676207184a634e.pibb" frameborder=0 ></iframe>

然后单独在把虾米音乐地址写在一行就行了。
[![WordPress](https://dn-mtimg.qbox.me/large/4eda25f5gw1ehccuhndl4j20fw061js6.jpg)](https://dn-mtimg.qbox.me/large/4eda25f5gw1ehccuhndl4j20fw061js6.jpg)  
效果演示：  
[WordPress效果演示](http://tool.miantiao.me/url/1io4A1V)  

不支持HTML5的浏览器将重定向到Flash播放器，预览(<a href="javascript:void(0)" onclick="(function(){document.getElementById('xiamiflash').height='200';document.getElementById('xiamiflash').src='http://www.xiami.com/res/app/img/swf/weibo.swf?dataUrl=http://www.xiami.com/app/player/song/id/45819/type/7/uid/0'}());">点击加载</a>)：  
<iframe id="xiamiflash" src="" frameborder="0" scrolling="0" width="430" height="0" allowtransparency></iframe>

代码已经开源的，有问题欢迎帮我解决。  
<iframe src="http://lab.lepture.com/github-cards/cards/medium.html?user=ccbikai&repo=musicplayer" frameborder="0" scrolling="0" width="400" height="300" allowtransparency></iframe>
