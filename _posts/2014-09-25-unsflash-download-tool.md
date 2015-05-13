---
author: ccbikai
comments: true
date: 2014-09-25 17:25:08 +0800
layout: post
slug: unsflash-download-tool
title: Unsplash 全站下载脚本
postid: 1627
categories:
- 一块分享
tags:
- Python
- 爬虫
- 工具
---
中午面试回来逛 [V2EX](http://tool.miantiao.me/url/1Dy4QIx) ，发现有个博友很喜欢 [Unsplash](http://tool.miantiao.me/url/1u144iZ) 这个网站的图片，于是写了个脚本，把全站爬了下来。

<!-- more -->
脚本用 Python 写的，依赖 Requests ，BeautifulSoup 模块，直接使用`pip install requests beautifulsoup4`即可安装，建议使用国外的 VPS 爬，速度很好。

我 2014 年 9 月 25 日爬的数据可以去百度云下载 [http://pan.baidu.com/s/1c0Ae5Cc](http://tool.miantiao.me/url/Zehflk) 密码：ludn 。

运行`python unsplash.py`，然后输入最小页数和最大页数即可下载到脚本所在目录的 unsplash 文件夹中。

<iframe width="100%" height="300" src="http://tool.miantiao.me/gist/ccbikai/5bac77d4b97d66aac795.pibb" frameborder="0"></iframe>
