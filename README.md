# SME Internationalization

   **Author:** Christoph Schößwendter

   ## Research Question
   Is there a statistically significant relationship between global economic instability and the Degree of Internationalization of listed Austrian, German, and Swiss companies during the period 2008–2023?

   ## Hypotheses
   - H1: Higher levels of global economic instability are negatively associated with the Degree of Internationalization of listed Austrian, German, and Swiss firms.
   - H2: The negative effect of global economic instability on DOI is more pronounced with a oneyear lag than contemporaneously, reflecting the time required for strategic adjustment under sunk costs.
   - H3: Geopolitical risk has a stronger negative effect on the Foreign Assets to Total Assets ratio than on the Foreign Sales to Total Sales ratio, due to the higher irreversibility of foreign physical assets relative to export sales.
   - H4:  Larger and more profitable firms exhibit a smaller (less negative) sensitivity of DOI to global economic instability, reflecting stronger uncertainty-management capabilities
   - H5: The effect of global economic instability on DOI varies significantly across industries: cyclical and manufacturing-intensive sectors display stronger negative effects than utilities, healthcare, or consumer staples.
   - H6:  Country-level heterogeneity exists: Swiss firms exhibit lower uncertainty-sensitivity than Austrian and German firms, attributable to the safe-haven status of the Swiss franc and the high global diversification of Swiss multinationals.
## Variables

### Dependent variable (Y)

| Construct | Data Item(s) | Formula | Role |
|-----------|--------------|---------|------|
| RoA | IB, AT | IB / AT | Primary |
| EBITDA margin | EBITDA, SALE | EBITDA / SALE | Robustness |

### Independent variable (X)

| Construct | Data Item(s) | Formula | Role |
|-----------|--------------|---------|------|
| R&D Intensity | XRD, AT | XRD / AT | Primary |
| Cash Holdings | CHE, AT | CHE / AT | Robustness |

### Controls

| Construct | Data Item(s) | Formula |
|-----------|--------------|---------|
| Firm size | AT | log(AT) |
| Leverage | DLTT, DLC, SEQ | (DLTT + DLC) / SEQ |
| Firm age (proxy: Compustat tenure) | FYEAR, GVKEY | FYEAR - min(FYEAR by GVKEY) |
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
