# Entry Level Stock Market Data Analysis (Python)

## 1. Overview

### Context

This project explores historical stock market data to analyze returns, volatility, and correlations between major companies.
The goal is to understand how different assets behave in terms of performance and risk, using real financial data.

### Objective

- Compute and analyze daily returns
- Measure Volatility (risk) of different stocks
- Compare performance over time
- Compute Sharpe's ratio and evaluate risk/reward
- Study correlations between assets
- Observe behavior during market stress periods (2020 crisis)

### Tools and technologies

- Python
- Pandas
- Numpy
- Matplotlib and seaborn
- yfinance
- Jupyter Notebook

---

## 2. Data Collection

### Source

The data used in this project is retrieved from **Yahoo Finance** using the 'yfinance' Python library.


### Assets analyzed

    - Apple (AAPL)
    - Microsoft (MSFT)
    - Nvidia (NVDA)
    - AMD (AMD)
Time period: 2016 - 2026

--- 

## 3. Methodology

### Returns

Daily returns are computed as:

\[
r_t = \frac{P_t - P_{t-1}}{P_{t-1}}
\]

where:
- \( P_t \) is the price at time \( t \)
- \( r_t \) is the return at time \( t \)

### Normalization

To compare assets with different price scales, prices are normalized:

\[
P_{norm} = \frac{P_t}{P_0}
\]

This allows comparison of relative growth over time rather than absolute price levels.



### Volatility

Volatility is measured as the standard deviation of returns:

\[
\sigma = \sqrt{\frac{1}{N} \sum_{t=1}^{N} (r_t - \bar{r})^2}
\]

- Higher volatility indicates higher risk and variability.


### Correlation

Correlation between two assets \( X \) and \( Y \) is defined as:

\[
\mathbb{C}or_{X,Y} = \frac{\mathbb{C}ov(X,Y)}{\sigma_X \sigma_Y}
\]

- Values range from -1 to 1:
  - 1 → perfect positive correlation
  - 0 → no correlation
  - -1 → perfect negative correlation

## Key visualizations

### Normalized Price Evolution
![Normalized Prices](Figures\stock_price_10y_N.png)

###