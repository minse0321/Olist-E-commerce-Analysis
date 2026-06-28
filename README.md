# 🛒 Olist 🇧🇷Brazilian E-Commerce Analysis

## Overview
End-to-end analysis of 100,000+ real Brazilian e-commerce transactions from Olist (2016–2018).  
This project goes beyond EDA to apply **statistical hypothesis testing** to validate business insights.

## Key Question
> **Does late delivery significantly impact customer review scores — and can we prove it statistically?**

## Key Findings
1. **Late delivery drops review scores by 1.649 points** (4.21 → 2.56, t=112.58, p<0.001)
2. **North region customers rate lower than South** (3.92 vs 4.11, t=7.41, p<0.001)
3. **Payment type significantly affects late delivery rate** (boleto 8.22% vs voucher 6.64%, χ²=21.61, p<0.001)
4. **Black Friday 2017** caused the single largest monthly revenue spike in the dataset
5. **bed_bath_table** is the top revenue category but scores below average in reviews

## Statistical Tests Applied
| Test | Question | Result |
|---|---|---|
| Independent t-test | On-time vs late delivery → review score | p < 0.001 ✅ Significant |
| Independent t-test | South vs North region → review score | p < 0.001 ✅ Significant |
| Chi-square test | Payment type → late delivery rate | p < 0.001 ✅ Significant |

## Business Recommendations
| Priority | Issue | Action |
|---|---|---|
| 🔴 High | Late delivery → review score drops to 2.56 | Proactive delay notification + automatic compensation coupon |
| 🟠 Medium | North region avg delivery 20+ days | Add logistics hub in Northern Brazil |
| 🟡 Low | Boleto payment has highest late rate (8.22%) | Automate boleto processing to reduce approval delay |

## Tech Stack
| Tool | Usage |
|---|---|
| Python (Google Colab) | Data cleaning, EDA, statistical testing |
| Pandas | Data wrangling, JOIN, aggregation |
| Matplotlib / Seaborn | Exploratory visualizations |
| SciPy | t-test, chi-square hypothesis testing |
| Tableau Public | Interactive dashboard |

## Data Pipeline
1. 9 raw CSV files (Olist Kaggle dataset)
2. Preprocessing — status filter, datetime conversion, outlier removal, 9-table JOIN
3. EDA — monthly / hourly / category / region analysis
4. Hypothesis Testing — t-test × 2, chi-square × 1
5. Business Recommendations
6. Tableau Dashboard

## Project Structure
olist-ecommerce-analysis/

├── README.md

├── Olist_Ecommerce_Analysis.ipynb

└── data/

└── olist_master.csv

## Dataset
- Source: [Kaggle — Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- Period: September 2016 – September 2018
- Original: 9 CSV files, 99,441 orders
- After preprocessing: 107,489 rows × 27 columns
- Note: Raw data not included due to file size. Download from Kaggle and run the notebook to reproduce.

## Dashboard
🔗 [[View on Tableau Public]](https://public.tableau.com/app/profile/minseo.choi4768/viz/Olist_E-commerce_Analysis/Olist_Dashboard?publish=yes)(#)
