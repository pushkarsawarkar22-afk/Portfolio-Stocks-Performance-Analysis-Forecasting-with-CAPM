# 📈 Portfolio Stocks Performance Analysis & Forecasting with CAPM

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-Visualization-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Yahoo Finance](https://img.shields.io/badge/yFinance-Market%20Data-720E9E?style=for-the-badge&logo=yahoo&logoColor=white)

**A comprehensive end-to-end financial analytics project** that evaluates portfolio performance, computes risk metrics, and forecasts stock returns using the Capital Asset Pricing Model (CAPM) — all powered by real market data.

[🔍 Explore the Notebook](#-project-structure) • [📊 Features](#-features) • [⚙️ Setup](#%EF%B8%8F-installation--setup) • [📐 CAPM Theory](#-capm-explained)

</div>

---

## 🌟 Project Highlights

| 🔢 Metric | 📋 Description |
|-----------|----------------|
| **📦 Stocks Analyzed** | Multi-stock portfolio from real market data |
| **📅 Time Horizon** | Customizable historical date range |
| **📐 Model** | Capital Asset Pricing Model (CAPM) |
| **📉 Risk Metrics** | Alpha, Beta, Sharpe Ratio, Volatility |
| **📈 Forecast** | Expected return prediction per stock |
| **📊 Visualizations** | Interactive Plotly charts & correlation heatmaps |

---

## 🎯 Objective

> **"Don't just track your portfolio — understand it."**

This project goes beyond simple return tracking. It applies **modern portfolio theory** to:

- 📌 Analyze historical price trends of selected stocks
- 📌 Compute each stock's **Beta** (market sensitivity) and **Alpha** (excess return)
- 📌 Benchmark performance against the **S&P 500** market index
- 📌 Forecast **expected returns** using the CAPM formula
- 📌 Visualize risk-return tradeoffs with rich, interactive charts

---

## 🚀 Features

### 🗃️ Data Collection
- Pulls **live stock data** using `yfinance` from Yahoo Finance
- Fetches the **S&P 500 (^GSPC)** as the market benchmark
- Supports any publicly traded ticker (e.g., `AAPL`, `TSLA`, `MSFT`, `GOOGL`)

### 📊 Exploratory Data Analysis
- Normalized price comparison across all portfolio stocks
- Daily and cumulative return calculations
- Rolling volatility & moving averages

### 📐 CAPM Implementation
- Regression-based **Beta** calculation per stock
- **Alpha** computation to identify outperformers/underperformers
- **Expected Return** forecast: `E(R) = Rf + β × (Rm - Rf)`
- Risk-Free Rate sourced from U.S. Treasury yields

### 📉 Risk Metrics
- **Sharpe Ratio** — reward per unit of risk
- **Standard Deviation** — individual stock volatility
- **Correlation Matrix** — inter-stock dependencies
- **VaR (Value at Risk)** — downside risk estimation *(if included)*

### 📈 Interactive Visualizations
- Line charts for portfolio price trends
- Scatter plots for Beta regression fits
- Heatmaps for correlation analysis
- Bar charts comparing Alpha & Expected Returns

---

## 📐 CAPM Explained

The **Capital Asset Pricing Model** is a cornerstone of modern financial theory:

```
E(Ri) = Rf + βi × (Rm − Rf)
```

| Symbol | Meaning |
|--------|---------|
| `E(Ri)` | Expected return of stock `i` |
| `Rf` | Risk-free rate (e.g., 10-Year Treasury yield) |
| `βi` | Beta — sensitivity of stock to market movements |
| `Rm` | Expected market return (S&P 500) |
| `Rm − Rf` | Market risk premium |

### 🧠 Key Concepts

- **Beta > 1** → Stock is more volatile than the market (high risk, high reward)
- **Beta < 1** → Stock is less volatile than the market (defensive stock)
- **Alpha > 0** → Stock outperformed the CAPM-predicted return (value generation)
- **Alpha < 0** → Stock underperformed relative to its risk level

---

## 🗂️ Project Structure

```
📁 Portfolio-Stocks-Performance-Analysis-Forecasting-with-CAPM/
│
├── 📓 CAPM_Analysis.ipynb          # Main Jupyter Notebook
│
├── 📁 data/                        # (Optional) Cached stock data
│   └── stock_data.csv
│
├── 📁 visuals/                     # Exported charts & plots
│   ├── portfolio_performance.png
│   ├── correlation_heatmap.png
│   └── beta_regression.png
│
├── 📄 requirements.txt             # Python dependencies
└── 📄 README.md                    # You are here!
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/pushkarsawarkar22-afk/Portfolio-Stocks-Performance-Analysis-Forecasting-with-CAPM.git
cd Portfolio-Stocks-Performance-Analysis-Forecasting-with-CAPM
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install yfinance pandas numpy matplotlib seaborn plotly scikit-learn scipy jupyter
```

### 3. Launch the Notebook

```bash
jupyter notebook CAPM_Analysis.ipynb
```

---

## 📦 Dependencies

| Library | Purpose |
|---------|---------|
| `yfinance` | Fetching real-time stock & market data |
| `pandas` | Data manipulation & time series |
| `numpy` | Numerical computations |
| `matplotlib` / `seaborn` | Static visualizations |
| `plotly` | Interactive charts |
| `scikit-learn` | Linear regression for Beta |
| `scipy` | Statistical analysis |

---

## 📊 Sample Results (Illustrative)

```
Stock     Beta    Alpha     Expected Return   Sharpe Ratio
─────────────────────────────────────────────────────────
AAPL      1.21    +0.045        14.8%             1.32
MSFT      1.08    +0.031        13.2%             1.18
TSLA      1.87    -0.012        21.5%             0.74
GOOGL     1.14    +0.018        13.9%             1.09
S&P 500   1.00     0.000        11.0%             1.00
```

> 📝 *Actual results depend on selected tickers, date range, and market conditions.*

---

## 📌 How to Customize

1. **Change stocks** — Edit the tickers list in the notebook:
   ```python
   tickers = ['AAPL', 'MSFT', 'TSLA', 'GOOGL', 'AMZN']
   ```

2. **Change date range**:
   ```python
   start_date = '2020-01-01'
   end_date   = '2024-01-01'
   ```

3. **Change risk-free rate**:
   ```python
   risk_free_rate = 0.05  # 5% annual (adjust to current Treasury yield)
   ```

---

## 🔮 Future Enhancements

- [ ] 🤖 LSTM / ARIMA-based price forecasting
- [ ] 🎛️ Streamlit / Gradio interactive dashboard
- [ ] 📊 Fama-French 3-Factor Model integration
- [ ] 📉 Monte Carlo simulation for portfolio risk
- [ ] 🌐 Real-time live market data streaming
- [ ] 📁 Multi-portfolio comparison support

---

## 👨‍💻 Author

<div align="center">

**Pushkar Sawarkar**

[![GitHub](https://img.shields.io/badge/GitHub-pushkarsawarkar22--afk-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/pushkarsawarkar22-afk)

*"Turning market data into actionable financial intelligence."*

</div>

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

---

<div align="center">

⭐ **If you found this project helpful, please give it a star!** ⭐

</div>
