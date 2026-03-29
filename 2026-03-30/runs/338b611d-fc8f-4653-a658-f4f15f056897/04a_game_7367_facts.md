# 步骤 4a — game_id=7367 · 事实与盘口（赛后流程：**已隐藏终场比分**，先验分析用）

```json
{
  "game_id": 7367,
  "match": "快船 vs 雄鹿",
  "away_team": "快船",
  "home_team": "雄鹿",
  "time": "2026-03-30 03:30",
  "date": "2026-03-30",
  "season": "2025-26",
  "status": "final",
  "rest_days": {
    "home": 1,
    "away": 2
  },
  "level_hint": 3,
  "missing_fields": [],
  "mismatch_fields": [],
  "odds_lines": {
    "dxf_over": {
      "line": 221.5,
      "odds_open": 1.66,
      "odds_close": 1.66,
      "scraped_at": "2026-03-30 00:06:06.569317+08:00"
    },
    "dxf_under": {
      "line": 221.5,
      "odds_open": 1.74,
      "odds_close": 1.74,
      "scraped_at": "2026-03-30 00:06:06.570743+08:00"
    },
    "rfsf_away": {
      "line": 15.5,
      "odds_open": 1.7,
      "odds_close": 1.7,
      "scraped_at": "2026-03-30 00:06:06.368686+08:00"
    },
    "rfsf_home": {
      "line": 15.5,
      "odds_open": 1.7,
      "odds_close": 1.7,
      "scraped_at": "2026-03-30 00:06:06.367456+08:00"
    },
    "sf_away": {
      "line": null,
      "odds_open": 1.12,
      "odds_close": 1.12,
      "scraped_at": "2026-03-29 22:02:40.067642+08:00"
    },
    "sf_home": {
      "line": null,
      "odds_open": 6.38,
      "odds_close": 6.38,
      "scraped_at": "2026-03-29 22:02:40.066087+08:00"
    },
    "sfc_away_11_15": {
      "line": null,
      "odds_open": 3.85,
      "odds_close": 3.85,
      "scraped_at": "2026-03-29 22:02:40.086780+08:00"
    },
    "sfc_away_16_20": {
      "line": null,
      "odds_open": 4.6,
      "odds_close": 4.6,
      "scraped_at": "2026-03-29 22:02:40.089204+08:00"
    },
    "sfc_away_1_5": {
      "line": null,
      "odds_open": 9.0,
      "odds_close": 9.0,
      "scraped_at": "2026-03-29 22:02:40.080904+08:00"
    },
    "sfc_away_21_25": {
      "line": null,
      "odds_open": 4.85,
      "odds_close": 4.85,
      "scraped_at": "2026-03-29 22:02:40.091687+08:00"
    },
    "sfc_away_26_plus": {
      "line": null,
      "odds_open": 3.2,
      "odds_close": 3.2,
      "scraped_at": "2026-03-29 22:02:40.093726+08:00"
    },
    "sfc_away_6_10": {
      "line": null,
      "odds_open": 4.75,
      "odds_close": 4.75,
      "scraped_at": "2026-03-29 22:02:40.083437+08:00"
    },
    "sfc_home_11_15": {
      "line": null,
      "odds_open": 38.0,
      "odds_close": 38.0,
      "scraped_at": "2026-03-29 22:02:40.088018+08:00"
    },
    "sfc_home_16_20": {
      "line": null,
      "odds_open": 55.0,
      "odds_close": 55.0,
      "scraped_at": "2026-03-29 22:02:40.090449+08:00"
    },
    "sfc_home_1_5": {
      "line": null,
      "odds_open": 16.0,
      "odds_close": 16.0,
      "scraped_at": "2026-03-29 22:02:40.082348+08:00"
    },
    "sfc_home_21_25": {
      "line": null,
      "odds_open": 90.0,
      "odds_close": 90.0,
      "scraped_at": "2026-03-29 22:02:40.092541+08:00"
    },
    "sfc_home_26_plus": {
      "line": null,
      "odds_open": 110.0,
      "odds_close": 110.0,
      "scraped_at": "2026-03-29 22:02:40.095699+08:00"
    },
    "sfc_home_6_10": {
      "line": null,
      "odds_open": 20.0,
      "odds_close": 20.0,
      "scraped_at": "2026-03-29 22:02:40.084735+08:00"
    }
  },
  "rfsf_home_line_semantics_zh": "括号内为正（+15.5）：主队「雄鹿」受让 15.5 分（判盘：主队得分 +15.5 与客队比；等价表述：客队「快船」让 15.5 分）。**禁止**写成「主队让 {sp:.1f} 分」——那是负线口径。判盘：让分主胜 ⟺ margin+line>0，line 为正即主队净胜分侧加 line。",
  "line_movement": {
    "spread": {
      "line": 15.5,
      "open": 1.7,
      "close": 1.7,
      "delta": 0.0
    },
    "total": {
      "line": 221.5,
      "open": 1.66,
      "close": 1.66,
      "delta": 0.0
    },
    "moneyline": {
      "home_open": 6.38,
      "home_close": 6.38,
      "delta_home": 0.0,
      "away_open": 1.12,
      "away_close": 1.12,
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