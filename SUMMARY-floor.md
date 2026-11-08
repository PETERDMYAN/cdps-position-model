# CDPS with put option: the books get the right answer, four years late

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

The position is closed at the end of year 4. Cash in is the settlement, the greater of the stock
price and the strike. What comes off the books is the CDPS at original cost plus whatever the option
leg is carried at by then, so the closing entry is the difference between the two.

## Bottom line

| Scenario | Stock, yr 4 | Reported, yrs 1 to 3 | Actual, yrs 1 to 3 | Gap before close | Year 4 reported | Total, both lines | IRR |
|---|---:|---:|---:|---:|---:|---:|---:|
| A Rises past the strike | 160 | **-6.75** | +63.00 | **-69.75** | **+90.75** | +84.00 | 17.58% |
| B Flat | 100 | +38.25 | +38.25 | 0.00 | +14.43 | +52.68 | 12.00% |
| C Falls below the strike | 60 | **+68.25** | +38.25 | **+30.00** | **-15.57** | +52.68 | 12.00% |

**Over the life of the trade the books are right.** Cumulative reported equals cumulative actual to
the cent in all three scenarios, because the closing entry releases the frozen option carrying value
against real cash. This is not a measurement problem. It is a timing problem, and the entire
correction arrives in a single period.

## The rally case, year by year

This is the scenario worth showing to anyone who reads the reported line.

| Year | Stock | Dividend | Option mark | Close-out | Reported | Actual | Cumulative gap |
|---|---:|---:|---:|---:|---:|---:|---:|
| 1 | 115 | +6.00 | -9.00 | | -3.00 | +21.00 | -24.00 |
| 2 | 130 | +6.00 | -8.28 | | -2.28 | +21.00 | -47.28 |
| 3 | 145 | +6.00 | -7.47 | | -1.47 | +21.00 | -69.75 |
| 4 | 160 | +6.00 | -6.57 | +91.32 | +90.75 | +21.00 | 0.00 |
| Total | | +24.00 | -31.32 | +91.32 | +84.00 | +84.00 | |

The books print a loss in every year the position is open, while the position earns 21.00 a year.
Then a single period books +90.75.

## Why it happens

The option carrying value is defined as the accreted value of the whole position minus the stock
price, so the stock enters reported earnings with the sign reversed. Meanwhile the CDPS is carried at
cost, so the stock is not marked on the asset either. Nothing puts the stock on the books with the
right sign until the position is closed, and then the closing entry does it all at once.

The accretion schedule itself is fixed at trade date: 100.00, 106.00, 112.72, 120.25, 128.68, which
is the 12% return less the 6.00 paid out in cash each year. It never moves with the stock, and its
year-4 value is exactly the put strike.

## Three concerns

1. **The reported line runs against the position for three years.** In the rally case the books and
   the economics sit on opposite sides of zero for the entire open life of the trade. Anyone reading
   the reported line as performance reads it backwards.

2. **Two economically identical scenarios sit 30 per share apart until the last day.** B and C both
   return 12% and both show +38.25 of economics through year 3, yet the books show +38.25 and
   +68.25. Make the fall deeper and that spread widens one for one while the economics do not move.

3. **The whole correction lands in one period.** Across these three paths the closing year books
   anywhere from -15.57 to +90.75 per share. On any meaningful size that is a P&L event we should be
   forecasting and explaining in advance, not at settlement.

## What the desk needs to know

- **The reported line is not a risk signal at any point before close.** Option carrying value is
  accreted value minus spot, so it restates the stock with the sign reversed and adds a fixed
  accretion on top. Risk has to come off the economic line.
- **This is a 12% instrument plus a call struck at 128.68, not a protected equity position.** Frame
  risk and hedging off that, not off the 100 entry price.
- **Size the closing period in advance.** It is deterministic once the terminal price is known, and
  it carries the entire difference. Forecast it from year 3.
- **Only the rally scenario carries real variance.** Below 128.68 the payoff is fixed, so the whole
  difference between B and C, and between any two fall paths, is accounting noise. The genuine
  question is the probability of finishing above 128.68.
- **Hedging the stock will destabilise the reported line further.** A short hedge into a rally loses
  at the same moment the option mark reports a loss. They compound through the open years and then
  both reverse at close.
- **The floor is only as good as the writer.** Every outcome except a rally past 128.68 depends
  entirely on the put paying. If the writer is connected to the stock that is falling, the protection
  is worth least exactly when it is needed, and nothing in the reporting flags that. This is the
  largest unmodelled risk here.
- **Dividend risk hits twice.** A suspension stops the income line and invalidates the accretion
  schedule at the same time, which also moves the strike that floors the IRR.

## Asks

1. Confirmation from Technical Accounting on the closing entry, releasing the CDPS at original cost
   alongside the option carrying value against settlement proceeds, since that single entry carries
   the whole correction.
2. Agreement on how we flag the closing-period swing in advance, given the range above.
3. A view on presenting the economic line next to the reported line for the open years, because the
   reported line on its own is not decision-grade until close.

---

*Illustrative model on round numbers. No position, counterparty or issuer data. A Black-Scholes put
premium is not computed on the page: that needs volatility, the risk-free rate and the exercise
style. Not investment advice and not an accounting opinion.*
