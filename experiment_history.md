# LLM-DIRECTED SHORT-TERM TRADING EXPERIMENT
## Complete History & Context Document
### Started: 2026-03-13 | Repository Initialized: 2026-03-31

---

## 1. EXPERIMENT PARAMETERS

**Objective:** Determine whether an LLM (Claude, Anthropic) can autonomously direct profitable short-term equity trades using common stock long positions only, with a human operator executing orders.

**Capital:** $1,000 per position (may deploy multiple positions simultaneously)
**Instruments:** Common stock, long positions only (no options, no shorting)
**Holding Period Target:** 1–5 trading days per position
**Risk Tolerance:** Moderate (~$100–150 max risk per position)
**Decision Authority:** LLM is fully autonomous on trade selection, entry, exit, and sizing. Human executes orders as directed.
**Data Inputs:**
- Daily bar data (OHLCV + buy/sell pressure %) from Polygon.io
- VSA (Volume Spread Analysis) position reviews from proprietary scanning system
- Key technicals: RSI, SMA, distance from 200d SMA, ATR, Volume Profile POC
- Morning economic/geopolitical news via web search
- Premarket prices provided by human operator

**Order Types Used:**
- Buy stop with limit (confirms momentum before entry)
- Stop loss (always defined before entry)
- Day-only orders (prevents stale fills in changed conditions)

**VSA System Signals Referenced:**
- Background Strength: Spring, Test, Bag Holding, Bottom Reversal, Absorption Volume
- Weakness Signals: No Demand, No Supply, Churning, Two consecutive down bars on rising volume
- Verdicts: HOLD, CLOSE, TIGHTEN STOP
- 1.5R Target alerts with breakeven stop recommendation

---

## 2. MARKET CONTEXT: MARCH 2026

The experiment took place during the US-Israel war on Iran, which began February 28, 2026. Key market dynamics:

- **Strait of Hormuz** effectively closed by Iran, disrupting ~20% of global oil supply
- **Oil prices** surged from ~$60 (pre-war) to $100+ (Brent peaked near $120)
- **S&P 500** entered correction, falling from January ATH of 7,002 to below 6,400
- **Fed** held rates at 3.50-3.75% on March 18, dot plot showed only one cut in 2026
- **PPI** came in hot at 0.7% vs 0.3% expected (March 18)
- **Q4 GDP** revised sharply down to 0.7% from 1.4% (reported March 13)
- **VIX** ranged from 25-31 throughout the period
- **Headlines** dominated by Trump ceasefire claims (often contradicted by Iran), oil price swings, and recession fears
- **Energy** was the only positive S&P 500 sector for the month (+12%), all others negative
- **Dow and Nasdaq** entered correction territory by month end
- **Consumer sentiment** (UMich) fell to 53.3, inflation expectations rose to 3.8% one-year

---

## 3. COMPLETE TRADE LOG

### Trade #1: DVN (Devon Energy) — WIN ✅

**Status:** CLOSED
**Entry:** 22 shares @ $46.05 on 2026-03-13 (buy stop triggered)
**Exit:** 22 shares @ ~$49.35 (market sell at open) on 2026-03-25
**Days Held:** 12 (original plan: 1-5 days)
**P/L:** +$72.60 (+7.2%)

**Thesis:** Long US shale oil producer as proxy for elevated crude prices driven by Iran/Strait of Hormuz crisis. DVN selected over OXY (RSI 73.8, overextended), CF (RSI 81.9, parabolic), CVX (RSI 71.2, chasing), and XOM (RSI 60.9, lower dollar upside due to share price). DVN offered RSI 64.9, clear POC support at $44.48, and 22 shares on $1,000 for meaningful dollar exposure.

**Entry Context:**
- DVN premarket: $45.79 (ex-dividend date, $0.24 adjustment)
- WTI crude: ~$96/barrel, Brent: $100+
- S&P 500 at 2026 lows, broad market in correction
- Strait of Hormuz effectively closed, Iran's new supreme leader pledged to maintain closure
- Piper Sandler PT raised to $67 from $59
- Pending Coterra merger to double production capacity

**Order Details:**
- Buy stop: $46.05 | Buy stop limit: $46.25
- Initial stop: $44.45 (below POC at $44.48)
- Target: $49.00

**Stop Trail History:**
| Date | Day | Stop Level | Reasoning |
|------|-----|-----------|-----------|
| 3/13 | 1 | $44.45 | Initial — below POC at $44.48 |
| 3/18 | 5 | $45.25 | Trail up — below 3/12 low of $45.26, reduces risk from $35 to $18. Fed day protection. |
| 3/20 | 7 | $46.05 | Breakeven — per VSA 1.5R target hit alert ($48.45). Risk-free trade. |
| 3/24 | 11 | $47.50 | Trail up — locks in $32 minimum profit. Yesterday's open. Ceasefire risk. |

