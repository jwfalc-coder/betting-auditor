# Standing Research Tasks

_Maintained by the Pi. Updated when a metric crosses a threshold or priorities change._

Last updated: 2026-06-27 (lay-only reorientation, MOD-280/281)

---

## Priority 1 — Lay-fade edge sustainability + golf dependence (ACTIVE)

**Context:** As of 2026-06-27 the bot is **lay-only** (MOD-280/281). A 292-trade audit found lays are the entire profit engine (69% WR, 44% ROI; backtest 79%/53%) and the keyword model is a favourite-fade engine. But **~55% of all P&L is golf** (outright Top-N / Winner lays), which is seasonal.

**Research questions:**
- Does a favourite-fade edge in multi-runner/outright markets persist as exchanges and other bettors adapt, or does it decay? Any evidence of overround/favourite-longshot bias narrowing on Betfair outrights?
- Is non-golf outright lay sourcing (tennis tournament winners, politics specials, other-sport Top-N) a durable edge, or is golf special? The bot now reserves outright research slots for non-golf to de-risk this.
- How exposed is the strategy to golf seasonality (off-season gaps)? What fills the calendar between majors?
- Search: "favourite longshot bias exchange outright markets", "laying favourites multi-runner betting edge", "golf outright top-10 market efficiency"

---

## Priority 2 — Lay liquidity & execution realism (ACTIVE)

**Context:** Backtested profit ranges from ~£500 to ~£2,400 depending entirely on stake size (£10 vs £50/lay) — i.e. on whether Kelly-sized lays can actually be matched. Per-bet lay liability is now capped at £50.

**Research questions:**
- Can lays of £20-£50 liability be matched at or near the quoted price on thin multi-runner/outright markets (golf Top-N, niche politics)? Typical matched depth?
- How much price slippage should be expected laying an overbet favourite vs the bot's logged price?
- Are there liquidity windows (e.g. tournament final round, pre-event) where outright lay liquidity is best?
- Search: "betfair exchange liquidity outright markets matched depth", "lay bet slippage thin markets"

---

## Standing weekly task — External benchmarking

Each run, briefly check:
- Recent discussion of exchange lay/fade strategies and multi-runner market efficiency
- Any Betfair API or platform changes (commission, market structure)
- Academic or community content on favourite-longshot bias and outright market pricing
- Whether any of the bot's flagged anomalies have known external explanations

---

## Closed tasks (for reference)

- **Back bet failure** (was Priority 1) — **RESOLVED 2026-06-27.** The investigation concluded backs are structurally break-even for this favourite-fade model (137 trades, 0.9% ROI, confirmed out-of-sample); the bot went **lay-only** (MOD-280/281) rather than try to fix backs. Do not re-open or research "why backs underperform" — the answer is settled and acted on.
- **Matchbook underperformance** (was Priority 2) — **CLOSED.** Matchbook is paused/data-only and off-limits to this auditor (see CLAUDE.md). Do not raise MB findings.
- **10-11pp edge band losing** (was Priority 3) — **CLOSED.** The losses in that band were largely back-driven; with backs suppressed it is moot. If lays in the 10-15pp band underperform in *live* data, that can be re-opened as a lay-specific task.
