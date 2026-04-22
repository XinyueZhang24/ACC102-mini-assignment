# ACC102 Data Product: US Tech vs Retail Profitability Analysis (2018–2024)

## 1. Project Overview
This data product uses Python and WRDS financial data to analyze and compare the profitability and revenue performance of three leading US listed companies: Apple (AAPL), Microsoft (MSFT), and Walmart (WMT) from 2018 to 2024.
The product provides clear visual trend charts and statistical summaries, helping accounting & finance students understand industry differences in corporate financial performance.

## 2. Analytical Purpose & Target User
### Analytical Problem
Compare net profit margin, annual revenue and net income trends between high-margin tech industry and low-turnover retail industry.

### Key Research Questions
1. How do net profit margins differ between tech and retail industries?
2. How do company revenue & profitability change during 2018-2024 economic cycles?
3. Does larger revenue scale bring higher corporate profitability?

### Target User
IBSS accounting & finance students, entry-level investors and financial analysis beginners.

## 3. Data Source
- Database: WRDS Compustat (comp.funda table)
- Sample Companies: AAPL (Apple), MSFT (Microsoft), WMT (Walmart)
- Research Period: Fiscal Year 2018 – 2024
- Financial Variables: tic (stock code), fyear (fiscal year), sale (total revenue), ni (net income)
- Data Access Date: April 2026

## 4. Python Analysis Workflow
1. Extract standardized financial data through WRDS SQL query
2. Data cleaning: format conversion, duplicate removal, missing value filling
3. Core indicator calculation: Net Profit Margin = (Net Income / Revenue) × 100%
4. Multi-dimensional data visualization:
   - Net profit margin annual trend line chart
   - Annual operating revenue comparison bar chart
   - Descriptive financial statistics summary table
5. Output charts & data analysis conclusions

## 5. Core Research Findings
1. Technology giants Apple & Microsoft have **far higher net profit margins** than retail giant Walmart.
2. Walmart owns huge revenue volume, but maintains low and stable profit margin, matching its low-margin high-volume business model.
3. Tech enterprises show stronger profitability resilience during economic volatility periods.
4. Enterprise revenue scale cannot directly determine the level of net profit margin.
