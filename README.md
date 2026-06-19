# Kou 双指数跳跃扩散模型 · 可视化

毕业设计配套的交互式网页，用浏览器本地的蒙特卡洛模拟展示 Kou (2002) 跳跃扩散模型：

- **§1 模型** — SDE 与跳跃密度公式（KaTeX 排版）
- **§2 跳跃剖析** — 非对称双指数密度，p / η₁ / η₂ 可拖动
- **§3 模拟路径** — 含跳跃标记的价格路径 + 终值分布对比纯扩散理论
- **§4 期权定价** — Kou（蒙特卡洛）vs Black–Scholes，反推隐含波动率微笑

纯前端实现（HTML + CSS + 原生 JS + [Chart.js](https://www.chartjs.org/) + [KaTeX](https://katex.org/)），不需要后端、不需要构建工具，所有公式和模拟代码都在 `index.html` 一个文件里。

## 本地预览

直接双击 `index.html`，用浏览器打开即可（Chrome / Edge / Safari 都行）。

## 部署到 GitHub Pages（零编程操作）

1. 在 GitHub 上新建一个仓库（Repository），比如叫 `kou-model-viz`。
2. 把 `index.html`（和这个 `README.md`）上传到仓库根目录：
   - 网页端操作：打开仓库页面 → **Add file → Upload files** → 把文件拖进去 → **Commit changes**。
3. 进入仓库的 **Settings → Pages**。
4. 在 **Build and deployment → Source** 选择 **Deploy from a branch**，Branch 选 `main`，目录选 `/ (root)`，点 **Save**。
5. 等 1–2 分钟，页面顶部会出现一个网址，形如：
   `https://你的用户名.github.io/kou-model-viz/`

打开这个网址就是上线后的网页，之后每次再上传新版本 `index.html` 覆盖旧文件即可自动更新。

## 内容来源

模型公式与定价框架参考 Kou, S. G. (2002), *A Jump-Diffusion Model for Option Pricing*, Management Science 48(8). 页面里的期权定价用的是蒙特卡洛模拟（而非论文中的解析解），方便对照展示，也避免了实现复杂特殊函数带来的出错风险；如果你的毕设需要展示解析解（涉及超几何函数 / Hh 函数的级数解），可以在此基础上单独加一节。

## 想自己改的话

- 颜色、字体等变量集中在 `index.html` 顶部的 `:root{...}` 和 Google Fonts 链接里。
- 每节的默认参数（S₀、σ、λ、p、η₁、η₂ 等）写在对应 `<input type="range">` 的 `value` 属性里，改那里就能换默认值。
- 蒙特卡洛模拟次数（路径数、期权定价模拟次数）写在 JS 里对应的 `nSims` / `nSteps` 常量上。
