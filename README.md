# 📈 Financial EDA — Stock Market Analysis (AAPL · TSLA · MSFT)

A complete Exploratory Data Analysis (EDA) project on stock market data,
built as part of my ATLAS self-directed ML engineering roadmap.

This project covers the full data science workflow: data collection,
cleaning, feature engineering, statistical analysis, and professional
visualization — applied to 3 years of stock price data.

---

## 🛠️ Tech Stack

| Tool             | Purpose                              |
| ---------------- | ------------------------------------ |
| Python 3.11      | Core language                        |
| Pandas           | Data loading, cleaning, manipulation |
| NumPy            | Numerical computing, returns math    |
| Matplotlib       | All chart visualizations             |
| Seaborn          | Correlation heatmap styling          |
| yfinance         | Yahoo Finance data API               |
| Jupyter Notebook | Interactive development environment  |

---

## 📁 Project Structure

financial-eda-project/
├── data/ # Raw and processed datasets
│ ├── close*prices.csv # Simulated price data (GBM)
│ ├── clean_prices.csv # Cleaned and validated prices
│ ├── daily_returns.csv # Daily % returns per stock
│ ├── cumulative_returns.csv # Compounded growth from day 1
│ ├── rolling_volatility.csv # 30-day rolling annualized vol
│ └── ma*[ticker].csv # Moving averages per stock
├── notebook/
│ └── financial_eda.ipynb # Full analysis notebook (30 cells)
├── outputs/ # All generated charts
│ ├── 01_price_history.png
│ ├── 02_moving_averages.png
│ ├── 03_returns_distribution.png
│ ├── 04_cumulative_returns.png
│ ├── 05_correlation_heatmap.png
│ └── 06_rolling_volatility.png
├── requirements.txt
└── README.md

---

## 🔬 Analysis Performed

### 1. Data Collection

- Stock prices simulated using **Geometric Brownian Motion (GBM)**
  with real starting prices and empirically calibrated volatility parameters
- GBM is the mathematical foundation of the Black-Scholes options
  pricing model — the same framework used in quantitative finance

### 2. Data Cleaning

- Missing value detection and handling
- Duplicate row removal
- Data type validation and enforcement
- Price sanity checks (no zeros or negatives)
- Outlier detection via Z-score analysis
- Date gap analysis for trading day continuity

### 3. Feature Engineering

- **Daily Returns:** `pct_change()` — % gain/loss per trading day
- **Cumulative Returns:** compounded growth from day 1
- **50-Day Moving Average:** short-term trend signal
- **200-Day Moving Average:** long-term trend signal
- **Rolling Volatility:** 30-day annualized standard deviation
- **Risk/Return Ratio:** simplified Sharpe-style metric

### 4. Exploratory Data Analysis

- Summary statistics (mean, std, min/max, skewness, kurtosis)
- Volatility comparison across stocks
- Correlation analysis of daily returns
- Extreme day identification (best/worst single-day moves)
- Risk-adjusted return ranking

---

## 📊 Charts

| Chart                | Description                                           |
| -------------------- | ----------------------------------------------------- |
| Price History        | 3-year price journey for all 3 stocks                 |
| Moving Averages      | AAPL with 50-day and 200-day MAs + Golden Cross zones |
| Returns Distribution | Histogram of daily returns per stock                  |
| Cumulative Returns   | Growth of $1 invested from Jan 2022                   |
| Correlation Heatmap  | Return correlation between stock pairs                |
| Rolling Volatility   | 30-day annualized volatility over time                |

---

## 🧠 Key Insights

### Volatility

- **TSLA** is the most volatile stock (~65% annualized) —
  roughly 2.5x more volatile than AAPL and MSFT
- AAPL and MSFT behave more like each other than either
  does like TSLA

### Returns

- **AAPL** delivered the strongest 3-year total return
- **TSLA** had the lowest return despite its extreme volatility —
  high risk did not translate to proportional reward
- **MSFT** had the best risk-adjusted return (highest Sharpe-style ratio)

### Correlation

- AAPL and MSFT are highly correlated — holding both provides
  less diversification benefit than their price difference suggests
- TSLA provides more diversification value due to lower correlation
  with the other two

### Moving Averages

- Golden Cross and Death Cross signals are visible in the AAPL chart
- The 200-day MA acts as strong support/resistance during trend reversals

---

## ⚙️ Setup & Run

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/financial-eda-project.git
cd financial-eda-project

# Create and activate environment
conda create -n atlas python=3.11
conda activate atlas

# Install dependencies
pip install -r requirements.txt

# Launch notebook
cd notebook
jupyter notebook financial_eda.ipynb
```

---

## 🚀 Future Improvements

- [ ] Pull live data via yfinance when rate limits allow
- [ ] Add Bollinger Bands for advanced trend analysis
- [ ] Build an interactive dashboard using Plotly/Dash
- [ ] Add portfolio optimization using Modern Portfolio Theory
- [ ] Extend to 10+ stocks across different sectors

---

## 👤 Author

**Ved** — Self-directed ML Engineering student  
Building toward MS in ML/AI (Canada, Fall 2028)  
ATLAS Roadmap — Phase 0

[GitHub](https://github.com/vedpatel-real-ai) ·
[LinkedIn](https://www.linkedin.com/in/ved-patel-93b780344/)

---

_Built as part of the ATLAS self-directed AI/ML engineering roadmap._
