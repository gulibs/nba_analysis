# 步骤 04d0 — game_id=7364 · ESPN 外部交叉验证（**须在下一次 04d 之前完成**）

- 对阵：`国王 vs 老鹰`
- **目的**：数据包仅含本系统同步的伤停/特征；本步要求你**主动拉取 ESPN 公开球队页**，与 **04b 走势名单、04c 特征信号** 交叉核对，补全「可能未入库」的公开信息或发现矛盾。
- **边界**：**体彩赔率与盘口事实**仍以数据包与体彩官网为准；ESPN **不**作为投注依据的唯一来源，仅作第三方 sanity check。

## 机器可读：本场两队 ESPN 链接
```json
{
  "away_team": "国王",
  "home_team": "老鹰",
  "match": "国王 vs 老鹰",
  "teams": [
    {
      "role": "away",
      "name_cn": "国王",
      "abbr": "sac",
      "slug": "sacramento-kings",
      "links": {
        "hub": "https://www.espn.com/nba/team/_/name/sac/sacramento-kings",
        "schedule": "https://www.espn.com/nba/team/schedule/_/name/sac/sacramento-kings",
        "roster": "https://www.espn.com/nba/team/roster/_/name/sac/sacramento-kings",
        "stats": "https://www.espn.com/nba/team/stats/_/name/sac/sacramento-kings",
        "depth": "https://www.espn.com/nba/team/depth/_/name/sac/sacramento-kings",
        "injuries": "https://www.espn.com/nba/team/injuries/_/name/sac/sacramento-kings",
        "transactions": "https://www.espn.com/nba/team/transactions/_/name/sac/sacramento-kings"
      }
    },
    {
      "role": "home",
      "name_cn": "老鹰",
      "abbr": "atl",
      "slug": "atlanta-hawks",
      "links": {
        "hub": "https://www.espn.com/nba/team/_/name/atl/atlanta-hawks",
        "schedule": "https://www.espn.com/nba/team/schedule/_/name/atl/atlanta-hawks",
        "roster": "https://www.espn.com/nba/team/roster/_/name/atl/atlanta-hawks",
        "stats": "https://www.espn.com/nba/team/stats/_/name/atl/atlanta-hawks",
        "depth": "https://www.espn.com/nba/team/depth/_/name/atl/atlanta-hawks",
        "injuries": "https://www.espn.com/nba/team/injuries/_/name/atl/atlanta-hawks",
        "transactions": "https://www.espn.com/nba/team/transactions/_/name/atl/atlanta-hawks"
      }
    }
  ],
  "doc_reference": "nba-projects docs/ESPN_NBA_TEAM_IMPORTANT_PAGES.md（URL 模式与 30 队 abbr/slug 速查）"
}
```

## 抓取方式与礼仪
- 使用 **HTTPS GET**（如 `curl -sL` 带合理 `User-Agent`、或 Gateway 提供的 **mcp_web_fetch / 浏览器自动化**）。**队与队之间间隔 ≥2 秒**，避免高频请求。
- **优先阅读**（验证预测方向时最相关）：`injuries` → `depth` → `stats`（球队/领袖数据）；`transactions` 用于近期阵容变动；`hub` 为总入口。
- 若某队 `links` 为 `null`：按中文队名在 [ESPN NBA 球队索引](https://www.espn.com/nba/team) 查找，或用手册 `docs/ESPN_NBA_TEAM_IMPORTANT_PAGES.md` 中的 `abbr`/`slug` 拼 URL。

## 本步任务（输出一段 Markdown，供下一步 04d 引用）
1. 对客队、主队各至少查看 **injuries** 与 **depth**（若页面不可达则说明原因）。
2. 输出 **【ESPN 外部验证摘要】**（建议 ≤500 字），包含：
   - 与 04b 伤停/名单要点是否一致，或 ESPN 是否多出/少记关键人；
   - 深度图与 04c 中首发/轮换叙述是否冲突；
   - 是否有可能影响方向判断的公开信息（一句话，**勿**编造）。
3. 若 ESPN 与数据包明显冲突：在摘要中写 **「以入库数据为准；ESPN 显示…」**，**不得**静默忽略。

## 与下一步 04d 的衔接
**下一会话的 04d（单场结论或先验分析）**须在论述中**吸收**本步摘要中的风险或补充点（可写在「风险」或「备注」）；**禁止**跳过本步已发现的重大矛盾而不回应。
**禁止**在正文中写本步骤文件名；读者看不到仓库结构。