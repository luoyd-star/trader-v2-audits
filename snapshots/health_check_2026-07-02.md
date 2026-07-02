# Trader-v2 Daily Health Check — 2026-07-02

_Generated at 2026-07-02 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1167` last_exit=`(never`
  - uptime/rss: `01-23:21:09  52384`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1163` last_exit=`(never`
  - uptime/rss: `01-23:21:09   6720`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 481.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **481.9h old** — news_agent may have stopped producing.

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

- **package_id**: `171`
- **generated_at**: `2026-07-02 09:45:33` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#172** (conf=0.42, horizon=3d, 5 symbols incl 1 primary)
  - Claim: Mixed elevated fragility favors fading broad beta rather than adding clean risk-on longs.
  - Falsification: Regime_Dashboard shifts from mixed to confirmed risk-on while turbulence and fragility both decline for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Semiconductor relative strength can restart a durable tech-led risk-on leg.
- Cross-market nonconfirmation has improved enough to remove defensive bias.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 2 | 2 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 3/3 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| price_invalidation | 1 | $-76.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 0 total — none

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
| 2026-07-02 | $73,462 |
| 2026-07-01 | $73,462 |
| 2026-06-30 | $73,462 |
| 2026-06-29 | $73,532 |
| 2026-06-28 | $73,566 |
| 2026-06-27 | $73,563 |
| 2026-06-26 | $73,538 |
| 2026-06-25 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1009 |
| Other ERROR | 64 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._