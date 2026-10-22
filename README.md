## Status
Working prototype, tested on 25 trading days of real MCX Bhavcopy (September to mid-October 2026).

## Results (preliminary)
- Four contracts, six pairs, same-expiry spreads. 57 trades from 17 distinct entry days.
- If trades are filled at the same close that produced the signal, gross P&L looks large (1293.6 Rs/g, break-even 3.7 bps per leg per side). This is optimistic, because it captures close-price noise.
- With a one-day execution delay, gross P&L drops to 247.7 Rs/g and break-even cost to 0.8 bps per leg per side. Above that cost the gain disappears.
- We report this as it is: on this sample, no spread signal clearly survives realistic costs.
## Costs
Statutory cost per leg round trip is about 1.72 bps (CTT 1.00, exchange 0.42, SEBI 0.02, stamp duty 0.20, GST 0.08), so about 0.86 bps per leg per side. Brokerage and slippage are excluded or assumed (one tick on GOLDPETAL is about 0.7 bps). Values come from broker and exchange documents; verification on the MCX page is pending. With a one-day delay the break-even cost is 0.8 bps, which is below statutory cost alone.

## Limitations
Small sample (25 days). Closing prices of thin contracts may be stale. Cost is a parameter (COST_BPS), not yet a verified figure. No margin or position limits modelled.
