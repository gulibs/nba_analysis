# 步骤 2 — 赛程清单与完整性

## 元数据（JSON）
```json
{
  "target_date": "2026-03-28",
  "game_ids_scope": [
    7351,
    7352,
    7353,
    7354,
    7355,
    7356,
    7357,
    7358,
    7359,
    7360
  ],
  "schedule_game_count": 10,
  "scope_game_count": 10,
  "odds_scraped_at_max": "2026-03-27T17:51:48.831954+08:00"
}
```

## 赛程表
| game_id | 客 | 主 | 开赛 | 状态 | 有赔率 | source |
|---:|---|---|---|---|---|---|
| 7351 | 快船 | 步行者 | 2026-03-28 07:00 | scheduled | True | sporttery |
| 7352 | 老鹰 | 凯尔特人 | 2026-03-28 07:30 | scheduled | True | sporttery |
| 7353 | 热火 | 骑士 | 2026-03-28 07:30 | scheduled | True | sporttery |
| 7354 | 火箭 | 灰熊 | 2026-03-28 08:00 | scheduled | True | sporttery |
| 7355 | 公牛 | 雷霆 | 2026-03-28 08:00 | scheduled | True | sporttery |
| 7356 | 鹈鹕 | 猛龙 | 2026-03-28 08:30 | scheduled | True | sporttery |
| 7357 | 爵士 | 掘金 | 2026-03-28 09:00 | scheduled | True | sporttery |
| 7358 | 奇才 | 勇士 | 2026-03-28 10:00 | scheduled | True | sporttery |
| 7359 | 独行侠 | 开拓者 | 2026-03-28 10:00 | scheduled | True | sporttery |
| 7360 | 篮网 | 湖人 | 2026-03-28 10:30 | scheduled | True | sporttery |

## 本步任务
1. 核对 **schedule 表行数** 与 `scope_game_count`：**仅当**二者无法对应（缺场、多场无法解释）时，说明原因并建议停止扩写；若仅为过滤导致的计数差异，说明即可，**勿**仅因此全盘否定后续分析。
2. 列出本包分析对象 `game_id` 列表（与表一致）。
3. **赔率缺口**不属本步硬终止条件；留给步骤 3–4 用 `missing_fields` 声明。