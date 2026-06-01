# Bitcoin Trader Performance vs Market Sentiment Analysis

## Project Overview

This project investigates the relationship between Bitcoin market sentiment and trader performance using the Bitcoin Fear & Greed Index and Hyperliquid historical trading data.

The objective is to determine how market sentiment influences:

* Trader profitability
* Win rates
* Trading activity
* Position sizing behavior
* Transaction costs
* Overall trading efficiency

The analysis combines over **211,000 real trading records** with daily Bitcoin market sentiment data to uncover actionable insights and hidden trading patterns.

---

## Datasets

### 1. Bitcoin Fear & Greed Index Dataset

**Records:** 2,644

**Columns:**

* Timestamp
* Value
* Classification
* Date

**Sentiment Categories:**

* Extreme Fear
* Fear
* Neutral
* Greed
* Extreme Greed

### 2. Hyperliquid Historical Trading Dataset

**Records:** 211,224 Trades

**Columns Used:**

* Account
* Coin
* Execution Price
* Size USD
* Size Tokens
* Direction
* Closed PnL
* Fee
* Timestamp IST

---

## Project Structure

```text
bitcoin-trader-analysis/
│
├── data/
│   ├── fear_greed_index.csv
│   └── historical_data.csv
│
├── notebooks/
│   └── analysis.ipynb
│
├── visualizations/
│   ├── avg_pnl_by_sentiment.png
│   ├── win_rate_by_sentiment.png
│   ├── trade_count_by_sentiment.png
│   ├── position_size_by_sentiment.png
│   └── top_10_traders.png
│
├── reports/
│   └── final_report.pdf
│
├── requirements.txt
└── README.md
```

---

## Methodology

### Data Preparation

* Loaded both datasets using Pandas
* Converted timestamps into a common date format
* Extracted trade dates from Hyperliquid timestamps
* Merged trading records with daily sentiment labels

### Feature Engineering

Created:

* Win Indicator (Closed PnL > 0)
* Sentiment-wise profitability metrics
* Trader-level performance summaries

### Analysis Performed

* Profitability Analysis
* Win Rate Analysis
* Trading Activity Analysis
* Position Size Analysis
* Fee Analysis
* Top Trader Analysis

---

## Key Findings

### Average Profitability by Sentiment

| Sentiment     | Average PnL |
| ------------- | ----------: |
| Extreme Greed |       67.89 |
| Fear          |       54.29 |
| Greed         |       42.74 |
| Extreme Fear  |       34.54 |
| Neutral       |       34.31 |

**Insight:** Extreme Greed periods generated the highest average profit per trade.

---

### Win Rate by Sentiment

| Sentiment     | Win Rate |
| ------------- | -------: |
| Extreme Greed |   46.49% |
| Fear          |   42.08% |
| Neutral       |   39.70% |
| Greed         |   38.48% |
| Extreme Fear  |   37.06% |

**Insight:** Traders were most successful during Extreme Greed periods.

---

### Trading Activity

| Sentiment     | Trade Count |
| ------------- | ----------: |
| Fear          |      61,837 |
| Greed         |      50,303 |
| Extreme Greed |      39,992 |
| Neutral       |      37,686 |
| Extreme Fear  |      21,400 |

**Insight:** Fear periods produced the highest trading activity.

---

### Average Position Size

| Sentiment     | Avg Position Size (USD) |
| ------------- | ----------------------: |
| Fear          |                   7,816 |
| Greed         |                   5,737 |
| Extreme Fear  |                   5,350 |
| Neutral       |                   4,783 |
| Extreme Greed |                   3,112 |

**Insight:** Traders deployed the largest positions during Fear periods.

---

### Average Trading Fee

| Sentiment     | Avg Fee |
| ------------- | ------: |
| Fear          |   1.495 |
| Greed         |   1.254 |
| Extreme Fear  |   1.116 |
| Neutral       |   1.045 |
| Extreme Greed |   0.676 |

**Insight:** Fear periods incurred the highest transaction costs.

---

## Top Trader Insights

The most profitable trader generated:

* Total Profit: **$2.14 Million**
* Win Rate: **33.7%**

Interestingly, another trader achieved:

* Win Rate: **81.1%**
* Total Profit: **$379K**

### Key Observation

A higher win rate does not necessarily lead to higher profitability.

Successful traders appear to focus on:

* Risk-reward optimization
* Position management
* Capturing large winning trades

rather than maximizing win frequency.

---

## Visualizations

The project includes:

* Average PnL by Sentiment
* Win Rate by Sentiment
* Trade Count by Sentiment
* Position Size by Sentiment
* Top 10 Traders by Profit
* PnL Distribution Analysis
* Correlation Heatmap

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Business Recommendations

### For Traders

* Avoid excessive position sizing during Fear periods.
* Focus on risk-reward ratio rather than win rate.
* Reduce unnecessary trading frequency to lower transaction costs.

### For Trading Platforms

* Implement risk-management alerts during high-fear markets.
* Provide analytics on trading efficiency.
* Educate traders on risk-reward optimization.

---

## Conclusion

The analysis demonstrates a clear relationship between Bitcoin market sentiment and trader behavior. Extreme Greed periods generate the highest profitability and win rates, while Fear periods drive the highest trading activity, largest position sizes, and highest transaction costs.

The findings suggest that disciplined risk management and effective trade execution are more important than simply increasing trade frequency or maintaining a high win rate.

---

## Author

**Sanket Dhonde**

## License

MIT License
