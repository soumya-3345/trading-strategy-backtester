# Trading Strategy Backtester

### SMA Crossover Strategy with Parameter Optimization and Walk-Forward Testing

**Author:** Soumya Gupta

---

## Overview
A research-grade backtesting framework for SMA crossover strategies 
on Indian equities (Nifty 50 stocks), featuring transaction costs, 
parameter optimization via grid search, and walk-forward testing 
to assess out-of-sample robustness.

## Features
- SMA Golden Cross / Death Cross strategy (50/200 day default)
- Transaction costs (0.1%) for realistic simulation
- Grid search optimization across MA parameter combinations
- Walk-forward testing (train: 2015–2019, test: 2020–2024)
- Performance metrics: Sharpe Ratio, Max Drawdown, Strategy vs Buy & Hold returns

## Key Findings
- MA crossover strategy significantly outperforms Buy & Hold on 
  declining stocks (RPOWER: Strategy +48% vs Buy & Hold -61%)
- Walk-forward optimization improves out-of-sample Sharpe ratio 
  for 4 out of 10 stocks and no effects are seen on 3 out of remaining stocks
- Optimal MA windows vary across sectors — no single parameter 
  set works universally
- Results highlight importance of out-of-sample validation in 
  quantitative strategy development

## Tech Stack
Python, Pandas, Plotly, Seaborn

## Data
Historical daily price data (2015–2024) for 10 NSE-listed stocks 
across 5 sectors: IT, Banking, Pharma, FMCG, Energy.

Download CSVs from Google Finance and place in the `data/` folder:
INFY, TCS, HDFCBANK, SBI, DRREDDY, SUNPHARMA, HUL, NESTLE, RPOWER, ONGC

## How to Run
1. Clone the repo
2. Download stock CSVs from Google Finance into `data/` folder
3. Open the notebook in Jupyter
4. Run all cells top to bottom

## Future Work
- Rolling walk-forward optimization with sliding windows
- EMA crossover strategy comparison
- Monte Carlo simulation for portfolio risk analysis
