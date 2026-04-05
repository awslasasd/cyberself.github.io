# Cyberself

一个基于 **MkDocs Material** 构建的个人学习与项目记录站点。本网站建立的核心原因，是为了服务 **NSEP 项目** 的学习、整理与展示需求：把课程资料、项目过程、工具经验和阶段成果统一沉淀到一个可持续维护的知识站点中。

## 项目背景

在 NSEP 项目的推进过程中，往往会同时产生多类内容，例如：

- 课程学习笔记
- 项目方案与开发记录
- 工具安装与使用经验
- 阶段性总结与复盘材料

如果这些内容分散在不同文档、聊天记录或本地文件夹中，后续检索、复用和展示都会比较困难。因此，这个站点的目标是：**围绕 NSEP 项目建立一个结构清晰、便于更新、方便展示的笔记与文档平台。**

## 项目目标

本仓库主要承担以下作用：

1. **记录过程**：持续整理 NSEP 项目中的学习过程与实践内容
2. **沉淀资料**：把零散内容转化为结构化文档
3. **支持展示**：通过 GitHub Pages 对外展示项目相关成果
4. **便于维护**：使用 Markdown + MkDocs 方式降低后续更新成本

## 内容结构

当前站点主要包括以下栏目：

- **Class**：课程笔记、复习资料、实验记录等
- **Project**：项目方案、开发日志、测试记录、复盘总结
- **Tools**：工具安装、配置说明、使用示例、排错经验
- **Links**：友链与相关站点跳转入口

## 目录结构

```text
.
├─ docs/                # 文档正文
│  ├─ Class/            # 课程内容
│  ├─ Project/          # 项目内容
│  ├─ Tools/            # 工具内容
│  ├─ links.md          # 友链页面
│  ├─ style/            # 自定义样式与脚本
│  └─ index.md          # 首页
├─ hooks/               # MkDocs 构建钩子
├─ overrides/           # 主题覆盖模板
├─ .github/workflows/   # GitHub Actions 部署流程
├─ mkdocs.yml           # MkDocs 主配置
└─ requirements.txt     # Python 依赖
```

## 本地运行

### 1. 安装依赖

```bash
pip install -r requirements.txt
```

### 2. 本地预览

```bash
mkdocs serve
```

默认情况下，可在本地浏览器访问：

```text
http://127.0.0.1:8000
```

### 3. 构建静态站点

```bash
mkdocs build
```

构建结果通常输出到 `site/` 目录。

## 部署方式

本项目通过 GitHub Actions 自动部署到 GitHub Pages。

- 工作流文件：`.github/workflows/static.yml`
- 站点配置文件：`mkdocs.yml`
- 当前目标地址：`https://awslasasd.github.io/cyberself/`

当你向主分支推送更新后，Actions 会自动重新构建并发布站点。

## 内容编写建议

为了让 NSEP 项目相关内容更便于积累和展示，建议：

1. 每个栏目使用独立 `index.md` 作为导航页
2. 项目过程尽量按照“背景 / 目标 / 过程 / 总结”组织
3. 工具页面尽量按照“介绍 / 安装 / 使用 / 排错”组织
4. 标题保持简洁明确，方便目录自动生成与后期检索

## 技术栈

- [MkDocs](https://www.mkdocs.org/)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- GitHub Pages
- GitHub Actions

## 维护说明

如果你后续要继续围绕 NSEP 项目扩展内容，可以优先修改以下位置：

- 新增页面：`docs/`
- 调整导航：`mkdocs.yml`
- 修改样式：`docs/style/css/`
- 修改脚本：`docs/style/js/`

## License

本仓库内容目前主要用于 NSEP 项目的学习记录与展示；如需公开分发或二次使用，请根据实际内容补充更明确的许可证说明。
