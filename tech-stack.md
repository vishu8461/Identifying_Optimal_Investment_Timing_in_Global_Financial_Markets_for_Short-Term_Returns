# Tech Stack for Short-Term Investment Timing Analysis

This project is a business intelligence and data analytics exercise. The selected technology stack is centered on Excel, Power BI, and SQL. Python and machine learning are intentionally excluded.

## Core Tools

- **Excel**
  - Data ingestion and preparation
  - Adjusted close price calculations
  - Monthly and quarterly return computation
  - Pivot tables for summary tables and cross-tab analysis
  - Charts for seasonality, asset performance, and risk comparisons
  - Scenario modeling for timing strategies and portfolio mixes

- **Power BI**
  - Import and model cleaned datasets from Excel or CSV
  - Create interactive dashboards and visuals
  - Build slicers for asset class, date range, and period views
  - Use DAX for key measures such as average returns, win rates, and volatility
  - Present findings in a business-friendly dashboard format

- **SQL** (optional but recommended for data organization)
  - Store normalized tables such as `Assets`, `PriceHistory`, and `Returns`
  - Run aggregate queries for data validation and intermediate summaries
  - Support a clean import pipeline into Excel or Power BI

## Project Constraints

- No Python usage
- No machine learning algorithms
- No advanced statistical packages beyond Excel and Power BI native features
- Focus is on descriptive analytics and visual insight

## Recommended Workflow

1. Collect raw historical price data
2. Store or stage the data using SQL tables if needed
3. Import or link data into Excel for cleansing and return calculations
4. Build PivotTables and charts in Excel to identify patterns
5. Import results into Power BI for dashboards and executive reporting
6. Use Excel for detailed numeric checks and Power BI for presentation

## Why This Stack Works

- Excel is widely used for financial analysis and allows direct control over calculations.
- Power BI delivers interactive visual storytelling for stakeholders.
- SQL provides structure and repeatability for data preparation.
- The combination keeps the project accessible to business users and avoids software development complexity.
