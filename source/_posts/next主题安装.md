---
title: next主题安装
date: 2019-05-27 17:10:15
tags:
---

这个大约折腾了我一天的时间吧，不过能做好就好了。

首先是从官方界面那里下载，虽然说那边推荐用 git clone 的方式但请各位相信我血泪的教训！**千万别！**在 release 界面挑选一个压缩包，放在 hexo 的 themes 文件夹下面。里面应该有一个默认的主题叫 `landscape` ，看到它那就没跑了，放在同级就可以。



如果如果你好死不死用了 git clone 的方式，那么暂且还有补救的方法……因为这样目前你的 git 仓库就有两个，一个是管理主站的一个是专门用在 next 这个主题上，如果直接 push 那是无法将 next 提交到 github 上的。应该是属于这种情况，具体可以看这个链接：

https://git-scm.com/book/zh/v2/Git-%E5%B7%A5%E5%85%B7-%E5%AD%90%E6%A8%A1%E5%9D%97

然后在 next 这个文件夹下面删除 .git 目录，rm -rf .git，这样 next 就是一个普通的文件夹，可以一起 push 了。

当然如果你没有删就 push，则会发现非常麻烦的……git 给你提示里面包含嵌入式仓库，直接 push 的话在 github 里文件夹显示的就是灰色的。你删除了也没用，它们会显示上下游一致……这时候就要删除缓存，啊我也不知道这是什么原理

`git rm -r --cached next`

这样就不会报上下游一致无法提交，直接重新 push 就好～



ref：

https://blog.csdn.net/weixin_38927964/article/details/84201322

[顺便熟悉一下 git md 吧][https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links ]

[一个看起来很不错的个人 blog，以后多参考][https://akilarlxh.github.io ]

[next 官网][https://theme-next.org/ ]

[hexo 官网][https://hexo.io ]



本文使用 typora 写作，目前觉得它很棒～





















