# 📈 Portfolio Optimization & Risk Analysis

This project explores how portfolio optimization techniques can be applied to real financial market data using Python. The analysis covers the full workflow from collecting historical stock prices to building optimized portfolios using Modern Portfolio Theory and Mean-Variance Optimization.

Using data from Yahoo Finance, the project analyzes the relationship between risk and return, simulates thousands of portfolios through Monte Carlo methods, and evaluates portfolio performance using financial risk metrics such as Sharpe Ratio, Variance, Sortino Ratio, and Maximum Drawdown.

# 🎯 Goals of the Project

This project was created to:
- Apply portfolio theory using real financial data
- Practice quantitative finance techniques in Python
- Explore the relationship between risk and return
- Build practical experience with financial optimization models
- Strengthen data analysis and financial modeling skills

---

# 🚀 Project Overview

The workflow of the project includes:

1. Collecting historical stock price data
2. Cleaning and preprocessing financial time series data
3. Performing exploratory risk and return analysis
4. Running Monte Carlo portfolio simulations
5. Visualizing the Efficient Frontier
6. Building optimized portfolios using `skfolio`

---

# 📊 Stocks Used

The portfolio consists of the following assets:

- Amazon (`AMZN`)
- Apple (`AAPL`)
- LG Display (`LPL`)
- Crocs (`CROX`)
- Eli Lilly (`LLY`)
- LPL Financial (`LPLA`)

Historical daily closing prices are downloaded directly from Yahoo Finance using the `yfinance` API.

---

# 🧹 Data Preprocessing

Before performing any financial analysis, the dataset is cleaned and validated.

### Preprocessing Steps
- Removed columns with entirely missing values
- Filled missing observations using forward-fill and backward-fill methods
- Checked for remaining missing values
- Visualized missing data using heatmaps

This ensures the portfolio analysis is based on clean and continuous financial data.

---

# 📈 Exploratory Financial Analysis

The project calculates key financial statistics for each stock, including:

- Daily Returns
- Mean Returns
- Variance
- Covariance Matrix
- Correlation Matrix

Several visualizations are created to better understand the behavior of the assets:
- Risk vs Return scatter plots
- Correlation heatmaps
- Representative stock analysis

The representative stock is created using the average return and average variance across all assets to serve as a benchmark point in the risk-return space.

---

# 🎲 Monte Carlo Portfolio Simulation

To explore different portfolio combinations, the project generates **10,000 random portfolios** using Monte Carlo simulation.

For each portfolio, the following metrics are calculated:
- Expected Annual Return
- Annualized Volatility
- Sharpe Ratio
- Portfolio Weights

This simulation helps visualize how different asset allocations affect risk and return.

---

# 📉 Efficient Frontier Analysis

The project visualizes the Efficient Frontier and highlights two important portfolios:

### Minimum Volatility Portfolio
The portfolio with the lowest overall risk.

### Maximum Sharpe Ratio Portfolio
The portfolio with the best risk-adjusted return.

The efficient frontier plot helps compare optimal portfolios against all simulated portfolios.

---

# 🤖 Portfolio Optimization with Skfolio

The project uses the `skfolio` library to perform Mean-Variance Optimization.

## Model 1 — Variance Minimization

The first model minimizes portfolio variance while evaluating portfolio performance on both training and testing datasets.

### Metrics Evaluated
- Annualized Mean Return
- Annualized Variance
- Sharpe Ratio
- Sortino Ratio
- Maximum Drawdown

---

## Model 2 — Target Return Optimization

The second model optimizes portfolios under different minimum return constraints.

### Target Returns
- 15%
- 20%
- 25%
- 30%
- 35%
- 40%

This analysis shows how portfolio risk changes as investors target higher expected returns.

---

# 🛠️ Technologies Used

### Programming Language
- Python

### Libraries
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- yfinance
- scikit-learn
- skfolio
