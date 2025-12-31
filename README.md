# Web3 Trading Analysis: Trader Behavior vs. Market Sentiment

## 🔗 Project Access

> **Note to Reviewers:** As per the assignment instructions, the full interactive analysis is available via Google Colab.
> **[Click here to view the Google Colab Notebook](https://colab.research.google.com/drive/1zhj4NputC7k2k65pnceD1w1NTIVP_WH7?usp=sharing)**

---

## 📂 Directory Structure

This repository strictly follows the standardized submission format required for the Data Science Assignment:

```text
ds_Tahseen/
├── notebook_1.ipynb       # Main analysis, data cleaning, and EDA (Google Colab)
├── ds_report.pdf          # Final summarized insights and strategic explanations
├── README.md              # Setup instructions and project overview
├── csv_files/             # Processed data and aggregated statistics
│   ├── sentiment_pnl_summary.csv
│   └── daily_trading_metrics.csv
└── outputs/               # Visual outputs, graphs, and charts
    ├── volume_analysis.png
    ├── profitability_analysis.png
    ├── leverage_risk.png
    └── trader_bias_signal.png

```

---

## 📈 Executive Summary

This project analyzes the relationship between the **Bitcoin Fear & Greed Index** and historical trader data from **Hyperliquid**.

The core finding is a **"Momentum Alpha" signal**: while trading volume peaks during market "Fear" (suggesting high activity during liquidations and dip-buying), the most successful trading behavior occurs during "Extreme Greed." Traders in this dataset are primarily momentum-driven, showing a **3x increase in capital efficiency** when the market sentiment is strongly bullish.

---

## 🔍 Key Insights & Hidden Trends

### 1. The Volume-Sentiment Paradox

* **Observation:** Total volume is highest during **Fear ($483M)**.
* **Trend:** High sentiment volatility acts as a catalyst for activity, but not necessarily for profitability.

### 2. The Profitability Zenith (Hidden Signal)

* **Observation:** Win rates surge to **89%** during **Extreme Greed**.
* **Signal:** Capital Efficiency (PnL per $1k traded) rises from **9.48 in Fear** to **28.24 in Greed**. This identifies a clear signal: the analyzed traders are highly effective at "trend-riding" but struggle in contrarian/reversal environments.

### 3. Leverage & Risk Behavior

* **Observation:** Usage of **Cross Leverage** expands significantly as sentiment moves from Neutral to Greed.
* **Risk:** This creates a "Liquidation Cliff"—traders are most over-leveraged exactly when the market is reaching a local top, increasing systemic risk.

---

## 🛠️ Technical Setup

### Data Sources

1. **Bitcoin Market Sentiment:** Daily Fear/Greed classification.
2. **Historical Trader Data:** Execution prices, PnL, leverage mode, and trade sizes.

### Requirements

To reproduce the analysis locally or in Colab, you will need:

* `pandas`
* `matplotlib`
* `seaborn`
* `numpy`

### How to Run

1. Clone the repository: `git clone https://github.com/TahseenRaza11/ds_Tahseen.git`
2. Upload `notebook_1.ipynb` to Google Colab.
3. Ensure the CSV datasets are in the same root directory as the notebook.
4. Run all cells to regenerate the `outputs/` and `csv_files/`.
