# Zhenyu's Blog

Zhenyu 的个人博客，记录代码、学习与日常，使用 Jekyll 构建并发布于 GitHub Pages。

博客采用沉浸式头图、叠加导航和双栏文章列表：首页展示最新文章、作者简介及标签，文章页、归档页和关于页共享统一的响应式设计。

## 目录结构

```text
├─ _layouts/          页面布局
├─ _posts/            Markdown 文章
├─ assets/css/        全站样式
├─ assets/img/        首页、页面及文章头图
├─ _config.yml        站点信息与 Jekyll 配置
├─ index.html         首页
├─ archive.html       文章归档
└─ about.md           关于页面
```

## 写新文章

在 `_posts` 中新建以 `YYYY-MM-DD-title.md` 命名的文件，并添加 Front Matter：

```yaml
---
layout: post
title: "文章标题"
subtitle: "可选副标题"
date: 2026-09-05 20:00:00 +0800
description: "显示在首页的文章摘要"
tags: [分类]
header_image: /assets/img/your-cover.jpg # 可选，省略时使用全站头图
---
```

Front Matter 后直接使用 Markdown 写正文。图片建议保存在 `assets/img/`，站内路径以 `/assets/img/` 开头。

## 修改站点信息

在 `_config.yml` 中可以修改：

- `title`：博客名称
- `tagline`：首页头图副标题
- `author`：作者姓名和邮箱
- `header_image`：默认头图
- `sidebar_description`：首页侧栏介绍
- `github_username`：页脚 GitHub 链接

修改 `_config.yml` 后，需要重新启动本地预览服务才能看到变化。

## 本地预览

请先安装 Ruby 与 Bundler，然后在仓库目录运行：

```bash
bundle install
bundle exec jekyll serve
```

浏览器访问 `http://127.0.0.1:4000`。如果需要同时预览草稿或未来日期的文章，可运行：

```bash
bundle exec jekyll serve --future
```

## 发布

将修改提交并推送至 GitHub 仓库的 `main` 或 `master` 分支。启用 GitHub Pages 后，GitHub 会自动完成构建和发布：

<https://xingfenyizhen.github.io>
