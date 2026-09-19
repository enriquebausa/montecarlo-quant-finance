# Monte Carlo Methods Applied to Quantitative Finance

A from-scratch implementation of Monte Carlo simulation, built progressively from first principles up to real quantitative finance applications: stochastic price modeling, portfolio risk (VaR), correlation-driven diversification, and derivative pricing validated against Black-Scholes.

## What this project covers

1. **Monte Carlo Fundamentals** — estimating π, and empirically verifying the theoretical 1/√N convergence rate of the error.
2. **Random Walks** — discrete stochastic processes, simulated in parallel using vectorized NumPy.
3. **Brownian Motion** — continuous stochastic processes with and without drift.
4. **Geometric Brownian Motion (GBM) & Value at Risk (VaR)** — the standard model for asset prices, used to simulate thousands of price paths and quantify downside risk via percentiles.
5. **Correlated Portfolio (Cholesky Decomposition)** — simulating multiple correlated assets, and quantifying the diversification benefit of holding uncorrelated assets versus highly correlated ones.
6. **Option Pricing: Monte Carlo vs. Black-Scholes** — pricing a European call option by simulation, and validating the result against the closed-form analytical solution.

## Why this structure

Each section builds directly on the previous one. The same statistical principle validated in Section 1 (more simulations → lower error, at a predictable rate) reappears at the end of the project when validating option prices against Black-Scholes — tying the simplest possible example to a real derivative pricing application.

## Tech stack

- **NumPy** — vectorized simulation (no explicit loops over simulations)
- **Matplotlib** — visualization of convergence, paths, and distributions
- **SciPy** — normal distribution CDF, used in the Black-Scholes formula

## How to run

```bash
pip install -r requirements.txt
jupyter notebook montecarlo.ipynb
```

## Sample results

*(add 2-3 images here once uploaded — see note below)*

---
This project was built as a self-directed learning exercise to establish strong foundations in stochastic simulation before moving into more advanced quantitative finance topics.
