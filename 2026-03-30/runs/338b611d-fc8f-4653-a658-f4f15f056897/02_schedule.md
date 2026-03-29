# 步骤 2 — 赛程清单与完整性

## 元数据（JSON）
```json
{
  "target_date": "2026-03-30",
  "game_ids_scope": [
    7367,
    7368,
    7369,
    7370,
    7371,
    7372,
    7373,
    7374,
    7375
  ],
  "schedule_game_count": 9,
  "scope_game_count": 9,
  "odds_scraped_at_max": "2026-03-30T07:58:42.249031+08:00"
}
```

## 赛程表
| game_id | 客 | 主 | 客分 | 主分 | 开赛 | 状态 | 有赔率 | source |
|---:|---|---|---|---|---|---|---|---|
| 7367 | 快船 | 雄鹿 |  |  | 2026-03-30 03:30 | final | True | sporttery |
| 7368 | 热火 | 步行者 |  |  | 2026-03-30 05:00 | final | True | sporttery |
| 7369 | 国王 | 篮网 | 78 | 90 | 2026-03-30 06:00 | scheduled | True | sporttery |
| 7370 | 凯尔特人 | 黄蜂 | 101 | 90 | 2026-03-30 06:00 | scheduled | True | sporttery |
| 7371 | 魔术 | 猛龙 | 68 | 113 | 2026-03-30 06:00 | scheduled | True | sporttery |
| 7372 | 奇才 | 开拓者 | 66 | 91 | 2026-03-30 06:00 | scheduled | True | sporttery |
| 7373 | 火箭 | 鹈鹕 | 56 | 38 | 2026-03-30 07:00 | scheduled | True | sporttery |
| 7374 | 尼克斯 | 雷霆 | 11 | 14 | 2026-03-30 07:30 | scheduled | True | sporttery |
| 7375 | 勇士 | 掘金 | 0 | 0 | 2026-03-30 10:00 | scheduled | True | sporttery |

## 本步任务
1. 核对 **schedule 表行数** 与 `scope_game_count`：**仅当**二者无法对应（缺场、多场无法解释）时，说明原因并建议停止扩写；若仅为过滤导致的计数差异，说明即可，**勿**仅因此全盘否定后续分析。
2. 列出本包分析对象 `game_id` 列表（与表一致）。
3. **赔率缺口**不属本步硬终止条件；留给步骤 3–4 用 `missing_fields` 声明。
4. 有比分则与 `status` 一并作事实核对。**赛后三步**场次的比分可能在表中被隐藏至 04e，勿当作缺失。