Automated Algorithmic Investment Model for NIFTY-50
Overview
"This is a fully automated and backtested algorithmic investment model designed for NIFTY-50 and other multi-asset trading. The model uses a combination of technical indicators and real-time market data to make trading decisions."

Screenshot (2)

Key Features
Fully automated trading along with 5 years extensive backtesting
Implements 5 and 15 EMA along with price action
Real-time data processing and decision making
Automatic entry and exit based on predefined conditions
Integrates with Fyers API for order execution
Performance Metrics (Backtest Results)
Screenshot (3)

Key Strengths
High profitability: Despite a low win rate, the strategy maintains a high profit factor of 2.82, indicating strong overall profitability.
Excellent risk-adjusted returns: High Sharpe (1.55) and Sortino (8.43) ratios suggest good risk-adjusted performance.
Strong growth potential: CAGR of 69.02% indicates significant annualized returns. Note- Fluctuations in these returns are highly depend on brokers plateform and liquidity. Before trading with high capital/real money it is highly recommeneded to do paper trading/ trading with low capital.
Robust to outliers: Outlier-adjusted profit factor (2.78) is close to the regular profit factor, suggesting consistency.
Areas for Improvement
Low win rate (33%): Our strategy have low win rate, compensated by high average profits.
Consecutive losses (up to 34): No worries we have high risk-reward. Despite of 34 consecutive losses we lose <3.5% of overall capital.
Technical Implementation
The model is implemented in Python, utilizing the following key components:

Fyers API for market data and order execution
Pandas for data manipulation and analysis and selenium for automation
Custom functions for technical indicator calculations (EMA)
Real-time websocket connection for live market data
Automated order placement and management
Setup and Configuration
To use this algorithmic trading model, follow these steps:

1. Fill Required Credentials
Open the fyers_integration.ipynb file and fill in the following credentials:

totp_key = "xxxxxxxxxxxxxx"  # totp_key (ex., "OMKRABCDCDVDFGECLWXK6OVB7T4DTKU5")
username = "xxxxxxxxxxxxxx"  # Fyers Client ID (ex., "TK01248")
pin = xxxx  # four-digit PIN
client_id = "xxxxxxxxxxxxxx"  # App ID of the created app (ex., "L9NY305RTW-100")
secret_key = "xxxxxxxxxxxxxx"  # Secret ID of the created app
redirect_uri = "xxxxxxxxxxxxxx"  # Redirect URL you entered while creating the app (ex., "https://trade.fyers.in/api-login/redirect-uri/index.html")
2. Update Variables
After filling in the credentials:

1.Change Scripts:

If you want to trade in options, change script's expiry in expiry. For multi-asset trading, put the script name in sym.

expiry = 'NSE:BANKNIFTY24522'
sym = 'NSE:NIFTYBANK-INDEX'
2.The script will automatically update several variables. Here are some screenshots showing how different variables are updated:

Screenshot (7) Screenshot (6) Screenshot (5) Screenshot (8)

Note- Above mentioned strategy code is kept publicly in github for educational purpose only. I am not responsible with your profit and losses.
