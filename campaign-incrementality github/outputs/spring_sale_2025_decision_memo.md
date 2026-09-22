# Decision memo: Spring Sale 2025

_Generated from pipeline run. Activation week 2025-03-31; measurement window 2025-04-07 to 2025-05-05 (5 weeks)._

## Headline

Net incrementality: **+0.0%** on GBV (90% interval -2.2% to +2.2%), worth **$0.0M**. Verdict: material effect.

| Build | Rate | Value |
| --- | ---: | ---: |
| Participating properties | +6.3% | $23.4M |
| Less cannibalisation of competitive set | -5.5% | $-23.4M |
| Total incrementality | +0.0% | $0.0M |

Room nights moved +9.3% against booking value's +6.3%; the gap is the discount reaching travellers.

## Drivers of growth

The GBV lift is carried by conversion rate at +8.1% and length of stay at +1.0%, partly given back through average daily rate at -2.8%.

| Driver | Lift | 90% interval | Share of movement |
| --- | ---: | ---: | ---: |
| Traffic (visits) | -0.1% | -1.4% to +1.5% | 1% |
| Conversion rate | +8.1% | +7.6% to +8.6% | 66% |
| Length of stay | +1.0% | +0.8% to +1.2% | 9% |
| Average daily rate | -2.8% | -3.0% to -2.7% | 24% |

Drivers compose to +5.98% against a directly estimated +6.28% — a residual of +0.30%, which reconciles.

## Money

| Line | USD |
| --- | --- |
| Incremental booking value | $0.01M |
| Incremental contribution | $0.00M |
| Cash-funded discount | $-0.85M |
| Fixed campaign cost | $-0.45M |
| Net value | $-1.30M |

Return on campaign spend: **0.00x** (net $-1.3M). Break-even lift: **2.7%**, against a measured 6.3%. Of the $10.7M discount granted, **$10.7M (100%)** went to demand the model says would have converted anyway.

## What the displacement test is worth

| | Gross of displacement | Net of displacement |
| --- | --- | --- |
| Incremental booking value | $23.4M | $0.0M |
| Effective lift | 6.3% | 0.0% |
| Return on spend | 2.24x | 0.00x |
| Net value | $1.62M | $-1.30M |

**These land on opposite sides of break-even.** Accepting the no-displacement assumption without testing it would have booked this campaign as value-creating. Testing it reverses the decision, which makes the comp-set test the analysis rather than a robustness check.

## Falsification scorecard

| Test | Result | Statistic | Detail |
| --- | --- | --- | --- |
| Rolling-origin backtest | PASS | 0.0221 | 22 origins, 5-week horizon, mean absolute error 2.21% |
| In-time placebo | PASS | 0.0045 | fake activation 2024-09-30 (26 weeks early) returns +0.45% |
| In-space placebo | PASS | 0.0625 | 15 untreated cohorts of 1000 properties; null sd 0.50%; observed +6.28% ranks 1/16 |
| Comp-set displacement | PASS | -0.0370 | untreated comp set moves -3.70% over the same weeks; netted off the headline as displacement |
| Control-pool leakage (underpowered) | PASS | -0.0223 | control pool reads -2.2% against unaffected demand, detectable only to +/-1.5% -- rules out gross contamination, cannot confirm the 1-2% that would matter; design does not use the pool as a control |
| Relationship stability | FAIL | 0.0353 | counterfactuals fitted on early vs late pre-period diverge 3.53%; forecast error 1.26x from older to recent origins (1.95% to 2.46%) |
| Specification sensitivity | FAIL | 0.0294 | 9 validated variants span +7.85% to +10.79% (2.94% wide) |

## Stacking

Stack-enabled properties outperformed stack-disabled participants by **+2.2%** (90% CI +1.6% to +2.8%, p=0.000). Parallel-trends check p=0.00 (FAILS -- treat as descriptive).

## What this does not answer

- Post-window carryover: the measurement stops at the campaign end date, so any repeat-booking effect is excluded and the estimate is a lower bound.
- Participation is not randomised. Properties opted into the campaign, so the estimate is the effect on participants, not the effect of extending the campaign to non-participants.
- The discount-depth ceiling holds volume fixed; a shallower discount would presumably have produced less lift.
