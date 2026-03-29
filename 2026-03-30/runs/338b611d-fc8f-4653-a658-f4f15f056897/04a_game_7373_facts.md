# 步骤 4a — game_id=7373 · 事实与盘口（仅数据）

```json
{
  "game_id": 7373,
  "match": "火箭 vs 鹈鹕",
  "away_team": "火箭",
  "home_team": "鹈鹕",
  "time": "2026-03-30 07:00",
  "date": "2026-03-30",
  "season": "2025-26",
  "status": "live",
  "home_score": 38,
  "away_score": 57,
  "total_points": 95.0,
  "game_phase": "pre",
  "vs_lines_post": null,
  "rest_days": {
    "home": 2,
    "away": 2
  },
  "level_hint": 3,
  "missing_fields": [],
  "mismatch_fields": [],
  "odds_lines": {
    "dxf_over": {
      "line": 228.5,
      "odds_open": 1.66,
      "odds_close": 1.66,
      "scraped_at": "2026-03-30 00:06:06.609494+08:00"
    },
    "dxf_under": {
      "line": 228.5,
      "odds_open": 1.74,
      "odds_close": 1.74,
      "scraped_at": "2026-03-30 00:06:06.610811+08:00"
    },
    "rfsf_away": {
      "line": 6.5,
      "odds_open": 1.7,
      "odds_close": 1.7,
      "scraped_at": "2026-03-30 00:06:06.404910+08:00"
    },
    "rfsf_home": {
      "line": 6.5,
      "odds_open": 1.7,
      "odds_close": 1.7,
      "scraped_at": "2026-03-30 00:06:06.404023+08:00"
    },
    "sf_away": {
      "line": null,
      "odds_open": 1.16,
      "odds_close": 1.16,
      "scraped_at": "2026-03-30 00:06:06.075254+08:00"
    },
    "sf_home": {
      "line": null,
      "odds_open": 3.15,
      "odds_close": 3.15,
      "scraped_at": "2026-03-30 00:06:06.074443+08:00"
    },
    "sfc_away_11_15": {
      "line": null,
      "odds_open": 5.4,
      "odds_close": 5.4,
      "scraped_at": "2026-03-30 00:06:07.005344+08:00"
    },
    "sfc_away_16_20": {
      "line": null,
      "odds_open": 7.5,
      "odds_close": 7.5,
      "scraped_at": "2026-03-30 00:06:07.006548+08:00"
    },
    "sfc_away_1_5": {
      "line": null,
      "odds_open": 4.25,
      "odds_close": 4.25,
      "scraped_at": "2026-03-30 00:06:07.002354+08:00"
    },
    "sfc_away_21_25": {
      "line": null,
      "odds_open": 11.0,
      "odds_close": 11.0,
      "scraped_at": "2026-03-30 00:06:07.007845+08:00"
    },
    "sfc_away_26_plus": {
      "line": null,
      "odds_open": 10.0,
      "odds_close": 10.0,
      "scraped_at": "2026-03-30 00:06:07.009504+08:00"
    },
    "sfc_away_6_10": {
      "line": null,
      "odds_open": 3.9,
      "odds_close": 3.9,
      "scraped_at": "2026-03-30 00:06:07.003987+08:00"
    },
    "sfc_home_11_15": {
      "line": null,
      "odds_open": 13.0,
      "odds_close": 13.0,
      "scraped_at": "2026-03-30 00:06:07.005959+08:00"
    },
    "sfc_home_16_20": {
      "line": null,
      "odds_open": 22.0,
      "odds_close": 22.0,
      "scraped_at": "2026-03-30 00:06:07.007161+08:00"
    },
    "sfc_home_1_5": {
      "line": null,
      "odds_open": 5.95,
      "odds_close": 5.95,
      "scraped_at": "2026-03-30 00:06:07.003162+08:00"
    },
    "sfc_home_21_25": {
      "line": null,
      "odds_open": 38.0,
      "odds_close": 38.0,
      "scraped_at": "2026-03-30 00:06:07.008581+08:00"
    },
    "sfc_home_26_plus": {
      "line": null,
      "odds_open": 44.0,
      "odds_close": 44.0,
      "scraped_at": "2026-03-30 00:06:07.010162+08:00"
    },
    "sfc_home_6_10": {
      "line": null,
      "odds_open": 6.5,
      "odds_close": 6.5,
      "scraped_at": "2026-03-30 00:06:07.004728+08:00"
    }
  },
  "rfsf_home_line_semantics_zh": "括号内为正（+6.5）：主队「鹈鹕」受让 6.5 分（判盘：主队得分 +6.5 与客队比；等价表述：客队「火箭」让 6.5 分）。**禁止**写成「主队让 {sp:.1f} 分」——那是负线口径。判盘：让分主胜 ⟺ margin+line>0，line 为正即主队净胜分侧加 line。",
  "line_movement": {
    "spread": {
      "line": 6.5,
      "open": 1.7,
      "close": 1.7,
      "delta": 0.0
    },
    "total": {
      "line": 228.5,
      "open": 1.66,
      "close": 1.66,
      "delta": 0.0
    },
    "moneyline": {
      "home_open": 3.15,
      "home_close": 3.15,
      "delta_home": 0.0,
      "away_open": 1.16,
      "away_close": 1.16,
      "delta_away": 0.0,
      "delta": 0.0
    }
  }
}
```

## 本步任务
仅阅读理解本 JSON；**禁止**输出完整单场分析、最终推荐方向或信心分。可写 1–2 句对盘口与 `game_phase` 的事实陈述。