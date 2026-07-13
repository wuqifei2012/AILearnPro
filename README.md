# AI Research Lab — Hugo Academic Site

> 基于 Hugo Blox (Wowchemy) Academic CV 主题构建的多语言学术主页

[![Deploy to GitHub Pages](https://github.com/wuqifei2012/ai/actions/workflows/deploy.yml/badge.svg)](https://github.com/wuqifei2012/ai/actions/workflows/deploy.yml)
![Hugo](https://img.shields.io/badge/hugo-0.164%20-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 📖 项目简介

这是一个面向 AI 研究学者的个人学术主页网站，使用 [Hugo](https://gohugo.io/) 静态站点生成器和 [Hugo Blox](https://hugoblox.com/) Academic CV 主题构建。

### ✨ 核心功能

- **多语言支持** — 英文 / 中文双语内容（EN/ZH）
- **个人主页** — Hero 横幅 + 自我介绍
- **论文展示** — 按年份/标签分类的出版物列表
- **项目介绍** — 研究成果与开源项目展示
- **经历时间线** — 学术与职业经历展示
- **博客系统** — 技术文章与新闻发布
- **联系表单** — 内置联系表单与社交链接
- **站内搜索** — Pagefind 全文搜索，支持中英双语
- **暗色模式** — 系统级明暗主题切换
- **响应式设计** — 完美适配桌面与移动端

## 🚀 快速开始

### 前置要求

- [Hugo](https://gohugo.io/installation/) v0.164+ (Extended version)
- [Go](https://go.dev/dl/) 1.22+ (用于 Hugo Modules)
- [Node.js](https://nodejs.org/) 20+ (用于 Pagefind 搜索)

### 本地开发

```bash
# 1. 克隆仓库
git clone https://github.com/wuqifei2012/ai.git
cd ai

# 2. 安装前端依赖
npm install

# 3. 获取 Hugo Modules（首次需要 Go）
go mod tidy

# 4. 启动本地服务器
hugo server -D

# 5. 访问 http://localhost:1313
```

### 构建部署

```bash
# 构建生产版本
hugo --minify --gc

# 运行站内搜索索引
npx pagefind --site public --output-subdir assets/pagefind

# 输出目录: public/
```

## 📁 项目结构

```
ai/
├── .github/workflows/     # CI/CD 工作流
├── config/
│   └── _default/          # Hugo 配置文件
│       ├── hugo.yaml      # 主配置
│       ├── languages.yaml # 多语言设置
│       ├── menus.yaml     # 导航菜单
│       ├── module.yaml    # Hugo Modules
│       └── params.yaml   # 主题参数
├── content/
│   ├── en/                # 英文内容
│   │   ├── authors/       # 作者资料
│   │   ├── home/          # 首页组件
│   │   ├── post/          # 博客文章
│   │   └── ...
│   └── zh/                # 中文内容
│       ├── authors/
│       ├── home/
│       ├── post/
│       └── ...
├── data/                  # 数据文件
├── i18n/                  # 国际化翻译
│   ├── en.yaml
│   └── zh.yaml
├── themes/
│   └── wowchemy/          # Hugo Blox 主题
├── static/                # 静态资源
├── go.mod                 # Hugo Modules 依赖
├── hugo.yaml              # 项目配置（覆盖主题默认值）
├── package.json           # 前端依赖
└── README.md
```

## ⚙️ 配置说明

### 修改个人信息

编辑以下文件：

- `config/_default/params.yaml` — 网站全局参数（名称、描述、联系方式等）
- `content/en/authors/_index.md` — 英文作者资料
- `content/zh/authors/_index.md` — 中文作者资料

### 管理导航菜单

编辑 `config/_default/menus.yaml` 添加或修改菜单项。

### 添加新论文

在 `content/publication/` 下创建新的 Markdown 文件：

```yaml
---
title: "论文标题"
date: 2025-01-01
authors:
  - admin
tags:
  - Deep Learning
featured: true
---
```

### 添加新项目

在 `content/project/` 下创建新的 Markdown 文件。

## 🌐 部署

### GitHub Pages（推荐）

本项目已配置 GitHub Actions 自动部署：

1. 推送代码到 `main` 分支
2. GitHub Actions 自动构建并发布到 `gh-pages` 分支
3. 网站将在 https://wuqifei2012.github.io/ai/ 访问

### Netlify

```bash
# 安装 Netlify CLI
npm install -g netlify-cli

# 本地预览
netlify dev

# 部署
netlify deploy --prod
```

### 手动部署

```bash
hugo --minify --gc
# 将 public/ 目录上传到服务器
```

## 🛠️ 技术栈

| 技术 | 用途 |
|------|------|
| [Hugo](https://gohugo.io/) | 静态站点生成器 |
| [Hugo Blox](https://hugoblox.com/) | Academic CV 主题 |
| [Tailwind CSS v4](https://tailwindcss.com/) | 样式框架 |
| [Pagefind](https://pagefind.app/) | 站内搜索 |
| [GitHub Actions](https://github.com/features/actions) | CI/CD 自动化部署 |

## 📄 License

MIT License — 详见 [LICENSE](LICENSE) 文件。

## 🔗 相关链接

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Hugo Blox Documentation](https://docs.hugoblox.com/)
- [Academic CV Theme](https://github.com/wowchemy/starter-academic)
