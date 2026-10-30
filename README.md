# portfolio-risk-and-derivatives

Historical VaR & Risk Contribution · European Option Pricing & Monthly Hedging

Independent, AI-assisted portfolio research using traceable public historical inputs. Real observations and analyst-created scenarios are labelled separately.

## Projects
- [Historical VaR & Risk Contribution](projects/historical-risk/README.md) — Market risk · Portfolio oversight
- [European Option Pricing & Monthly Hedging](projects/option-hedging/README.md) — Derivatives analytics · Model risk

## Reproduce
Requires Node.js 22 or later; no third-party packages. Run `node analysis.mjs`. Frozen inputs are included under data/. Calculated outputs are in projects/. Raw source documentation and assumptions are in each project README.

## Data provenance
Kenneth French Data Library: https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html. September 2026 CRSP vintage; monthly rows 200001–202512. Original percentages converted to decimal returns. Only the first value-weighted monthly table is used. Upstream historical revisions mean these are not point-in-time data. Download files: F-F_Research_Data_Factors_CSV.zip and 6_Portfolios_2x3_CSV.zip under https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/ftp/.

Retrieved 2026-10-30. Upstream data remain subject to their source terms; no ownership of source data is claimed.

## Checks
The script checks date alignment, valid observations, risk contribution totals, a standard option-pricing reference value and the projected balance-sheet equation.
