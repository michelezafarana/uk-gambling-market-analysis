# UK Gambling Market Analysis (2018–2022)

## Overview
This project analyses market concentration in the UK gambling industry across three years: 2018, 2020, and 2022. Using firm-level data from the Orbis database, it computes key concentration indices to assess the competitive structure of the market and the impact of COVID-19.

## Data
- **Source:** Orbis database (Bureau van Dijk)
- **Sample:** 174 companies in England, NACE Rev.2 code 9200 (Gambling)
- **Variable:** Operating revenue (turnover) in GBP millions
- **Years:** 2018, 2020, 2022

## Methods
- Descriptive statistics: mean turnover, standard deviation, firm size distribution
- Market share computation for all firms
- Concentration indices:
  - **CR1** — market share of the largest firm (market leader)
  - **CR4** — combined share of the top 4 firms
  - **CR10** — combined share of the top 10 firms
  - **HHI** — Herfindahl-Hirschman Index
- Interpretation using Van Dam et al. (2021) thresholds
- Software: R and Stata

## Key Findings
| Year | CR1 (%) | CR4 (%) | CR10 (%) | HHI |
|------|---------|---------|----------|-----|
| 2018 | 15.81 | 39.97 | 71.00 | 654.45 |
| 2020 | 17.28 | 46.49 | 77.89 | 788.65 |
| 2022 | 13.90 | 44.99 | 72.41 | 696.89 |

- HHI below 1500 in all years → **unconcentrated market**
- CR4 between 40–46% → **moderate oligopolistic structure**
- Market concentration **increased in 2020** (COVID-19 effect: larger firms strengthened their position)
- Market concentration **decreased in 2022** → improved competitive conditions
- **William Hill Limited** was the market leader in all three years

## Structure
```
├── gambling_market_analysis.R   # Main analysis script
├── README.md                    # Project documentation
└── data/                        # Place your Orbis dataset here
    └── gambling_data.csv
```

## How to Run
1. Clone the repository
2. Place your Orbis dataset in the `data/` folder as `gambling_data.csv`
3. Open `gambling_market_analysis.R` and update the data loading section
4. Run the script in R or RStudio

## Requirements
```r
install.packages(c("dplyr", "ggplot2", "tidyr"))
```

## References
- Van Dam, Y. et al. (2021). Market Concentration and Competition Analysis.
- Orbis Database, Bureau van Dijk.

## Author
Michele Zafarana — MSc Business Analytics, University of Bologna
