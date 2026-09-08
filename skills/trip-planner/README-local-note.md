# 本地化说明（README-local-note）

本目录是从 GitHub 仓库 [skywain/trip-planner-skill](https://github.com/skywain/trip-planner-skill)（MIT，版权归原作者）引入的旅行规划 skill。

为确保持续可用的**方法论核心**（`SKILL.md`、`references/`、`scripts/`、`themes/` 渲染器代码、`README.md`、`LICENSE`）完整保留，同时让本仓库可被 git 正常推送，**未纳入**体积较大的可重建美术素材与示例页面：

- `themes/assets/**/*.webp`（主题图片库，含 `stock/`、`portal/`）——约数十 MB，属可重建资产。
- `docs/showcase/*.webp`（展示图）。
- `examples/**/*.html`（内嵌 base64 图片的整页渲染示例）。

如需这些素材，请从上游仓库获取：
https://github.com/skywain/trip-planner-skill

完整素材与示例仅影响「主题化渲染 / 展示页」这一可选环节；本 skill 的**旅行规划、行程编排、机票/酒店比价、验证规则、脚本工具**均不依赖它们，可直接使用。
