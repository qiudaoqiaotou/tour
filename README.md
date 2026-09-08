# 旅行看板 · National Day 2026 Travel Dashboard

> 从上海出发的 2026 国庆（10/1–10/7）出行看板。所有产出物放在本仓库（https://github.com/qiudaoqiaotou/tour.git）。

## 这是什么

本仓库是一份 **国庆出行决策看板**，主线为「**地区 → 城市**」的漏斗，分四步：

1. **区域人流**：按「国内省份 / 周边国家」分类，展示国庆前后（9/20–10/10）的人流激增幅度，以上海（出发地）为核心。
2. **城市筛选**：从各「地区」中下沉到核心城市（**国内 + 国外统一评分**），按「人流量 C · 知名度 F · 人流稳定 S · 无营销炒作 M（各1–5）」打分。
3. **交通**：为**每个候选目的地**展示上海⇄当地的**价格曲线（9/20–10/10）与时长**，定位低溢价、便宜的走法。
4. **计划**：对最终候选给出「交通 + 住宿（住好/有特色/近景点）+ 景点 + 住宿↔景点/景点之间接驳」，国外候选附「签证/入境」说明。

## 目录结构

```
旅行看板/
├── README.md                     # 本文件：项目总览
├── skills/
│   └── trip-planner/             # 从 GitHub 引入的现成旅行规划 skill（skywain/trip-planner-skill，MIT）
├── data/                         # 分析数据（CSV）
│   ├── regions_crowd.csv         # 地区（省/国家）人流激增
│   ├── city_crowd_analysis.csv   # 城市筛选评分（国内外统一）
│   ├── transport_routes.csv      # 上海⇄各目的地 价格/时长（9/20–10/10）
│   └── hotel_itinerary.csv       # 住宿/景点/接驳/签证
├── docs/
│   ├── methodology.md            # 计算口径、筛选逻辑、数据标签说明
│   └── sources.md                # 数据来源清单（含 as-of 日期）
└── dashboard/
    └── index.html                # 可视化看板（自包含）
```

## 数据与口径

- 日期窗口：**2026-09-20 至 2026-10-10**；核心假日为 **2026 国庆（10/1–10/7）**。
- 每条数据都标注来源与 `as-of` 日期；查不到实时数据之处用代表性/历史数据估算，并明确标注「估算」。
- 数据标签约定：
  - `[official-data]`：官方统计/公告（交通部、文旅部、目的地政府等）。
  - `[report-estimate]`：OTA/机构报告与预测（携程、同程、去哪儿、飞猪、美团等）。
  - `[news-forecast]`：媒体预测/新闻。
  - `[estimate]`：无公开来源时，基于历史行为的合理推算（看板上明确标注）。
  - `[unverified]`：未能核实，需自行确认。

## 引入的 Skill

`skills/trip-planner/` 来自 GitHub 仓库 [skywain/trip-planner-skill](https://github.com/skywain/trip-planner-skill)，MIT 协议，版权归原作者所有。用途：行程规划、机票比价、酒店筛选、小时级行程与主题化渲染方法论框架。本看板的具体数据与分析由本项目自行产出。

> 为便于 git 推送，本仓库保留了该 skill 的**方法核心**（`SKILL.md`、`references/`、`scripts/`、`themes/` 渲染器代码、`README.md`、`LICENSE`），未纳入体积较大的可重建美术素材与整页示例（`themes/assets/*.webp`、`docs/showcase/*.webp`、`examples/**/*.html`）。详情见 `skills/trip-planner/README-local-note.md`；素材可到上游仓库获取。
