# Investment Portfolio Optimization using Modern Portfolio Theory (MPT)

## Overview
This project aims to create an optimized investment portfolio using **Modern Portfolio Theory (MPT)** by selecting and allocating top-performing stocks across different sectors. The objective is to predict and balance the risk and return of the portfolio while achieving diversification through sector-specific stock selection.

## Project Structure

### Data Collection and Preparation

- **Data Sources:**
  - Historical stock price data from Yahoo Finance (2017-2022).
  - Sector-wise ticker symbols extracted from Wikipedia using `BeautifulSoup`.

- **Data Cleaning:**
  - Removed tickers with missing data for over a year.
  - Final datasets consist of cleaned historical price data for Industrials, Financials, and Materials sectors.

### Sector Analysis and Stock Selection

- **Industrials Sector:** `['FDX', 'ROL', 'PAYC']`
- **Financials Sector:** `['WFC', 'CMA', 'AIG']`
- **Materials Sector:** `['CF', 'NUE', 'MOS']`

Stocks were selected based on predicted future performance using a **Linear Regression model**.

### Linear Regression Model

- Transformed data to include current, past, and future prices.
- Calculated ratios like `c/p3`, `c/p2`, and `c/p1` for model training.
- Predicted future performance of stocks and selected the top 3 stocks from each sector.

### Portfolio Optimization

- Defined variables for mean and covariance of stocks.
- Utilized the **Bonmin solver** to solve the optimization problem.
- Optimized allocation of investments across sectors to minimize risk while maximizing returns.
- Identified optimal investment proportions for each stock in the portfolio.

### Buy & Hold Strategy

- Simulated a **Buy & Hold strategy** for the selected MPT portfolio.
- Compared performance against the **S&P 500 index**.
- Calculated metrics such as monthly returns, volatility, and cumulative returns.

### Monte Carlo Simulation

- Conducted 1000 simulations to estimate the probability of portfolio returns.
- Analyzed the distribution of portfolio returns and individual stock risks.
- Highlighted the importance of diversification and the impact of individual stock performance on overall portfolio risk.

### Performance Comparison and Conclusion

- MPT strategy demonstrated more consistent returns and lower volatility compared to the S&P 500 Buy & Hold strategy.
- Identified the best-performing stocks and optimal allocations to maximize returns while minimizing risks.
- Recommendations provided for investors considering the use of MPT principles in their investment approach.

## Key Takeaways

- **Stock Selection:** Stocks like _PAYC_, _ROL_, and _CMA_ were found to be better suited for the portfolio based on their performance and risk characteristics.
- **Risk-Return Trade-off:** Efficient frontier analysis showed that not all high-risk stocks yield high returns, highlighting the importance of careful stock selection.
- **Diversification:** Effective diversification significantly reduces overall portfolio risk compared to individual stock risks.
- **Monte Carlo Analysis:** Provided insights into the probability of losing money, helping to set realistic expectations for investment performance.

