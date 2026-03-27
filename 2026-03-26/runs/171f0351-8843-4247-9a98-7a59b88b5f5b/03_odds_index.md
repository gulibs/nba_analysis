# 步骤 3 — 盘口覆盖索引（全量）

以下 `level_hint` 由本系统库内赔率行推断，**须与体彩四页面核对**。
```json
[
  {
    "game_id": 7336,
    "match": "老鹰 vs 活塞",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7337,
    "match": "湖人 vs 步行者",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7338,
    "match": "公牛 vs 76人",
    "level_hint": 0,
    "missing_fields": [
      "sf",
      "rfsf",
      "dxf",
      "sfc"
    ],
    "mismatch_fields": []
  },
  {
    "game_id": 7339,
    "match": "雷霆 vs 凯尔特人",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7340,
    "match": "热火 vs 骑士",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7341,
    "match": "马刺 vs 灰熊",
    "level_hint": 2,
    "missing_fields": [
      "sf",
      "sfc"
    ],
    "mismatch_fields": []
  },
  {
    "game_id": 7342,
    "match": "奇才 vs 爵士",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7343,
    "match": "火箭 vs 森林狼",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7344,
    "match": "独行侠 vs 掘金",
    "level_hint": 2,
    "missing_fields": [
      "sf"
    ],
    "mismatch_fields": []
  },
  {
    "game_id": 7345,
    "match": "篮网 vs 勇士",
    "level_hint": 2,
    "missing_fields": [
      "sf"
    ],
    "mismatch_fields": []
  },
  {
    "game_id": 7346,
    "match": "雄鹿 vs 开拓者",
    "level_hint": 2,
    "missing_fields": [
      "sf"
    ],
    "mismatch_fields": []
  },
  {
    "game_id": 7347,
    "match": "猛龙 vs 快船",
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