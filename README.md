# Market Analysis and Stock Segmentation Using RFM
**6BUIS017W CRM & CM with Business Intelligence – Individual Coursework (CWK1)**

Segments S&P 500 shares using (1) risk-return features (mean weekly return, weekly beta) and
(2) adapted RFM trading-activity features, with Ward and K-means clustering, sensitivity analysis
and a data mart design.

## How to run
1. Open `CRM_CM_CW1.ipynb` in Google Colab (link at the top of the notebook).
2. **Runtime → Run all.** The notebook loads the preserved data snapshot from `data/`,
   so results reproduce exactly without re-downloading.

## Study settings
| Item | Value |
|---|---|
| Constituent list | Wikipedia S&P 500 list, retrieved 2026-11-21 (503 securities) |
| Price data | Yahoo Finance via yfinance, 2021-01-01 to 2025-01-01 (end exclusive) |
| Benchmark | ^GSPC |
| Valid shares | 486 (17 excluded – see `outputs/exclusion_log.csv`) |
| Observation date | 2024-12-31 |
| Package versions | Printed in notebook Cell 1; download versions in `data/download_metadata.json` |

## Repository structure
| Folder / file | Contents |
|---|---|
| `CRM_CM_CW1.ipynb` | Full analysis: Task 1 (data and features), Task 2 (clustering), Task 3 (BI review) |
| `data/` | Preserved snapshots: ticker list, daily prices (parquet), download metadata |
| `outputs/` | Feature table, exclusion and validation logs, cluster assignments, figures |

## Development
Each task was developed on its own branch (`task1_data_prep`, `task2_clustering`,
`task3_bi_review`) and merged into `main` via pull requests.

## Use of generative AI
Claude (Anthropic) assisted with planning, explaining concepts, and writing and debugging code,
building on the module tutorial notebooks. See the AI declaration in the report appendix.
