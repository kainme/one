---
author: ccbikai
comments: true
date: 2014-05-30 16:26:15 +0800
layout: post
slug: a-wechat-public-platform
title: 微信公众号“在南邮”开发笔记
postid: 1616
categories:
- 扯淡文章
tags:
- 微信
- 大学
- Python
---
前几天花了两天时间开发了一个微信公众号，主要拿来查我们学校教务系统成绩。今天有空就给加上了代理和统计功能。
[![登陆界面](https://dn-mtimg.qbox.me/large/4eda25f5gw1egwd49vgooj20d4091wek.jpg)](https://dn-mtimg.qbox.me/large/4eda25f5gw1egwd49vgooj20d4091wek.jpg)

<!-- more -->
感觉Python写东西真的很好，好多人性化的模块，像我这种新手写程序感觉就是调用调用调用。只要处理好逻辑，基本就没有问题。这次开发注意用了Flask做WEB框架，用来与微信后台通信（前些日子写“吃面条么”公众号，摸熟了微信回复消息方法，这次就顺利了一些）。HTTP抓网页相关的用的是人性化的Requests模块，比urllib2好用多了。抓到的页面就用BeautifulSoup分析，把成绩表格找出来，加入到字典。返回给微信的时候遍历输出就OK了。

[![查询界面](https://dn-mtimg.qbox.me/large/4eda25f5gw1egwd78kjfuj20ps0j3gor.jpg)](https://dn-mtimg.qbox.me/large/4eda25f5gw1egwd78kjfuj20ps0j3gor.jpg)

服务器部署在SAE上，主要是与微信后台通信快，而且我没有已经备案的域名，所以国内的服务器用不了。存储用的是新浪的KVDB，感觉就是给redis改了个名字，调用方法基本就差不多。以前测试没有几个流量，就没有用代理，但是想到以后如果人多了，肯定会被学校的人封了SAE的IP，所以还是早点用上代理。本来想自己网上抓代理，但是十分不稳定，就在V2EX上边问前辈们写爬虫的时候是怎么处理IP的，果然找到了神奇的淘宝，一块钱5000个代理，够我用一段时间了。刚开始是为了给我自己查成绩，写着就写成了多用户的，自己给自己改需求，以后要是做了产品经理会不会给程序员给打死啊。今天又给加了简单的计数统计功能，统计了绑定次数，查询次数，成功次数。看看这个期末能帮助多少人。

现在又计划给添加等级考试成绩查询，和课表查询功能。等有时间再加进去，还有坑爹的软件工程实验报告（一学期的）没有写呢，苦逼啊。
