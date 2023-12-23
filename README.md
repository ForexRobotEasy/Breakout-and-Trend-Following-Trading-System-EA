# Breakout and Trend Following Trading System EA

This code is an Expert Advisor (EA) for trading in the forex market. The EA is designed to identify breakouts and follow trends in the market to place buy and sell trades. It uses a simple breakout strategy to determine entry and exit points.

## Developer's Site
This code is developed by the Forex Robot Easy Team. For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/review-breakout-trend-following-ea-boost-your-forex-trades/). 

Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

## Libraries Used
The code includes the following library:

- Trade.mqh: A library that provides trading functions and methods.

## Constants
The following constants are defined in the code:

- SYMBOLS: A list of symbols to trade. The code will loop through each symbol in this list.
- TIMEFRAME: The trading timeframe.
- STOP_LOSS: The stop loss in pips.
- TAKE_PROFIT: The take profit in pips.
- LOT_SIZE: The lot size for trading.

## Global Variables
The code uses a global variable:

- trade: An object of the CTrade class, which provides trading operations.

## Entry Function - OnTick()
The entry function is called `OnTick()`. It is executed on each tick of the market. The function performs the following steps for each symbol in the `SYMBOLS` list:

1. Selects the current symbol using `trade.SelectSymbol()`.
2. Calculates the high and low of the previous candle.
3. Calculates the breakout levels based on the high and low.
4. Checks if the current price is above the buy level. If true, it opens a buy trade using `trade.Buy()` and prints a message.
5. Checks if the current price is below the sell level. If true, it opens a sell trade using `trade.Sell()` and prints a message.

## Exit Function - OnDeinit()
The exit function is called `OnDeinit()`. It is executed when the EA is removed or the terminal is closed. The function performs the following steps:

1. Closes all open trades using `trade.CloseAll()`.
2. Prints a message indicating that all trades have been closed.

Please note that this code is a basic example and may require modifications and additional features to suit specific trading strategies.
