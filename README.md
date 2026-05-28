# Project 01 — Statistical Analysis and Modeling of Stock Market Data

## Stocks Analyzed
`AAPL` · `AMZN` · `GOOGL` · `MSFT` · `NVDA`  
**Period:** 2022-01-03 — 2025-12-31 (1003 trading days)

---

## Project Structure

```
├── main.ipynb                  # Main notebook — all analysis
├── requirements.txt            # Python dependencies
├── data/
│   ├── close_prices_full.csv   # Adjusted close prices (raw)
│   ├── simple_returns_full.csv # Daily simple returns
│   └── log_returns_full.csv    # Daily log-returns (primary variable)
└── plots/
    ├── price_rolling_mean.png  # Close prices + 30-day rolling mean
    ├── simple_returns.png      # Simple returns per ticker (subplots)
    ├── log_daily_returns.png   # Log-returns per ticker (subplots)
    ├── histograms.png          # Return histograms per ticker
    ├── boxplots.png            # Return boxplots all tickers
    ├── heatmap.png             # Correlation matrix heatmap
    ├── scatter_plots.png       # Pairwise scatter plots (10 pairs)
```

---

## Notebook Structure (`main.ipynb`)

### Part 1 — Data Collection and Preparation
- Download adjusted close prices via `yfinance`
- Compute simple and log-returns

### Part 2 — Descriptive Statistics
- Price time series + 25-day rolling mean
- Simple and log-return time series
- Summary statistics (mean, std, skewness, kurtosis)
- Histograms, boxplots

### Part 3 — Comparative and Interrelation Analysis
- Correlation matrix
- Heatmap, pairwise scatter plots, pair plot

### Part 4 — Hypothesis Testing
- One-sample t-test: mean log-return vs zero (per ticker)
- Two-sample t-test: MSFT vs GOOGL mean returns

### Part 5 — Modeling (Multiple Linear Regression)
- OLS regression: NVDA ~ AAPL + AMZN + GOOGL + MSFT
- Coefficient interpretation, R², F-statistic

---

## Setup

```bash
pip install -r requirements.txt
jupyter notebook main.ipynb
```
