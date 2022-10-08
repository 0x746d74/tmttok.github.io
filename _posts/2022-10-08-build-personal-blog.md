---
title: 免费搭建个人博客
date: 2022-10-08 15:41:00 +0800
categories: [GitHub, Blog]
tags: [blog]
---

使用 [GitHub](https://github.com/) + [Chirpy Jekyll Theme](https://github.com/cotes2020/jekyll-theme-chirpy) 免费搭建个人博客。


## 1. 创建 GitHub 仓库

从 [Chirpy Starter](https://github.com/cotes2020/chirpy-starter/generate) 创建一个仓库，并命名为 `你的用户名.github.io`。

## 2. 设置 GitHub Pages
1. 点击仓库的【Settings】选项卡->【Pages】->【Build and deployment】下的【Source】选择【GitHub Actions】。
2. 推送任何提交到远程以触发 GitHub Actions 工作流。在仓库的【Actions】选项卡中，可以查看工作流。当构建成功后，自动部署站点。
3. 访问 GitHub 所指定网站 `https://你的用户名.github.io/`。

## 3. 设置图标

1. 使用在线工具 [Real Favicon Generator](https://realfavicongenerator.net/) 生成图标
2. 下载生成包并解压，只拷贝 *.PNG 和 *.ICO 到 `assets/img/favicons/`{: .filepath} 目录下

## 4. 设置头像

使用在线工具 [CIRCLE CROP IMAGE](https://crop-circle.imageonline.co/) 生成圆形头像，然后设置配置文件 `_config.yml` 中的 `avatar`。

## 5. 根据个人需求修改配置文件

## 6. 开启评论系统

设置配置文件 `_config.yml` 中的 `comments.active` 为 `giscus`，然后在 [giscus](https://giscus.app/zh-CN) 中选择配置，最后拷贝 `giscus` 元素值到对应配置文件 `_config.yml` 中的 `giscus` 下。