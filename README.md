# SME Internationalization

   **Author:** Christoph Schößwendter

   ## Research Question

   Does R&D intensity positively affect firm performance among European SMEs, and does firm size moderate this relationship?

   *Note: The originally planned DOI (Degree of Internationalization) variable was dropped because `pifo` (foreign income) is not available in Compustat Global, and `rect/sale` produces extreme outliers for SMEs. The research design was updated to R&D intensity, which has 100% coverage in our sample.*

## Hypotheses

   - **H1:** R&D intensity affects RoA (expensing effect expected in short run)
   - **H2:** Firm size positively moderates the R&D intensity – RoA relationship
   
## Variables

| Variable | Field(s) | Formula | Role |
|----------------|-------------|----------------------|----------------|
| RoA | ib, at | ib / at | Dependent (Y) |
| R&D intensity | xrd, at | xrd.fillna(0) / at | Independent |
| R&D x Size | - | rd_intensity x ln_at | H2 interaction |
| Firm size | at | log(at) | Moderator+Ctrl |
| Leverage | dltt, at | dltt / at | Control |
| CAPX intensity | capx, at | capx / at | Control |
| Cash ratio | che, at | che / at | Control |

## Data

| Item | Detail |
|------|--------|
| Source | WRDS / Compustat Global |
| Table | comp_global_daily.g_funda |
| Downloaded | 2026-06-09 |
| License | WRDS subscriber agreement |
| Fiscal years | 2015–2024 |
| Raw rows | 338,491 |
| Clean rows | 26,091 |
| Geography | All (no country filter) |

## Results

- R&D intensity has a robust negative effect on contemporaneous RoA among European SMEs (β = -0.55, p < 0.001 in TWFE), consistent with the expensing hypothesis (H1 supported).
- Firm size does not moderate this relationship (β(R&D × size) = 0.09, n.s.), so larger SMEs do not benefit disproportionately from R&D investment (H2 not supported, although the sign points in the predicted direction).
- The R&D effect shrinks by ~30% when moving from OLS to two-way fixed effects (-0.79 → -0.55), indicating substantial omitted-variable bias in pooled estimates — firm-level heterogeneity is essential to control for.
