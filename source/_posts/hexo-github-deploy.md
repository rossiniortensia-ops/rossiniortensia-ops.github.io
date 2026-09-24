---
title: Hexo + GitHub Pages 部署博客完整教程（2025最新版）
date: 2025-08-31 22:45:38
updated: 2025-08-31 22:45:38
categories:
  - 博客教程
tags:
  - Hexo
  - GitHub
  - 部署
  - 教程
  - 博客搭建
keywords: 'Hexo部署, GitHub Pages教程, 博客搭建, SSH配置, 静态博客, 免费博客, Hexo教程'
description: 2025年最新版Hexo+GitHub Pages部署教程：从SSH密钥配置、GitHub连接测试、Hexo配置文件修改、部署插件安装到一键部署，详解每个步骤，附常见问题解决方案。
author: 裕裕裕
reading_time: 10分钟
comments: true
copyright: true
abbrlink: 65417
---

# Hexo + GitHub Pages 部署博客完整教程（2025最新版）

<!--more-->

在搭建个人博客的过程中，**Hexo + GitHub Pages** 是最受欢迎的方案之一。本文将详细介绍如何从零开始完成配置与部署，帮助你快速拥有一个属于自己的在线博客。

## 本教程适合人群

- 🎯 零基础新手，想搭建个人博客
- 🎯 有一定编程基础，想快速上手
- 🎯 想要免费、稳定的博客托管方案

## 你将学到什么

- ✅ 如何配置SSH连接GitHub
- ✅ 如何安装和配置Hexo
- ✅ 如何一键部署博客到GitHub Pages
- ✅ 常见问题的解决方案

## 目录

- [一、使用 Git 连接 GitHub 账户](#一使用-git-连接-github-账户推荐-ssh-方式)
- [二、配置 Hexo 与 GitHub 关联](#二配置-hexo-与-github-关联)
- [三、发布博客到 GitHub Pages](#三发布博客到-github-pages)
- [四、常见问题与解决方法](#四常见问题与解决方法)

## 一、使用 Git 连接 GitHub 账户（推荐 SSH 方式）

在部署过程中，我们需要让本地环境能够与 GitHub 通信。推荐使用 **SSH
连接**，避免每次都输入账号密码。

1. 打开命令行（Windows 用 Git Bash 或 cmd，macOS/Linux
   用终端），输入以下命令生成 SSH 密钥：
   
   ```bash
   ssh-keygen -t rsa -C "your_email@example.com"
   ```
   
   > 注意：将 `your_email@example.com` 替换为你注册 GitHub 的邮箱。

2. 按 3 次回车（默认路径、默认不设密码），密钥文件会保存在：
   
   - Windows: `C:\Users\你的用户名\.ssh`\
   - macOS/Linux: `~/.ssh`

3. 找到 **id_rsa.pub** 文件（公钥），用文本编辑器打开并复制全部内容。

4. 登录 GitHub → 右上角头像 → **Settings** → **SSH and GPG keys** →
   **New SSH key**。
   
   - Title 填一个容易记的名字（如 "My PC"）
   - Key 粘贴公钥内容 → 点击 **Add SSH key**
     ![GitHub SSH密钥添加页面](https://photo.yu-blog.top/2.webp)

5. 测试是否成功连接：
   
   ```bash
   ssh -T git@github.com
   ```
   
   输入 `yes` 后，若提示：
   
       Hi 用户名! You've successfully authenticated...
   
   即表示 SSH 配置成功。

------------------------------------------------------------------------

## 二、配置 Hexo 与 GitHub 关联

完成 GitHub 连接后，我们需要修改 Hexo 配置文件，实现自动部署。

### 1. 修改 `_config.yml`

在博客根目录下找到 `_config.yml`，滚动到文件末尾，修改 **deploy** 部分：

```yaml
deploy:
  type: git
  repo: https://github.com/用户名/用户名.github.io.git   # 仓库地址（可用 SSH：git@github.com:用户名/用户名.github.io.git）
  branch: main   # GitHub 仓库默认分支，新版是 main，旧版可能是 master
```

### 2. 安装部署插件

确保在博客目录下执行：

```bash
npm install hexo-deployer-git --save
```

### 3. 配置 Git 用户信息

在命令行里设置全局 Git 用户信息（首次配置时需要）：

```bash
git config --global user.name "yourname"
git config --global user.email "youremail@example.com"
```

检查是否配置正确：

```bash
git config user.name
git config user.email
```

------------------------------------------------------------------------

## 三、发布博客到 GitHub Pages

完成配置后，就可以将本地博客推送到 GitHub Pages 了。

1. **新建测试文章**（可选）：
   
   ```bash
   hexo new "我的第一篇 Hexo 博客"
   ```
   
   文章会保存在 `source/_posts` 文件夹下（Markdown 格式）。
   
   ![Hexo新建文章命令执行结果](https://photo.yu-blog.top/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-11-01%20193029.webp)

2. **生成静态文件**：
   
   ```bash
   hexo clean   # 清理旧文件
   hexo g       # 等同于 hexo generate，生成新静态页面
   ```
   
   ![命令运行截图](https://photo.yu-blog.top/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-11-01%20193210.webp)

3. **部署到 GitHub**：
   
   ```bash
   hexo d   # 等同于 hexo deploy
   ```
   
   如果是 SSH 方式，不需要输入账号密码。
   
   ![命令运行截图](https://photo.yu-blog.top/20251101193652743.webp)

4. **访问博客**：\
   等待 1\~5 分钟，打开浏览器输入：
   
       https://用户名.github.io
   
   即可访问。

------------------------------------------------------------------------

## 四、常见问题与解决方法

1. **找不到 GitHub 用户名？**\
   打开 GitHub 个人主页，网址里 `/` 后面的就是你的用户名，例如：\
   `https://github.com/octocat` → 用户名是 `octocat`。
   ![GitHub用户名位置示例](https://photo.yu-blog.top/3.webp)

2. **Git 配置问题**\
   设置 Git 用户时，注意 `user.name` 和 `"yourname"`
   之间要有空格，例如：
   
   ```bash
   git config --global user.name "yourname"
   git config --global user.email "youremail@example.com"
   ```

3. **上传失败或连接超时**\
   可能需要配置网络代理，或者使用 SSH 方式连接 GitHub。

------------------------------------------------------------------------

## 总结

至此，你已经学会了：

- 通过 **SSH 连接 GitHub**\
- 修改 Hexo 配置，实现自动部署\
- 使用 `hexo g` 和 `hexo d` 将博客推送到 GitHub Pages

这样，你就拥有了一个完全属于自己的个人博客！ 🚀

---

## 相关文章推荐

- [安装软件教程](https://yu-blog.top/10422/)
- [使用 Hexo 编写并发布第一篇博客](https://yu-blog.top/28146/)
- [建站过程：从零开始搭建个人博客](https://yu-blog.top/49874/)
