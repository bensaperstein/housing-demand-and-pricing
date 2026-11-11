# Methods and results

[Back to overview](../README.md)

## Choice structure

The supplied survey contains 50 respondents, each choosing between two housing alternatives in ten tasks:

| Unit | Count |
| --- | ---: |
| Respondents | 50 |
| Choice tasks | 500 |
| Alternative-level rows | 1,000 |

The data were reshaped from respondent-level wide form into choice-task records, expanded to two alternatives, and merged with the corresponding option attributes. The saved output reports all 1,000 rows matched.

## Model 1: Housing characteristics

The baseline conditional-logit specification included rent, walking time, room size, apartment type, two bathrooms, in-unit laundry, in-building laundry, utilities included, furnishing, and cleaning.

A choice-set identifier grouped the two alternatives for each respondent/task combination.

## Model 2: Consumer-characteristic interactions

The expanded model retained the ten baseline regressors and added:

- High budget × rent
- High budget × utilities
- High budget × furnishing
- Dorm resident × furnishing
- Dorm resident × utilities
- Off-campus house resident × cleaning
- Off-campus house resident × two bathrooms

“High budget” was defined in the saved code as budget category 4 or above, corresponding to at least $1,200 monthly per person.

## Selected estimates from the saved output

| Term | Baseline coefficient | Expanded coefficient | Expanded p-value |
| --- | ---: | ---: | ---: |
| Rent | −0.0073933 | −0.0099437 | 0.284 |
| Furnished | 0.7208978 | 0.9760447 | 0.054 |
| High budget × rent | — | 0.0048349 | 0.002 |
| High budget × furnished | — | −0.6286743 | 0.028 |
| Dorm resident × furnished | — | 0.7360215 | 0.026 |

These are historical estimates and nominal p-values from the saved specification. They have not been recalculated here. The commands shown do not specify respondent-clustered standard errors; repeated choices within respondents matter for inference.

The positive high-budget/rent interaction offsets part of the negative baseline rent coefficient. The furnishing interactions describe differences relative to the relevant reference group, not standalone segment-specific effects.

## Model fit

| Statistic | Baseline | Expanded |
| --- | ---: | ---: |
| Regressors | 10 | 17 |
| Log likelihood | −323.47535 | −309.36353 |
| McFadden pseudo-R² | 0.0666 | 0.1074 |

These describe in-sample fit. No holdout sample, cross-validation, or forecast performance is established by the project records.

## Willingness to pay

The report converts utility coefficients into willingness to pay using the negative rent coefficient as a denominator.

With interactions, the relevant numerator and rent denominator can both depend on segment. The rent estimates are imprecise, so coefficient ratios can be unstable. This repository therefore explains the framework without promoting large dollar estimates as dependable prices.

## From preferences to housing packages

The final report proposes budget, convenience, and premium bundles. It recommends comparing willingness to pay with monthly cost per student and considering optional add-ons where appropriate.

This is a decision framework. There is no actual cost dataset, estimated revenue uplift, realized profitability, implemented product, or real client adoption.

## Survey recommendations

1. Add a “neither option” alternative.
2. Recruit more respondents.
3. Ask about year, roommates, current rent, financial aid, car access, and housing preferences.
4. Vary amenities more independently to reduce confounding among attributes.

## Limits

The small sample, fixed tasks, repeated responses, correlated design, missing outside option, and conditional-logit assumptions constrain the conclusions. Segment comparisons and willingness-to-pay calculations warrant caution.

These notes preserve the original analysis; they do not correct the report, generate new estimates, or reconstruct a runnable pipeline.
