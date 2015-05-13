---
author: ccbikai
comments: true
date: 2014-04-16 22:24:10 +0800
layout: post
slug: push-wordpress-comment-with-pushbullet
title: 巧用Pushbullet推送Wordpress评论
postid: 1609
categories:
- 科技牛逼
tags:
- 博客
- 推送
- 安卓
- 苹果
---
虽然Wordpress自带新评论邮件通知功能，但是用起来不够极(zhuāng)客(bī)范，现在就让面条来教你长长逼格。
[![推送](https://dn-mtimg.qbox.me/large/005ygACVjw1efhs4p6x4hj30xc0hzmz3.jpg)](https://dn-mtimg.qbox.me/large/005ygACVjw1efhs4p6x4hj30xc0hzmz3.jpg)

<!-- more -->
工欲善其事，必先利其器。先得找个推送软件，经过我的耳目打听，现有四款“民用”软件供我使用。首先是高贵的[Push.co][1]，可是这家伙只有iOS客户端，善良的面条怎么能不考虑用安卓的筒子们呢？果断抛弃！还有个[Pushover][2]，虽然支持安卓客户端，但是要美国的人民币，社会主义国家要节约，所以就让他收他的去吧。举贤不避亲的来看看台湾同胞做[Qpush][3]，虽然有点像企鹅的东西，不过做的还不错，但是也只有iOS客户端，而且没有API，不得不大义灭亲。最后只剩下可爱的[Pushbullet][4]了，客户端覆盖Android，iOS，Windows , Chrome ,Firefox，支持推送文件，图片，笔记，地图，列表，链接。而且还可以在客户端之间互传，实乃居家旅行必备。面条这次就翻它的牌了！

工具选好就是方法了，凭着面条不那么丰富的网络知识，找到了三个方法。  
1.  [使用Zapier](http://tool.miantiao.me/url/1hJq7W7) 。这方法虽然简单，但是有1-15分钟的延迟，而且还要告诉[Zapier][5]一个Wordpress帐号和密码。面条有3秒就能收到推送的方法，怎么还能用它呢？不过[Zapier][6]真不错，比IFTTT功能更强大的IFTTT，下次再介绍吧。  
2.  [使用插件](http://tool.miantiao.me/url/1t9RSeI)。[Pushbullet][7] 有自己的Wordpress插件，不过功能太多，那些总是喜欢把插件代码化的人怎么受得了呢？逼格提高的程度不高，还是算了吧！  
3.  插件不用，肯定就要用代码了，别担心，面条已经连夜写好，摸黑调试了，如果您看到这里有点感动，留给面条[加个茶叶蛋][8]吧。  

好了，前边都是一堆废话，现在开始提高逼格。  
**前戏**：要推送肯定要去  [Pushbullet][9] 注册帐号了，不对，不是注册，直接用谷歌帐号登录就行了。什么？你没有谷歌帐号，下面的内容不用看了，面条没法帮你了。  
**发展**：帐号有了就在你需要推送的设备上装客户端，[安卓2M][10]([豌豆荚][11])，[苹果1M][12]，你没看错，苹果有一兆大小的软件，其他客户端自己在官网找，实在找不到，下课后来我办公室。设备装好，登录后，在 [这里][13] 找到你的Apikey，抄在左手心。然后用下边的秘籍找到设备ID，抄在右手心。
[![KEY](https://dn-mtimg.qbox.me/large/005ygACVjw1efhs6zhoh4j30ic09bjsi.jpg)](https://dn-mtimg.qbox.me/large/005ygACVjw1efhs6zhoh4j30ic09bjsi.jpg)
**高潮**：修改你主题的functions.php文件，在`<?php` 后边加入下边的代码，别忘了把你手心的对应代码誊上去，不然就推送给都教兽了。
<iframe width="100%" height="300" src="http://tool.miantiao.me/gist/ccbikai/10881201.pibb" frameborder=0 ></iframe> 

到现在你就可以加速了，去你博客找篇文章，然后冒充自己，发表一条像样的评论，别被Akismet牌Condom给挡住了，不出意外，3秒内就可以把评论发射当你的手机上了。
[![详细](https://dn-mtimg.qbox.me/large/005ygACVjw1efhs2chzidj30xc0n9mzt.jpg)](https://dn-mtimg.qbox.me/large/005ygACVjw1efhs2chzidj30xc0n9mzt.jpg)

喂，别急着走，还有**后戏**，装个Wordpress客户端，收到评论后，马上回复下，让小伙伴惊呆一次。


番外篇：现在觉得推送软件挺好用的，配合Zapier和IFTTT可以让好多不支持推送的网站让他支持推送，比如说心仪的妹子发了条新微博，你就可以在几分钟内收到推送。由于Zapier和IFTTT都不支持新浪微博，所以只能用RSS，你可以用网上的工具，也可以自己搭建。
下边是面条的超贱天气预报。
[![天气预报][14]](https://dn-mtimg.qbox.me/large/005ygACVjw1efhrzvrlrkj30sw0esjsm.jpg)


  [1]: http://tool.miantiao.me/url/P53WxC
  [2]: http://tool.miantiao.me/url/1gAESWV
  [3]: http://tool.miantiao.me/url/1ipcOtG
  [4]: http://tool.miantiao.me/url/1gAFdc1
  [5]: http://tool.miantiao.me/url/1eyEvAH
  [6]: http://tool.miantiao.me/url/1eyEvAH
  [7]: http://tool.miantiao.me/url/1gAFdc1
  [8]: http://tool.miantiao.me/url/1iZSCek
  [9]: http://tool.miantiao.me/url/1gAFdc1
  [10]: http://tool.miantiao.me/url/1p9TVA3
  [11]: http://tool.miantiao.me/url/P55dEX
  [12]: http://tool.miantiao.me/url/1gGhdHZ
  [13]: http://tool.miantiao.me/url/1eyDZCS
  [14]: https://dn-mtimg.qbox.me/large/005ygACVjw1efhrzvrlrkj30sw0esjsm.jpg
