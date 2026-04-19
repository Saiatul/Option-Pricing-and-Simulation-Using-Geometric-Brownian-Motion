# Option Pricing & Simulation using Geometric Brownian Motion

## Overview
This project implements stock price simulation using Geometric Brownian Motion (GBM) and applies Monte Carlo methods to price different types of options.

The goal is to understand how stochastic processes are used in derivatives pricing and how key parameters impact option valuation.

---

## Models Implemented

### 1. Geometric Brownian Motion (GBM)
- Simulates stock price paths using stochastic differential equations  
- Captures drift (expected return) and volatility  
- Generates multiple price paths for analysis  

---

### 2. Option Pricing

#### European Call Option
- Payoff based on final price at maturity  
- \( max(S_T - K, 0) \)

#### Asian Call Option
- Payoff based on average price over time  
- \( max(\bar{S} - K, 0) \)

#### Barrier Call Option (Knock-In)
- Activated only if price crosses a barrier  
- Payoff depends on path behavior  

---

## Methodology
- Simulate multiple price paths using GBM  
- Compute payoffs for each option type  
- Discount expected payoff using risk-free rate  
- Estimate option price using Monte Carlo averaging  

---

## Key Parameters
- `S0` – Initial stock price  
- `mu` – Expected return  
- `sigma` – Volatility  
- `T` – Time to maturity  
- `K` – Strike price  
- `r` – Risk-free rate  
- `M` – Number of simulations  

---

## Results (Sample)
- European Option Price: ~9.26  
- Asian Option Price: ~2.89  
- Barrier Option Price: ~5.38  

---

## Insights
- Higher volatility increases option prices  
- Path-dependent options (Asian, Barrier) behave differently from European options  
- Monte Carlo simulation provides flexible pricing for complex derivatives  

---

## Future Improvements
- Add variance reduction techniques  
- Compare with Black-Scholes analytical pricing  
- Improve simulation efficiency  
