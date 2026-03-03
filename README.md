# Dynamic Trading with Predictable Returns & Transaction Costs

Capstone Project – MS Financial Engineering  
Stevens Institute of Technology

## Overview
This project implements the dynamic trading framework proposed by Gârleanu & Pedersen (2013) to optimize portfolio allocation under predictable returns and transaction costs.

The goal is to evaluate whether dynamic portfolio rebalancing improves risk-adjusted returns compared with traditional static allocation strategies.

---

## Dataset
• Fama-French factors + Momentum  
• 10 Industry Portfolios  
• Period: 1963–2024  
• Frequency: Daily → Monthly

---

## Strategies Compared
• Dynamic Trading Strategy (Gârleanu–Pedersen framework)  
• Markowitz Mean-Variance Portfolio  
• Equal-Weight Portfolio Benchmark  
• Reinforcement Learning (PPO)

---

## Methodology
• Factor return prediction using Fama-French signals  
• Signal persistence modeling using VAR(1)  
• Risk estimation using Ledoit-Wolf covariance shrinkage  
• Portfolio optimization with transaction cost constraints  
• Reinforcement Learning environment for adaptive allocation

---

## Evaluation Metrics
• Sharpe Ratio  
• Maximum Drawdown  
• Turnover  
• Information Coefficient  
• Signal-to-Noise Ratio

---

## Repository Structure
data/ → dataset used for analysis  
report/ → full capstone report  
presentation/ → final presentation slides

---

## Authors
Mrinal Gupta  
Siddharth Jain  
Venkata Bhargava  
Varda Matalia
