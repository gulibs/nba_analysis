# 步骤 3 — 盘口覆盖索引（全量）

以下 `level_hint` 由本系统库内赔率行推断，**须与体彩四页面核对**。
```json
[
  {
    "game_id": 7367,
    "match": "快船 vs 雄鹿",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7368,
    "match": "热火 vs 步行者",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7369,
    "match": "国王 vs 篮网",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7370,
    "match": "凯尔特人 vs 黄蜂",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7371,
    "match": "魔术 vs 猛龙",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7372,
    "match": "奇才 vs 开拓者",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7373,
    "match": "火箭 vs 鹈鹕",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7374,
    "match": "尼克斯 vs 雷霆",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7375,
    "match": "勇士 vs 掘金",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  }
]
```

## 官方四玩法入口
- 胜负 https://www.sporttery.cn/jc/jsq/lqsf/
- 让分 https://www.sporttery.cn/jc/jsq/lqrfsf/
- 大小分 https://www.sporttery.cn/jc/jsq/lqdxf/
- 胜分差 https://www.sporttery.cn/jc/jsq/lqsfc/

## 本步任务
输出 Markdown 表：每行 game_id | match | level_hint | missing_fields | mismatch_fields | **可讨论的玩法范围**（例如：缺 sfc 则注明「胜分差未入库，其余可讨论」）。
**勿**用「Level 2 = 不建议分析」这类表述；`level_hint` 仅表示入库覆盖度。若某场 Level 0 或 mismatch 严重，单独说明该场限制即可，不必因单场问题否定 scope 内全部场次。