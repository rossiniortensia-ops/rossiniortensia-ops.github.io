---
title: 使用Hexo编写并发布第一篇博客到GitHub Pages完整教程
date: 2025-09-21 12:00:00
updated: 2025-09-21 12:00:00
categories:
  - 博客教程
tags:
  - Hexo
  - 博客搭建
  - GitHub Pages
  - 教程
keywords: 'Hexo教程, 博客写作, GitHub Pages部署, Markdown教程, 博客发布, 新手教程'
description: Hexo博客写作入门教程：手把手教你用hexo new命令新建文章，讲解Markdown基础语法，使用hexo s本地预览效果，最后通过hexo g和hexo d一键部署到GitHub Pages。
author: 裕裕裕
reading_time: 5分钟
comments: true
copyright: true
---

# 使用Hexo编写并发布第一篇博客到GitHub Pages完整教程

<!--more-->

在上一篇文章中，我们已经完成了 Hexo 的基本环境搭建，并成功将站点部署到**GitHub Pages**。今天，我们就来写一篇自己的第一篇博客，并把它发布到线上。

## 本教程你将学到

- ✅ 如何新建Hexo博客文章
- ✅ 如何使用Markdown写作
- ✅ 如何本地预览博客效果
- ✅ 如何一键部署到GitHub Pages

## 1. 新建一篇文章

在 Hexo 项目根目录中执行以下命令：

```bash
hexo new post "我的第一篇博客"
```

执行后，会在 `source/_posts/` 目录下生成一个 Markdown 文件，文件名为
`我的第一篇博客.md`。

你可以用喜欢的编辑器（如 VS Code）打开它，写下文章内容。例如：

```markdown
---
title: 我的第一篇博客
date: 2025-09-21 12:00:00
tags: [随笔, Hexo]
---

这是我使用 Hexo 写的第一篇博客！

未来我会在这里分享更多技术文章。
```

------------------------------------------------------------------------

## 2. 本地预览效果

写完后，可以在本地启动 Hexo 的预览服务器：

```bash
hexo s
```

在浏览器访问 `http://localhost:4000`，就能看到新文章是否显示在主页上。

------------------------------------------------------------------------

## 3. 生成静态文件

如果预览没有问题，就可以生成静态文件：

```bash
hexo generate
```

（简写命令为 `hexo g`）

生成的文件会放在 `public/` 文件夹中。

------------------------------------------------------------------------

## 4. 部署到 GitHub Pages

最后一步就是把文章发布到线上。直接执行：

```bash
hexo deploy
```

（简写命令为 `hexo d`）

等待几秒，部署完成后，你就可以在自己的 GitHub Pages
地址中访问这篇文章了。\
比如：`https://你的GitHub用户名.github.io/`

------------------------------------------------------------------------

## 5. 小结

这就是用 Hexo 写第一篇博客并发布到 **GitHub Pages** 的完整流程。\
总结一下：

1.  `hexo new post "文章名"` → 新建文章\
2.  编辑文章内容\
3.  `hexo s` → 本地预览\
4.  `hexo g` → 生成静态文件\
5.  `hexo d` → 部署到 GitHub Pages
6.  每次发布文章前记得先用  `hexo clean` 来清理旧的缓存文件！！！
是不是很简单？🎉\
接下来你就可以根据需要，继续写更多文章，或者美化你的主题啦！

---

## 相关文章推荐

- [安装软件教程](https://yu-blog.top/10422/)
- [Hexo + GitHub Pages 部署博客教程](https://yu-blog.top/65417/)
- [建站过程：从零开始搭建个人博客](https://yu-blog.top/49874/)
