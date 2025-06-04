# Octagon Stock Market Data MCP

![Favicon](https://docs.octagonagents.com/logo.svg) The Octagon Stock Market Data MCP server provides specialized AI-powered stock market data and valuation analysis capabilities by integrating with advanced stock data agents. Real-time market data, comprehensive technical indicators, and unlimited market intelligence. Add unlimited stock market data functionality to any MCP client including Claude Desktop, Cursor, and other popular MCP-enabled applications.

**Powered by [Octagon AI](https://docs.octagonagents.com)** - Learn more about the Stock Data Agent at [docs.octagonagents.com](https://docs.octagonagents.com/guide/agents/stock-data-agent.html)

[![Demo](https://img.youtube.com/vi/yh1cyrm9aus/0.jpg)](https://youtu.be/yh1cyrm9aus)

## 🏆 Why Teams Choose Octagon's Enterprise-Grade Stock Market Data API

👉 **Real-time market data** — Access live stock prices, trading volumes, and market indicators  
👉 **Comprehensive analysis** — Technical indicators, valuation metrics, and performance benchmarks  
👉 **Unlimited queries** — No rate limits on stock data requests (unlike other providers)  

## 🚀 Core Differentiators

✅ **No Rate Limits** - Execute unlimited stock market data queries without restrictions  
✅ **Real-Time Data** - Live stock prices, trading volumes, and market indicators  
✅ **Comprehensive Coverage** - Stock indices, sector performance, and industry analysis  
✅ **Universal MCP Integration** - Add stock market data functionality to any MCP client  
✅ **Advanced Analytics** - Technical indicators, valuation ratios, and price patterns  
✅ **Multi-Market Support** - NYSE, NASDAQ, and other major exchanges  

## Features

✅ **Stock Market Data**
   - Real-time and historical stock prices
   - Trading volumes and patterns
   - Market capitalization data
   - Price movements and volatility metrics
     
✅ **Valuation Analysis**
   - P/E ratios by company, sector, and industry
   - EV/Sales and other valuation multiples
   - Analyst price targets and ratings
   - Market performance benchmarks
     
✅ **Technical Analysis**
   - Technical indicators and chart patterns
   - Trading volume analysis
   - Price trend identification
   - Support and resistance levels

## Get Your Octagon API Key

To use Octagon Stock Market Data MCP, you need to:

1. Sign up for a free account at [Octagon](https://app.octagonai.co/signup/?redirectToAfterSignup=https://app.octagonai.co/api-keys)
2. After logging in, from left menu, navigate to **API Keys** 
3. Generate a new API key
4. Use this API key in your configuration as the `OCTAGON_API_KEY` value

## Prerequisites

Before installing or running Octagon Stock Market Data MCP, you need to have `npx` (which comes with Node.js and npm) installed on your system.

### Mac (macOS)

1. **Install Homebrew** (if you don't have it):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. **Install Node.js (includes npm and npx):**
   ```bash
   brew install node
   ```
   This will install the latest version of Node.js, npm, and npx.

3. **Verify installation:**
   ```bash
   node -v
   npm -v
   npx -v
   ```

### Windows

1. **Download the Node.js installer:**
   - Go to [https://nodejs.org/](https://nodejs.org/) and download the LTS version for Windows.
2. **Run the installer** and follow the prompts. This will install Node.js, npm, and npx.
3. **Verify installation:**
   Open Command Prompt and run:
   ```cmd
   node -v
   npm -v
   npx -v
   ```

If you see version numbers for all three, you are ready to proceed with the installation steps below.

## Installation

### Running on Claude Desktop

To configure Octagon Stock Market Data MCP for Claude Desktop:

1. Open Claude Desktop
2. Go to Settings > Developer > Edit Config
3. Add the following to your `claude_desktop_config.json` (Replace `your-octagon-api-key` with your Octagon API key):
```json
{
  "mcpServers": {
    "octagon-stock-market-data-mcp": {
      "command": "npx",
      "args": ["-y", "octagon-stock-market-data-mcp@latest"],
      "env": {
        "OCTAGON_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```
4. Restart Claude for the changes to take effect

### Running on Cursor

Configuring Cursor Desktop 🖥️
Note: Requires Cursor version 0.45.6+

To configure Octagon Stock Market Data MCP in Cursor:

1. Open Cursor Settings
2. Go to Features > MCP Servers 
3. Click "+ Add New MCP Server"
4. Enter the following:
   - Name: "octagon-stock-market-data-mcp" (or your preferred name)
   - Type: "command"
   - Command: `env OCTAGON_API_KEY=your-octagon-api-key npx -y octagon-stock-market-data-mcp`

> If you are using Windows and are running into issues, try `cmd /c "set OCTAGON_API_KEY=your-octagon-api-key && npx -y octagon-stock-market-data-mcp"`

Replace `your-octagon-api-key` with your Octagon API key.

After adding, refresh the MCP server list to see the new tools. The Composer Agent will automatically use Octagon Stock Market Data MCP when appropriate, but you can explicitly request it by describing your stock market data needs. Access the Composer via Command+L (Mac), select "Agent" next to the submit button, and enter your query.

### Running on Windsurf

Add this to your `./codeium/windsurf/model_config.json`:

```json
{
  "mcpServers": {
    "octagon-stock-market-data-mcp": {
      "command": "npx",
      "args": ["-y", "octagon-stock-market-data-mcp@latest"],
      "env": {
        "OCTAGON_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```

### Running with npx

```bash
env OCTAGON_API_KEY=your_octagon_api_key npx -y octagon-stock-market-data-mcp
```

### Manual Installation

```bash
npm install -g octagon-stock-market-data-mcp
```

## Documentation

For comprehensive documentation on using Stock Market Data capabilities, please visit our official documentation at:
[https://docs.octagonagents.com](https://docs.octagonagents.com)

Specifically for the Stock Data Agent: [Stock Data Agent Guide](https://docs.octagonagents.com/guide/agents/stock-data-agent.html)

The documentation includes:
- Detailed API references
- Market data methodology guidelines
- Examples and use cases
- Best practices for stock market analysis
- Advanced features and capabilities

## Available Tool

### octagon-stock-data-agent
Specialized agent for stock market data and valuation analysis.

The tool uses a single `prompt` parameter that accepts a natural language query. Include all relevant details in your prompt for optimal results.

# Octagon Stock Data Agent

**Model Name**: `octagon-stock-data-agent`

Specialized agent for stock market data and analysis, providing comprehensive insights into market performance and valuation.

## Capabilities

- Analyze stock price and indices movements
- Track trading volumes and patterns
- Monitor market trends
- Assess technical indicators
- Compare stock performance against benchmarks
- Provide detailed valuation insights

## Use Cases

The Stock Data Agent is best for:
- Stock market research
- Equity analysis
- Trading pattern identification
- Performance benchmarking
- Identifying price catalysts
- Valuation analysis and assessment

## Example Queries

### Get Batch Market Cap

Fetch market capitalization data for multiple given companies.

```
@octagon-stock-data-agent Retrieve market capitalization data for the following companies: AAPL, MSFT, GOOG.
```

### Get Company Market Cap

Retrieve current market capitalization data for a given company.

```
@octagon-stock-data-agent Get a snapshot of financial ratings for the symbol AAPL with a limit of 10 results.
```

### Get Ratings Snapshot

Obtain a snapshot of financial ratings for a specific company.

```
@octagon-stock-data-agent Get a snapshot of financial ratings for the symbol AAPL with a limit of 10 results.
```

### Get Price Target Summary

Access analysts' price-target summaries for a given company's stock.

```
@octagon-stock-data-agent Retrieve the analysts' price-target summary for the stock symbol AAPL.
```

### Get Price Target Consensus

Fetch consensus analyst price targets for a specific company's stock.

```
@octagon-stock-data-agent Retrieve consensus price targets for the stock symbol AAPL.
```

### Get Stock Grades

Obtain the latest stock grades from leading analysts and financial institutions for a given company.

```
@octagon-stock-data-agent Get the latest stock grades for the symbol AAPL from top analysts and financial institutions.
```

### Get Sector PE Ratios

Retrieve current sector price-to-earnings ratios filtered by exchange and sector.

```
@octagon-stock-data-agent Retrieve the latest sector P/E ratios for 2025-02-03, filtered by exchange NASDAQ and sector Technology.
```

### Get Industry PE Ratios

Fetch current industry price-to-earnings ratios filtered by exchange and industry.

```
@octagon-stock-data-agent Retrieve the latest industry P/E ratios for 2025-02-03, filtered by exchange NYSE and industry Semiconductors.
```

### Get Sector Performance Snapshot

Obtain a snapshot of market sector performance filtered by date, exchange, and sector.

```
@octagon-stock-data-agent Retrieve a snapshot of market sector performance for 2025-02-03, filtered by exchange NASDAQ and sector Technology.
```

### Get Industry Performance Snapshot

Retrieve daily industry performance overview filtered by date, exchange, and industry.

```
@octagon-stock-data-agent Retrieve a daily overview of industry performance for 2025-02-03, filtered by exchange NASDAQ and industry Biotechnology.
```

### Get Historical Market Cap

Access historical market capitalization data for a given company within a specified date range.

```
@octagon-stock-data-agent Retrieve historical market capitalization data for AAPL from from 2025-01-01 to 2025-04-30, limited to 1000 records.
```

### Get Historical Index Full Chart

Fetch complete historical end-of-day price data for a specified market index within a given date range.

```
@octagon-stock-data-agent Retrieve full historical end-of-day price data for the ^GSPC index from from 2025-01-01 to 2025-04-30.
```

### Get Historical Index Light Chart

Obtain historical end-of-day prices for a specified market index over a given period.

```
@octagon-stock-data-agent Get historical end-of-day prices for the ^GSPC index from 2025-01-01 to 2025-04-30.
```

### Get Stock Price Change

Retrieve statistics on price changes for a specific company's stock.

```
@octagon-stock-data-agent Get stock price change statistics for the symbol AAPL.
```

### Get Stock Quote

Fetch a real-time stock quote for a specific company.

```
@octagon-stock-data-agent Get real-time stock quote for the symbol AAPL.
```

## Code Examples

::: code-group

```Python
response = client.responses.create(
    model="octagon-stock-data-agent",
    input="How has Apple's stock performed compared to the S&P 500 over the last 6 months?",
)
```

```JavaScript
const response = await client.responses.create({
  model: "octagon-stock-data-agent",
  input: "How has Apple's stock performed compared to the S&P 500 over the last 6 months?",
});
```

```cURL
curl -X POST https://api-gateway.octagonagents.com/v1/responses \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer your-octagon-api-key" \
  -d '{
    "model": "octagon-stock-data-agent",
    "input": "How has Apple's stock performed compared to the S&P 500 over the last 6 months?",
    "stream": true
  }' \
  --no-buffer
```

::: 


## How to Create Effective Prompts for Stock Data Analysis

When querying stock data, consider these strategies:

1. **Specify precise time ranges**: Include exact date ranges to limit the data scope.
   - Example: "Analyze AAPL price movement between January 1, 2023 and March 15, 2023."

2. **Indicate data granularity**: Specify whether you need tick-by-tick, minute, hour, day, or other timeframes.
   - Example: "Extract hourly volume data for TSLA during market hours on February 14, 2024."

3. **Clarify the metrics needed**: Be specific about which data points you're interested in.
   - Example: "Calculate the average daily trading range for NVDA over the past 30 trading days."

4. **Request comparative analysis**: Ask for comparisons between securities or time periods.
   - Example: "Compare the daily VWAP for AMZN, GOOG, and META during the last earnings season."

5. **Define visualization preferences**: Specify chart types or visualization needs.
   - Example: "Generate a candlestick chart with 50-day and 200-day moving averages for SPY."

6. **Focus on specific events**: Target data around particular market events.
   - Example: "Analyze the trading volume pattern for MSFT in the 48 hours following their Q4 earnings announcement."

7. **Include technical indicators**: Specify which technical analysis metrics to calculate.
   - Example: "Calculate and plot the RSI, MACD, and Bollinger Bands for AMD over the past 3 months."

8. **Request pattern identification**: Ask for detection of specific price or volume patterns.
   - Example: "Identify any instances of gap up openings followed by price reversals for COIN in 2023."

## Stock Data Available Fields

### Market Data (Real-time & Historical)

| Field | Description |
|-------|-------------|
| Open | Opening price for the specified time period |
| High | Highest price reached during the specified time period |
| Low | Lowest price reached during the specified time period |
| Close | Closing price for the specified time period |
| Volume | Number of shares traded during the specified time period |
| VWAP | Volume Weighted Average Price |
| Timestamp | Exact time of the data point |
| After Hours | After-hours trading price |
| Pre-market | Pre-market trading price |
| Adjusted Close | Close price adjusted for splits and dividends |
| Trade Count | Number of individual trades executed |
| Tick Size | Minimum price movement increment |
| Weighted Average | Weighted average price based on specified criteria |
| Spread | Difference between ask and bid prices |
| Number of Trades | Count of executed trades within the time period |
| Dividend Yield | Annual dividend payments as percentage of share price |
| 52-Week High | Highest price in the past 52 weeks |
| 52-Week Low | Lowest price in the past 52 weeks |
| Average Volume | Average daily trading volume |
| Market Cap | Total market value of outstanding shares |
| Historical Market Cap | Historical market value of outstanding shares over time period|
| Enterprise Value | Market cap plus debt minus cash |

### Technical Indicators

| Field | Description |
|-------|-------------|
| Simple Moving Average (SMA) | Average price over a specified number of periods |
| Exponential Moving Average (EMA) | Weighted moving average giving more importance to recent prices |
| Relative Strength Index (RSI) | Momentum oscillator measuring speed and change of price movements |
| Moving Average Convergence Divergence (MACD) | Trend-following momentum indicator |
| Bollinger Bands | Volatility bands placed above and below a moving average |
| Average True Range (ATR) | Market volatility indicator |
| On-Balance Volume (OBV) | Volume-based momentum indicator |
| Stochastic Oscillator | Momentum indicator comparing closing price to price range |
| Fibonacci Retracement | Potential support/resistance levels based on Fibonacci sequence |
| Ichimoku Cloud | Collection of indicators showing support/resistance, momentum, and trend direction |
| Volume Profile | Distribution of volume at different price levels |
| Money Flow Index (MFI) | Volume-weighted RSI |
| Average Directional Index (ADX) | Trend strength indicator |

### Volatility Metrics

| Field | Description |
|-------|-------------|
| Historical Volatility | Standard deviation of price changes over a specified period |
| Implied Volatility | Market's forecast of likely movement derived from options prices |
| Average True Range (ATR) | Average of true ranges over specified time period |
| Beta | Measure of stock's volatility compared to the overall market |
| Volatility Surface | Three-dimensional plot of implied volatility across strike prices and expirations |
| Volatility Smile | Pattern of implied volatility across different strike prices |
| Volatility Term Structure | Pattern of implied volatility across different expiration dates |
| Volatility Skew | Difference in implied volatility between out-of-money options |
| CBOE Volatility Index (VIX) Data | Market's expectation of 30-day forward-looking volatility |
| Realized Volatility | Actual historical volatility over a specific period |
| Volatility Ratio | Comparison of short-term to long-term volatility |

### Price Pattern Analysis

| Field | Description |
|-------|-------------|
| Gap Up/Down | Price difference between previous close and current open |
| Support Levels | Price levels where downward trends tend to pause |
| Resistance Levels | Price levels where upward trends tend to pause |
| Price Channels | Parallel lines that contain price movement |
| Chart Patterns | Identified patterns such as head and shoulders, double tops, etc. |
| Trend Lines | Lines connecting price highs or lows to identify trends |
| Breakout/Breakdown Points | Prices at which security moves outside established patterns |
| Pivot Points | Calculated levels used to determine potential support/resistance |
| Price Reversals | Points where price trend changes direction |
| Average Daily Range | Average price movement within a trading day |
| Volume Spikes | Unusual increases in trading volume |
| Price Momentum | Rate of acceleration in price movement |
| Consolidation Zones | Areas where price moves sideways within a range |

### Company Reference Data

| Field | Description |
|-------|-------------|
| Ticker | Stock trading symbol |
| Company Name | Legal name of the company |
| Exchange | Stock exchange where the security is listed |
| Industry | Primary industry classification |
| Sector | Broader market sector classification |
| Market Cap | Total market value of outstanding shares |
| Shares Outstanding | Total number of shares issued by the company |
| Float | Number of shares available for public trading |
| Primary Exchange | Main exchange where the stock is listed |
| Currency | Currency in which the stock is traded |
| Country | Country where the company is headquartered |
| CIK | Central Index Key (SEC identifier) |
| FIGI | Financial Instrument Global Identifier |
| ISIN | International Securities Identification Number |
| CUSIP | Committee on Uniform Security Identification Procedures identifier |

### Corporate Actions

| Field | Description |
|-------|-------------|
| Dividends | Cash payments distributed to shareholders |
| Stock Splits | Division of existing shares into multiple shares |
| Reverse Splits | Consolidation of shares to form fewer, higher-priced shares |
| Spinoffs | Creation of independent company through distribution of shares |
| Mergers & Acquisitions | Information about corporate combinations |
| Rights Offerings | Issuance of rights to purchase additional shares |
| Symbol Changes | Updates to ticker symbols |
| IPO Date | Initial public offering date |
| Delisting Events | Removal from trading on an exchange |
| Name Changes | Changes to company name |
| Dividend Ex-Date | Date when shares begin trading without dividend rights |
| Dividend Record Date | Date determining which shareholders receive dividends |
| Dividend Payment Date | Date when dividends are actually paid |
| Split Ratio | Ratio for stock splits (e.g., 2:1, 3:1) |

### Valuation Ratios

| Metric | Description |
|--------|-------------|
| PE Ratio | Price per share divided by earnings per share |
| PEG Ratio | PE ratio divided by earnings growth rate |
| Forward PEG Ratio | Forward PE ratio divided by expected earnings growth rate |
| PB Ratio | Price per share divided by book value per share |
| PS Ratio | Price per share divided by sales per share |
| PCF Ratio | Price per share divided by free cash flow per share |
| POCF Ratio | Price per share divided by operating cash flow per share |
| Price to Fair Value | Current price divided by estimated fair value |
| EV to Sales | Enterprise value divided by sales |
| EV to Operating Cash Flow | Enterprise value divided by operating cash flow |
| EV to EBITDA | Enterprise value divided by EBITDA |

## Troubleshooting

1. **API Key Issues**: Ensure your Octagon API key is correctly set in the environment or config file.
2. **Connection Issues**: Make sure the connectivity to the Octagon API is working properly.
3. **Rate Limiting**: No rate limits apply to Stock Market Data MCP - execute unlimited queries.

## License

MIT 

---

⭐ Star this repo if you find it helpful for your stock market analysis needs!
