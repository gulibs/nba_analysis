# OpenClaw 分步执行说明

## 用法
按 **文件名数字顺序** 将每个 `.md` 作为**独立一轮对话的 user prompt**（或等价输入）依次交给 OpenClaw；**不要**一次性合并全部文件，以免上下文溢出。

## 完整性（须遵守）
- **禁止**以时间、篇幅、token、上下文为由省略 `manifest.game_ids_scope` 内任一场的 `04` 步骤，或宣称「其余场次稍后」却同时写入 `meta.json` 的 `status: "completed"` / 终稿串关。
- **「分批」**仅指**多轮对话**中每场单独执行 `04_game_<id>.md`；**不是**在单轮内跳过场次。
- **写 `output/` 前自检**：是否已对 scope 内每个 `game_id` 完成单场推理？**是** → 再进入 05→06；`meta.json` 须含 `completed_game_ids`（与 scope 一致）、`finished_steps` 中逐项列出 `04_game_<id>`；`parlay_recommendation.json` 须设 `analysis_complete: true`（与 `completed` 同步）。

## 建议工作流（分步是为了控制上下文与可复核，不是「判卷」）
1. 执行 `01` → 用 **5 条以内** 要点确认已理解：场景（赛前/赛后）、Fail Fast 仅何时适用、`level_hint` 与 `missing_fields` 的含义。
2. 执行 `02` → 核对赛程与 scope；**仅当**场次无法与逐场摘要对齐时说明「无法继续」原因；否则列出 `game_id` 即可。
3. 执行 `03` → 输出全量 `level_hint` / 缺失盘汇总表（**事实表**，不因 Level 2 就判「不做分析」）。
4. 对每个 `04_game_*.md` **分别执行**（一场一轮），写单场推理；**多轮**中按 `game_id` 顺序逐场完成，勿合并多场于一轮。
5. 将各场结论**摘要**带入 `05`（或会话历史），合成串关。
6. 执行 `06` 统一排版（可选）。

## 本包元信息
- 赛程日: `2026-03-27`
- scope game_ids: `[7348, 7349, 7350]`
- 生成 UTC: `2026-03-27T14:25:30.969821+00:00`
- 赔率最近入库: `2026-03-27T05:29:59.439648+08:00`

## 数据边界
数据来自本系统库表同步，**非**体彩四页面实时抓取；与官网不一致时以 **sporttery** 为准。

## 磁盘输出 `output/`
- **`meta.json`**：`status` 为 `completed` 时须已含 `completed_game_ids`（与上列 scope 一致）、`finished_steps` 含每场 `04_game_<id>`。
- **`parlay_recommendation.json`**：须含 **`analysis_complete": true`**（与终稿一致）；可选 **`scope_game_ids`**（若填则与 scope 一致）。
- 可选 **`report_markdown_zh`**：完整 Markdown 报告正文，同步后管理端可渲染为「解析报告」（与结构化 `parlays` 并列）。
- **强烈建议 `step_transcript.json`**：每场 / 每步长文摘要（与技能 `nba-parlay-steps` 契约一致），便于「同步 → DB」后管理端展示分步与单场分析；**一键 Gateway** 若只写在对话不落盘，后端无法同步这些正文。

每条 `parlays[].legs[]` **必须**含 `game_id`，且**必须**写清对阵，任选其一或并列填写：
- **`matchup_zh`**（推荐）：如「湖人（主） vs 老鹰（客）」，与步骤 2 赛程表一致；
- 或并列 **`home_team`**、**`away_team`**（与库表 `games` 队名一致）。

**`pick_zh` 与各玩法方向**（勿仅用 `game_id` 指代场次）：大小分须写 **大分/小分** + 总分线；胜负须写 **主胜/客胜** 或 **某队胜**；胜分差须写 **主/客胜 + 档位**；让分须写 **让分主胜/让分主负** + **（客）… vs …（±线）**（详见 `01_rules.md` 第八节表格）。
