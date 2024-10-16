# Real-Time Stock Dashboard

This is a real-time stock dashboard web application built using Streamlit and Plotly. It allows users to input a stock ticker, select a time period, choose a chart type, and add technical indicators to visualize stock data interactively.

# Features 
1. Real-Time Stock Data: Fetches stock price data in real-time using the Yahoo Finance API (yfinance).
2. Customizable Chart: Users can select from candlestick or line chart visualizations.
3. Technical Indicators: The app provides options to add simple moving averages (SMA) and exponential moving averages (EMA) to the stock charts.
4. Stock Metrics: Displays essential stock data such as last close price, daily change, high, low, and volume.
5. Historical Data Table: Users can view historical data with open, high, low, close prices, and volume.
6. Sidebar for Quick Stock Prices: Displays real-time prices for popular stock symbols (e.g., AAPL, GOOGL, AMZN, MSFT, TSLA) in the sidebar.

# Setup and Installation
## Prerequisites
1. Streamlit library
2. Plotly library
3. yfinance library for fetching stock data
4. ta library for calculating technical indicators

## Install Required Packages

Run the folloing command to install the required libraries

```bash
  pip install streamlit plotly yfinance ta-lib

```
## Running the Application 
to run the app, follow these steps:
1. clone the repository or download the Python script. 
2. Open a terminal or command prompt and navigate to the project directory.
3. Run the Streamlit app with the following command: 

```bash
  streamlit run <your_script_name>.Python
````
4. the app will open in a new browser tab. 

## Usage
1. Sidebar Parameter:
- Ticker: Enter the stock ticker symbol (e.g., AAPL for Apple).
- Time Period: Select the time range fro the stock data (1 day, 1 week, 1 month, 1 year, or max)
- Chart Type: Choose either a candlestick chart or a line chart.
- Technical Indicators: Optionally, add SMA 20 or EMA 20 to the chart.

2. Main Dashboard: 
- The main section displays the chart based on the selected parameters and metrics like last close price, high, low, and volume.
- Below the chart, the historical data and technical indicators (if selected) are displayed in a table.

3. Real-Time Stock Prices:
- The sidebar shows real-time stock prices for popular symbols like AAPL, GOOGL, AMZN, MSFT, and TSLA.

## Functions Overview
1. #### fetch_stock_data(ticker, period, interval)
Fetches stock data for a given ticker symbol, period (1 day, 1 week, etc.), and interval (e.g., 1 minute, 1 day).

2. #### process_data(data)
Processes the raw stock data to ensure the timestamps are timezone-aware and converts them to 'US/Eastern'. It also renames the Date column to Datetime.

3. #### calculate_metrics(data)
Calculates and returns stock metrics including the last close price, change, percent change, high, low, and total volume.

4. #### add_technical_indicators(data)
Adds technical indicators such as Simple Moving Average (SMA) and Exponential Moving Average (EMA) to the data.

5. #### Streamlit Dashboard
The Streamlit interface is split into:
- Sidebar: Takes user inputs for stock symbol, time period, and chart preferences.
- Main Content Area: Displays the selected stock’s chart and key metrics.

## License

[MIT](https://choosealicense.com/licenses/mit/)


## Screenshots

![App Screenshot](images/Dashboard_picture_1.png)

![App Screenshot](images/Dashboard_picture_2.png)
