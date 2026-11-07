# CDPS with put option: reported earnings run inverse to the position

**Model:** https://peterdmyan.github.io/cdps-position-model/

## Bottom line

Under the agreed treatment, our reported result moves in the **opposite direction** to the position.

| Scenario | Stock, year 4 | Reported, 4 years | Actual, 4 years | Realised IRR |
|---|---:|---:|---:|---:|
| Stock rises | 160 | **-7.3** | +84.0 | 17.6% |
| Stock flat | 100 | +52.7 | +24.0 | 6.0% |
| Stock falls, above strike | 90 | +62.7 | +14.0 | 3.6% |
| Stock falls, through strike | 60 | **+92.7** | +4.0 | 1.1% |

Ranked by reported earnings, our worst outcome looks like our best. Figures are per share on an
entry price of 100, with a put struck at 80.

## Why it happens

The option is marked at accreted value minus stock price. The accreted value is fixed at trade date
and never moves, so the stock enters reported earnings with a negative sign. Every point the stock
gains is booked as an option loss. The dividend leg cannot offset it: carried at cost it prints the
same 6.00 every year in every scenario, so it carries no information about how the position is
doing.

## Three concerns

1. **Signal.** Reported option P&L is a restatement of the stock price with the sign flipped, not a
   measure of the option. Anyone using it to judge the position will read it backwards.

2. **Timing.** Nothing pulls reported back towards economics before settlement. The entire gap, up
   to 91 per share, lands as a single true-up in the closing period. On a position of any size that
   is a one-off P&L event we should be explaining well before it happens, not at settlement.

3. **Substance.** The carrying value accretes as though 12% were certain. With the put struck 20%
   below spot, only one of the four scenarios reaches 12%; the realised range is 1.1% to 17.6%. The
   book is asserting a return the structure does not guarantee.

## What the desk needs to know

- **Hedging will not stabilise the book.** A short hedge against a rising stock produces a hedge
  loss at the same time as the option plug produces a reported loss. The two move together, not
  against each other. Expect reported volatility of roughly the full notional delta, sign reversed.
- **Do not read reported option P&L as exposure.** Risk has to come off the economic line.
- **Forecast the closing true-up from year 3.** It is deterministic once the terminal stock price is
  known. It should be socialised, not discovered.
- **The protection gap is the real exposure.** Between the strike at 80 and the 128.68 the book
  assumes, the position is unhedged. That band of 48.68 per share is where the structure fails to
  deliver the accreted return, and nothing in the reporting flags it.
- **Dividend risk hits twice.** A suspension stops the income line and invalidates the accretion
  schedule at the same time.

## Asks

1. Confirmation from Technical Accounting that the dividend leg qualifies for cost method and that
   the option plug is the agreed mark.
2. A decision on whether the accretion resets once a scenario becomes unlikely, rather than running
   to maturity and truing up in one period.
3. The term sheet strike, so we can describe the 12% accurately as a floor or as a target.

## One open point

A strike that makes 12% a contractual floor would have to sit at 128.68, which is 28.7% above spot.
At that level the stock is below the strike from day one and the four scenarios collapse into one.
The scenarios only stay distinct with a strike below spot, and a strike below spot means 12% is an
underwriting target rather than a guarantee. The model covers both readings; the term sheet decides
which one is ours.

---

*Illustrative model on round numbers. No position, counterparty or issuer data. Not investment
advice and not an accounting opinion.*
