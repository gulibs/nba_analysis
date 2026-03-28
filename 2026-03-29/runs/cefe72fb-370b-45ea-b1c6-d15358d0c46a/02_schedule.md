# 步骤 2 — 赛程清单与完整性

## 元数据（JSON）
```json
{
  "target_date": "2026-03-29",
  "game_ids_scope": [
    7361,
    7362,
    7363,
    7364,
    7365,
    7366
  ],
  "schedule_game_count": 6,
  "scope_game_count": 6,
  "odds_scraped_at_max": "2026-03-28T23:19:31.067252+08:00"
}
```

## 赛程表
| game_id | 客 | 主 | 客分 | 主分 | 开赛 | 状态 | 有赔率 | source |
|---:|---|---|---|---|---|---|---|---|
| 7361 | 马刺 | 雄鹿 | 0 | 0 | 2026-03-29 03:00 | scheduled | True | sporttery |
| 7362 | 活塞 | 森林狼 | 0 | 0 | 2026-03-29 05:30 | scheduled | True | sporttery |
| 7363 | 76人 | 黄蜂 | 0 | 0 | 2026-03-29 06:00 | scheduled | False | espn |
| 7364 | 国王 | 老鹰 | 0 | 0 | 2026-03-29 07:30 | scheduled | True | sporttery |
| 7365 | 公牛 | 灰熊 | 0 | 0 | 2026-03-29 08:00 | scheduled | True | sporttery |
| 7366 | 爵士 | 太阳 | 0 | 0 | 2026-03-29 10:00 | scheduled | True | sporttery |

## 本步任务
1. 核对 **schedule 表行数** 与 `scope_game_count`：**仅当**二者无法对应（缺场、多场无法解释）时，说明原因并建议停止扩写；若仅为过滤导致的计数差异，说明即可，**勿**仅因此全盘否定后续分析。
2. 列出本包分析对象 `game_id` 列表（与表一致）。
3. **赔率缺口**不属本步硬终止条件；留给步骤 3–4 用 `missing_fields` 声明。
4. 有比分则与 `status` 一并作事实核对。**赛后三步**场次的比分可能在表中被隐藏至 04e，勿当作缺失。