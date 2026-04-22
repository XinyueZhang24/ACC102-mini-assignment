# ACC102 Data Product: Multi-Dimensional Financial Analysis of AAPL, MSFT and WMT (2018-2024)

## 1. Project Title
Comprehensive Financial Performance Analysis of US Tech and Retail Giants Based on WRDS and Python (2018-2024)

## 2. Problem & User
### Research Problem
This project uses Python to calculate core financial indicators (Net Profit Margin, ROE, Debt to Asset Ratio, YoY Growth) for AAPL, MSFT, WMT (2018-2024) and visualize trends, to compare industry differences in financial performance.

### Key Research Questions
1. How do profitability indicators (Net Profit Margin/ROE) differ between tech and retail companies?
2. What are the solvency and growth characteristics of different industry enterprises?

### Target User
IBSS accounting/finance students learning financial data analysis with Python, financial analysis beginners, and anyone who needs to learn WRDS database operation, Python financial data processing and visualization.

## 3. Data Source
- Database: WRDS Compustat (comp.funda table)
- Companies: AAPL, MSFT, WMT
- Period: 2018-2024
- Variables: tic, fyear, sale, ni, at, lt, ceq
- Data Access Date: April 2026

## 4. Methods / Python Workflow
1. Data extraction: WRDS + SQL
2. Data cleaning: fyear to int, drop duplicates
3. Indicator calculation:
   - Profit_Margin = (ni/sale)*100
   - Debt_Asset_Ratio = (lt/at)*100
   - ROE = (ni/ceq)*100 (code line 24)
   - Sale_YoY = pct_change()*100
4. Visualization: 3×2 subplots (Net Profit Margin/Revenue/ROE/Debt Ratio/Growth)
5. Statistics: describe() grouped by tic 

## 5. Key Findings (from code output)
1. Profitability Differences: Microsoft (MSFT) maintains the highest average net profit margin (around 30-35%) among the three companies, followed by Apple (AAPL, around 20-25%), while Walmart (WMT) has a relatively low but stable margin (around 2-3%), reflecting differences in industry characteristics (technology vs. retail).
2. Leverage Level: Walmart has the highest debt-to-asset ratio (consistently above 60%), indicating higher financial leverage and reliance on debt financing; Apple and Microsoft maintain lower leverage (around 30-40%), showing stronger solvency.
3. ROE Performance: Microsoft and Apple have significantly higher ROE (usually above 30%) than Walmart (around 10-15%), which means the two technology companies have higher efficiency in using shareholders’ equity to generate profits.
4. Growth Volatility: Revenue YoY growth of Apple and Microsoft is more volatile (ranging from -5% to 15%) due to the impact of technology product cycles; Walmart’s revenue growth is more stable (around 2-5%), benefiting from its stable retail business model.
5. Overall Trend: All three companies maintained stable financial performance from 2018 to 2024, with no significant negative growth in net income, indicating strong operational resilience.

## 6. How to Run (match code exactly)
1. Install libraries: pip install wrds pandas matplotlib
2. Replace 'Your WRDS username' in code line 7 with your account
3. Run the script: all plots and statistics will output automatically

## 7. Product Link / Demo Video
- GitHub: https://github.com/XinyueZhang24/ACC102-mini-assignment
- Demo Video: [Your video link here]

## 8. Limitations & Next Steps (based on current code)
### Limitations (code's current constraints)
1. Code only analyzes 3 companies (no more in SQL query)
2. Code calculates only 5 basic indicators (no cash flow/asset turnover)
3. Code uses fillna(0) for missing values (simplified processing)
4. Code has no regression/correlation analysis (only basic plot)

### Next Steps (code improvement plan)
1. Expand Sample Size: Add more companies from different industries to enhance the representativeness of the analysis.
2. Add Quarterly Data: Retrieve and analyze quarterly financial data to capture short-term performance trends.
3. In-depth Analysis: Conduct correlation analysis between indicators (e.g., the relationship between debt-to-asset ratio and ROE) and add industry benchmark comparison.
4. Visualization Optimization: Fill the empty subplot with additional indicators (e.g., net income YoY growth) or adjust the figure layout to improve readability.
5. Add Error Handling: Add exception handling code (e.g., WRDS connection failure, missing data) to improve code robustness.
