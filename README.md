ReadMe file for the code - mql5

# Sydney MT5 Expert Advisor

Sydney MT5 is an Expert Advisor (EA) designed to automate trading in the MetaTrader 5 platform. This EA is developed by the Forex Robot Easy Team and can be downloaded from [ForexRobotEasy.com](https://www.forexroboteasy.com). Please note that ForexRobotEasy is not the official developer of this product, and this code is provided as a sample that can work as described in the product.

For detailed reviews and trading results of this product, please visit the [Sydney MT5 Software Review](https://forexroboteasy.com/forex-robot-review/sydney-mt5-software-review-forex-trading-results-download/) page on ForexRobotEasy.com.

## Features

- Fully automated trading system for the MetaTrader 5 platform
- Uses a custom indicator to identify trading opportunities
- Opens a market order when a trading opportunity is found
- Supports stop loss and take profit levels
- Closes existing orders when the EA starts
- Runs continuously until manually stopped
- Provides order opening and closing status messages

## Installation

1. Download the Sydney MT5 Expert Advisor from [ForexRobotEasy.com](https://www.forexroboteasy.com).
2. Open the MetaTrader 5 platform.
3. Go to 'File' > 'Open Data Folder' to open the data folder.
4. Copy the Sydney MT5 Expert Advisor file (Sydney MT5.mq5) into the 'MQL5/Experts' folder.
5. Restart the MetaTrader 5 platform.
6. Open a chart of the desired currency pair.
7. Drag and drop the Sydney MT5 Expert Advisor from the Navigator window onto the chart.
8. Adjust the input parameters (LotSize, StopLoss, TakeProfit) as desired.
9. Enable automated trading and allow live trading in the platform settings.
10. Click the 'AutoTrading' button in the toolbar to start the EA.

## Input Parameters

- LotSize: The lot size for trading. Default: 0.01
- StopLoss: The stop loss level in pips. Default: 20
- TakeProfit: The take profit level in pips. Default: 40

## Custom Indicator Function

The custom indicator function (FindOpportunity) is responsible for identifying trading opportunities. You can add your own algorithm and trading strategy in this function. Return 1 if a trading opportunity is found, otherwise return 0. For example, you can use moving averages, RSI, or any other indicator.

## Opening and Closing Orders

The OpenOrder function is used to open a market order. It checks if a trading opportunity is available, calculates the stop loss and take profit prices, and then opens the order using the OrderSend function. If the order is opened successfully, the ticket number and order type are printed.

The CloseOrder function is used to close an existing order. It checks if the order is still open, and then closes the order using the OrderClose function. If the order is closed successfully, the ticket number is printed.

## Expert Advisor Functions

- OnInit: This function is called during the EA initialization process. Set up necessary parameters and indicators here. Returns INIT_SUCCEEDED if initialization is successful.
- OnStart: This function is called when the EA starts. It closes any existing orders and then continuously checks for trading opportunities. If a trading opportunity is found, it opens both a buy and sell order. Sleeps for 1 second before checking for trading opportunities again.
- OnDeinit: This function is called during the EA deinitialization process. Perform any necessary cleanup here.

## Disclaimer

Please note that ForexRobotEasy is not the official developer of the Sydney MT5 Expert Advisor. We only provide this code as a sample that can work as described in the product. To find the official developer of this product, please use the MQL5 website.

For detailed reviews and trading results of this product, please visit the [Sydney MT5 Software Review](https://forexroboteasy.com/forex-robot-review/sydney-mt5-software-review-forex-trading-results-download/) page on ForexRobotEasy.com.
