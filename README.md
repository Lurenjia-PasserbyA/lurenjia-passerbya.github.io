# lurenjia-passerbya.github.io

路人甲_PasserbyA（陈弘宇）的个人站点，托管在 GitHub Pages 上。

在线地址：<https://lurenjia-passerbya.github.io/>

## 结构

```
.
├── index.html          主页（纯静态，无构建步骤）
├── 404.html            404 页
├── .nojekyll           关闭 GitHub Pages 的 Jekyll 处理
└── assets/
    ├── style.css       全部样式（CSS 变量 + 自动深浅色）
    └── favicon.svg     SVG 图标
```

无第三方依赖、无 CDN、无构建步骤 —— 改完直接推送即可。

## 本地预览

```bash
python -m http.server 8000
# 打开 http://localhost:8000
```

或者直接双击 `index.html`。

## 部署

推到 `main` 分支就会自动发布。仓库名必须是 `lurenjia-passerbya.github.io`，
这样 Pages 才会挂到根路径上。

```bash
git add -A
git commit -m "更新站点"
git push
```

## 改哪里

- **文字内容**：`index.html`，各区块有 `<section id="...">` 定位
- **配色 / 字号 / 间距**：`assets/style.css` 顶部的 `:root` 变量
- **深浅色**：跟随系统。想固定成深色，删掉 `@media (prefers-color-scheme: light)` 那段即可
- **新增项目卡片**：复制 `index.html` 里任意一个 `<article class="card">` 改内容