---
title: 博客环境搭建：Node.js、Git、Hexo安装完整指南
date: 2025-08-29 15:33:46
updated: 2025-08-29 15:33:46
categories:
  - 博客教程
tags:
  - Hexo
  - 教程
  - 博客
  - 环境搭建
  - Node.js
  - Git
keywords: 'Hexo安装教程, Node.js安装, Git安装, 博客环境搭建, 开发环境配置, 博客搭建'
description: 搭建博客必备环境安装教程：详细介绍Node.js、Git、Hexo CLI的下载安装方法，包含版本验证命令，讲解Hexo目录结构（config.yml、source、public文件夹的作用）。
author: 裕裕裕
reading_time: 4分钟
comments: true
copyright: true
abbrlink: 10422
---

# 博客环境搭建：Node.js、Git、Hexo安装完整指南

<!--more-->

本文将介绍如何安装搭建博客所需的基础软件环境，包括 Node.js、Git 和 Hexo。这是搭建博客的第一步，也是最关键的一步。

## 安装前准备

在开始安装之前，请确保：

- 💻 你的电脑有足够的存储空间（至少2GB）
- 🌐 网络连接稳定
- 👨‍💻 有管理员权限（Windows用户）

## 需要安装的软件

- [Git下载页面](https://git-scm.com/downloads)

- [Node.js下载页面](https://nodejs.org/zh-cn/download/)安装完成后，Win+R 输入 cmd 并打开，依次输入 node -v、npm -v 和 git --version 并回车，出现程序版本号即可。

- ![Node.js和Git版本检查截图](https://photo.yu-blog.top/1.webp)

- Hexo CLI(windows系统打开管理员权限的cmd)（要新建一个文件夹，这个文件夹是用来存放你博客的相关文件的，安装时先进入这个文件夹的相关目录）
  
  ```
  npm install -g hexo-cli
  ```

- 然后文件夹里会多出来很多文件，其中，config.yml是Hexo的配置文件，想要修改网站的名字等都在里面修改；source文件夹是存放你的博客文章（.md格式的）等；public文件夹是存放已经编译成html格式的博客文章。

## 常见问题

- 安装命令执行后报错
  文件夹不是空的
- 还未发现其他问题.......

## 总结

完成以上步骤后，你的博客开发环境就搭建好了！

---

## 相关文章推荐

- [Hexo + GitHub Pages 部署博客教程](https://yu-blog.top/65417/)
- [使用 Hexo 编写并发布第一篇博客](https://yu-blog.top/28146/)
- [建站过程：从零开始搭建个人博客](https://yu-blog.top/49874/)