### Project Overview 👨‍💻

- Conducted data analysis for an India-based hardware company's sales data.
- Developed ETL processes using SQL to transform unstructured data, clean it, and design a star schema data model in Tableau.
- Created Tableau dashboards to visualize key insights, including revenue, profit margins, and performance across different regions.

## Technologies Used ⚙️

* [Advance Excel]

* [MySQL]

* [Tableau]

* [Statistics]

## Project Highlights

### Problem Statements
1. Revenue breakdown by cities.
2. Revenue breakdown by years & months.
3. Top 5 customers by revenue & sales quantity.
4. Top 5 products by revenue.
5. Net Profit & Profit Margin by Market.

### Approach
1. **Purpose**: Provide actionable sales insights to support decision-making and automate manual data gathering processes.
2. **Stakeholders**: Sales Director, IT Team, Customer Service, Data & Analytics Team.
3. **End Result**: Automated dashboard for quick access to sales insights.
4. **Success Criteria**: Improved decision-making, 10% cost savings, 20% reduction in manual data gathering.

## Data Analysis Using SQL
Some SQL queries used in this project:

```sql
-- Show all customer records
SELECT * FROM customers;

-- Show total number of customers
SELECT count(*) FROM customers;

-- Show transactions for Chennai market
SELECT * FROM transactions where market_code='Mark001';

-- Show distinct product codes sold in Chennai
SELECT distinct product_code FROM transactions where market_code='Mark001';

-- Show transactions in 2020
SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

-- Show total revenue in 2020
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;
