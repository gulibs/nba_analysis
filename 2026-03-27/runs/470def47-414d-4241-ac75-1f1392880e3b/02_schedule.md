# 步骤 2 — 赛程清单与完整性

## 元数据（JSON）
```json
{
  "target_date": "2026-03-27",
  "game_ids_scope": [
    7348,
    7349,
    7350
  ],
  "schedule_game_count": 3,
  "scope_game_count": 3,
  "odds_scraped_at_max": "2026-03-26T14:28:42.772346+08:00"
}
```

## 赛程表
| game_id | 客 | 主 | 开赛 | 状态 | 有赔率 | source |
|---:|---|---|---|---|---|---|
| 7348 | 尼克斯 | 黄蜂 | 2026-03-27 07:00 | scheduled | True | sporttery |
| 7349 | 鹈鹕 | 活塞 | 2026-03-27 07:00 | scheduled | True | sporttery |
| 7350 | 国王 | 魔术 | 2026-03-27 07:00 | scheduled | True | sporttery |

## 本步任务
1. 确认 **schedule 行数** 与 `scope_game_count` 是否一致；不一致则输出 **Fail Fast** 原因。
2. 列出本场次日分析对象 `game_id` 列表（与表一致）。
3. 若无法继续，输出固定句：**「盘口数据聚合失败，终止分析」** 或说明缺什么。