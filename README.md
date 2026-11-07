# CDPS with Put Option: Reported versus Actual

An illustrative four-year model of a CDPS position held alongside a put option, built to show
where book reporting and economic reality diverge.

**Live page:** https://PETERDMYAN.github.io/cdps-position-model/

## What it models

| Input | Value |
|---|---|
| Entry price / spot | 100 |
| CDPS cash dividend | 6% on cost, recognised yearly |
| Position IRR | 12% |
| Tenor | 4 years |

Accounting treatment, as specified:

- **CDPS dividend** is carried at cost. Income is recognised yearly at the coupon on original cost.
- **Put option** is marked to market, with carrying value defined as
  `PV(CDPS with option) - stock price`.

## The headline finding

The stock price enters reported earnings with a negative sign, while the accreted value is fixed at
trade date. Reported results therefore move in the opposite direction to the position: the best
economic scenario prints as a loss and the worst prints as a gain, with the whole difference
arriving as a single true-up at close.

## Scenarios

Four stock paths over the four years: up, flat, down but above the put strike, and down through the
put strike. The page is interactive, so every input and every terminal stock price can be changed.

## Caveats

Round numbers throughout. No position, counterparty or issuer data. Not investment advice and not an
accounting opinion.
