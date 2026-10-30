# European Option Pricing & Monthly Hedging

How large is discrete hedging error on historical return paths?

## Role relevance
Derivatives analytics · Model risk

## Data
2000–2025 monthly data; evaluation 2010–2025. Source: https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html. Retrieved 2026-10-30.

## Method
Create a total-return index rebased to 100 at each January. Price a hypothetical one-year ATM European call using Black–Scholes, 36 trailing monthly log returns for volatility, and the preceding RF month annualized as a constant financing rate. Sell one call and delta-hedge monthly, with 5bp per dollar traded, including entry and terminal liquidation. Repeat 2010–2025.

## Findings
Across 16 historical paths, mean replication error was -0.06 index units; mean absolute error was 1.86.

- 16 historical paths
- MAE 1.86 index points
- 5bp trading cost

## Interpretation and limits
The underlying path is derived from real market total returns; the contract is hypothetical. Prices are model values, not observed option quotes or implied volatilities. Monthly observations miss intramonth hedging risk. The index reinvests dividends, so the model uses no separate dividend yield.

See [computed results](results.csv). Reproduce with `node analysis.mjs` from the repository root. This is an independent, AI-assisted portfolio case study, not employment experience or a company-issued forecast.
