# Market Screener Expert Advisor

This is an Expert Advisor (EA) called 'Market Screener' developed by the Forex Robot Easy Team. This EA is designed to scan the market for overbought and oversold assets based on the RSI (Relative Strength Index) indicator.

## Input Parameters

The EA has the following input parameters:

- **TimeFrame**: The timeframe for analysis. The default value is PERIOD_H1 (1 hour).
- **Inst**: The instrument for trading. The default value is SYMBOL_INFO_POINT.
- **OverboughtLevel**: The level for identifying overbought assets. The default value is 70.
- **OversoldLevel**: The level for identifying oversold assets. The default value is 30.

## Global Variables

The EA uses the following global variable:

- **lastCheckTime**: The last time the market was checked. It is initialized with a value of 0.

## Expert Initialization Function

The `OnInit()` function is the initialization function of the EA. In this function, you can set the necessary indicators or initialize any required variables. In this code, the function does not perform any specific initialization tasks and returns `INIT_SUCCEEDED` to indicate successful initialization.

## Expert Deinitialization Function

The `OnDeinit()` function is the deinitialization function of the EA. It is called when the EA is removed from the chart or when the terminal is shut down. In this function, you can clean up any resources used by the expert. In this code, the function is empty.

## Expert Tick Function

The `OnTick()` function is the main function of the EA that is executed on each tick of the chart. In this function, the EA checks if enough time has passed since the last market check and performs the market scan for overbought or oversold assets.

The EA checks if 60 seconds have passed since the last market check using the condition `TimeCurrent() - lastCheckTime < 60`. If not enough time has passed, the function returns.

The EA then retrieves the current price and RSI value for the specified symbol and timeframe. The RSI calculation is performed using the `iRSI()` function with the parameters `_Symbol`, `TimeFrame`, `14`, `PRICE_CLOSE`, `0`.

The EA checks if the current RSI value is above the OverboughtLevel. If it is, the EA performs actions for overbought assets (not specified in the code) and prints a message indicating that the asset is overbought.

The EA also checks if the current RSI value is below the OversoldLevel. If it is, the EA performs actions for oversold assets (not specified in the code) and prints a message indicating that the asset is oversold.

After performing the necessary actions and printing the messages, the EA updates the last check time to the current time.

## Product Description

This code serves as a sample implementation of the 'Market Screener' EA developed by the Forex Robot Easy Team. It is not the official code of the product, but it demonstrates how the EA can work based on the provided input parameters and logic.

The 'Market Screener' EA is designed to scan the market for overbought and oversold assets using the RSI indicator. It allows traders to identify potential trading opportunities based on these market conditions.

To find the official developer of the 'Market Screener' EA or for detailed reviews and trading results of the product, please visit the following link: [Market Screener for MT4 - Review, Download, Real Results](https://forexroboteasy.com/forex-robot-review/market-screener-for-mt4-review-download-real-results-professional-forex-trader/). Please note that Forex Robot Easy is not the official developer of this product and only provides a sample code that can work as described in the product. For official information and support, please refer to the developer's website or use MQL5.
