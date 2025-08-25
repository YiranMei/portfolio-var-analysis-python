# Portfolio Value at Risk (VaR) Analysis

**Author:** Winifred Mei  
**Date:** August 21, 2025  

This repository demonstrates how to calculate the **Value at Risk (VaR)** for a stock portfolio using three common methods:

1. **Historical VaR** – Computes VaR based on historical portfolio returns.  
2. **Parametric VaR** – Uses portfolio mean, standard deviation, and normal distribution assumptions to calculate VaR.  
3. **Monte Carlo VaR** – Simulates thousands of portfolio outcomes to estimate risk using a Monte Carlo approach.


---

## Features

- Download historical stock data using **yfinance**.  
- Calculate **daily log returns** for each stock.  
- Build an **equally weighted portfolio** and compute portfolio statistics.  
- Estimate **VaR at different confidence levels**.  
- Visualize the **distribution of portfolio returns** and VaR thresholds.  
- Compare the results of **historical, parametric, and Monte Carlo methods**.  

---
## Methodology

### Historical VaR
- **Approach:** Uses historical simulation to calculate VaR by analyzing past daily returns of the portfolio over a 10-year period.  
- **Portfolio:** Five tech stocks (AAPL, MSFT, GOOGL, AMZN, TSLA) with equal weighting and an initial value of $500,000.  
- **Computation:**  
  1. Calculate daily log returns for each stock.  
  2. Compute 60-day rolling cumulative portfolio returns.  
  3. Determine VaR by finding the 1st percentile of these rolling returns.  

### Parametric VaR
- **Approach:** Variance-covariance method assumes normally distributed returns.  
- **Portfolio:** Same five tech stocks with a portfolio value of $600,000.  
- **Computation:**  
  1. Calculate daily log returns and annualized covariance matrix.  
  2. Compute portfolio standard deviation using stock weights and covariance.  
  3. Calculate VaR at 90%, 95%, and 99% confidence levels using the normal distribution's inverse CDF.  

### Monte Carlo VaR
- **Approach:** Simulates a large number of potential portfolio outcomes to model risk.  
- **Portfolio:** Same five tech stocks, initial value $500,000.  
- **Computation:**  
  1. Calculate historical daily log returns, expected portfolio return, and standard deviation.  
  2. Simulate 10,000 random portfolio outcomes over a 20-day window.  
  3. Determine VaR by finding the percentile corresponding to the desired confidence level.  

---

## Insights from Analysis Results

### Historical VaR
- **99% Confidence VaR:** $140,458.55  
- **Interpretation:** There is a 1% chance that the portfolio could lose $140,458.55 or more over a 60-day period based on the past 10 years of returns.  

### Parametric VaR
- **90% Confidence VaR:** $-31,837.87  
- **95% Confidence VaR:** $-40,079.31  
- **99% Confidence VaR:** $-55,538.87  
- **Interpretation:** The parametric method estimates potential losses under the assumption of normally distributed returns. Negative values indicate the magnitude of potential losses at different confidence levels.  

### Monte Carlo VaR
- **99% Confidence VaR:** $82,331.47  
- **Interpretation:** There is a 1% chance that the portfolio could lose $82,331.47 or more over a 20-day period. Monte Carlo simulation captures a broader range of potential outcomes and accounts for complex correlations among assets.  

---

## Requirements & Usage

This repository uses the following Python packages:


- numpy
- pandas
- yfinance
- matplotlib
- scipy


Install all required packages with:


```bash
pip install numpy pandas yfinance matplotlib scipy
```

