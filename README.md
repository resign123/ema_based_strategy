# Automated Algorithmic Investment Model for NIFTY-50

## Overview

"This is a fully automated and backtested algorithmic investment model designed for NIFTY-50 and other multi-asset trading. The model uses a combination of technical indicators and real-time market data to make trading decisions."

![Screenshot (2)](https://github.com/user-attachments/assets/6b45bd14-8760-4cf6-a965-b930dc2b413a)

## Key Features

- Fully automated trading along with 5 years extensive backtesting
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
2. Consecutive losses (up to 34): No worries we have high risk-reward. Despite of 34 consecutive losses we lose <3.5% of overall capital.

## Technical Implementation

The model is implemented in Python, utilizing the following key components:

- Fyers API for market data and order execution 
- Pandas for data manipulation and analysis and selenium for automation
- Custom functions for technical indicator calculations (EMA)
- Real-time websocket connection for live market data
- Automated order placement and management

## Setup and Configuration

To use this algorithmic trading model, follow these steps:

### 1. Fill Required Credentials

Open the `fyers_integration.ipynb` file and fill in the following credentials:

``` python
totp_key = "xxxxxxxxxxxxxx"  # totp_key (ex., "OMKRABCDCDVDFGECLWXK6OVB7T4DTKU5")
username = "xxxxxxxxxxxxxx"  # Fyers Client ID (ex., "TK01248")
pin = xxxx  # four-digit PIN
client_id = "xxxxxxxxxxxxxx"  # App ID of the created app (ex., "L9NY305RTW-100")
secret_key = "xxxxxxxxxxxxxx"  # Secret ID of the created app
redirect_uri = "xxxxxxxxxxxxxx"  # Redirect URL you entered while creating the app (ex., "https://trade.fyers.in/api-login/redirect-uri/index.html")
```
### 2. Update Variables 
After filling in the credentials:

1.Change Scripts:

If you want to trade in options, change script's expiry in expiry.
For multi-asset trading, put the script name in sym.

``` python
expiry = 'NSE:BANKNIFTY24522'
sym = 'NSE:NIFTYBANK-INDEX'
```

2.The script will automatically update several variables. Here are some screenshots showing how different variables are updated:

![Screenshot (7)](https://github.com/user-attachments/assets/69876065-2804-4ba7-bef8-34bd180fd7f9)
![Screenshot (6)](https://github.com/user-attachments/assets/d2e4f3d0-86be-4c42-93e2-093209d7167f)
![Screenshot (5)](https://github.com/user-attachments/assets/8e573068-2fcf-435b-a4b0-37a724312118)
![Screenshot (8)](https://github.com/user-attachments/assets/860d6e26-4cc3-40d8-b824-819732957766)

Note- Above mentioned strategy code is kept publicly in github for educational purpose only. I am not responsible with your profit and losses.
