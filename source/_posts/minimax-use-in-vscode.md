---
title: 如何在VSCode中使用Minimax大模型：AI辅助编程完整教程
date: 2025-11-09 12:42:28
updated: 2025-11-09 12:42:28
categories:
  - 编程工具
tags:
  - minimax
  - VSCode
  - AI编程
  - 大模型
  - Claude Code
  - 国产AI
keywords: 'Minimax教程, VSCode AI编程, M2模型, Claude Code配置, 国产大模型, AI辅助编程, 编程工具'
description: 在VSCode中使用Minimax-M2大模型的完整教程：从Minimax官网注册获取API密钥，到安装Claude Code插件、配置环境变量和模型选择，一步步实现国产大模型AI辅助编程。
author: 裕裕裕
reading_time: 6分钟
comments: true
copyright: true
abbrlink: 86547
---

# 如何在VSCode中使用Minimax大模型：AI辅助编程完整教程

<!--more-->

那么，大家最近应该都听说过minimax这一个新的国产大模型吧，他刚刚发布了M2模型，并且我感觉是唯一一个有希望追上chatgpt的国产大模型，我试用过觉得挺好用的，遂推荐给大家。

## 什么是Minimax？

以下来自网络：

MiniMax（上海稀宇科技）是2021年12月成立的中国大模型初创公司，总部位于上海，专注于研发文本、语音、视觉多模态融合的通用人工智能技术，推出ABAB系列大模型及Glow、[海螺AI](https://baike.baidu.com/item/%E6%B5%B7%E8%9E%BAAI/65707496?fromModule=lemma_inlink)等应用产品。

而M2是他们最新发布的一个大模型。

## 为什么选择Minimax？

- 🇨🇳 **国产大模型**：数据安全有保障
- 💰 **免费额度**：新用户送15元代用金
- 🚀 **性能优秀**：有望追上ChatGPT
- 🔧 **易于集成**：支持多种编程工具

## 如何在VSCode中使用Minimax-M2大模型帮助开发

Minimax支持通过API调用，那么，通过Vscode中的**Claude Code for VS Code**插件我们可以实现在开发时调用M2模型协助开发，改代码等。

话不多说，教程开始：

1. 打开Minimax官网的API开放平台[MiniMax开放平台登录页面](https://platform.minimaxi.com/login?redirect=%2Fuser-center%2Fbasic-information)注册并登录

2. 进去后完成实名认证，会送15元代用金。（不实名应该用不了的）

3. 左侧点击接口密钥，然后新建一个密钥，名称随便，密钥复制保存好，只会展现一次！！！

   ![Minimax接口密钥页面](https://photo.yu-blog.top/20251109130142560.webp)

4. 打开vscode，左侧扩展，点开

   ![VSCode扩展商店页面](https://photo.yu-blog.top/20251109130433065.webp)

5. 搜索Claude Code for VS Code插件，下载

   ![Claude Code插件搜索结果](https://photo.yu-blog.top/20251109130708990.webp)

6. 点开小齿轮，点设置

   ![VSCode插件设置页面](https://photo.yu-blog.top/20251109130831655.webp)

7. 然后Claude Code: Selected Model这一栏填MiniMax-M2

   ![Claude Code模型选择设置](https://photo.yu-blog.top/20251109130807569.webp)

8. Claude Code: Environment Variables在看到这一栏，点击在settings.json中编辑

9. 进入到这个页面，' "claudeCode.selectedModel":'里填"MiniMax-M2"

   ![settings.json配置页面](https://photo.yu-blog.top/20251109131229136.webp)

10. 然后在claudeCode.environmentVariables里填以下内容，可在这里复制[MiniMax官方文档：在 AI 编程工具里使用 M2](https://platform.minimaxi.com/docs/guides/text-ai-coding-tools#configure-minimax-api)
    
    API就填你复制的密钥
    
    ![环境变量配置示例](https://photo.yu-blog.top/20251109131553262.webp)
    
    按Ctrl+s保存，退出

11. 点击右上角的小橙球

    ![Claude Code启动界面](https://photo.yu-blog.top/20251109131735058.webp)

12. 然后就可以开心的使用了~~~///(^v^)\\\~~~

---

## 相关文章推荐

- [好用的 Python 编程工具推荐](https://yu-blog.top/63190/)
