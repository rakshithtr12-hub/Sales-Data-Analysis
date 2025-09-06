# Sales Data Analysis – SQL Project

## About  
Analyzing sales data to identify high-performing branches and products, analyze the sales patterns of various products, and understand customer behavior. The primary objective is to enhance and optimize sales strategies. The dataset utilized in this project is sourced from the Kaggle Sales Forecasting Competition.

## Purpose of the Project  
The main goal of this project is to gain insights from the sales data, exploring the various factors that influence sales across different branches.

## About the Data  
This project's data was obtained from the Kaggle Sales Forecasting Competition and encompasses sales transactions from three branches situated in **Mandalay**, **Yangon**, and **Naypyitaw**. The data contains **17 columns** and **1000 rows**:

| Column              | Description                                         | Data Type         |
|---------------------|-----------------------------------------------------|-------------------|
| invoice_id          | Invoice of the sales made                           | VARCHAR(30)       |
| branch              | Branch at which sales were made                     | VARCHAR(5)        |
| city                | The location of the branch                          | VARCHAR(30)       |
| customer_type       | The type of the customer                            | VARCHAR(30)       |
| gender              | Gender of the customer making purchase              | VARCHAR(10)       |
| product_line        | Product line of the product sold                    | VARCHAR(100)      |
| unit_price          | The price of each product                           | DECIMAL(10, 2)    |
| quantity            | The amount of the product sold                      | INT               |
| VAT                 | The amount of tax on the purchase                   | FLOAT(6, 4)       |
| total               | The total cost of the purchase                      | DECIMAL(12, 4)    |
| date                | The date on which the purchase was made             | DATETIME          |
| time                | The time at which the purchase was made             | TIME              |
| payment             | The total amount paid                               | DECIMAL(10, 2)    |
| cogs                | Cost Of Goods sold                                  | DECIMAL(10, 2)    |
| gross_margin_pct    | Gross margin percentage                             | FLOAT(11, 9)      |
| gross_income        | Gross Income                                        | DECIMAL(12, 4)    |
| rating              | Rating                                              | FLOAT(2, 1)       |

---

## Analysis List

### Product Analysis
Perform an analysis on the data to gain insights into different product lines, determine the top-performing product lines, and identify areas for improvement in other product lines.

### Sales Analysis
The objective of this analysis is to understand the sales trends of various products. The outcomes of this analysis can assist in evaluating the effectiveness of current sales strategies and identify areas for improvement.

### Customer Analysis
This analysis is focused on identifying various customer segments, understanding purchasing trends, and evaluating the profitability associated with each of these customer segments.

---

## Approach Used

### 1. Data Wrangling

- Examine the data to detect any NULL or missing values.
- Since `NOT NULL` constraints were applied during table creation, there are no null values present in the dataset.

### 2. Feature Engineering

Generate new insights by creating the following columns:

- `time_of_day`: Classify each transaction as Morning, Afternoon, or Evening.
- `day_name`: Extract the day of the week from each transaction.
- `month_name`: Extract the month from each transaction.

These columns help analyze when sales peak during the day, week, or month.

### 3. Exploratory Data Analysis (EDA)

Conducted to address the project's key questions and objectives.

---

## Business Questions to Answer

### Generic Questions

- How many distinct cities are present in the dataset?  
- In which city is each branch situated?

### Product Analysis

- How many distinct product lines are there in the dataset?  
- What is the most common payment method?  
- What is the most selling product line?  
- What is the total revenue by month?  
- Which month recorded the highest Cost of Goods Sold (COGS)?  
- Which product line generated the highest revenue?  
- Which city has the highest revenue?  
- Which product line incurred the highest VAT?  
- Retrieve each product line and add a column `product_category`, indicating 'Good' or 'Bad,' based on whether its sales are above the average.  
- Which branch sold more products than the average product sold?  
- What is the most common product line by gender?  
- What is the average rating of each product line?

### Sales Analysis

- Number of sales made in each time of the day per weekday  
- Identify the customer type that generates the highest revenue  
- Which city has the largest tax percent/VAT (Value Added Tax)?  
- Which customer type pays the most VAT?

### Customer Analysis

- How many unique customer types does the data have?  
- How many unique payment methods does the data have?  
- Which is the most common customer type?  
- Which customer type buys the most?  
- What is the gender of most of the customers?  
- What is the gender distribution per branch?  
- Which time of the day do customers give most ratings?  
- Which time of the day do customers give most ratings per branch?  
- Which day of the week has the best average ratings?  
- Which day of the week has the best average ratings per branch?

---

