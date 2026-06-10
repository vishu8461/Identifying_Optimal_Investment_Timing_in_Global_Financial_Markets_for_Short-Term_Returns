# Dataset Specification for Investment Timing Analysis

This document describes the recommended dataset structure for the project. The goal is to collect enough historical asset data to compare short-term returns across major asset classes and identify calendar-based timing patterns.

## Dataset Objective

Collect historical price data that supports:
- 1-month and 3-month return analysis
- monthly and quarterly seasonality studies
- asset class performance comparisons
- portfolio scenario modeling

## Required Fields

Each record should include:
- `Date` (preferably month-end or quarterly date)
- `Asset Name`
- `Asset Type` (e.g. Equity, Bond, Commodity, Currency, Crypto, REIT)
- `Region` or `Market`
- `Ticker` or `Symbol`
- `Currency` (USD preferred for consistency)
- `Adjusted Close Price`
- `Source` (e.g. Yahoo Finance, FRED, index provider)
- `Data Frequency` (monthly, quarterly, or daily)
- `Notes` or `Quality Flag` for missing or estimated values

## Recommended Asset Groups

- **Equities**
  - S&P 500 index
  - MSCI World index
  - MSCI Emerging Markets index
  - Major regional indices if available (Europe, Asia Pacific)

- **Bonds**
  - Bloomberg US Aggregate Bond index or equivalent
  - Global government bond index
  - Corporate bond index

- **Commodities**
  - Gold price
  - Crude oil price
  - Silver or copper price

- **Currencies**
  - US Dollar Index (DXY)
  - EUR/USD
  - USD/JPY

- **Cryptocurrencies**
  - Bitcoin

- **Real Estate**
  - Global REIT index or US REIT index

## Data Granularity

- Monthly data is preferred because it directly matches the short-term timing objective.
- Daily data is acceptable if it can be reliably aggregated into monthly and quarterly periods.
- Use adjusted closing prices for equity indices or ETF proxies.

## Source Recommendations

Collect data from trusted, publicly accessible sources:
- Yahoo Finance (adjusted close prices for indices and ETFs)
- FRED (bond index series and macro indicators)
- Exchange or provider downloads for commodity prices
- Public index provider data for REIT and global bond series
- Cryptocurrency exchange historical price exports for Bitcoin

## Dataset Use Cases

With this dataset, the project can answer:
- Which asset classes had the best 1-month and 3-month returns historically?
- Which months or quarters produced the strongest returns for each asset?
- How did different assets behave in weak or strong market periods?
- What simple timing rules can be derived for short-term allocation?

## Practical Data Collection Notes

- Prefer USD-denominated prices so all assets are comparable.
- If using daily data, use month-end values to compute monthly returns.
- Document any gaps, index changes, or data adjustments clearly.
- Keep the dataset narrow enough for Excel and Power BI to handle comfortably.

## Recommended Output Structure

For Excel or Power BI, the cleaned dataset should be shaped as a flat table with one row per date-and-asset combination. Example columns:
- `Date`
- `Asset Name`
- `Asset Type`
- `Region`
- `Ticker`
- `Currency`
- `Adjusted Close`
- `Monthly Return`
- `Quarterly Return`
- `Source`
- `Notes`

This provides a clean foundation for pivoting, filtering, and dashboarding without requiring code or advanced tools.
