# Financial-Sales-Insights-using-Tableau

**India based Hardware company(Atliq) Sales Insights - A Financial and Data Analysis Project performed on Tableau & SQL** 

### About Project 

- Performed India based company(Atliq) sales insights and financial analysis.

- Developed ETL mappings using SQL to extract the data and transform it to conduct data cleaning and designed star schema data model on Tableau.

- Created a Tableau dashboard that automatically analyzes data and generates visualizations to reveal insights about the factors impacting the company's performance over time. This information is used to identify areas for improvement and suggest business solutions.

## India based Hardware company(Atliq) Sales Insights - A Financial and Data Analysis Project performed on Tableau & SQL
  
### [Tableau Dashboard Link](https://public.tableau.com/app/profile/kshitij.kaithal/viz/Sales_Analytics_Project/Dashboard?publish=yes)

### Problem Statements
Sales director wants to know the performance of the company in various Indian states & accordingly provide some discount

- Q1. Revenue breakdown by cities.

- Q2. Revenue brekdown by years & months.

- Q3. Top 5 customers by revenue & sales quantity.

- Q4. Top 5 Products by revenue.

### Approach - Project Planning & [Aims Grid](https://www.youtube.com/watch?v=6118I9HViuQ)
  
#### 1. Purpose: What? Why? What do we want to achieve?
To reveal sales insights that are not visible before the sales team for decision support & automate them to reduced manual time spent in data gathering and cleaning

#### 2. Stake Holders: Who will be involved?
- Sales Director, 
- I.T. Team, 
- Customer Service Team, 
- Data & Analytics Team.

#### 3. End Result: What do we want to achieve?
To develop a dashboard that automatically updates with the latest sales data, providing real-time insights to support data-driven decision making

#### 4. Success Criteria: What will be our success criteria?
- Automated Dashboards uncovering sales and financial insights with latest data available
- Sales team will be able to take better decision and thus prove that 10% cost savings happened

### Data Analysis - Approach
<p  align="center"><a href="https://github.com/kshitijk20"><img width="80%" src="https://github.com/kshitijk20/Financial-Sales-Insights-using-Tableau/blob/main/Images/workflow.jpg" /></a></p>
  
## Data Analysis Using SQL
  
1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai.

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars.

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table.

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";`


## Data Analysis Using Tableau 
  
### Tableau Public Dashboards: [Revenue & Finance Analysis](https://public.tableau.com/views/Sales_Analytics_Project/Dashboard?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)

#### Tableau Dashboard - [Revenue Analysis](https://public.tableau.com/views/Sales_Analytics_Project/Dashboard?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)
	
<p  align="center"><a href="https://public.tableau.com/views/Sales_Analytics_Project/Dashboard?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"><img width="100%" src="https://github.com/kshitijk20/Financial-Sales-Insights-using-Tableau/blob/main/Images/dashboard.png" /></a></p>
