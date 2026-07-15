# Javarock 的博客

欢迎来到我的个人博客！这是一个基于 Jekyll 的 Markdown 博客。

## 座右铭

> 一边生存，一边生活

## 快速开始

### 本地开发

1. 安装依赖：
```bash
bundle install
```

2. 启动本地服务器：
```bash
bundle exec jekyll serve
```

3. 访问 `http://localhost:4000` 查看博客

### 创建新文章

在 `_posts` 目录中创建新文件，命名格式：`YYYY-MM-DD-title.md`

```markdown
---
layout: post
title: "文章标题"
date: 2026-07-15
author: Your Name
tags: [标签1, 标签2]
---

文章内容...
```

## 目录结构

```
.
├── _config.yml          # Jekyll 配置文件
├── _layouts/            # 页面布局
│   ├── default.html     # 默认布局
│   └── post.html        # 文章布局
├── _posts/              # 博客文章
├── _includes/           # 可复用组件
├── assets/              # 资源文件（CSS、图片等）
├── index.md             # 主页
├── about.md             # 关于页面
├── blog.md              # 博客页面
├── Gemfile              # Ruby 依赖
└── README.md            # 本文件
```

## 功能特性

✨ **现代设计** - 响应式布局，适配各种设备
📝 **Markdown 支持** - 用 Markdown 轻松编写文章
🏷️ **标签系统** - 为文章添加标签便于分类
📅 **文章归档** - 所有文章集中管理
🎨 **代码高亮** - 支持代码块高亮显示

## 部署到 GitHub Pages

1. 确保仓库名为 `username.github.io`
2. 推送代码到 `master` 分支
3. 访问 `https://username.github.io` 查看博客

## 许可证

MIT License

---

期待与你的交流！💬
