# 个人文档
## 这是个人存放的文档

根据您的问题，您想了解如何部署从 `f/awesome-chatgpt-prompts` 仓库拉取下来的代码。<cite/>

## 部署方式

这个项目使用 Jekyll 静态网站生成器，有两种主要的部署方式：

### 1. 自动部署（推荐）

项目已经配置了 GitHub Actions 自动部署流程 [1](#0-0) 。当您推送代码到 `main` 分支时，会自动触发部署：

- 设置 Ruby 3.2 环境 [2](#0-1) 
- 安装依赖并构建 Jekyll 网站 [3](#0-2) 
- 自动部署到 GitHub Pages [4](#0-3) 

### 2. 本地部署

如果您想在本地运行和测试：

1. **安装 Ruby 3.2** [5](#0-4) 
2. **安装依赖**：
   ```bash
   gem update --system
   bundle update --bundler
   bundle install
   ``` [6](#0-5) 

3. **构建并运行网站**：
   ```bash
   bundle exec jekyll build
   bundle exec jekyll serve
   ``` [7](#0-6) 

## 网站架构

该项目是一个 Jekyll 静态网站，主要组件包括：
- 布局模板 `_layouts/default.html` [8](#0-7) 
- JavaScript 交互逻辑 `script.js` [9](#0-8) 
- 自动化的 CSV 验证和发布流程 [10](#0-9) 

## Notes

这个项目的部署流程已经完全自动化，您只需要 fork 仓库并推送到 main 分支即可。GitHub Actions 会自动处理构建和部署到 GitHub Pages 的整个过程。如果您需要自定义域名或其他配置，可以参考 Jekyll 和 GitHub Pages 的相关文档。

Wiki pages you might want to explore:
- [Website Architecture (f/awesome-chatgpt-prompts)](/wiki/f/awesome-chatgpt-prompts#3.1)
- [GitHub Automation (f/awesome-chatgpt-prompts)](/wiki/f/awesome-chatgpt-prompts#5)
