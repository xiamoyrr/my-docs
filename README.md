# 我的技术文档

基于 [MkDocs](https://www.mkdocs.org/) + Material 主题的静态文档站点，通过 GitHub Actions 自动构建并部署到 GitHub Pages。

## 目录结构

```
.
├── docs/                      # Markdown 文档
│   ├── index.md               # 主页
│   ├── about.md               # 关于
│   ├── guide.md               # 使用指南
│   └── api.md                 # API 参考
├── .github/workflows/deploy.yml   # 自动部署工作流
├── mkdocs.yml                 # MkDocs 配置
└── README.md
```

## 本地预览

```bash
pip install mkdocs-material
mkdocs serve    # http://127.0.0.1:8000
```

## 部署

推送到 `main` 分支后，GitHub Actions 会自动运行 `mkdocs build` 并把生成的 `site/` 目录
发布到 `gh-pages` 分支。站点地址：`https://<用户名>.github.io/<仓库名>/`。
