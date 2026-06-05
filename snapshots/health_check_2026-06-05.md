# Trader-v2 Daily Health Check — 2026-06-05

_Generated at 2026-06-05 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2808` last_exit=`(never`
  - uptime/rss: `01-10:55:43  11920`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2806` last_exit=`(never`
  - uptime/rss: `01-10:55:44   7584`

---

## News-agent Freshness

- **latest folder**: `2026-06-05_09-30-09` (age: 1.9h)
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

- **package_id**: `61`
- **generated_at**: `2026-06-05 09:45:44` (age: 1.7h, today's: **YES**)
- **active_theses count**: 3 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#62** (conf=0.62, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Pre-NFP low-vol equity strength is fragile rather than clean risk-on.
  - Falsification: Equity-VIX correlations normalize toward the longer-window negative pattern while HYG/IRX pressure eases and crypto repairs trend references for two consecutive sessions.
- **#63** (conf=0.68, horizon=5d, 4 symbols incl 1 primary)
  - Claim: Crypto remains the weakest risk-on confirmation chain and should not be treated as equity beta upside.
  - Falsification: BTCUSDT and ETHUSDT both repair major trend references and stop acting as the weakest beta cluster while equity risk-on remains intact for two sessions.
- **#64** (conf=0.57, horizon=4d, 5 symbols incl 1 primary)
  - Claim: AI semis are in a phase-1 climax where AVGO shock raises de-risking risk, not chase quality.
  - Falsification: AVGO shock remains isolated while NVDA and the broader semiconductor cohort regain clean leadership alignment with QQQ for multiple sessions.

### Alternative hypotheses (rejected counter-theses)
- The market is simply in healthy risk-on continuation.
- AVGO shock is fully idiosyncratic and irrelevant to the AI cohort.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_7_PairsContrarian | 2 | 2 | 100% |

**System total: 2/2 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| time_stop | 1 | $0.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 0 total — none

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| FAILURE | FAIL | WARN | 1 |
| FAILURE | PASS | WARN | 1 |
| MIXED | PASS | PASS | 1 |

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
| 2026-06-05 | $73,538 |
| 2026-06-04 | $73,538 |
| 2026-06-03 | $73,538 |
| 2026-06-02 | $73,885 |
| 2026-06-01 | $73,495 |
| 2026-05-31 | $73,203 |
| 2026-05-30 | $73,182 |
| 2026-05-29 | $73,179 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 836 |
| Other ERROR | 279 |
| Python Traceback | 113 |
2 categories worth attention.

---

_End of snapshot._