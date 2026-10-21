# summit-syndicate-mcx-gold
## Status
Working prototype, tested on 25 trading days of real MCX Bhavcopy (September to mid-October 2026).

## Results (preliminary)
- Four contracts, six pairs, same-expiry spreads. 57 trades from 17 distinct entry days.
- If trades are filled at the same close that produced the signal, gross P&L looks large (1293.6 Rs/g, break-even 3.7 bps per leg per side). This is optimistic, because it captures close-price noise.
- With a one-day execution delay, gross P&L drops to 247.7 Rs/g and break-even cost to 0.8 bps per leg per side. Above that cost the gain disappears.
- We report this as it is: on this sample, no spread signal clearly survives realistic costs.

## Limitations
Small sample (25 days). Closing prices of thin contracts may be stale. Cost is a parameter (COST_BPS), not yet a verified figure. No margin or position limits modelled.
