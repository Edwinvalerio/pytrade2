# 3:1 Risk-Reward Stock Trading Strategy

This repository contains a simple stock trading strategy based on support and resistance levels with a 3:1 risk-reward ratio. The provided Python code fetches historical price data, calculates support and resistance levels, and determines whether to buy a stock based on the potential profit (distance to resistance) being at least three times the potential loss (distance to support).

How the strategy works

Fetch historical prices from a specified URL using the get_prices(url) function.
Calculate support and resistance levels based on historical prices using the get_support_and_resistance(prices) function.
Determine the nearest support and resistance levels to the current stock price using the nearest_support_and_resistance(current_price, support_and_resistance) function.
Decide whether to buy the stock using the should_buy_stock(resistance, current_price, support) function, which checks if the distance to resistance is at least three times the distance to support.
High-level algorithm

Collect historical price data for a stock or set of stocks.
For each stock:
a. Calculate support and resistance levels based on historical prices.
b. Determine the nearest support and resistance levels to the current price.
c. Decide whether to buy the stock based on the 3:1 risk-reward ratio criterion.
d. If the criterion is met, buy the stock and set a take-profit target at the resistance level and a stop-loss order at the support level.
Monitor the stock positions, and exit the trade when the stop-loss or take-profit target is reached.
Disclaimer

This strategy is a simple example and should not be used for actual trading without thorough backtesting and optimization. Factors such as trading fees, slippage, and market conditions can affect the performance of this strategy.

Usage

The provided Python functions can be imported and used in your trading or backtesting script. You will need to supply historical price data for the stocks you want to analyze, and modify the code to handle fetching and updating the stock data as needed.

Requirements

Python 3
requests library (for fetching historical prices)
