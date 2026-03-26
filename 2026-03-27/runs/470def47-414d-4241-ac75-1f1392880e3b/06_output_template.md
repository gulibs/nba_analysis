# 步骤 6 — 最终输出排版（可选）

将最终结论按以下骨架排版（可合并进步骤 5）：

【比赛清单】总场次 N；每场 Level 与覆盖

【单场分析】…

【串关组合】…

【终止条件】若数据不具备分析价值，输出固定放弃语。

## `output/parlay_recommendation.json`（若本步写入磁盘）
- **强烈推荐** 写入可选字段 **`report_markdown_zh`**：字符串，将上述 Markdown 骨架的**完整正文**放入该字段（含标题与小节），便于分析服务同步后在管理端「解析报告」区渲染；与 `parlays` / `summary_zh` 并存。
- 每条 leg 除 `pick_zh`、`bet_type_hint` 外，**必须**含 **`matchup_zh`**（或 `home_team` + `away_team`），与步骤 2 赛程表队名一致，避免仅写盘线而不知对阵。