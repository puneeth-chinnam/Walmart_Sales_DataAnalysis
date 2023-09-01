# Walmart_Sales_DataAnalysis

This project analyzes Walmart sales data to gain insights into the company's highest-performing stores and products, sales trends across different product categories, and customer purchasing behavior. The goal is identifying opportunities to enhance and optimize Walmart's sales strategies. The raw data was sourced from a Kaggle competition focused on forecasting Walmart sales. By studying historical sales patterns across Walmart's branches, products, and customer segments, this project aims to uncover actionable ways the retail giant can boost revenues in the future.


**Purposes Of The Project**
The major aim of the project is to gain insight into the sales data of Walmart to understand the different factors that affect sales of the different branches.

**About Data**
The dataset was obtained from the Kaggle Walmart Sales Forecasting Competition. This dataset contains sales transactions from three different branches of Walmart, located in Mandalay, Yangon, and Naypyitaw. The data contains 17 columns and 1000 rows:
https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting

**Column	Description	Data Type**
| Column | Description | Data Type |
|-|-|-|  
| invoice_id | Invoice of sales made | VARCHAR(30) |
| branch | Branch at which sales were made | VARCHAR(5) |
| city | The location of the branch | VARCHAR(30) |
| customer_type | The type of the customer | VARCHAR(30) |
| gender | Gender of the customer making purchase | VARCHAR(10) |
| product_line | Product line of the product solf | VARCHAR(100) |
| unit_price | The price of each product | DECIMAL(10, 2) |
| quantity | The amount of the product sold | INT |
| VAT | The amount of tax on the purchase | DECIMAL(6, 4) |
| total | The total cost of the purchase | DECIMAL(10, 2) |
| date | The date on which the purchase was made | DATE |
| time | The time at which the purchase was made | TIMESTAMP | 
| payment_method | The total amount paid | DECIMAL(10, 2) |
| cogs | Cost Of Goods sold | DECIMAL(10, 2) |
| gross_margin_percentage | Gross margin percentage | DECIMAL(11, 9) |
| gross_income | Gross Income | DECIMAL(10, 2) |
| rating | Rating | DECIMAL(2, 1) |

# Analysis List

**Product Analysis**
This project will analyze Walmart's product data to identify top-selling items, underperforming product lines, and opportunities to optimize the company's merchandise mix. The goal is to understand which products drive the most sales and profits for Walmart so they can double down on winning categories while reevaluating slower-moving items.

**Sales Analysis**
By examining historical sales data across products, stores, seasons, and customer demographics, this analysis aims to uncover sales trends and patterns. The findings will be used to measure the effectiveness of current sales strategies and determine where changes may be needed to improve revenues. Sales analysis provides actionable insights to boost performance.

**Customer Analysis**
This portion of the project will focus on segmenting Walmart shoppers based on their purchase behaviors over time. The goal is to identify the most valuable customer groups, trends, and profitability levels. These customer insights can inform marketing and merchandising decisions to optimize satisfaction and loyalty across segments.

---Approach Used

**Data Wrangling:** This is the first step where data inspection is done to ensure NULL values and missing values are detected and data replacement methods are used to replace missing or NULL values.

Build a database

A table is created, and the data is inserted.

Columns with null values are selected. There are no null values in our database as in creating the tables, we set NOT NULL for each field; hence null values are filtered out.

**Feature Engineering:** This will help us generate some new columns from existing ones.

A new column named time_of_day is added to give insight into Morning, Afternoon, and Evening sales. This will help answer the question of when most sales are made during the day.

A new column named day_name is added that contains the extracted days of the week on which the given transaction took place (Mon, Tue, Wed, Thur, Fri). This will help answer the question of which day of the week each branch is busiest.

A new column named month_name is added, containing the extracted months of the year on which the given transaction took place (Jan, Feb, Mar). This could help figure out which month of the year has the most sales and profit.

**Exploratory Data Analysis (EDA):** Exploratory data analysis is done to answer this project's listed questions and aims.

Conclusion:

Business Questions To Answer


What was the top-selling product?

***

Which branch made the most sales? 

***

What days of the week had the highest sales?

***

What times of day were busiest for sales? 

***

What months had the highest sales and profits?

***

Which customer type spent the most?

***

What payment types were most common?

***

How did ratings impact sales amounts?

***

What product categories were most profitable?

*** 

How did costs and margins vary by product type?

***

What customer demographics made the most purchases?

***

How can Walmart optimize its sales and marketing strategies based on these insights?


**Revenue And Profit Calculations**

$ COGS = unitsPrice * quantity $

$ VAT = 5% * COGS $

 is added to the 
 and this is what is billed to the customer.

$ total(gross_sales) = VAT + COGS $

$ grossProfit(grossIncome) = total(gross_sales) - COGS $

Gross Margin is gross profit expressed in percentage of the total(gross profit/revenue)

$ \text{Gross Margin} = \frac{\text{gross income}}{\text{total revenue}} $

**Example with the first row in our DB:**

Data given:

$ \text{Unite Price} = 45.79 $
$ \text{Quantity} = 7 $
$ COGS = 45.79 * 7 = 320.53 $

$ \text{VAT} = 5% * COGS\= 5% 320.53 = 16.0265 $

$ total = VAT + COGS\= 16.0265 + 320.53 = 

$ \text{Gross Margin Percentage} = \frac{\text{gross income}}{\text{total revenue}}\=\frac{16.0265}{336.5565} = 0.047619\\approx 4.7619% $

