---
author: ccbikai
comments: true
date: 2014-09-24 17:00:28 +0800
layout: post
slug: zhihu-daily-rss
title: 知乎日报 RSS
postid: 1626
categories:
- 一块分享
tags:
- 知乎
- RSS
- 工具
---
之前用的知乎日报 RSS 是别人的，但是最近不工作了，所以只能自己动手折腾一个。 
[![知乎日报](https://dn-mtimg.qbox.me/large/c74746f0gw1ei8pvavboij20r808cmz2.jpg)](https://dn-mtimg.qbox.me/large/c74746f0gw1ei8pvavboij20r808cmz2.jpg)

<!-- more -->
用 Fiddler 抓包，然后 Python 模拟安卓客户端获取内容，用模板渲染一次，加上缓存就 OK 了。不过知乎日报的的API太简陋，不输出更新时间和作者，让人感觉很不舒服。而且有的文章还是站外的，只能去输出一个链接了。首页 14 分钟更新一次，分类的缓存有效期 30 分钟，超过 30 分钟访问时会刷新一次。

知乎日报首页 RSS： http://zhihurss.miantiao.me/dailyrss 。

分类RSS：  
“足球日报” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/8  
“动漫日报” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/9  
“设计日报” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/4  
“开始游戏” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/2  
“财经日报” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/6  
“电影日报” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/3  
“电子音乐” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/7  
“不许无聊” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/11  
“大公司日报” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/5  
“互联网安全” 的 RSS 为 http://zhihurss.miantiao.me/daily/id/10  

其他日报的RSS请访问 http://zhihurss.miantiao.me/theme 。

合集RSS：  
“深夜食堂”的 RSS 为：http://zhihurss.miantiao.me/section/id/1  
“瞎扯”的 RSS 为：http://zhihurss.miantiao.me/section/id/2  
“吃很重要”的 RSS 为：http://zhihurss.miantiao.me/section/id/3  
“知天下”的 RSS 为：http://zhihurss.miantiao.me/section/id/5  
“苗炜专栏”的 RSS 为：http://zhihurss.miantiao.me/section/id/6  
“小道消息”的 RSS 为：http://zhihurss.miantiao.me/section/id/7  
“硬科技”的 RSS 为：http://zhihurss.miantiao.me/section/id/8  
“最美应用”的 RSS 为：http://zhihurss.miantiao.me/section/id/9  
“鲜柚游戏周报”的 RSS 为：http://zhihurss.miantiao.me/section/id/10  
“豌豆荚设计奖”的 RSS 为：http://zhihurss.miantiao.me/section/id/11  
“#一周一折腾#”的 RSS 为：http://zhihurss.miantiao.me/section/id/12  
“麻省理工科技评论”的 RSS 为：http://zhihurss.miantiao.me/section/id/14  
“#周末话题优秀评论精选#”的 RSS 为：http://zhihurss.miantiao.me/section/id/15  
“整点儿新闻”的 RSS 为：http://zhihurss.miantiao.me/section/id/16  
“饿了”的 RSS 为：http://zhihurss.miantiao.me/section/id/17  

如果合集 RSS 不全，请留言。
