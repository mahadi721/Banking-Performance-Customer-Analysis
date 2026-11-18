Banking Performance & Customer Analytics Dashboard
Project Overview
This project uses Microsoft Power BI to analyse banking data and present key information about customers, accounts, loans, and transactions in an interactive dashboard.
The dashboard helps users explore banking performance, understand customer and account activity, monitor loan statuses, and review transaction patterns across channels and regions.
Objectives
Analyse customer demographics and customer segments.
Understand account distribution, account status, and account balances.
Examine loan portfolios, loan types, and loan statuses.
Evaluate transaction volumes, values, channels, and statuses.
Present key performance indicators (KPIs) in an interactive report to support data-driven decision-making.
Dataset
The project uses five related datasets:
Dataset	Description
`Customers`	Customer details, including registration date, segment, gender, and occupation.
`Accounts`	Account type, opening date, status, balance, and related customer and branch IDs.
`Branches`	Branch information, including region and city.
`Loans`	Loan date, type, status, amount, and interest rate.
`Transactions`	Transaction date, type, channel, status, amount, and account ID.
The datasets contain 180 customers, 220 accounts, 120 branches, 160 loan records, and 1,200 transaction records.
Tools and Technologies
Microsoft Power BI – dashboard development and data visualisation.
Power Query – data importing, cleaning, and transformation.
DAX – measures and calculations.
Microsoft Excel / CSV files – source data and initial data inspection.
Data Preparation
The preparation process included:
Reviewing the five datasets and their fields.
Checking and assigning appropriate data types.
Standardising category values and text formatting where necessary.
Reviewing missing values and considering suitable treatment, such as an `Unknown` category where appropriate.
Checking for duplicate records and data-quality issues.
Creating a calendar table for date-based analysis.
Building relationships between the datasets in the Power BI data model.
Data Model
The datasets are connected using shared identifiers:
`Customers[Customer_ID]` → `Accounts[Customer_ID]`
`Customers[Customer_ID]` → `Loans[Customer_ID]`
`Branches[Branch_ID]` → `Accounts[Branch_ID]`
`Accounts[Account_ID]` → `Transactions[Account_ID]`
A calendar table supports time-based analysis of customer registrations, account openings, loan dates, and transaction dates. Date relationships are configured according to the date role being analysed.
Dashboard Pages
1. Banking Performance Overview
An executive summary of the banking data through KPIs and high-level visuals.
Total customers and accounts.
Total account balance.
Total loans and loan amount.
Total transactions.
Transaction activity over time.
Account distribution by account type.
Loan amount by loan status.
Account balance by region.
2. Customer & Account Analysis
Explores customer characteristics and account activity.
Customer distribution by segment and location.
Accounts by type and status.
Average account balance by customer segment.
Customer registrations over time.
Active and dormant account analysis.
3. Loan & Transaction Analysis
Focuses on lending activity and transaction performance.
Loan amount by loan type.
Loan distribution by status.
Loan amounts over time.
Transaction volume by channel.
Transaction status by channel.
Transaction amount by transaction type.
Loan defaults and transaction success rates.
Key Metrics
Total Customers – distinct count of customer IDs.
Total Accounts – distinct count of account IDs.
Total Account Balance – sum of account balances.
Total Loans – distinct count of loan IDs.
Total Loan Amount – sum of recorded loan amounts.
Total Transactions – distinct count of transaction IDs.
Active Accounts – accounts with an Active status.
Dormant Accounts – accounts with a Dormant status.
Default Rate – defaulted loans divided by total loans.
Transaction Success Rate – successful transactions divided by total transactions.
Selected Findings
Metric	Result
Customers	180
Accounts	220
Account balance	Approximately 22.09 million
Loan records	160
Total loan amount	Approximately 37.28 million
Active accounts	152
Dormant accounts	27
Active loans	71
Defaulted loans	12
Loan default rate	7.5%
Transactions	1,200
Successful transactions	1,026
Failed transactions	74
Transaction success rate	85.5%
Note: The source data does not clearly specify the currency for account balances and loan amounts, so the amounts are shown without a currency symbol. The remaining transactions include statuses other than successful and failed; they should not all be treated as failed transactions.
How to Use the Dashboard
Open the Power BI report (`.pbix`) in Power BI Desktop.
If prompted, update the source-file paths to point to the five dataset files.
Refresh the data.
Use the slicers to filter by available dates, regions, cities, customer segments, account types, loan statuses, and transaction channels.
Navigate between the three report pages to explore different areas of banking performance.
Project Limitations and Considerations
The analysis reflects the records and date ranges available in the supplied datasets.
Account balances and loan amounts are shown without a currency label because the source files do not establish the currency.
The default rate is calculated by loan count, not by the value of outstanding loans.
Transaction amounts should not automatically be interpreted as revenue, profit, or net cash flow. Transaction types and statuses must be considered when interpreting totals.
Findings may change when the source data is updated or refreshed.
Recommendations
The dashboard can help stakeholders:
Monitor account activity and identify dormant accounts for further investigation.
Track loan statuses and review defaulted loans.
Monitor transaction success and failure patterns.
Compare account balances across regions.
Explore customer segments and account usage for further analysis.

Conclusion
This project demonstrates the use of Power Query, data modelling, DAX, and Power BI visualisations to transform multiple banking datasets into an interactive analytical report. It brings customer, account, loan, and transaction information together to make key metrics easier to explore and interpret.
