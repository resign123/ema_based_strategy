# Automated Algorithmic Investment Model for NIFTY-50

## Overview

"This is a fully automated and backtested algorithmic investment model designed for NIFTY-50 and other multi-asset trading. The model uses a combination of technical indicators and real-time market data to make trading decisions."

![Screenshot (2)](https://github.com/user-attachments/assets/6b45bd14-8760-4cf6-a965-b930dc2b413a)

## Key Features

- Fully automated trading
- Uses 5-minute and 15-minute timeframes
- Implements 5 and 15 EMA along with price action
- Real-time data processing and decision making
- Automatic entry and exit based on predefined conditions
- Integrates with Fyers API for order execution

## Performance Metrics (Backtest Results)

![Screenshot (3)](https://github.com/user-attachments/assets/b2459d46-351d-4706-bbdd-4fe697f89348)


## Key Strengths

1. High profitability: Despite a low win rate, the strategy maintains a high profit factor of 2.82, indicating strong overall profitability.
2. Excellent risk-adjusted returns: High Sharpe (1.55) and Sortino (8.43) ratios suggest good risk-adjusted performance.
3. Strong growth potential: CAGR of 69.02% indicates significant annualized returns. Note- Fluctuations in these returns are highly depend on brokers plateform and liquidity.
   Before trading with high capital/real money it is highly recommeneded to do paper trading/ trading with low capital.
5. Robust to outliers: Outlier-adjusted profit factor (2.78) is close to the regular profit factor, suggesting consistency.

## Areas for Improvement

1. Low win rate (33%): Our strategy have low win rate, compensated by high average profits.
2. Consecutive losses (up to 34): No worries we have high risk-reward.

## Technical Implementation

The model is implemented in Python, utilizing the following key components:

- Fyers API for market data and order execution 
- Pandas for data manipulation and analysis
- Custom functions for technical indicator calculations (EMA)
- Real-time websocket connection for live market data
- Automated order placement and management
