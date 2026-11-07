# Hedge P&L Mismatch: Summary and Trader Awareness

**Model:** https://peterdmyan.github.io/cdps-position-model/

Our CDP position with a put works economically, but reported P&L does not show its real performance until we close. The CDPs and their dividends are carried at cost, while the put is marked to market (PV of CDPs with the put − CDP market price). Over the 4-year hold, reported and actual P&L can sit up to S$504k apart, and the whole difference is booked on the day we close.

## Concerns

Illustrative case: 10,000 CDP units at S$100 (S$1.0m), 6% dividend, closed at the end of year 4. The 4-year S$95 put is worth **S$19.03 per CDP (S$190.3k, 19% of notional)** on day one: PV of the CDP with the put, S$119.03, minus the S$100 market price. It is expensive because the 6% dividend exceeds the 3% rate, which puts the 4-year forward at S$88.69, below the strike. The up case is set to a 12% position IRR.

Four-year totals by reporting line, S$k (per CDP in brackets):

| Scenario (price at year 4) | CDP dividend | CDP option MTM | CDP sold at close | Total P&L | Position IRR |
| --- | ---: | ---: | ---: | ---: | ---: |
| Up, +10.7% a year (S$150.42) | +300.2 (S$30.02) | −190.3 (−S$19.03) | +504.2 (S$50.42) | +614.1 | 12.0% |
| Flat (S$100.00) | +240.0 (S$24.00) | −190.3 (−S$19.03) | 0 | +49.7 | 1.1% |
| Down, above strike, −1% a year (S$96.06) | +234.9 (S$23.49) | −190.3 (−S$19.03) | −39.4 (−S$3.94) | +5.3 | 0.1% |
| Down, below strike, −10.7% a year (S$63.46) | +190.1 (S$19.01) | +125.1 (S$12.51) | −365.4 (−S$36.54) | −50.2 | −1.2% |

The timing is the problem. Year 4 alone reports +S$579k in the up case, −S$272k in the deep fall and −S$77k in the mild fall, because the option's last-year decay or payoff and the whole CDP gain or loss land together. The year-by-year split is on the model page.

1. **Performance understated when the market rises.** For the first two years reported P&L is near zero, because put losses offset the dividends, while the position has actually made over S$230k. The desk can look like it is missing a 12% IRR deal that is on track.
2. **False profit when the market falls below the strike.** Reported P&L climbs to S$315k because put gains and dividends are booked but the CDP loss is not. Closing turns this into −S$50k, a S$365k hit in a single period.
3. **A small fall is the quiet worst case.** If the price drifts down but stays above S$95, the put expires worthless. Reported P&L shows S$83k early in year 4, then drops to S$5k at close: the S$190k put cost is fully lost and the protection never paid.
4. **Pressure to act on the wrong signal.** Weak reported P&L in a rising market invites cutting the put. Strong reported P&L in a falling market can encourage more risk or bonuses on gains that are not real.
5. **Year-4 cliff.** Put time decay is heaviest in the last year, and every CDP price move is realized at close, so year-4 P&L will be volatile in every scenario.

## Trader awareness

Traders should read their reported P&L as put plus dividends only, not as the result of the position.

- **A falling CDP price is not a good month.** Put gains offset a CDP loss that is not yet booked; check actual P&L.
- **Know where the strike is.** Above S$95 at close, the put pays nothing and its full S$190k cost is lost; below it, the put caps the loss. Track the price against the strike as year 4 approaches.
- **Expect near-zero reported P&L early in a rising market.** That is the put cost absorbing the dividends, not underperformance.
- **Do not unwind or restructure the put to improve reported P&L.** Any change to the hedge is a risk decision and needs approval.
- **Plan the close.** The CDP gain or loss realized at year 4 lands in one period; agree timing and messaging with Finance in advance.
- **Watch the impairment trigger.** A deep fall could force an impairment before year 4 and bring the loss forward.
- **Report both lines every month:** reported, and actual (CDPs at market + dividends + put).

## Ask

- [ ] Approve a monthly two-line P&L view (reported vs actual) for this position
- [ ] Agree that the desk is judged on actual P&L and position IRR, not reported P&L alone
- [ ] Ask Finance whether fair value or hedge accounting for the CDPs can remove the mismatch
- [ ] Brief traders on the points above and confirm the impairment trigger level

Numbers are illustrative. The put cost, 19% of notional here, drives their size; rerun them with the actual put terms before wider circulation.

---

*An alternative reading, with the 12% IRR as a contractual floor and a strike of 128.68, is in [SUMMARY-floor.md](SUMMARY-floor.md) and on [floor.html](https://peterdmyan.github.io/cdps-position-model/floor.html). Illustrative model, not investment advice and not an accounting opinion.*
