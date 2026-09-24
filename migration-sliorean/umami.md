---
title: Butterfly主题配置umami统计替代不蒜子完整教程
date: 2025-11-01 19:29:57
updated: 2025-11-01 19:29:57
categories:
  - 网站统计
tags:
  - umami
  - 网站统计
  - butterfly
  - Hexo
  - 隐私保护
keywords: 'umami教程, 网站统计, hexo统计, butterfly主题, 隐私保护, 替代不蒜子'
description: Butterfly主题配置Umami统计替代不蒜子教程：从Umami官网注册账号、添加网站、获取Website ID，到修改Butterfly主题配置文件填入serverURL和website_id，解决不蒜子加载慢的问题。
author: 裕裕裕
reading_time: 5分钟
comments: true
copyright: true
---

# Butterfly主题配置umami统计替代不蒜子完整教程

<!--more-->

## 前言

众所周知，不蒜子的官方服务加载速度非常的慢，甚至成了拖慢博客加载的"罪魁祸首"，所以，今天介绍如何使用umami来替代不蒜子的统计服务。

## 为什么选择umami？

相比不蒜子，umami有以下优势：

- ⚡ **加载速度快**：不会拖慢博客加载
- 🔒 **隐私保护**：符合GDPR政策
- 📊 **数据丰富**：提供详细的访问统计
- 🆓 **免费使用**：云端版本免费
- 🌐 **数据分享**：可以公开分享统计数据

## 什么是umami

Umami 是一个简单、快速、注重隐私、开源的分析解决方案。Umami是 Google Analytics 的一个更好的选择，因为它可以让你完全控制你的数据，并且不会侵犯用户的隐私。Umami 不使用 Cookie，不跟踪用户，且所有收集的数据都会匿名化处理，符合 GDPR 政策，资源占用很低，虽然功能简单，但分析的数据内容很丰富。

## 如何使用

因为本博客使用的是butterfly主题，所以用此主题为例（其他主题也可适当参考）

1. 首先在官网注册一个账号[Umami官网注册地址](https://cloud.umami.is/signup?ref=umami-nav-header)
   ![注册网站首页](https://photo.yu-blog.top/20251101224124835.webp)

2. 注册完账号后，登录，然后在首页中的侧边栏点击网站，然后添加网站
   ![Umami控制台首页](https://photo.yu-blog.top/20251101224413299.webp)

3. 在添加网站的页面中填写你给这个网站监测起的名字和你网站的域名（好像可以不加http：//的）
   ![添加网站页面](https://photo.yu-blog.top/20251101224729922.webp)

4. 添加完成后，当前页面会出现你添加的网站

5. 看回第二步的图片，你的网站监测项目最右边有一个笔的图案，点进去

6. 来到这个页面，复制网站ID
   ![设置页面](https://photo.yu-blog.top/20251101225540863.webp)

7. 然后打开你的butterfly主题配置文件（不是hexo的配置文件，不要弄混了喔∑( 口 ||），在里面查找umami的字样（vscode和记事本都有查找的功能）

8. 找到相关代码后，按照图片填入相关数据（serverURL照图片填，website_id填你第六步复制的ID，记得在填serverURL和website_id与数据的中间插个空格，不然会报错）
   ![Butterfly主题umami配置示例](https://photo.yu-blog.top/20251101230019476.webp)

9. 重新部署hexo博客就可以了。

10. 设置外链给用户访问，回到网站，刚刚复制ID的那个页面，往下滑有一个启用共享链接，启用，然后生成的网址可以用来给你的用户访问。

## 总结

umami统计虽然功能不多，但足够博客的日常数据分析使用了，而且还可以分享数据给用户查看。学会了快去试试吧！(●'◡'●)

## 注意事项

最后提一嘴，本站的文章全面使用cloudflare的R2存储作为图床，所以如果打不开照片的用户，可能是因为网络原因而已。

---

## 相关文章推荐

- [建站过程：从零开始搭建个人博客](https://yu-blog.top/49874/)
- [Hexo + GitHub Pages 部署博客教程](https://yu-blog.top/65417/)
