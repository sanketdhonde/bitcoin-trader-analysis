# Bitcoin Trader Performance vs Market Sentiment Analysis

Analysis of the relationship between trader performance on Hyperliquid and Bitcoin market sentiment (Fear/Greed Index).

## Project Overview

This project explores hidden patterns and correlations between:
- **Trader Performance Metrics**: Win rates, PnL, leverage, risk-adjusted returns
- **Market Sentiment**: Fear/Greed Index classifications
- **Trading Behavior**: Volume, position sizes, risk-taking patterns

## Datasets

1. **Bitcoin Market Sentiment Dataset**
   - Columns: Date, Classification (Fear/Greed)
   - Source: Fear & Greed Index

2. **Historical Trader Data from Hyperliquid**
   - Columns: account, symbol, execution price, size, side, time, start position, event, closedPnL, leverage, etc.

## Project Structure

```
bitcoin-trader-analysis/
├── data/
│   ├── raw/
│   │   ├── hyperliquid_traders.csv
│   │   └── fear_greed_index.csv
│   ├── processed/
│   └── README.md
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_trader_performance_analysis.ipynb
│   ├── 04_sentiment_analysis.ipynb
│   └── 05_pattern_discovery.ipynb
├── src/
│   ├── __init__.py
│   ├── data_loader.py
│   ├── data_cleaner.py
│   ├── performance_metrics.py
│   ├── sentiment_analyzer.py
│   └── visualizations.py
├── reports/
│   ├── analysis_summary.md
│   └── insights.md
├── requirements.txt
├── .gitignore
└── README.md
```

## Key Analysis Areas

### 1. Data Exploration & Preparation
- Load and understand both datasets
- Data quality assessment
- Timestamp alignment
- Missing value handling

### 2. Trader Performance Metrics
- Win rate calculation
- Average PnL analysis
- Risk-adjusted returns (Sharpe ratio)
- Win/loss ratios
- Leverage analysis

### 3. Market Sentiment Analysis
- Fear vs Greed period identification
- Sentiment transitions
- Trader behavior during different sentiment phases

### 4. Pattern Discovery
- Correlation analysis: Sentiment vs Performance
- Trader archetypes identification
- Optimal trading conditions
- Risk-taking behavior patterns

### 5. Insights & Recommendations
- Key findings visualization
- Strategy recommendations
- Risk management insights

## Installation

### Prerequisites
- Python 3.8+
- pip

### Setup

```bash
# Clone the repository
git clone https://github.com/sanketdhonde/bitcoin-trader-analysis.git
cd bitcoin-trader-analysis

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start Jupyter
jupyter notebook
```

## Usage

1. **Place your data files in `data/raw/`**:
   - `hyperliquid_traders.csv`
   - `fear_greed_index.csv`

2. **Run notebooks in order**:
   - `01_data_exploration.ipynb` - Initial data assessment
   - `02_data_cleaning.ipynb` - Data preparation
   - `03_trader_performance_analysis.ipynb` - Calculate metrics
   - `04_sentiment_analysis.ipynb` - Sentiment analysis
   - `05_pattern_discovery.ipynb` - Find patterns & correlations

## Key Findings (To be updated)

Coming soon as analysis progresses...

## Dependencies

- pandas: Data manipulation
- numpy: Numerical computations
- matplotlib: Visualization
- seaborn: Statistical visualizations
- scipy: Statistical analysis
- scikit-learn: Machine learning utilities

See `requirements.txt` for full list.

## Author

sanketdhonde

## License

MIT License
