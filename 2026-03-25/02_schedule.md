# 步骤 2 — 赛程清单与完整性

## 元数据（JSON）
```json
{
  "target_date": "2026-03-26",
  "game_ids_scope": [
    7336,
    7337,
    7338,
    7339,
    7340,
    7341,
    7342,
    7343,
    7344,
    7345,
    7346,
    7347
  ],
  "schedule_game_count": 12,
  "scope_game_count": 12,
  "odds_scraped_at_max": "2026-03-25T21:18:16.836870+08:00"
}
```

## 赛程表
| game_id | 客 | 主 | 开赛 | 状态 | 有赔率 | source |
|---:|---|---|---|---|---|---|
| 7336 | 老鹰 | 活塞 | 2026-03-26 07:00 | scheduled | True | sporttery |
| 7337 | 湖人 | 步行者 | 2026-03-26 07:00 | scheduled | True | sporttery |
| 7338 | 公牛 | 76人 | 2026-03-26 07:00 | scheduled | False | espn |
| 7339 | 雷霆 | 凯尔特人 | 2026-03-26 07:30 | scheduled | True | sporttery |
| 7340 | 热火 | 骑士 | 2026-03-26 07:30 | scheduled | True | sporttery |
| 7341 | 马刺 | 灰熊 | 2026-03-26 08:00 | scheduled | True | sporttery |
| 7342 | 奇才 | 爵士 | 2026-03-26 09:00 | scheduled | True | sporttery |
| 7343 | 火箭 | 森林狼 | 2026-03-26 09:30 | scheduled | True | sporttery |
| 7344 | 独行侠 | 掘金 | 2026-03-26 10:00 | scheduled | True | sporttery |
| 7345 | 篮网 | 勇士 | 2026-03-26 10:00 | scheduled | True | sporttery |
| 7346 | 雄鹿 | 开拓者 | 2026-03-26 10:00 | scheduled | True | sporttery |
| 7347 | 猛龙 | 快船 | 2026-03-26 10:30 | scheduled | True | sporttery |

## 本步任务
1. 确认 **schedule 行数** 与 `scope_game_count` 是否一致；不一致则输出 **Fail Fast** 原因。
2. 列出本场次日分析对象 `game_id` 列表（与表一致）。
3. 若无法继续，输出固定句：**「盘口数据聚合失败，终止分析」** 或说明缺什么。