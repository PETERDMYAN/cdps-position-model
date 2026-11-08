# CDPS with put option: two economic outcomes, three reported numbers

**Model:** https://peterdmyan.github.io/cdps-position-model/floor.html

## The structure

The position carries a contractual floor of 12%. With a 6% cash dividend on cost, the put strike
that delivers that floor is **128.68**, which is 28.68% above the entry price of 100. The stock
starts below the strike and stays there unless it rallies more than 28.68%, so in most outcomes the
put is exercised and the floor pays. The put is not tail protection here. It is the main source of
return.

One consequence is worth stating up front. The brief asked for a fall that stops short of the strike
and a fall that breaks through it. Because the strike sits above spot from day one, those are the
same case, so they are shown as one scenario. Three scenarios remain, covering two economic
outcomes: a rally past the strike, or the floor.

## Bottom line

| Scenario | Stock, year 4 | Settles at | Reported, 4 years | Actual, 4 years | IRR |
|---|---:|---:|---:|---:|---:|
| A Rises past the strike | 160 | 160.00 | **-7.32** | +84.00 | 17.58% |
| B Flat | 100 | 128.68 | +52.68 | +52.68 | 12.00% |
| C Falls below the strike | 60 | 128.68 | **+92.68** | +52.68 | 12.00% |

**B and C are the same deal.** Both settle at the floor and both return exactly 12%. Reported
earnings are +52.68 and +92.68, a spread of 40 per share that corresponds to no difference in
economics whatsoever. Make the fall deeper and that spread widens one for one, while the economics
stay where they are.

## Why it happens

The option carrying value is defined as accreted value minus stock price, so a falling stock inflates
reported earnings. At the same time the CDPS is carried at cost, so the stock's decline is never
recognised on the asset itself. The stock move is booked once, with the wrong sign, and never where
it belongs.

The arithmetic is exact: when the floor binds, reported exceeds economics by the unrecognised stock
move. Stock down 40, reported overstates by 40.

## Three concerns

1. **One outcome, as many reported numbers as there are paths to it.** Every stock price below
   128.68 produces the same 12% return and a different reported figure, 40 per share apart over the
   range shown here. Anyone managing to the reported line is managing noise.

2. **Reported is right only by coincidence.** Scenario B matches to the cent because the stock
   happens to end exactly at the entry price. Move it either way and the two separate immediately.

3. **The rally case inverts completely.** The best real outcome, +84.00 and 17.58%, is the only one
   that prints a loss. The divergence there runs at twice the stock move, because the rally is
   subtracted through the option plug and added through economics at the same time. The gap reaches
   91.32 per share and lands as a single true-up at close.

## What the desk needs to know

- **This is a 12% instrument plus a call struck at 128.68, not a protected equity position.** Risk
  and hedging should be framed off that, not off the 100 entry price.
- **Reported option P&L is the stock price with a minus sign.** Read as exposure it points the wrong
  way. Risk has to come off the economic line.
- **Hedging the stock will destabilise the book.** A short hedge into a rally loses at the same
  moment the option plug reports a loss. They compound rather than offset.
- **Only the rally scenario carries real variance.** Below 128.68 the payoff is fixed, so the whole
  difference between B and C, and between any two fall paths, is accounting noise. The genuine
  question is the probability of finishing above 128.68.
- **The floor is only as good as the writer.** Every outcome except a rally past 128.68 depends
  entirely on the put paying. If the writer is connected to the stock that is falling, the protection is worth least
  exactly when it is needed, and nothing in the reporting flags that. This is the largest unmodelled
  risk here.
- **Dividend risk hits twice.** A suspension stops the income line and invalidates the accretion
  schedule at the same time, which also moves the strike that floors the IRR.

## Asks

1. Confirmation from Technical Accounting that a cost-carried CDPS plus an option plug defined as
   accreted value minus spot is the agreed treatment, given that it leaves the stock unmarked.
2. A view on whether the position is better presented as what it economically is, a 12% instrument
   plus a call struck at 128.68.
3. A decision on forecasting and disclosing the closing true-up ahead of the period it lands in.

---

*Illustrative model on round numbers. No position, counterparty or issuer data. A Black-Scholes put
premium is not computed: that needs volatility, the risk-free rate and the exercise style. Not
investment advice and not an accounting opinion.*
