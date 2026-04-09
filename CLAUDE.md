# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a research documentation repository for an LLM-directed trading experiment. The thesis: can an LLM autonomously direct profitable short-term equity trades (common stock long positions only), with a human operator executing orders?

- **Capital:** $1,000 per position (multiple simultaneous positions allowed)
- **Holding period target:** 1–5 trading days
- **LLM authority:** Fully autonomous on trade selection, entry price, stop loss, target, and sizing
- **Human role:** Executes orders as directed; supplies pre-market data and bar data each session

Two AI models are compared in parallel, each making independent decisions on the same market data:
- `claude/` — Claude (Anthropic) session logs
- `deepseek/` — DeepSeek session logs

## Repository Structure

All content is markdown session logs — no executable code exists in this repo.

```
claude/
  experiment_history.md     # Canonical running record of all trades, lessons, rules
  YYYY-MM-DD.md             # Daily session log
deepseek/
  YYYY-MM-DD.md             # Daily session log
```

## Session Log Format

Each daily session file follows this structure:
1. **Pre-Market Context** — futures, VIX, economic calendar, geopolitical news
2. **Open Positions** — current holdings with entry, stop, target, R/R, VSA verdict
3. **VSA System Review Summary** — signals from the proprietary scanner
4. **Closed Positions Today** — filled exits with realized P/L
5. **New Orders Placed** — buy stops, stop losses placed this session
6. **Trades Considered But Rejected** — with rationale
7. **Decision Rationale** — LLM reasoning for all actions
8. **Bar Data Reviewed** — OHLCV data that informed decisions
9. **Lessons / Observations**
10. **Running Cumulative P/L**
11. **Next Session Prep**

## Technical Analysis Framework (VSA)

**Data inputs per session:** Daily OHLCV from Polygon.io, RSI, SMA-20, SMA-200, ATR, Volume Profile POC, pre-market price, morning news.

**VSA Background Strength signals:** Spring, Test, Bag Holding, Bottom Reversal, Absorption Volume

**VSA Weakness signals:** No Demand, No Supply, Churning, Two consecutive down bars on rising volume

**VSA Verdicts:** HOLD, CLOSE, TIGHTEN STOP, Target Alert (1.5R → move stop to breakeven)

**Order types used:** Buy stop with limit (momentum confirmation), stop loss (always defined pre-entry), day-only orders (no stale fills), GTC orders.

## Trading Rules (Established During Experiment)

- Minimum 1:1.5 reward-to-risk ratio on all new trades
- Do not enter on high-volatility days (Fed days, major data releases) unless thesis is exceptionally strong
- Do not chase pre-market gaps >10% — wait for pullback
- Unverifiable headline-driven entries (e.g., unconfirmed ceasefire claims) require extra confirmation
- Defensive stocks can become liabilities at macro inflection points — avoid during sector rotation
- Cash preservation is a position; not trading is a valid decision

## Experiment Context

Conducted during the US-Israel war on Iran (February 28 – April 8, 2026), with the Strait of Hormuz effectively closed. A bilateral ceasefire was reached April 8, 2026 (brokered by Pakistan). This created extreme sector rotation: Energy was the only positive S&P sector (+12%), all others negative. VIX ranged 25–31 throughout.

## Adding a New Session

When recording a new session, create `claude/YYYY-MM-DD.md` (or `deepseek/`) following the standard format above, then update `claude/experiment_history.md` with the trade outcomes and any new rules or observations.
