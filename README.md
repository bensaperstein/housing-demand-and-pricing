# What Do Students Value in Off-Campus Housing?
### Demand Estimation and Pricing · ECON 349 Industrial Economics · Spring 2026

I used discrete-choice survey data and Stata to explore how Northwestern students trade off rent, location, and housing amenities—and how those preferences might inform housing packages.

**50 respondents · 500 choice tasks · 1,000 alternative-level rows · 2 conditional-logit specifications**

[Original report](https://docs.google.com/document/d/1iJ0LufFGdxyDRL1TMuc9pA1sRtVlR1msDCfr5XwHHyc/edit) · [Methods and results](docs/methods-and-results.md) · [Project scope and authorship](docs/project-notes.md)

## The question

> Which amenities do students value, how do preferences vary by budget and current living situation, and how should a housing provider use that information?

The final assignment placed me in a consulting scenario for **Lakeside Property Group**, a hypothetical company entering Northwestern's off-campus housing market. This was a course project using supplied survey data, rather than a client engagement or a survey I administered.

## Data and approach

Each respondent selected between two housing alternatives in ten tasks. The survey also recorded current living situation and housing budget.

| Step | What I analyzed |
| --- | --- |
| Data preparation | Reshaped choices into long format and matched each option to its housing characteristics |
| Baseline model | Estimated a conditional logit with 10 housing characteristics |
| Segmentation model | Added 7 interactions with budget and current living situation |
| Economic interpretation | Used coefficient ratios to discuss willingness to pay |
| Strategy | Proposed budget, convenience, and premium packages, conditional on costs and uncertainty |

The saved Stata output records **1,000 matched alternative-level rows**. These represent 50 people making repeated choices, not 1,000 independent survey respondents.

## Results

| Specification | Log likelihood | McFadden pseudo-R² |
| --- | ---: | ---: |
| Baseline | −323.47535 | 0.0666 |
| With consumer-characteristic interactions | −309.36353 | 0.1074 |

The expanded model fit the observed choices better in sample. This is not an out-of-sample prediction result, and pseudo-R² is not the fraction of variance explained by an OLS model.

Some interaction estimates suggested differences between student segments: higher-budget students were less price-sensitive in the fitted model, and current dorm residents showed an additional preference for furnishing. Most individual amenity estimates were imprecise, and the rent coefficient was not statistically significant in either model.

## Strategic implications

The report proposed three packages:

- **Budget:** lower rent and basic amenities.
- **Convenience:** furnishing, utilities, and laundry access.
- **Premium:** selected higher-service amenities and location/space features.

The economic framework is to compare the value students place on an amenity with its cost of provision. Actual amenity-cost data were not available, so these are proposed packages, not demonstrated profit-maximizing products.

## What I would improve in the survey

I recommended a larger sample, a “neither option” choice, more student characteristics, and more independent variation in amenities. Those changes would help separate preferences and make the choice setting more realistic.

## Important limitations

The study has only 50 respondents and ten fixed choice tasks. Responses repeat within people, some features move together, and many estimates have wide uncertainty. Willingness-to-pay ratios are particularly sensitive to the imprecisely estimated rent coefficient, so I do not headline dollar valuations here.

The [methods notes](docs/methods-and-results.md) explain these limits and distinguish historical results from interpretation.

## My contribution and materials

I authored the final report and used AI assistance with the software. This repository's portfolio narrative was prepared later with AI assistance from that report, the assignment, and the saved Stata output.

This is documentation of the completed project. The original report and analysis have not been changed or rerun. No respondent-level survey data, raw Stata session log, or reconstructed code is included.

The report link retains its current Drive permissions; this repository does not change access to the source document.
