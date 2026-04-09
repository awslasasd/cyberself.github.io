# Cyberself

**CyberSelf** 是浙江大学 NSEP（学生资助对象教育实践项目）立项项目，聚焦于帮助同学们从零搭建个人网站。项目围绕**学业笔记、科研展示、竞赛项目**三大场景，通过"个人构建 → 经验总结 → 学院共建 → 实操活动"四步走路径，提供可复用的网站模板与技术教程。

模板仓库基于 MkDocs Material 构建，支持一键部署到 GitHub Pages，适合零基础同学快速上手。

**在线预览：** [https://awslasasd.github.io/cyberself/](https://awslasasd.github.io/cyberself/)

## 项目意义

在 AI 时代，个人网站已经不只是一个“展示页面”，更是学习轨迹、科研成果与实践项目的数字窗口。相比零散文档或静态简历，个人网站更适合持续更新、结构化展示和对外分享。

这个仓库存在的意义，主要包括：

- 服务 NSEP 项目的个人网站模板建设与经验沉淀
- 帮助同学们从 0 到 1 快速搭建自己的笔记或展示网站
- 支持升学、求职、项目申请等场景中的内容整理与能力展示
- 为后续教程输出、共建共享和学院公共资源沉淀提供基础模板

## 目录结构

```text
.
├─ docs/                       # 网站正文内容目录
│  ├─ Class/                   # 课程笔记、复习资料、实验记录等
│  │  ├─ Class1/               # 课程 1（example1~4.md）
│  │  ├─ Class2/               # 课程 2（example1~4.md）
│  │  └─ index.md              # 课程笔记索引页
│  ├─ Project/                 # 项目方案、开发日志、测试记录等
│  │  ├─ Project1/             # 项目 1（example1~4.md）
│  │  └─ index.md              # 项目索引页
│  ├─ Tools/                   # 工具介绍、安装配置、使用示例等
│  │  ├─ Tools1/               # 工具 1（example1~4.md）
│  │  └─ index.md              # 工具索引页
│  ├─ friends/                 # 友链数据
│  │  └─ README.md
│  ├─ img/                     # 静态图片资源
│  │  └─ favicon.ico
│  ├─ style/                   # 自定义 CSS 与 JavaScript
│  │  ├─ css/                  # counter.css, custom.css, flink.css, toc.css 等
│  │  └─ js/                   # mathjax.js, toc.js 等
│  ├─ index.md                 # 网站首页
│  └─ links.md                 # 友链页面
├─ hooks/                      # MkDocs 构建钩子
├─ overrides/                  # 主题覆盖模板
├─ .github/workflows/          # GitHub Actions 自动部署配置
├─ mkdocs.yml                  # 站点导航、主题、插件等主配置文件
├─ requirements.txt            # 项目依赖列表
└─ README.md
```

## 安装与使用

### 1. 克隆仓库

```bash
git clone https://github.com/awslasasd/cyberself.git
cd cyberself
```

### 2. 安装依赖

建议先创建虚拟环境，再安装依赖：

```bash
pip install -r requirements.txt
```

### 3. 本地预览

```bash
mkdocs serve
```

启动后可在本地访问：

```text
http://127.0.0.1:8000
```

### 4. 构建静态站点

```bash
mkdocs build
```

构建完成后，生成的静态文件通常位于 `site/` 目录。

## 使用方式建议

如果你想把它作为自己的个人网站模板来用，可以按下面的顺序修改：

1. 修改 `docs/index.md`，替换成自己的首页内容
2. 修改 `mkdocs.yml`，调整站点名称、导航栏和仓库链接
3. 在 `docs/Class/`、`docs/Project/`、`docs/Tools/` 中补充自己的内容
4. 在 `docs/style/css/` 中调整页面风格与布局细节
5. 推送到 GitHub 后，通过 GitHub Pages 进行部署

## 部署说明

本项目支持通过 **GitHub Actions + GitHub Pages** 自动部署。

- 站点配置文件：`mkdocs.yml`
- 工作流目录：`.github/workflows/`
- 默认部署目标：GitHub Pages

当仓库内容更新并推送后，Actions 会自动构建并发布网站。

## 技术栈

- [MkDocs](https://www.mkdocs.org/)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- GitHub Pages
- GitHub Actions

## 说明

本仓库当前主要用于 NSEP 项目的模板实践、学习记录与网站展示。如需继续扩展，可以优先从 `docs/` 和 `mkdocs.yml` 开始修改。
