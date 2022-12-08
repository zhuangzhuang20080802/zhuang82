---
title: About This Blog
date: 2022-12-08 08:08:46
---
# 关于此博客  
**这大概是我的第三个博客了😅**

今年的8月14日，我构建了我的第一个博客，那时动机很简单，我学会了翻🧱，逐渐不满于国内平台的审核机制，希望有一个平台来自由的发表观点，于是我就找到了GitHub Pages，并用Bootstrap5写作，博客源码至今还能在[zhuangzhuang20080802/blogfirst](https://github.com/zhuangzhuang20080802/blogfirst)中找到。

但很快我就发现了一个问题，即每写一篇博文，我都要使用HTML语言一点点编辑样式，效率实在太低，我也懒得打字，所以很快，那个博客就被废弃了。

之后我学习了Markdown，并用[Apostrophe](https://apps.gnome.org/zh-CN/app/org.gnome.gitlab.somas.Apostrophe/)导出为HTML，新的博客只有一个`index.html`，不同博文用目录中的语法类似`[...](#...)`（好像叫锚点）实现跳转，维护起来很容易，所以至今还能用<https://zhuangzhuang20080802.github.io/>访问。

但是很快，新问题出现了，Apostrophe会默认把所有Markdown中引用的图片在HTML中以Base64呈现，导致那一个`index.html`异常庞大，如图

![filesize](/images/2212081.png)

GitHub Pages国内本来就不快，这样一来，加载完博客界面基本需要十几秒，实在慢的不可忍受，即使后来在Cloudflare Pages上建立了一个镜像站，也不尽如人意。

接着，我就考虑建立这个博客。

我不想夸Hexo有多好，Hexo的文档写的简直不可理解，但在网络教程的帮助下，再加上一个极简的主题，我终于把这个博客打磨成我想要的样子，并托管在Cloudflare Pages上~~以获得高访问速度~~。

***

目前`*.pages.dev`在国内大部分地区超时，估计是最近发生的某事的缘故，等我注册完独立域名后博客才能正式运营，着急的朋友就用VPN或Tor吧。

最后

![gfw](/images/2212082.png)