# 步骤 4e — game_id=7367 · **真实赛果与客观盘口对照**

以下为**唯一**权威终场数据与相对入库盘口的客观字段；用于下一步复盘对照。

```json
{
  "game_id": 7367,
  "match": "快船 vs 雄鹿",
  "away_team": "快船",
  "home_team": "雄鹿",
  "rfsf_home_line_semantics_zh": "括号内为正（+15.5）：主队「雄鹿」受让 15.5 分（判盘：主队得分 +15.5 与客队比；等价表述：客队「快船」让 15.5 分）。**禁止**写成「主队让 {sp:.1f} 分」——那是负线口径。判盘：让分主胜 ⟺ margin+line>0，line 为正即主队净胜分侧加 line。",
  "status": "final",
  "game_phase": "post",
  "home_score": 113,
  "away_score": 127,
  "total_points": 240.0,
  "vs_lines_post": {
    "home_margin": -14.0,
    "total_points": 240.0,
    "dxf_line": 221.5,
    "over_hit_line": true,
    "under_hit_line": false,
    "rfsf_spread_line_home": 15.5,
    "rfsf_home_favorite_covers": true
  },
  "note": "终场客观事实与相对入库盘口的对照；用于与 04d 先验分析对照复盘，禁止据此虚构「当时一定命中」。"
}
```

## 本步任务
确认已阅读 JSON；**勿**在本步写长篇复盘（复盘在 **04f**）。