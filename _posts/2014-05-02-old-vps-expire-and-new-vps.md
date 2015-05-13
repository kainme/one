---
author: ccbikai
comments: true
date: 2014-05-02 18:07:21 +0800
layout: post
slug: old-vps-expire-and-new-vps
title: VPS到期，新入了个超低价VPS
postid: 1611
categories:
- 扯淡文章
tags:
- 网站
- 新浪
---
两个域名到期，两台VPS到期。

<!-- more -->
[In笔记](http://tool.miantiao.me/url/1hC1Zpg)用的是一台一年8美元的超小VPS（128M内存），流量不大，所以还挺稳定，准备再续费一年放着。另外一台是专门折腾用的。DO的VPS从去年的八月就在开始免费用着，土豪公司一直送钱，[注册就给10美元（最低配置可以玩两个月）](http://tool.miantiao.me/url/1fDJ6SJ)，所以前前后后给了我40刀，让我用了大半年时间。不过到现在撑不下去了，只能自己去买低价的VPS了。

前两天买了个[一年4美元的VPS(256M)](http://tool.miantiao.me/url/1hjHBEq)，之所以这么便宜主要是没有IPv4的公网IP，不过有5个IPv6的IP。IPv4访问要靠服务商机器端口转发，不过够我用了，我也就需要三个端口就行了。一个SSH，一个Shadowsockes，一个AMH面板管理，自定义后记着就行了。注意这个VPS是个三无VPS：无IPv4公网IP，无技术支持，无工单支持。

拿到机器后，没有办法直接链接，先在SolusVM面板里边开了个Serial Console，修改了SSH端口号，禁用密码登录，只许密钥登录（安全第一），然后重启SSHD，就可以用Xshell直接连接了。挂了[Vagex](http://tool.miantiao.me/url/PWzMNH)的脚本，希望能赚回本。然后装上Shadowsockes，做梯子用，测了一下速度，下载时能跑慢宿舍的12M带宽。之后就装了AMH面板，简单方便，本来以为AMH面板支持IPv6的，没有想到不支持。只能自己重新编译一下Nginx，然后恢复数据，把网站放了上去。用Cloudflare的CDN，可以将IPv6的地址转换成IPv4，网站就可以访问了，虽然Cloudflare在国内访问有些不方便，不过[那个网站](http://tool.miantiao.me/url/1kviq49)只是我抓数据的，访问不了没有关系。

还有两个域名到期了，一个cn的，一个pw的，品相都不好看，就不再续费了，由他去吧。

重写了新浪微博RSS生成脚本，支持多图多用户了。里边有点黑科技，哪位朋友要是需要用到，可以找我，我把你加入白名单（没钱买服务器，只能……）。  
预览：[http://www.miantiao.me/weiborss/1649913047](http://tool.miantiao.me/url/1n9Rucw) 

友情提示：以上的一些链接含有AFF，点击注册对你没有坏处，对我有点好处，有需要的就注册吧。
