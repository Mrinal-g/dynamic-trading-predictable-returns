# Dynamic Trading with Predictable Returns & Transaction Costs

**Capstone Project — MS Financial Engineering**  
Stevens Institute of Technology  

Quantitative Finance | Portfolio Optimization | Reinforcement Learning

---

## Overview

This project implements the **dynamic trading framework proposed by Gârleanu & Pedersen (2013)** to study optimal portfolio allocation when returns are predictable and trading incurs transaction costs.

Traditional portfolio strategies such as **Markowitz mean-variance optimization** ignore trading frictions and signal decay. This project evaluates whether **dynamic portfolio rebalancing** improves long-term performance when these realistic constraints are incorporated.

The study also extends the analytical framework by exploring **Reinforcement Learning (PPO)** as an adaptive trading strategy.

---

## Research Objective

The main objectives of this project are:

- Implement a **dynamic trading strategy** that accounts for transaction costs
- Model **signal persistence using VAR(1)**
- Compare dynamic allocation against **classical portfolio strategies**
- Evaluate whether **reinforcement learning can enhance portfolio optimization**

---

## Dataset

The analysis uses widely studied academic factor datasets:

- **Fama-French factors + Momentum**
- **10 Fama-French Industry Portfolios**

**Period:** 1963 – 2024  
**Frequency:** Daily data aggregated to monthly observations

These datasets are commonly used in empirical asset pricing and portfolio optimization research.

---

## Strategies Compared

The following portfolio strategies were evaluated:

**Dynamic Trading Strategy**  
Transaction-cost aware portfolio optimization based on the Gârleanu–Pedersen framework.

**Markowitz Mean-Variance Portfolio**  
Classical static portfolio optimization without transaction costs.

**Equal-Weight Portfolio**  
Naïve diversification benchmark.

**Reinforcement Learning Strategy (PPO)**  
Adaptive allocation strategy trained using policy optimization.

---

## Methodology

The modeling pipeline consists of the following steps:

**Factor Return Prediction**  
Predictable return signals derived from Fama-French factors.

**Signal Persistence Modeling**  
VAR(1) model used to capture the persistence of predictive signals.

**Risk Estimation**  
Covariance matrix estimated using **Ledoit-Wolf shrinkage**.

**Dynamic Portfolio Optimization**  
Portfolio weights adjusted gradually to balance expected return and transaction costs.

**Reinforcement Learning Extension**  
A custom financial market environment was implemented using **Gymnasium** and **Stable-Baselines3** to train PPO agents.

---

## Evaluation Metrics

Strategy performance was evaluated using the following metrics:

- Total Return  
- Annualized Return  
- Sharpe Ratio  
- Maximum Drawdown  
- Portfolio Volatility  
- Turnover  
- Information Coefficient (IC)  
- Signal-to-Noise Ratio (SNR)

---

## Strategy Performance

### Dynamic vs Static Portfolio Strategies

The figure below compares cumulative portfolio value for the dynamic trading strategy and classical benchmark portfolios.

![Strategy Comparison](results/strategy_comparison.png)

Dynamic portfolio optimization generates higher cumulative returns relative to static allocation strategies by accounting for predictable returns and trading costs.

---

### Reinforcement Learning Strategy

The reinforcement learning agent was trained to adaptively allocate portfolio weights under the same market environment.

![RL Strategy](results/rl_strategy_performance.png)

The RL strategy demonstrates competitive performance and illustrates the potential of machine learning methods in portfolio management.

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

results/
    strategy_comparison.png
    rl_strategy_performance.png
```

---

## Key Insights

- Dynamic portfolio optimization improves long-term returns by incorporating **signal persistence and trading costs**
- Static strategies such as Markowitz ignore trading frictions and may underperform in realistic trading environments
- Reinforcement learning provides a flexible framework for **adaptive portfolio allocation**

---

## Authors

Mrinal Gupta  
Siddharth Jain  
Venkata Bhargava  
Varda Matalia

---

## Reference

Gârleanu, N., & Pedersen, L. H. (2013).  
**Dynamic Trading with Predictable Returns and Transaction Costs**  
Journal of Finance.
