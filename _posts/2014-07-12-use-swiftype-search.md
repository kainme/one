---
author: ccbikai
comments: true
date: 2014-07-12 13:43:11 +0800
layout: post
slug: use-swiftype-search
title: 使用 Swiftype 解决 Jekyll 等静态博客搜索功能
postid: 1624
categories:
- 一块分享
tags:
- 搜索
- 代码
---
自从去年六月开始使用 Jekyll 已经有一年时间了，这段时间内一直使用谷歌自定义搜索来解决Jekyll的搜索功能。但是随着傻逼二逼加蠢逼的 GFW 开始大量封锁网站，谷歌自定义搜索也不能用了（翻墙除外），在 V2EX 上边看到有人推荐 Swiftype 看了一下感觉不错，而且对中文支持也不错，就选用 Swiftype 来解决搜索问题。

<!-- more -->
Swiftype 基本使用很简单，注册，添加你的网站，它会自动搜索你 Sitemap 或者 RSS 等功能来索引你的网站。我博客是有 Sitemap 的，所以173篇日志几分钟就全部收录了。安装很简单，先把它给你的安装代码添加在你的主题模板里边，然后在你的搜索表单添加对应的ID就可以了。当然，高手还可以自定义搜索界面，收录信息。演示在我博客右上角的搜索框。

官网：https://swiftype.com

[![安装](https://dn-mtimg.qbox.me/large/4eda25f5tw1ei9yflb1vdj20li0g9n05.jpg)](https://dn-mtimg.qbox.me/large/4eda25f5tw1ei9yflb1vdj20li0g9n05.jpg)

Swiftype 不仅支持自定义搜索，还开放API，这样通过简单调用我的微信公众号 “吃面条么” 就可以搜索我博客的文章了，以前羡慕WordPress可以做到，现在各种网站都可以了。扫码可以关注我微信噢。

[![二维码](https://dn-mtimg.qbox.me/large/4eda25f5tw1ei9ye9xt1hj20zk0zkadw.jpg)](https://dn-mtimg.qbox.me/large/4eda25f5tw1ei9ye9xt1hj20zk0zkadw.jpg)

Swiftype 的基本使用就这么多，以后要是遇到啥好玩的，我还会继续介绍。
