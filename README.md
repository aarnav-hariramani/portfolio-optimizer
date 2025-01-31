# portfolio-optimizer

Portfolio Optimization with Historical Stock Data

Overview

This project optimizes a stock portfolio using historical stock price data. It leverages financial mathematics and statistical modeling to construct a well-balanced investment portfolio that maximizes returns while managing risk.

How It Works

1. Data Preparation
The script reads a CSV file containing historical stock prices and loads it into a Pandas DataFrame.
It calculates log returns, which measure percentage changes in asset values over time. These will be used later for portfolio optimization.
2. Portfolio Optimization
The script calculates expected returns (mu) using the historical mean returns of the stocks.
The covariance matrix (S) is estimated using the Ledoit-Wolf shrinkage method, which provides a more stable and reliable estimate for high-dimensional data.
The Efficient Frontier is initialized to optimize the portfolio, incorporating L2 regularization to prevent extreme asset weightings and promote a more evenly distributed allocation.
The portfolio is optimized for quadratic utility, balancing risk and return based on the user’s risk aversion level (default: 7.5). A lower risk aversion value increases the Sharpe ratio, which measures risk-adjusted return.
3. Portfolio Allocation
After determining the optimal asset weights, the script calculates the expected return, volatility, and Sharpe ratio of the portfolio.
Using the latest stock prices, the script applies Discrete Allocation to determine the exact number of shares to buy for each stock with an initial investment of $100,000.
The final output includes the number of shares per stock, their portfolio weight, and any remaining cash balance.
Key Features

✅ Uses real historical stock data for a realistic portfolio construction.
✅ Employs advanced statistical techniques (Ledoit-Wolf shrinkage, covariance estimation).
✅ Optimizes portfolio allocation using the Efficient Frontier.
✅ Balances risk and return through L2 regularization and quadratic utility.
✅ Calculates exact share allocations for practical implementation.
