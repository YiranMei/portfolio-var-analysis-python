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

### Usage

* **Historical VaR:** `historical_var.ipynb` – Computes X-day rolling VaR
* **Parametric VaR:** `parametric_var.ipynb` – Calculates VaR using portfolio mean, covariance, and normal assumptions
* **Monte Carlo VaR:** `monte_carlo_var.ipynb` – Simulates 10,000 portfolio outcomes to estimate VaR

Each notebook is fully self-contained and includes Markdown explanations, code chunks, and visualizations.

```
```

