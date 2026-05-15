# 📈 Stock Performance Analyzer

A Python-based financial data analysis project that pulls real market data, calculates key performance metrics, and visualizes 1-year stock returns against the S&P 500 benchmark.

---

## 🔍 Project Overview

This project answers a simple but important question: **How did a selection of major stocks perform over the past year — and did they beat the market?**

Using real market data fetched via the `yfinance` library, this notebook walks through a full data analysis workflow: data ingestion, cleaning, metric calculation, visualization, and interpretation.

---

## 📊 Key Findings

Analysis was run on **MSFT, AAPL, JPM, GS, and SPY** over a 1-year period:

| Ticker | Total Return | Volatility | Sharpe-like Ratio |
|--------|-------------|------------|-------------------|
| GS     | +59.90%     | 1.68%      | 0.1204            |
| AAPL   | +39.00%     | 1.42%      | 0.0999            |
| SPY    | +27.23%     | 0.76%      | **0.1308**        |
| JPM    | +18.17%     | 1.33%      | 0.0568            |
| MSFT   | -8.52%      | 1.49%      | -0.0164           |

**Notable takeaways:**
- **GS** was the top raw performer, more than doubling the SPY benchmark return
- **SPY** had the best risk-adjusted return (Sharpe-like ratio), reinforcing why it's the standard benchmark
- **MSFT's** negative return despite being an AI infrastructure leader illustrates that strong businesses don't always mean strong near-term stock performance — valuation compression after years of outsized growth played a role
- Only **GS and AAPL** meaningfully outperformed the benchmark on a raw return basis

---

## 🛠️ Tech Stack

- **Python 3.13**
- **yfinance** — real market data fetching
- **pandas** — data manipulation and summary statistics
- **matplotlib / seaborn** — data visualization
- **Jupyter Notebook** — interactive analysis environment

---

## 📁 Project Structure

```
project1-stock-analyzer/
│
├── project1_stock_analyzer.ipynb   # Main analysis notebook
├── cumulative_returns.png          # Line chart: cumulative returns over time
├── total_returns_bar.png           # Bar chart: total return by ticker
└── README.md                       # This file
```

---

## 🚀 How to Run

1. **Clone the repo**
   ```bash
   git clone https://github.com/bdubs78/project1-stock-analyzer.git
   cd project1-stock-analyzer
   ```

2. **Install dependencies**
   ```bash
   pip install yfinance pandas matplotlib seaborn jupyter
   ```

3. **Launch Jupyter**
   ```bash
   jupyter notebook
   ```

4. Open `project1_stock_analyzer.ipynb` and run cells sequentially.

> **Note:** Data is fetched live from Yahoo Finance each time the notebook runs, so results will reflect the most recent 1-year window from your run date.

---

## 📖 Skills Demonstrated

- Fetching and ingesting real financial time-series data with `yfinance`
- DataFrame manipulation with `pandas` (`pct_change()`, `cumprod()`, `groupby()`, `describe()`)
- Calculating financial metrics: total return, daily return, volatility, and Sharpe-like ratio
- Data visualization with `matplotlib` and `seaborn`
- Working with date ranges and time-series indexing
- Translating raw data into business insights

---

## 👤 Author

**Bryan White**
- 📧 bmichaelw1778@gmail.com
- 💼 [LinkedIn](https://www.linkedin.com/in/bryan-white-54486b1a8/)
- 🐙 [GitHub](https://github.com/bdubs78)

---

## 🗺️ What's Next

This is **Project 1 of 3** in my Python data science portfolio, built as part of a structured transition from enterprise data architecture into data science.

- **Project 2:** S&P 500 Sector Analysis — groupby, merging DataFrames, correlation heatmaps
- **Project 3:** Earnings Surprise & Stock Reaction Study — hypothesis testing, date joins, storytelling with data
