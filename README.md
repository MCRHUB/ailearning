# 大模型应用开发初级考试题库

基于 MkDocs + Material 主题构建的静态文档站点，包含大模型应用开发初级考试的复习资料库。

## 技术栈

- **MkDocs** - 静态站点生成器
- **mkdocs-material** - Material 主题
- **pymdown-extensions** - Markdown 扩展
- **Python 3.12** - 运行环境

## 本地运行

### 1. 环境准备

确保已安装 Python 3.8 或更高版本：

```bash
python --version
```

### 2. 安装依赖

```bash
pip install mkdocs mkdocs-material pymdown-extensions
```

### 3. 启动本地开发服务器

```bash
mkdocs serve
```

启动后访问 http://127.0.0.1:8000 即可查看站点，修改 Markdown 文件后页面会自动热更新。

### 4. 构建生产版本

```bash
mkdocs build
```

构建产物将生成在 `site/` 目录下。

## 项目结构

```
.
├── docs/                    # Markdown 源文件目录
│   ├── index.md            # 首页
│   ├── TestForecast.md     # 考试预测题
│   ├── TestPaper1.md       # 单选题库（一）
│   ├── TestPaper2.md       # 单选题库（二）
│   ├── TestPaper3.md       # 多选题库
│   └── TestProject.md      # 工程实践题
├── site/                    # 构建产物（自动生成）
├── .github/workflows/
│   └── mkdocs.yml          # GitHub Actions 部署配置
├── mkdocs.yml              # MkDocs 配置文件
└── README.md
```

## 常用命令

| 命令 | 说明 |
|------|------|
| `mkdocs serve` | 启动本地开发服务器（带热更新） |
| `mkdocs build` | 构建静态站点到 `site/` 目录 |
| `mkdocs build --strict` | 严格模式构建（遇到警告即终止） |
| `mkdocs new [dir-name]` | 创建新的 MkDocs 项目 |

## 部署

本项目已配置 GitHub Actions 自动部署到 GitHub Pages。推送代码到 `main` 或 `master` 分支即可触发部署流程。

部署配置位于 `.github/workflows/mkdocs.yml`。