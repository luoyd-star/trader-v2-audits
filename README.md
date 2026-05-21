# trader-v2 Audits

Auto-generated daily health-check snapshots from the trader-v2 system.

Each `snapshots/health_check_<YYYY-MM-DD>.md` is produced by
`scripts/daily_health_check.py` at 11:30 JST, capturing:

- Process state
- Today's Strategist output (theses)
- Planner thesis usage rate
- Manager close-reason distribution
- Reviewer 2x2 verdicts
- Equity trend
- Open positions
- Errors & red flags

This repo is the bridge that lets a remote Claude routine read local
state for AI-driven daily interpretation.
