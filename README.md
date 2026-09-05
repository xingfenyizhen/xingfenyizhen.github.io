# Zhenyu's Blog

一个精简的 Jekyll 个人博客，发布于 GitHub Pages。

## 写新文章

在 `_posts` 目录中新建 `YYYY-MM-DD-title.md`，并添加：

```yaml
---
layout: post
title: 文章标题
date: 2026-09-05
description: 一句话摘要
tags: [分类]
# 可选：为文章设置独立头图
# header_image: /assets/img/your-cover.jpg
---
```

随后直接写 Markdown 正文。推送到 `main` 或 `master` 分支后，GitHub Pages 会自动构建。
