# 动手学大模型 · 学习平台（GitHub Pages 部署包）

基于《Dive into LLMs》仓库制作的纯静态学习平台：课程导航 / 图文教程（79 节深度讲解）/ 代码速览 / 小测验 / 学习进度跟踪。

## 文件说明

- `index.html` — 平台入口（全部界面、样式、交互内嵌，约 33KB）
- `data.js` — 11 章课程数据（讲解正文、代码、测验，约 270KB）
- `.nojekyll` — 防止 GitHub Pages 按 Jekyll 处理（保险起见）

无任何外部依赖（无 CDN、无字体、无后端），打开 `index.html` 即可本地使用。

## 部署到 GitHub Pages（两种方式任选）

### 方式一：网页上传（最快，1 分钟）

1. 打开 https://github.com/new 新建仓库，仓库名如 `dive-into-llms-learning`（Public 即可）
2. 进入仓库页面 → Add file → Upload files，把 `index.html`、`data.js`、`.nojekyll` 三个文件拖进去 → Commit
3. 仓库 Settings → Pages → Source 选 `Deploy from a branch` → 分支 `main` → 目录 `/ (root)` → Save
4. 等 1~2 分钟，访问 `https://<你的用户名>.github.io/dive-into-llms-learning/`

### 方式二：git 命令行

```bash
git init
git add index.html data.js .nojekyll
git commit -m "deploy learning platform"
git branch -M main
git remote add origin https://github.com/<你的用户名>/dive-into-llms-learning.git
git push -u origin main
# 然后按方式一的第 3 步启用 Pages
```

## 访问地址说明

- 若仓库名为 `dive-into-llms-learning`，地址为 `https://<用户名>.github.io/dive-into-llms-learning/`
- 若想让地址成为 `https://<用户名>.github.io/`，需把仓库命名为 `<用户名>.github.io` 且文件放仓库根目录

## 后续更新内容

内容更新时（例如修改讲解），只需重新上传新的 `data.js`（或 `index.html`）覆盖即可，无需重新配置。学习进度保存在浏览器 localStorage，与 WPS 在线版（https://comate.wpsgo.com/s/bPnQtQu7vR6o/）互相独立。

## 版权说明

课程内容整理自开源项目 https://github.com/Lordog/dive-into-llms （张倬胜等，公益免费），讲解为学习用途的整理与扩写，请勿用于商业牟利；转载注明出处。