**Key Events During Hold:**
- 3/16: Oil surged further on Kharg Island strikes. DVN gapped up.
- 3/18: Fed held rates, PPI hot at 0.7%. Powell said inflation progress "not as much as hoped." Market sold off 1.36%.
- 3/19: DVN hit $49.83 intraday — first touch of target zone. Did not sell (mistake in retrospect).
- 3/20: Distribution day — 56M volume (3x normal), 81% sell pressure. Warning sign not acted on.
- 3/23: Trump announced 5-day ceasefire on Iranian energy infrastructure. Oil crashed 8%. DVN dropped to $46.80 intraday (within $0.75 of breakeven stop) before recovering to close $48.49.
- 3/24: DVN rallied to $50.70 high, closed $50.27. Target exceeded.
- 3/25: Sold at market open ~$49.35. Decision driven by thesis reversal (oil dropping on ceasefire), RSI 76.5 (most overbought of entire hold), and capital rotation into DAL peace trade.

**VSA Performance on DVN:**
- Called HOLD correctly for 12 consecutive sessions
- Spring signal confirmed institutional accumulation at entry
- 1.5R alert on day 7 triggered breakeven stop — excellent risk management
- Did not flag 3/20 distribution (56M volume, 81% sell) as a warning

**Post-Trade Audit Answers:**
1. Geopolitical catalyst held for 10 of 12 days, then began reversing on Trump ceasefire announcement
2. Entry timing was good — bought on momentum confirmation, not at the peak
3. POC-based stop at $44.45 proved to be valid support (never touched)
4. DVN outperformed XOM over the period; OXY ran further but from a more overbought starting point
5. Position sizing was appropriate — 22 shares gave meaningful dollar exposure

---

### Trade #2: PANW (Palo Alto Networks) — LOSS (SCRATCH) ❌

**Status:** CLOSED (VSA CLOSE signal)
**Entry:** 6 shares @ $168.50 on 2026-03-17 (buy stop triggered)
**Exit:** 6 shares @ ~$167.45 on 2026-03-18
**Days Held:** 1
**P/L:** -$6.30 (-0.6%)

**Thesis:** Long leading cybersecurity platform during active Iran war cycle with escalating state-sponsored cyberattacks on US companies (Stryker confirmed hit). Diversification play — different aspect of same Iran conflict, uncorrelated with DVN energy position.

**Why PANW Over Alternatives:**
- CRWD ($442/share) — only 2 shares on $1,000, severely limited dollar upside
- NVDA — sell-the-news candle on GTC keynote day (ran to $188.88, closed $183.22, 76% sell pressure on 217M volume)
- Defense stocks (LMT, RTX, GD) — surprisingly weak despite war escalation, all showing sell pressure
- PANW consolidating in tight $165-$171 range, RSI 56.8, POC at $165.20 providing floor

