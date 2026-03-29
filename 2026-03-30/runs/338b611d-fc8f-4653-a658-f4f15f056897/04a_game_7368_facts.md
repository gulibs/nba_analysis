# 步骤 4a — game_id=7368 · 事实与盘口（赛后流程：**已隐藏终场比分**，先验分析用）

```json
{
  "game_id": 7368,
  "match": "热火 vs 步行者",
  "away_team": "热火",
  "home_team": "步行者",
  "time": "2026-03-30 05:00",
  "date": "2026-03-30",
  "season": "2025-26",
  "status": "final",
  "rest_days": {
    "home": 2,
    "away": 2
  },
  "level_hint": 3,
  "missing_fields": [],
  "mismatch_fields": [],
  "odds_lines": {
    "dxf_over": {
      "line": 246.5,
      "odds_open": 1.66,
      "odds_close": 1.66,
      "scraped_at": "2026-03-30 00:06:06.576212+08:00"
    },
    "dxf_under": {
      "line": 246.5,
      "odds_open": 1.74,
      "odds_close": 1.74,
      "scraped_at": "2026-03-30 00:06:06.577333+08:00"
    },
    "rfsf_away": {
      "line": 9.5,
      "odds_open": 1.7,
      "odds_close": 1.7,
      "scraped_at": "2026-03-30 00:06:06.374748+08:00"
    },
    "rfsf_home": {
      "line": 9.5,
      "odds_open": 1.7,
      "odds_close": 1.7,
      "scraped_at": "2026-03-30 00:06:06.373481+08:00"
    },
    "sf_away": {
      "line": null,
      "odds_open": 1.07,
      "odds_close": 1.07,
      "scraped_at": "2026-03-30 00:06:06.051800+08:00"
    },
    "sf_home": {
      "line": null,
      "odds_open": 4.08,
      "odds_close": 4.08,
      "scraped_at": "2026-03-30 00:06:06.048394+08:00"
    },
    "sfc_away_11_15": {
      "line": null,
      "odds_open": 4.15,
      "odds_close": 4.15,
      "scraped_at": "2026-03-30 00:06:06.941307+08:00"
    },
    "sfc_away_16_20": {
      "line": null,
      "odds_open": 5.5,
      "odds_close": 5.5,
      "scraped_at": "2026-03-30 00:06:06.943728+08:00"
    },
    "sfc_away_1_5": {
      "line": null,
      "odds_open": 6.05,
      "odds_close": 6.05,
      "scraped_at": "2026-03-30 00:06:06.934945+08:00"
    },
    "sfc_away_21_25": {
      "line": null,
      "odds_open": 6.9,
      "odds_close": 6.9,
      "scraped_at": "2026-03-30 00:06:06.945752+08:00"
    },
    "sfc_away_26_plus": {
      "line": null,
      "odds_open": 5.9,
      "odds_close": 5.9,
      "scraped_at": "2026-03-30 00:06:06.947777+08:00"
    },
    "sfc_away_6_10": {
      "line": null,
      "odds_open": 3.85,
      "odds_close": 3.85,
      "scraped_at": "2026-03-30 00:06:06.939054+08:00"
    },
    "sfc_home_11_15": {
      "line": null,
      "odds_open": 21.0,
      "odds_close": 21.0,
      "scraped_at": "2026-03-30 00:06:06.942674+08:00"
    },
    "sfc_home_16_20": {
      "line": null,
      "odds_open": 29.0,
      "odds_close": 29.0,
      "scraped_at": "2026-03-30 00:06:06.944765+08:00"
    },
    "sfc_home_1_5": {
      "line": null,
      "odds_open": 9.0,
      "odds_close": 9.0,
      "scraped_at": "2026-03-30 00:06:06.937075+08:00"
    },
    "sfc_home_21_25": {
      "line": null,
      "odds_open": 55.0,
      "odds_close": 55.0,
      "scraped_at": "2026-03-30 00:06:06.946715+08:00"
    },
    "sfc_home_26_plus": {
      "line": null,
      "odds_open": 50.0,
      "odds_close": 50.0,
      "scraped_at": "2026-03-30 00:06:06.948429+08:00"
    },
    "sfc_home_6_10": {
      "line": null,
      "odds_open": 10.0,
      "odds_close": 10.0,
      "scraped_at": "2026-03-30 00:06:06.940245+08:00"
    }
  },
  "rfsf_home_line_semantics_zh": "括号内为正（+9.5）：主队「步行者」受让 9.5 分（判盘：主队得分 +9.5 与客队比；等价表述：客队「热火」让 9.5 分）。**禁止**写成「主队让 {sp:.1f} 分」——那是负线口径。判盘：让分主胜 ⟺ margin+line>0，line 为正即主队净胜分侧加 line。",
  "line_movement": {
    "spread": {
      "line": 9.5,
      "open": 1.7,
      "close": 1.7,
      "delta": 0.0
    },
    "total": {
      "line": 246.5,
      "open": 1.66,
      "close": 1.66,
      "delta": 0.0
    },
    "moneyline": {
      "home_open": 4.08,
      "home_close": 4.08,
      "delta_home": 0.0,
      "away_open": 1.07,
      "away_close": 1.07,
      "delta_away": 0.0,
      "delta": 0.0
    }
  },
  "game_phase": "pre_analysis",
  "post_workflow": {
    "phase": "before_result_reveal",
    "note": "本场已结束，但本 JSON 故意不含终场比分与 vs_lines_post。请先完成 04d 的先验分析，再在 04e 读真实结果，最后在 04f 对照复盘。"
  }
}
```

## 本步任务
仅阅读理解本 JSON；**禁止**输出完整单场分析、最终推荐方向或信心分。可写 1–2 句对盘口的事实陈述（**勿**猜终场比分）。