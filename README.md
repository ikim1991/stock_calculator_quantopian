# Stock Calculator on Quantopian

## Getting Started

Using the Quantopian IDE and Jupyter Notebook, this application performs a fundamental analysis of US Equities looking at the financial statement data, liquidity/solvency metrics, profitability metrics, and growth/return metrics. The [./stock_calculator_quantopian.ipynb](./stock_calculator_quantopian.ipynb) file is only for reference and can only be executed on the Quantopian IDE. To run and utilize this code, as well as many of Quantopian's features, it is recommended to sign up at https://www.quantopian.com/home. The stock calculator uses Python's Pandas and Matplotlib libraries to query and visualize the financial data for the user.

The stock calculator consists of four different pipelines used to query different sets of financial data for analysis. These include the company profile, balance sheet, income statement, and the cash flow statement. As an example the stock calculator looks at Apple Inc ('AAPL') from '2014-01-01' to '2019-03-25'.

A fundamental analysis looks at the intrinsic value of a company assessed from the balance sheet, income statement and cash flow statement found in the company's financial statements. The financial statement mainly outlines the general health of the company, the profitability/earnings potential, and its prospects for growth. When making investment decisions the fundamentals should only be used as a guideline and should not be the sole indicator as equity prices depend on many variables where all the risks cannot be accounted for.

## Company Profile Pipeline

The company reference pipeline takes in the stock ticker, and the most recent date to query financial data about the company's profile. The following financial data and metrics are calculated using this pipeline. This pipeline mainly looks at:
  - The Trading Price
  - Market Capitalization
  - Price to Earnings Ratio
  - Price to Book Value Ratio
  - Earnings per Share
  - Book Value per Share
  - Dividend per Share
  - Earning Multiple
  - Margin of Safety

## Balance Sheet Pipeline

The balance sheet pipeline takes in the stock ticker, and the start and end dates to be analyzed. The balance sheet pipeline outputs the quarter-end balance sheet items including:
  - Total Assets
  - Cash and Cash Equivalents
  - Total Liabilities
  - Total Equity
  - Retained Earnings
  - Tangible Book Value
  - Tangible Book Value/Share
  - Current Ratio
  - Debt to Assets Ratio
  - Debt to Equity Ratio

Using Pandas, the quarter-end financial data is consolidated into annualized data.

## Income Statement Pipeline

The balance sheet pipeline takes in the stock ticker, and the start and end dates to be analyzed. The income statement pipeline outputs the quarter-end income statement items including:
  - Revenue
  - Normalized Net Income
  - Diluted EPS
  - Cost of Goods Sold
  - Operating Expense
  - Gross Margin
  - Operating Margin
  - Net Margin

Using Pandas, the quarter0end financial data is consolidated into annualized data.

## Cash Flow Statement Pipeline

The balance sheet pipeline takes in the stock ticker, and the start and end dates to be analyzed. The cash flow statement pipeline outputs the quarter-end cash flow statement items including:
  - Operating Cash Flow
  - Capital Expenditure
  - Investing Cash Flow
  - Free Cash Flow
  - Financing Cash Flow

## Financial Metrics

Using the financial statement data from the balance sheet, income statement and cash flow statement pipelines, the following metrics are accounted for:
  - Margin of Safety
  - Return on Assets
  - Return on Equity
  - Current Ratio
  - Debt to Assets
  - Debt to Equity
  - Company Margins (Gross / Operating / Net)

## Visualizations on Matplotlib

Using Matplotlib the financial data is plotted for the user. Given that the company is not pre-revenue or operating under a loss, the data is also normalized using Pandas and plotted in Matplotlib.
