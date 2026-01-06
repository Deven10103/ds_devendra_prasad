# Trader Behavior Analysis Under Fear and Greed Market Regimes

## Project Overview

This project analyzes how trader behavior varies across different market sentiment regimes using historical trade-level data and the Bitcoin Fear & Greed Index. Trader activity and outcomes are aggregated at a daily level and compared across Fear and Greed regimes using distributional analysis and non-parametric statistical tests. The repository contains a reproducible Google Colab notebook, derived datasets, visual outputs, and a summarized report of key findings.

---

## Datasets Used

### 1. Market Sentiment Dataset
- Source: Bitcoin Fear & Greed Index  
- Granularity: Daily  
- Sentiment labels grouped as:
  - **Fear regime:** Fear, Extreme Fear  
  - **Greed regime:** Greed, Extreme Greed  

### 2. Trader Activity Dataset
- Trade-level historical data  
- Key fields used:
  - Timestamp
  - Account identifier
  - Trade size (USD)
  - Realized profit and loss (`Closed PnL`)
- Outcome-related metrics are computed **only for trades with realized PnL**.

---

## Repository Structure
```
ds_devendra_prasad/
├── notebooks/
│   └── Notebook_1.ipynb          # Google Colab notebook with full analysis pipeline
│
├── csv_files/                    # Derived and intermediate datasets
│   ├── fear_greed_index.csv
│   ├── fg_df_date_check.csv
│   ├── historical_data.csv
│   ├── daily_market_activity.csv
│   ├── daily_trader_behavior.csv
│   ├── daily_behavior_with_sentiment.csv
│   ├── trade_outcomes_distribution.csv
│   ├── accounts_trade_frequency.csv
│   └── fear_vs_greed_comparison.csv
│
├── outputs/                      # Saved visualizations and figures
│   ├── Behavioral Metrics.png
│   ├── Behavioral Trading Activity Timeline.png
│   ├── Market Sentiment Distribution.png
│   ├── Market Sentiment Monthly Distribution.png
│   ├── Market Sentiment Timeline.png
│   ├── Market Sentiment Timeline (Heatmap).png
│   ├── PnL Analysis Distribution.png
│   ├── PnL Analysis Gain vs Loss.png
│   └── PnL Analysis Timeline.png
│
├── ds_report.pdf                 # Final consolidated report
└── README.md                     # Project overview, methodology, and execution guide
```

---

## Analysis Flow

The analysis follows a structured and reproducible workflow:

1. Data loading and preprocessing  
2. Time parsing and separation of activity vs outcome metrics  
3. Exploratory data analysis for scale and distribution understanding  
4. Daily aggregation of trader behavior  
5. Data quality filtering and validation  
6. Alignment with sentiment data  
7. Regime-based comparison between Fear and Greed  
8. Visualization and statistical testing  

---

## Key Deliverables

- **`notebook_1.ipynb`**  
  Reproducible Google Colab notebook containing the complete analysis.

- **`ds_report.pdf`**  
  Concise report summarizing methodology, findings, interpretation, and limitations.

- **`csv_files/`**  
  Intermediate and final datasets used for regime comparison.

- **`outputs/`**  
  Visual evidence supporting the reported insights.

---

## How to Review / Reproduce

1. Open the Google Colab notebook using the provided link.  
2. Notebook access is set to **“Anyone with the link can view.”**  
3. Run all cells sequentially to reproduce the analysis and outputs.  
4. Refer to `ds_report.pdf` for summarized insights and interpretation.

---

## Notes and Assumptions

- This analysis is **observational** and does not establish causality.  
- Trader behavior is aggregated at a **daily level** to align with sentiment data.  
- Low-activity days are filtered to ensure statistical reliability.  
- The Fear & Greed Index is used as a coarse proxy for market sentiment.

---



