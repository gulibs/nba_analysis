# 步骤 3 — 盘口覆盖索引（全量）

以下 `level_hint` 由本系统库内赔率行推断，**须与体彩四页面核对**。
```json
[
  {
    "game_id": 7348,
    "match": "尼克斯 vs 黄蜂",
    "level_hint": 2,
    "missing_fields": [
      "sfc"
    ],
    "mismatch_fields": []
  },
  {
    "game_id": 7349,
    "match": "鹈鹕 vs 活塞",
    "level_hint": 3,
    "missing_fields": [],
    "mismatch_fields": []
  },
  {
    "game_id": 7350,
    "match": "国王 vs 魔术",
    "level_hint": 2,
    "missing_fields": [
      "sf"
    ],
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
输出 Markdown 表：每行 game_id | match | level_hint | missing_fields | mismatch_fields | 是否建议进入深度分析（是/否）。
若存在无法接受的 mismatch 或 Level0 占比异常，说明是否终止。