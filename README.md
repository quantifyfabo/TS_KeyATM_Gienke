# Tracking Foreign News Attention: Tagesschau vs. Google Trends

R pipeline that identifies topics in Tagesschau foreign news (2024, n = 5,316 articles)
using Structural Topic Models (STM) and Keyword-Assisted Topic Models (keyATM)
and tests how well coverage matches public interest in Google Trends search data.

**Paper:** [Working paper (PDF / ResearchGate [link](https://doi.org/10.13140/RG.2.2.30589.32484))]

## Key findings
- Coverage of "USA", "Middle East" and "Ukraine" tracks public interest closely over the year.
- Other topics, notably "EU", show no significant correlation.

![Topic prevalence vs. Google Trends](figures/[your_best_plot].png)

## Pipeline
| Step | Script | Purpose |
|------|--------|---------|
| 1 | `TS_01_API.Rmd` | Collect articles from the Tagesschau API |
| 2 | `TS_02_GoogleTrends_Setup.R` | Collect Google Trends data |
| 3 | `TS_03_DataPreperation.R` | Clean and prepare text data |
| 4 | `TS_04_STM.R`, `TS_04_keyATM.R` | Fit topic models |
| 5 | `TS_05_Merging.R` | Merge topics with Google Trends |
| 6 | `TS_06_Visualize.R` | Produce figures |

## Data
`datasets/` contains [a sample of the data / the aggregated topic-share and Google Trends
series]. [Short note on what is included and what is not.]

## Reproduce
Run the scripts in order (TS_01 to TS_06). Required packages:
`dplyr, tidyverse, quanteda, httr, jsonlite, lubridate, rvest, xml2, tibble, magrittr, stm, keyATM`

## Tools
R, STM, keyATM, quanteda, Google Trends data, tidyverse
