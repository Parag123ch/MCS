# MCS — Portfolio Optimization and Long-Term Forecasting using Monte Carlo Simulation

MCS is a financial analytics project that uses Monte Carlo Simulation to optimize a stock portfolio and estimate its long-term performance under uncertainty. The project pulls historical stock price data from Yahoo Finance, computes returns and covariance, simulates thousands of random portfolio allocations, identifies optimal portfolios using Sharpe ratio and volatility, and then projects portfolio growth over a 30-year horizon.

## Overview

This project applies Monte Carlo Simulation in two stages:

1. **Portfolio Optimization**
   - Generates thousands of random portfolio weight combinations
   - Computes expected return, portfolio risk, and Sharpe ratio for each allocation
   - Identifies:
     - the portfolio with the **maximum Sharpe ratio**
     - the portfolio with the **minimum standard deviation**

2. **Future Portfolio Simulation**
   - Uses the selected portfolio statistics
   - Runs long-horizon simulations over 30 years
   - Estimates how an initial investment may grow under uncertainty
   - Visualizes simulation paths and distribution of outcomes

## Features

- Fetches historical stock price data using Yahoo Finance
- Computes daily returns and covariance matrix
- Simulates 10,000 random portfolio allocations
- Optimizes portfolio based on:
  - maximum Sharpe ratio
  - minimum volatility
- Runs 10,000 long-term Monte Carlo simulations for selected portfolios
- Visualizes portfolio growth trajectories
- Plots histograms of simulated final portfolio values
- Estimates percentage of profitable scenarios

## Tech Stack

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **yFinance**
- **pandas-datareader**

## Dataset / Portfolio Universe

The project uses historical adjusted close prices for a basket of stocks downloaded from Yahoo Finance.

Example symbols used in the notebook:
- XOM
- GE
- MSFT
- BP
- C
- PG
- WMT
- PFE
- HBC
- TM

## Workflow

### 1. Data Collection
Historical adjusted closing prices are fetched from Yahoo Finance for a predefined list of stocks over a selected time range.

### 2. Return and Risk Calculation
The project computes:
- percentage returns
- mean returns
- covariance matrix

These values form the foundation for portfolio simulation.

### 3. Monte Carlo Portfolio Optimization
The model generates 10,000 random portfolio allocations. For each allocation, it calculates:
- expected portfolio return
- portfolio standard deviation
- Sharpe ratio

All simulation results are stored and analyzed to identify the most efficient portfolios.

### 4. Maximum Sharpe Portfolio Analysis
The portfolio with the highest Sharpe ratio is selected and used for long-term simulation. A second Monte Carlo process projects the growth of an initial investment over a 30-year horizon.

### 5. Minimum Volatility Portfolio Analysis
The portfolio with the lowest standard deviation is also selected and simulated separately to compare risk-focused performance.

### 6. Visualization
The project includes:
- simulation line plots for long-term portfolio trajectories
- histograms of final portfolio values
- profitability estimates across simulated scenarios

## Example Outputs

- Optimized portfolio weights
- Expected return and risk values
- Maximum Sharpe ratio portfolio
- Minimum volatility portfolio
- Simulated future portfolio paths
- Distribution of final values after long-term simulation
- Percentage of profitable scenarios

## Learning Outcomes

This project demonstrates:
- practical use of Monte Carlo Simulation in finance
- portfolio optimization using risk-return tradeoffs
- Sharpe ratio–based investment analysis
- probabilistic forecasting of long-term portfolio outcomes
- financial data handling and visualization in Python

## Future Improvements

- Add Efficient Frontier visualization
- Include risk-free rate adjustment in Sharpe ratio calculation
- Support user-defined stock baskets
- Add VaR and CVaR metrics
- Compare Monte Carlo results with mean-variance optimization
- Build a Streamlit or React dashboard for interactive use

## How to Run

1. Install the required Python libraries
2. Open the notebook
3. Run all cells in sequence
4. Review optimization metrics and simulation plots

## Author

**Parag Chhalotre**

This project was built independently to explore portfolio optimization, simulation-based forecasting, and financial analytics using Python.
