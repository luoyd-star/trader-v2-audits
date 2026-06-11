# Trader-v2 Daily Health Check — 2026-06-11

_Generated at 2026-06-11 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1413` last_exit=`(never`
  - uptime/rss: `04-12:26:38   7696`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1408` last_exit=`(never`
  - uptime/rss: `04-12:26:38   4944`

---

## News-agent Freshness

- **latest folder**: `2026-06-11_09-30-08` (age: 1.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓

---

## Morning Batch (recent log markers)

Status of morning-batch markers in last ~5MB of log:
- `DAILY STRATEGIST START`: ✓
- `DAILY STRATEGIST END`: ✓
- `DAILY PLANNER START`: ✓
- `DAILY PLANNER END`: ✓
- `DAILY MACRO MANAGER START`: ✓
- `DAILY MACRO MANAGER END`: ✓
- `DAILY REVIEWER START`: ✓
- `DAILY REVIEWER END`: ✓

**Note**: presence in log means it ran *recently*, not necessarily today. Cross-reference with DB sections below for today-specific evidence (Strategist generated_at, plans created_at, etc.).

---

## Strategist Output (latest package)

- **package_id**: `89`
- **generated_at**: `2026-06-11 09:45:33` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#90** (conf=0.58, horizon=5d, 4 symbols incl 1 primary)
  - Claim: US mega-cap index strength is fragile until volatility and credit confirm risk-on.
  - Falsification: Risk-on is repaired if VIX falls back below the stated stress threshold, HYG reclaims EMA200, and QQQ/SPY strength broadens beyond mega-cap leadership for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Crypto weakness becomes the dominant short theme today.
- Gold or silver should be bought as monetary-debasement protection.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_3_Macro | 2 | 2 | 100% |

**System total: 3/3 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

(no closes in last 7d)

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| FAILURE | FAIL | WARN | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

(no open trades)

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-06-11 | $73,538 |
| 2026-06-10 | $73,538 |
| 2026-06-09 | $73,538 |
| 2026-06-08 | $73,538 |
| 2026-06-07 | $73,538 |
| 2026-06-06 | $73,538 |
| 2026-06-05 | $73,538 |
| 2026-06-04 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 840 |
| Other ERROR | 257 |
| Python Traceback | 81 |
2 categories worth attention.

---

_End of snapshot._