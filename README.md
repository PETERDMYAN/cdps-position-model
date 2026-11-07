# CDPS with Put Option: Reported versus Actual

An illustrative four-year model of a CDPS position held alongside a put option, built to show
where book reporting and economic reality diverge.

**Live page:** https://peterdmyan.github.io/cdps-position-model/  &nbsp;&nbsp;·&nbsp;&nbsp; **Management summary:** [SUMMARY.md](SUMMARY.md)

## What it models

| Input | Value |
|---|---|
| Entry price / spot | 100 |
| CDPS cash dividend | 6% on cost, recognised yearly |
| Position IRR | 12%, contractual floor |
| Put strike | 128.68, the level that delivers the floor |
| Tenor | 4 years |

Accounting treatment, as specified:

- **CDPS dividend** is carried at cost. Income is recognised yearly at the coupon on original cost.
- **Put option** is marked to market, with carrying value defined as
  `PV(CDPS with option) - stock price`.

## The headline finding

Because 12% is a floor, three of the four scenarios settle at the same strike and return exactly
12%. They are economically identical. Reported earnings across them still differ by 40 per share.

The cause is that the stock price enters reported earnings through the option plug with a negative
sign, while the CDPS is carried at cost and the stock's move is never recognised on the asset
itself. When the floor binds, reported exceeds economics by exactly the unrecognised stock move. In
the rally case the position prints a loss while earning 17.58%.

## Scenarios

Four stock paths over the four years: rises past the strike, flat, falls moderately, falls hard. The
page is interactive, so every input and every terminal stock price can be changed. The strike is
locked to the IRR floor by default and can be unlocked to test other structures.

## Caveats

Round numbers throughout. No position, counterparty or issuer data. Not investment advice and not an
accounting opinion.
