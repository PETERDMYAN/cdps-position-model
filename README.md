# CDPS with Put Option: Reported versus Actual

An illustrative four-year model of a CDPS position held alongside a put option, built to show
where book reporting and economic reality diverge.

Two readings of the same deal terms live here side by side.

| Page | Reading | Summary |
|---|---|---|
| [Priced-put model](https://peterdmyan.github.io/cdps-position-model/) | 12% IRR is the up-case return; S$95 strike; put priced with Black-Scholes at S$19.03 | [SUMMARY.md](SUMMARY.md) |
| [IRR-floor model](https://peterdmyan.github.io/cdps-position-model/floor.html) | 12% IRR is a contractual floor; strike solved at 128.68; no premium priced | [SUMMARY-floor.md](SUMMARY-floor.md) |

## Priced-put model

| Input | Value |
|---|---|
| CDP price | S$100, 10,000 units (S$1.0m) |
| Dividend | 6% a year on market price, paid quarterly, booked as income |
| Put | 4-year European put, strike S$95, 25% volatility, 3% rate |
| Put value on day one | S$19.03 per CDP, S$190.3k in total |
| Hold | 4 years, closed at the end of year 4 |

Accounting treatment:

- **CDPS and dividend** carried at cost; dividends booked as income; the CDP price change is booked only when sold.
- **Put option** marked to market as `PV(CDPS with option) - stock price`.

Four scenarios: price rises (+10.7% a year, 12% position IRR), flat, falls but stays above the strike
(−1% a year), and falls below the strike (−10.7% a year). The page shows reported and actual P&L by
year, the put calculation, and a year-by-year split of dividend, option MTM and the CDP gain or loss
realized at close.

### Headline finding

Reported and actual P&L can sit up to S$504k apart before close, and the gap is booked in one
period at year 4. A falling price shows a reported profit (+S$315k) that turns into −S$50k at close.
A small fall above the strike is the quiet worst case: the put expires worthless and the position
ends at +S$5k.

## Caveats

Round numbers throughout. No position, counterparty or issuer data. Volatility and strike in the
priced-put model are assumptions, and the put cost drives the size of every figure. Not investment
advice and not an accounting opinion.
