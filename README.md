# 风柳骑士个人博客（GitHub Pages）

这是一个可直接部署到 **GitHub Pages** 的静态个人博客，当前以“知乎文章分类 + 文章详情页”的结构组织内容。

## 目录结构

```text
/
├── index.html                # 首页
├── about.html                # 关于我
├── zhihu/
│   └── index.html            # 知乎文章分类页
├── articles/
│   ├── index.html            # 文章列表
│   ├── docker-network-wsl.html
│   ├── local-llm-evaluation.html
│   └── daily-log.html
└── assets/
    └── style.css             # 全站样式
```

## 本地运行方式

你可以使用任意静态服务器启动本地预览。

### 方式一：Python

```bash
python3 -m http.server 8000
```

打开：`http://localhost:8000/`

### 方式二：Node（可选）

```bash
npx serve .
```

## GitHub Pages 部署说明

1. 将代码推送到仓库默认分支（如 `main`）。
2. 进入 GitHub 仓库设置：`Settings -> Pages`。
3. 在 **Build and deployment** 中选择：
   - Source: `Deploy from a branch`
   - Branch: `main`（或你的发布分支）
   - Folder: `/ (root)`
4. 保存后等待部署完成。

若仓库名为 `liukaiyang11.github.io`，站点地址即为：
- `https://liukaiyang11.github.io/`
- `https://liukaiyang11.github.io/zhihu/`

## 后续扩展建议

- 在 `articles/` 继续新增文章页面，并在 `zhihu/index.html` 和 `articles/index.html` 增加入口。
- 未来可将文章抽离为 Markdown + 构建脚本（例如 Hexo/Hugo）来自动生成列表与标签页。
- 可在 `assets/` 中加入图片、图标与主题切换脚本，增强可读性与交互性。
