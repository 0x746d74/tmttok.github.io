---
title: 免费搭建个人图床
date: 2022-10-08 13:51:00 +0800
categories: [GitHub, PicHost]
tags: [pichost]
---

使用 [GitHub](https://github.com/) + [jsDelivr](https://www.jsdelivr.com/) 免费搭建高速稳定的图床，使用 [PicGo](https://github.com/Molunerfinn/PicGo) 上传图片。


## 1. 创建 GitHub 仓库

创建一个公开仓库，上传图片到该仓库中，可以使用浏览器端上传，也可以使用 Git 进行上传。

上传后可以在浏览器通过地址 `https://raw.githubusercontent.com/你的用户名/你的仓库名/main/文件路径` 来访问所上传的图片。

## 2. 使用 jsDelivr 进行 CDN 加速

由于 GitHub 在国内访问很慢，甚至经常打不开，这时候就可以用 jsDelivr 进行免费加速。

使用方法也非常的简单，直接在浏览器通过地址 `https://cdn.jsdelivr.net/gh/你的用户名/你的仓库名@发布的版本号/文件路径` 就可以访问 GitHub 上的图片，其中 `@发布的版本号` 可以直接省略，默认加载最新版本，即直接可以简写为 `https://cdn.jsdelivr.net/gh/你的用户名/你的仓库名/文件路径`

## 3. 使用 PicGo 上传图片

由于使用传统的方法向 GitHub 上传图片太麻烦了，所以推荐一个开源图床工具 PicGo 来作为我们的图片上传工具。

下载并安装 PicGo，打开 PicGo，找到【图床设置】->【GitHub图床】 进行设置：
- 设定仓库名【必填】：填写你的用户名/你的仓库名
- 设定分支名【必填】：填写main
- 设定Token【必填】：在 GitHub 主页点击自己头像后，依次选择【Settings】->【Developer settings】->【Personal access tokens】->【Generate new token】，填写 Note 描述，设置过期时间Expiration为永不过期 No expiration，勾选【repo】，然后点击下方的【Generate token】生成一个Token，这个Token只会显示一次，自行保存，然后复制到 PicGo 中。
- 指定存储路径【选填】：填写图片要存储的路径，比如填【img/】，这样就会在仓库下创建一个名为 img 的文件夹，图片将会储存在此文件夹中。
- 设定自定义域名【选填】：图片上传后，PicGo 会按照【自定义域名+上传的图片名】的方式生成访问链接，放到剪贴板上，因为我们要使用 jsDelivr 进行加速，因此这里设置为 `https://cdn.jsdelivr.net/gh/你的用户名/你的仓库名`。

设置完成后，可以在【上传区】将图片上传，上传成功后，会自动复制URL。