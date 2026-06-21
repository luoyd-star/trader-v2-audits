# Trader-v2 Daily Health Check — 2026-06-21

_Generated at 2026-06-21 11:30:00 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `08-16:13:43   7040`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `08-16:13:43   3664`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 217.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **217.9h old** — news_agent may have stopped producing.

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

- **package_id**: `127`
- **generated_at**: `2026-06-21 09:45:30` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#128** (conf=0.32, horizon=1d, 4 symbols incl 1 primary)
  - Claim: Skipped Sunday pipeline means there is no fresh directional edge; broad risk should be treated defensively until confirmation returns.
  - Falsification: A full next-session pipeline produces a structured handoff with coherent risk-on breadth across macro, indices, and at least two growth cohorts.

### Alternative hypotheses (rejected counter-theses)
- Weekend calm could justify staying fully neutral with no symbol implications.
- Mega-cap AI and semiconductor leadership may resume immediately next session.

---

## Planner Thesis Usage (today)

**No plans created today yet.** Either Planner hasn't run, or it produced 0 plans (correct behavior if no fitting thesis).

---

## Manager Close Reasons (last 7 days)

(no closes in last 7d)

---

## Reviewer 2x2 (last 7 days)

(no reviews in last 7d)

---

## Open Positions

(no open trades)

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-06-21 | $73,538 |
| 2026-06-20 | $73,538 |
| 2026-06-19 | $73,538 |
| 2026-06-18 | $73,538 |
| 2026-06-17 | $73,538 |
| 2026-06-16 | $73,538 |
| 2026-06-15 | $73,538 |
| 2026-06-14 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 855 |
| Other ERROR | 185 |
| Python Traceback | 1 |
2 categories worth attention.

---

_End of snapshot._