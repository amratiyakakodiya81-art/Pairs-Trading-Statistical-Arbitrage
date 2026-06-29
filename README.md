# Pairs Trading & Statistical Arbitrage
### By: Amartiya Kakodiya | IIT Kharagpur

## Overview
This project implements a pairs trading strategy based on 
statistical arbitrage. We identify cointegrated stock pairs 
using the Engle-Granger cointegration test and ADF stationarity 
checks. Z-score based entry/exit signals are built on the spread 
and the strategy is backtested computing Sharpe ratio, total 
return and max drawdown.

## Tools
Python | NumPy | Pandas | Matplotlib | Statsmodels

## Methodology
1. Simulate cointegrated stock pair with common stochastic trend
2. Run ADF test to confirm non-stationarity of individual series
3. Run Engle-Granger cointegration test on the pair
4. Compute hedge ratio via OLS regression
5. Build z-score based entry/exit signals on the spread
6. Backtest strategy and compute performance metrics

## Key Results
- Trading Days:            753
- Cointegration Test:      Engle-Granger ✓ (p-value < 0.05)
- Hedge Ratio (Beta):      0.2608
- Rolling Window:          30 days
- Entry Threshold:         Z-Score ± 2.0
- Exit Threshold:          Z-Score ± 0.5
- Long Signals Generated:  13
- Short Signals Generated: 16
- Total Trades:            28

## Backtest Performance
| Metric          | Value      |
|-----------------|------------|
| Starting Capital| $100,000   |
| Final Capital   | $101,130   |
| Total Return    | 1.13%      |
| Sharpe Ratio    | 0.38       |
| Max Drawdown    | -0.59%     |
| Total Trades    | 28         |

## Key Insights
1. ADF test confirms individual series are non-stationary
2. Engle-Granger test confirms pair is cointegrated
3. Z-score signals successfully capture mean reversion
4. Low max drawdown of -0.59% shows risk is well controlled
5. Positive Sharpe ratio confirms strategy has edge
6. Pairs trading is market neutral — profits regardless 
   of overall market direction

## Visualisations
- stock_prices.png — normalised price comparison
- spread.png — cointegrated spread over time
- zscore_signals.png — z-score with entry/exit signals
- backtest_results.png — portfolio value and drawdown
