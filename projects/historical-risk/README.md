# Historical VaR & Risk Contribution

How often does a rolling historical loss estimate fail?

## Role relevance
Market risk · Portfolio oversight

## Data
2000–2025 monthly inputs; rolling VaR evaluation 2005–2025. Source: https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html. Retrieved 2026-10-30.

## Method
Equal-weight six equity style portfolios, rebalanced monthly, gross of costs. Each monthly 95% VaR and expected shortfall estimate uses only the preceding 60 months. Quantile uses floor(0.05 × (n−1)); tail average includes observations at or below that quantile. Variance contributions use the 2010–2025 covariance matrix. Examine 2008 and 2020 directly in results.

## Findings
14 of 252 months breached the rolling loss threshold (5.56%). Portfolio risk contributions sum to 100%.

- Breach rate 5.56%
- 252 rolling observations
- 60-month lookback

## Interpretation and limits
A 60-month sample provides very few tail observations. VaR is a one-month return-loss estimate, not a daily measure or a maximum possible loss. Six equity styles offer limited cross-asset diversification.

See [computed results](results.csv). Reproduce with `node analysis.mjs` from the repository root. This is an independent, AI-assisted portfolio case study, not employment experience or a company-issued forecast.
