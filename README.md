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



## 2. Data Collection

### Source

The data used in this project is retrieved from **Yahoo Finance** using the 'yfinance' Python library.


### Assets analyzed

    - Apple (AAPL)
    - Microsoft (MSFT)
    - Nvidia (NVDA)
    - AMD (AMD)
Time period: 2016 - 2026



## 3. Methodology

### Returns

Daily returns are computed as:


$$ r_t = \frac{P_t - P_{t-1}}{P_{t-1}} $$


where:
- $ P_t $ is the price at time  $t$
- $ r_t $ is the return at time $t$

### Normalization

To compare assets with different price scales, prices are normalized:


$$ P_{norm} = \frac{P_t}{P_0} $$


This allows comparison of relative growth over time rather than absolute price levels.



### Volatility

Volatility is measured as the standard deviation of returns:


$$ \sigma = \sqrt{\frac{1}{N} \sum_{t=1}^{N} (r_t - \bar{r})^2} $$


- Higher volatility indicates higher risk and variability.


### Correlation

Correlation between two assets \( X \) and \( Y \) is defined as:


 $$Cor(X,Y) = \frac{Cov(X,Y)}{\sigma_X \sigma_Y} $$


- Values range from -1 to 1:
  - 1 → perfect positive correlation
  - 0 → no correlation
  - -1 → perfect negative correlation

### Sharpe Ratio

The Sharpe ratio is defined as:

$$ S= \frac{R_p - R_f}{\sigma_p}$$

with:
  - $R_p$ = portfolio/asset return
  - $R_f$ = risk-free rate
  - $\sigma_p$ = volatility 


Yet for an individual asset, the Sharpe ratio is computed as:

$$
S = \frac{\mu - R_f}{\sigma}
$$

with: 
  - $\mu$ = average return over time period
  - $\sigma$ = volatility
  - $R_f$ = risk-free rate

In this analysis, the risk-free rate is approximated to 0 for simplicity.

In practice, the risk-free rate corresponds to returns on short-term government bonds.
However, since these rates are relatively small compared to stock market returns,
this approximation does not significantly affect comparative results.

## 4. Key visualizations

### Normalized Price Evolution
![Normalized Prices](https://github.com/Thomas-Giovanopoulos/Stock-market-analysis/blob/c47184084baf64fc6932c8e53df83b334df09457/Figures/stock_price_10y_N.png)

### Daily returns
![Returns](https://github.com/Thomas-Giovanopoulos/Stock-market-analysis/blob/638bdcb8e92b177c759151967eaf85dc23dc4aa1/Figures/daily_returns.png)

### Correlation Matrix

![Correlation Matrix Heatmap](https://github.com/Thomas-Giovanopoulos/Stock-market-analysis/blob/638bdcb8e92b177c759151967eaf85dc23dc4aa1/Figures/Corr_M_10y.png)

### Volatility Comparison

![Volatility](https://github.com/Thomas-Giovanopoulos/Stock-market-analysis/blob/638bdcb8e92b177c759151967eaf85dc23dc4aa1/Figures/Y_Volatility_10y.png)

### Tables

Summary statistics include:

- Mean daily returns
- Annualized returns
- Volatility
- Correlation matrix


Sharpe Ratio table:

    Ticker
    AAPL    0.906949
    AMD     0.973193
    MSFT    0.972633
    NVDA    1.359236

### Observations

- Growth trends differ significantly between assets
- Some stocks exhibit much higher volatility than others
- Correlations between major tech stocks are generally positive


## 5. Discussion

### Why NVIDIA Dominates

NVIDIA shows exceptional growth due to its exposure to:

- Artificial intelligence
- GPU computing
- Data centers

This leads to exponential price appreciation compared to other assets.


### Why AMD is Volatile

AMD shows high volatility due to:

- Competitive positioning in the semiconductor market
- Sensitivity to market cycles
- Rapid shifts in investor sentiment


### Why Correlations are High

Tech stocks often exhibit high correlations because:

- They are influenced by similar macroeconomic factors
- They respond similarly to interest rates and market trends
- Sector-wide movements affect them collectively


### Limitations

- Only daily data is used (no intraday analysis)
- Simplified assumptions
- No consideration of external macroeconomic variables
- Past performance does not guarantee future results


## 6. Conclusion

### Summary

This project provided an overview of:

- Stock price behavior over time
- Return computation and interpretation
- Volatility as a measure of risk
- Correlation between assets
- Risk-adjusted performance metrics (Sharpe ratio)

### What I Learned

- Practical use of Python libraries such as `pandas`, `numpy`, and `matplotlib` and `yfinace`
- How to manipulate and analyze financial data
- How to interpret key financial metrics


### Possible Extensions

- Portfolio optimization 
- Moving averages and technical indicators
- Time-series modeling (ARIMA, GARCH)
- Inclusion of macroeconomic indicators