**Entry Context:**
- PANW premarket: $168.49
- Fed meeting next day (known binary risk)
- Market flat, digesting Monday's 1% bounce
- Buy stop adjusted from original $169.00 (3/16, didn't fill) to $168.50

**Exit Reasoning:**
- VSA issued CLOSE signal morning of 3/18: "Two consecutive down bars followed by No Demand up bar. Williams' explicit end-of-uptrend signal."
- Closed immediately per system rules
- Saved potentially larger loss — market sold off 1.36% that day on hot PPI and hawkish Fed

**Key Lesson:** The VSA system earned significant trust on this trade. Respecting the CLOSE signal limited the loss to essentially a scratch.

---

### Trade #3: DAL (Delta Air Lines) — LOSS ❌

**Status:** CLOSED (stop triggered)
**Entry:** 14 shares @ $67.53 on 2026-03-25 (buy stop triggered)
**Exit:** 14 shares @ $63.48 (stop triggered) on 2026-03-30
**Days Held:** 5
**P/L:** -$56.70 (-6.0%)

**Thesis:** Long major US airline as direct beneficiary of oil price collapse driven by Iran de-escalation. "Peace trade" — the inverse of DVN. Oil had dropped from $100 WTI to $87 on Trump's 5-day ceasefire announcement and claims of productive talks with Iran. Every $5 decline in fuel prices translates to ~5-10% improvement in airline EPS (Jefferies estimates). DAL had raised Q1 revenue guidance.

**Why DAL:**
- RSI 54.9 — healthy, not overbought
- 3/24 bar showed textbook reversal: opened $64, dropped to $63.54, surged to $66.97 close with 91% buy pressure
- POC at $71.12 — clear volume magnet target
- Raised Q1 guidance provided fundamental catalyst beyond oil speculation

**What Went Wrong:**
- Iran rejected the 15-point ceasefire proposal on 3/25 (same day as entry)
- Oil reversed from $87 back above $100+ over the following days
- DAL sold off for four consecutive days: sell pressure of 23%, 16%, 12%, 12%
- The trade was fundamentally a bet on a geopolitical outcome (peace) that did not materialize
- Trump's ceasefire claims proved unreliable — Iran denied any direct talks

**Stop Details:**
- Stop: $63.50 (below 3/24 intraday low of $63.54)
- Triggered on 3/30 when DAL hit $62.95 intraday
- Actual fill: $63.48

**Key Lesson:** Trading against the dominant trend based on unverifiable diplomatic headlines is speculation, not analysis. The LLM had no ability to assess whether Trump's claims were accurate, yet built an entire thesis around them.

---

### Trade #4: AM (Antero Midstream) — PENDING/OPEN

**Status:** Buy stop order placed 2026-03-31, day order only
**Order:** 43 shares, buy stop $23.35, limit $23.55
**Stop:** $22.40
**Target:** $24.50
**Premarket:** $23.24 (below trigger)

**Thesis:** Long midstream energy (pipeline/toll-road model) as a lagging participant in the energy rally. AM has RSI 59.9 while upstream names are RSI 75-83. Midstream benefits from elevated activity levels regardless of exact oil price — less binary on ceasefire outcome than upstream or airlines. Consolidating in $22.45-$23.84 range for two weeks. 3/25 bar showed 94% buy pressure (accumulation) followed by healthy pullback on lighter volume. VSA confirms healthy uptrend with background strength (Test 7 bars ago).

**Why AM Over Other Energy Names:**
- MGY: RSI 79.7 — overbought
- OXY: RSI 82.5 — overbought
- XLE: RSI 76.7 — overbought, yesterday 89% sell pressure (distribution)
- AM: RSI 59.9 — only energy name not overbought. $23/share gives 43 shares for excellent dollar exposure.

---

## 4. TRADES AVOIDED (DISCIPLINE LOG)

These are trades that were considered but not taken, either by LLM recommendation or because day-only orders didn't fill. Several of these avoided significant losses.

| Date | Ticker | Reason Not Taken | Outcome if Taken |
|------|--------|-----------------|------------------|
| 3/18 | Any | Fed day — recommended cash, couldn't monitor 2:30-3:30 window | Market sold off 1.36% after hawkish Fed |
| 3/19 | NTR | Buy stop $79.25 did not fill (day order). Price was $78.90 premarket. | NTR fell to $76 the next day. Avoided ~$38 loss. |
| 3/20 | Any | Recommended cash — market too ugly, no edge | S&P fell further |
| 3/24 | Any | Recommended cash — Iran situation binary, waiting for clarity | Market whipsawed |
| 3/24 | Various energy (VLO, MPC, PSX) | All RSI 70+, showing distribution. Refused to chase. | Mixed — some continued up, some pulled back |
| 3/24 | Various tech (AAPL, MSFT, FDX) | Share prices too high for $1,000, sell pressure dominant | All continued lower |
| 3/24 | Various (SOFI, PLTR, HOOD) | No edge independent of Iran outcome | SOFI continued lower |
| 3/26 | Any | Market having worst day since war started — recommended holding DAL with stop, no new positions | Correct — adding risk would have increased losses |

---

## 5. CUMULATIVE PERFORMANCE

| Metric | Value |
|--------|-------|
| Total Trades Closed | 3 |
| Wins | 1 (DVN) |
| Losses | 2 (PANW, DAL) |
| Win Rate | 33% |
| Total Gross P/L | +$9.60 |
| Net Return on Capital | +0.96% |
| Best Trade | DVN: +$72.60 (+7.2%) |
| Worst Trade | DAL: -$56.70 (-6.0%) |
| Average Win | +$72.60 |
| Average Loss | -$31.50 |
| Profit Factor | 1.15 (total wins / total losses) |
| Max Drawdown (single trade) | -$56.70 |
| Days in Market | ~18 of 13 trading days |
| Days in Cash (by choice) | ~5 trading days |
| Trades Avoided by Discipline | 6+ |

**Benchmark Comparison (same period):**
- S&P 500: ~-7% (March 13–31)
- Nasdaq: ~-9%
- Dow: ~-7%
- Energy (XLE): ~+12%
- Experiment: +0.96%

*Note: The experiment outperformed the broad market significantly but underperformed the energy sector that was the primary trade thesis.*

---

## 6. KEY LESSONS LEARNED (CUMULATIVE)

### Trading Rules Established:

1. **Trade the dominant trend or don't trade at all.** In a crisis-driven market, there is usually one clear winning theme. Stick with it until the thesis breaks.

2. **Unverifiable information is not a catalyst.** Presidential social media posts about diplomatic progress cannot be confirmed independently. Do not build trade theses around them.

3. **When the target is hit, take profit.** Especially on a short-term trade that has exceeded its planned timeframe. Trailing stops complement profit-taking but don't replace it.

4. **Cash is a position.** In a headline-driven market where every thesis is binary on a geopolitical outcome, the highest-probability "trade" is often no trade.

5. **The VSA system is a valuable guardrail but not sufficient alone.** It excels at reading price action and volume but needs supplementing with macro awareness.

6. **Day-only orders are excellent risk management.** Prevents stale orders from triggering in changed conditions. The NTR non-fill saved ~$38.

7. **Position sizing matters.** Stocks above $150/share only allow 5-6 shares on $1,000, severely capping dollar upside. Target $20-50 price range for 20-50 shares.

8. **Buy stops confirm momentum.** Every successful entry was on a buy stop, not a market order. This ensures you're buying strength, not falling knives.

9. **Respect the VSA CLOSE signal immediately.** PANW's CLOSE signal on day 1 saved significant capital. Don't second-guess the system on exits.

10. **Don't fight the tape looking for diversification.** When one sector is clearly winning, forcing trades in other sectors for diversification's sake leads to losses.

---

## 7. OPEN QUESTIONS FOR FUTURE SESSIONS

1. Is a 33% win rate sustainable if the average win significantly exceeds the average loss?
2. Should the LLM use a fixed timeframe (exit on day 5 regardless) or flexible (system-driven exits)?
3. How should the LLM weight VSA signals vs. macro/geopolitical awareness when they conflict?
4. Should the experiment allow multiple simultaneous positions, or one at a time?
5. At what trade count does the sample become statistically meaningful? (Target: 15-20 trades)
6. Should position sizing increase after wins and decrease after losses (anti-martingale)?

---

## 8. DAILY SESSION DOCUMENT TEMPLATE

*Use this template for each trading day's session notes. Save as `sessions/YYYY-MM-DD.md`*

```markdown
# TRADING SESSION: YYYY-MM-DD

## Pre-Market Context
- **Futures:** [S&P / Dow / Nasdaq premarket %]
- **Oil:** [WTI / Brent prices and direction]
- **Key Headlines:** [Top 2-3 market-moving news items]
- **VIX:** [Level and direction]
- **Economic Calendar:** [Any data releases or Fed speakers today]

## Open Positions
| Ticker | Entry Date | Entry Price | Current Price | Stop | Target | Unrealized P/L | VSA Verdict |
|--------|-----------|-------------|---------------|------|--------|----------------|-------------|
| | | | | | | | |

## VSA System Review Summary
[Key signals from today's VSA position review — CLOSE signals, TIGHTEN STOP, new background strength, etc.]

## Closed Positions Today
| Ticker | Entry | Exit | Shares | P/L | Reason |
|--------|-------|------|--------|-----|--------|
| | | | | | |

## New Orders Placed
| Ticker | Order Type | Trigger | Limit | Stop | Target | Shares | Day/GTC | Thesis |
|--------|-----------|---------|-------|------|--------|--------|---------|--------|
| | | | | | | | | |

## Orders That Did NOT Fill
| Ticker | Trigger Price | Market Price | Why It Didn't Fill |
|--------|--------------|-------------|-------------------|
| | | | |

## Trades Considered But Rejected
| Ticker | Reason Rejected |
|--------|----------------|
| | |

## LLM Decision Rationale
[Verbose explanation of today's decisions — what was considered, what was chosen, and why]

## Bar Data Reviewed
[List of tickers with bar data pulled and key observations]

## Lessons / Observations
[Any new insights, pattern recognition, or rule adjustments from today's session]

## Running Cumulative P/L
| Total Trades | Wins | Losses | Net P/L | Win Rate |
|-------------|------|--------|---------|----------|
| | | | | |

## Next Session Prep
[What to watch overnight, any pending orders, key events tomorrow]
```

---

*Document Version: 1.0*
*Last Updated: 2026-03-31*
*Maintained by: Human operator + Claude (Anthropic)*
