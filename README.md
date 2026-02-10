# Gold Volatility Analysis

Quantitative study comparing **GARCH(1,1)** volatility estimates with market-implied volatility (**GVZ**) for Gold (GLD), identifying periods of **Volatility Risk Premium**.

---

## Overview
This project analyzes how **statistical volatility** differs from **market expectations**:

- **GARCH(1,1):** Realized volatility based on historical GLD prices  
- **GVZ:** Forward-looking market-implied volatility  

**Volatility Risk Premium:** Occurs when GVZ systematically exceeds GARCH predictions.

---

## Methodology
1. **Data Alignment:** Historical GLD & GVZ data synchronized via Yahoo Finance  
2. **Modeling:** Fit GARCH(1,1) in-sample; estimate parameters (\(\alpha, \beta\))  
3. **Validation:** Out-of-sample testing for predictive accuracy  

---

## Visualization

![Volatility Comparison](output_chart.png)

- **Blue (GVZ):** Market-implied volatility  
- **Green (GARCH):** Statistical estimate  

**Interpretation:**  
- **GVZ > GARCH:** Market expects higher risk (Volatility Risk Premium)  
- **GVZ ≈ GARCH:** Market sentiment aligns with statistical risk  

---

## Requirements
```bash
pip install yfinance pandas numpy arch plotly
