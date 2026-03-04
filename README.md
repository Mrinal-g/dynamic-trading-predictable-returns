# Dynamic Trading with Predictable Returns & Transaction Costs

Capstone Project — MS Financial Engineering  
Stevens Institute of Technology

This project implements the dynamic trading framework proposed by **Gârleanu & Pedersen (2013)** to study portfolio allocation under predictable returns and transaction costs. The model is extended with a **Reinforcement Learning (PPO)** trading agent to explore adaptive portfolio strategies.

---

## Research Objective

The project evaluates whether **dynamic portfolio rebalancing** improves performance compared with classical static allocation strategies.

Key goals:

- Implement the **Gârleanu–Pedersen dynamic trading framework**
- Model signal persistence using **VAR(1)**
- Compare dynamic allocation against **Markowitz and Equal-Weight portfolios**
- Explore **Reinforcement Learning** as an adaptive trading strategy

---

## Dataset

The analysis uses widely studied empirical asset pricing datasets.

- **Fama-French factors + Momentum**
- **10 Fama-French Industry Portfolios**

Period: **1963 – 2024**

---

## Methodology

The modeling pipeline consists of:

1. Factor-based return prediction using **Fama-French signals**
2. Signal persistence modeling using **VAR(1)**
3. Covariance estimation using **Ledoit-Wolf shrinkage**
4. Dynamic portfolio optimization with **transaction costs**
5. Reinforcement Learning trading agent using **PPO**

---

## Strategy Performance (γ = 3)

| Strategy | Annual Return | Volatility | Sharpe Ratio | Max Drawdown |
|----------|--------------|-----------|--------------|--------------|
| Dynamic Strategy | 14.33% | 20.70% | 0.69 | -55.6% |
| Markowitz Portfolio | 10.41% | 12.95% | 0.80 | -33.8% |
| Equal Weight Portfolio | 14.33% | 20.70% | 0.69 | -55.6% |
| RL Strategy (PPO) | 14.14% | 21.72% | 0.65 | - |

The dynamic trading strategy achieves higher cumulative returns relative to classical static allocation methods, reflecting the value of incorporating predictable returns and trading costs.

---

## Repository Structure

```
dynamic-trading-portfolio-optimization

data/
    dataset_fama_french_industry_returns.csv

report/
    dynamic_trading_capstone_report.pdf

presentation/
    dynamic_trading_capstone_presentation.pptx
```

---

## Reference

Gârleanu, N., & Pedersen, L. H. (2013).  
**Dynamic Trading with Predictable Returns and Transaction Costs**  
Journal of Finance.          
