# 旅行看板 · National Day 2026 Travel Dashboard

> 从上海出发的 2026 国庆（10/1–10/7）出行看板。所有产出物放在本仓库（https://github.com/qiudaoqiaotou/tour.git）。

## 这是什么

本仓库是一份 **国庆出行决策看板**，回答五个问题：

1. **人流**：中国及周边国家城市在国庆前后（9/20–10/10）的人流/出行变化，以上海（出发地）为核心。
2. **城市筛选**：从人流量出发，挑出「人不多、有一定知名度、国庆前后人流波动不大、无过度景区营销风险」的候选城市。
3. **交通**：上海 ⇄ 候选城市的往返交通方式、时间、成本（9/20–10/10 全程），并定位溢价低、价格相对便宜的走法。
4. **玩法**：候选城市的游玩空间、住宿酒店（靠近景点/有接送/特色温泉酒店优先）与旅行计划。
5. **签证**：如涉及出国，给出当地的签证办理流程与时间。

## 目录结构

```
旅行看板/
├── README.md                     # 本文件：项目总览
├── skills/
│   └── trip-planner/             # 从 GitHub 引入的现成旅行规划 skill（skywain/trip-planner-skill，MIT）
├── data/                         # 分析数据（CSV）
│   ├── city_crowd_analysis.csv   # 城市人流/出行分析
│   ├── transport_routes.csv      # 上海⇄城市交通路线（9/20–10/10）
│   └── hotel_itinerary.csv       # 住宿与行程
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
