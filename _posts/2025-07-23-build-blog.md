---
layout: post
title: 手把手使用Github Pages + Jekyll搭建个人博客
subtitle: 以及踩过的坑
categories: markdown
tags: [blog]
---

## 写在开头
最近在研究使用GitHub Pages搭建博客，好处有两点：
1. 免费，简单，不用租服务器买域名，一键部署
2. 教程多，出问题方便在网上找解决方案

GitHub Pages也支持很多博客框架，这里我用的官方推荐的Jekyll，当然用其他的Hexo，gitbook等等也都是可以的，网上教程也很多，部署流程也大同小异。

今天总结一下我的搭建过程，以及中途遇到的一些坑，照着这篇文档，应该能一次搭建成功。

## 参考教程
如果只是搭建一个最简单的博客，直接参考官方教程和以下教程即可，十分钟搞定直接开写：

[使用Jekyll + GitHub Pages搭建个人博客]:https://blog.csdn.net/zzy979481894/article/details/132678717
[GitHub Pages快速入门]:https://docs.github.com/zh/pages/quickstart
[GitHub Action]:https://docs.github.com/zh/actions/tutorials
[Jekyll主题大全]:http://jekyllthemes.org/
[Jekyll-yat主题]:https://github.com/jeffreytse/jekyll-theme-yat
[A GitHub Action to deploy the Jekyll site conveniently for GitHub Pages]:https://github.com/jeffreytse/jekyll-deploy-action
[Jekyll在windows上的安装]:https://jekyllrb.com/docs/installation/windows/
[Error: Invalid CSS after " @if meta": expected "{", was ".function-exist..." on line 72]:https://github.com/jeffreytse/jekyll-theme-yat/issues/177
[css conversion error with github pages]:https://github.com/jeffreytse/jekyll-theme-yat/issues/173
[如何处理 Github Action 报出的 remote: Permission to xx x denied to github-actions bot 问题]:https://www.ixiqin.com/2023/02/18/how-to-deal-with-making-the-action-report-remote-permission-denied-to-xx-x-to-making-the-actions-bot-problem/

[使用Jekyll + GitHub Pages搭建个人博客]

[GitHub Pages快速入门]


但是刚开始搭建博客时，总喜欢折腾一些好看的主题，Jekyll的主题很多，更换主题也很方便，但是还是会有一些小坑。

最主要的问题就是[GitHub Action]的配置，Jekyll可以使用在线主题，但是github默认支持的在线主题很少，如果想用其他的主题，就要修改博客项目中的默认的Action和workflow的配置，保证博客仓库有更新时，github可以自动部署博客到网页上。

解决问题的方式很简单，只是第一次遇到有点懵而已。具体参考了以下链接：

* 在这里找到自己喜欢的主题：[Jekyll主题大全]

* 我使用的主题：[Jekyll-yat主题]

* 使用以上主题时，需要使用配套的Github Action配置：[A GitHub Action to deploy the Jekyll site conveniently for GitHub Pages]

* 安装Jekyll：[Jekyll在windows上的安装]

一些疑难杂症的解决方案：
* [如何处理 Github Action 报出的 remote: Permission to xx x denied to github-actions bot 问题]

* [Error: Invalid CSS after " @if meta": expected "{", was ".function-exist..." on line 72]

* [css conversion error with github pages]