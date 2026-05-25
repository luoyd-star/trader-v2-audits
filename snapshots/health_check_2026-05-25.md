# Trader-v2 Daily Health Check — 2026-05-25

_Generated at 2026-05-25 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1294` last_exit=`(never`
  - uptime/rss: `02-12:15:54  28688`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1292` last_exit=`(never`
  - uptime/rss: `02-12:15:54  12288`

---

## News-agent Freshness

- **latest folder**: `2026-05-23_19-46-17` (age: 39.7h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **39.7h old** — news_agent may have stopped producing.

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

## Strategist Output (latest package) ⚠ NOT TODAY

- **package_id**: `11`
- **generated_at**: `2026-05-24 09:50:25` (age: 25.7h, today's: **NO — STALE**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 1 (expected ≥1)

### Active theses (the spine of today's trading)
- **#12** (conf=0.75, horizon=14d, 1 symbols incl 1 primary)
  - Claim: Gold remains in a fiscal-dominance-driven monetary identity mode, functioning as a duration proxy rather than a real-yield or safe-haven asset, sustaining its bid through the pre-N…
  - Falsification: GC=F-TLT 7d rolling correlation drops below 0.70 AND GC=F-SPY 7d rolling correlation drops below +0.50 — this would signal the fiscal-dominance duration convergence is unwinding and gold is repricing away from monetary-p…
- **#13** (conf=0.65, horizon=10d, 5 symbols incl 1 primary)
  - Claim: AI capital rotation has entered Phase 2 infrastructure scaling, directing persistent relative-strength flows into foundry and custom-silicon enablers while speculative periphery re…
  - Falsification: TSMUSDT underperforms NVDAUSDT by more than 4% over a 3-day rolling window AND TSMUSDT-NVDAUSDT 7d rolling correlation drops below 0.50 — this would signal the Phase 2 infrastructure rotation is stalling and liquidity ti…

### Alternative hypotheses (rejected counter-theses)
- Rising real yields finally snap the gold-duration divergence and reassert the traditional inverse real-yield driver, causing gold to sell off as rates rise.

---

## Planner Thesis Usage (today)

**No plans created today yet.** Either Planner hasn't run, or it produced 0 plans (correct behavior if no fitting thesis).

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| (null) | 5 | $334.0 |
| time_stop | 3 | $389.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 1 total — time_stop:1

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| INVALIDATION_EXIT | PASS | CONSISTENT | 1 |
| LOSS | OPENING_PLAN_OBEYED, HOLDING_PLAN_VIOLATED, CLOSING_PLAN_VIOLATED | PARTIAL | 1 |
| NEGATIVE | VIOLATION | VIOLATION | 1 |
| invalidation_not_respected | partial | unknown | 1 |
| profitable_but_premature | entry_and_hold_ok_exit_violation | intact | 1 |
| scratch_loss | PASS_WITH_NOTES | unknown | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A7_PairsContrarian | TSMUSDT | LONG | 397.5 | $1409 | 100.3h / 120h | 84% | (legacy) |
| A5_Contrarian | METAUSDT | LONG | 596.53 | $2200 | 75.4h / 120h | 63% | (legacy) |
| A1_Momentum | NVDAUSDT | LONG | 221.5 | $2487 | 110.8h / 240h | 46% | (legacy) |
| A1_Momentum | ARMUSDT | LONG | 265.63 | $2500 | 80.6h / 240h | 34% | (legacy) |
| A5_Contrarian | XAUUSDT | LONG | 4515.49 | $1800 | 27.1h / 120h | 23% | 7 |

Total open: 5. Pre-Phase-2 legacy (no parent_thesis_id): 4.
⚠ 1 positions ≥80% of max_hold — approaching time stop.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-05-25 | $73,170 |
| 2026-05-24 | $73,017 |
| 2026-05-23 | $72,248 |
| 2026-05-22 | $72,498 |
| 2026-05-21 | $71,789 |
| 2026-05-20 | $70,852 |
| 2026-05-19 | $70,706 |
| 2026-05-18 | $70,839 |
**Today vs yesterday: +$153**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 898 |
| Other ERROR | 459 |
| Python Traceback | 306 |
2 categories worth attention.

---

_End of snapshot._