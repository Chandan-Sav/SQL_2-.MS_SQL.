# Pizza Sales Data Analysis

## About

This project aims to explore the Pizza Sales data to understand top performing branches and products, sales trend of of different products, customer behaviour. The aims is to study how sales strategies can be improved and optimized. The dataset was obtained from the [Pizza Sales Dataset](https://www.kaggle.com/datasets/chandansav/pizza-sales).

"In this recruiting competition, job-seekers are provided with historical sales data for 45 Walmart stores located in different regions. Each store contains many departments, and participants must project the sales for each department in each store. To add to the challenge, selected holiday markdown events are included in the dataset. These markdowns are known to affect sales, but it is challenging to predict which departments are affected and the extent of the impact." [source](https://www.kaggle.com/datasets/chandansav/pizza-sales)

## Purposes Of The Project

The major aim of thie project is to gain insight into the sales data of Pizza Store to understand the different factors that affect sales of the different branches.

## About Data

The dataset was obtained from the [Pizza Sales](https://www.kaggle.com/datasets/chandansav/pizza-sales). This dataset contains sales transactions from a three different categories of Pizza's, respectively. The data contains 12 columns and 21K+ rows:

| Column                  | Description                             | Data Type      |
| :---------------------- | :-------------------------------------- | :------------- |
| order_id              | Order of the pizza made               | VARCHAR(30)    |
| pizza_name                 | Name of a Pizza         | VARCHAR(50)     |
| quantity                   | total quantity of the pizza made per order          | VARCHAR(5)    |
| order_date          | Date on which pizza were ordered               | DATETIME    |
| order_time                  | Time when which pizza were ordered   |TIME   |
| unit_price           | The price of each product       | DECIMAL(10, 2)   |
| total_price            | The price of each product               | DECIMAL(10, 2) |
| pizza_size               | The amount of the product sold          | VARCHAR(5)           |
| pizza_category                 | The amount of tax on the purchase       | VARCHAR(20)    |
| pizza_ingredients                  | All ingredients through which pizza was made          | VARCHAR(150) |
| pizza_name                   |Name of a Pizza | DATE           |


### Analysis List

1. Product Analysis

> Conduct analysis on the data to understand the different pizza_category, the pizza_category performing best and the pizza_category that need to be improved.

2. Sales Analysis

> This analysis aims to answer the question of the sales trends of pizzas . The result of this can help use measure the effectiveness of each sales strategy the business applies and what modificatoins are needed to gain more sales.

3. Customer Analysis

> This analysis aims to uncover the different customers segments, order id and the profitability of each customer segment.

## Approach Used

1. **Data Wrangling:** This is the first step where inspection of data is done to make sure **NULL** values and missing values are detected and data replacement methods are used to replace, missing or **NULL** values.

> 1. Build a database
> 2. Create table and insert the data.
> 3. Select columns with null values in them. There are no null values in our database as in creating the tables, we set **NOT NULL** for each field, hence null values are filtered out.



2. **Exploratory Data Analysis (EDA):** Exploratory data analysis is done to answer the listed questions and aims of this project.

3. **Conclusion:**

## Business Questions To Answer

### KPI's

1. Total Revenue ?
2. Average Order ?
3. Total Pizza's Sold ?
4. Overall Total Order ?
5. Average Pizza per Order ?


### Product

1. What is the Daily Total Order?
2. What is the Monthy Total Order?
6. Top 5 Pizzas by Revenuee?
5. Bottom 5 Pizzas by Revenue?
6. Top 5 Pizzas by Quantity?
7. Bottom 5 Pizzas by Quantity?
8. Top 5 Pizzas by Total Orders?
9. Bottom 5 Pizzas by Total Orders?
12. What is the average rating of each product line?

### Sales

1. What is the % Sale by pizza_category?
2. What is the % Sale by pizza_size?
3. What were total sales by pizza_category?




## Code

For the rest of the code, check the [SQL_queries.sql](https://github.com/Chandan-Sav/SQL_2-.MS_SQL./blob/main/pizza%20sales.sql) file

```sql
-- Create database
CREATE DATABASE IF NOT EXISTS pizza db;

-- Create table
CREATE TABLE IF NOT EXISTS pizza_sales(
	order_id VARCHAR(30) NOT NULL PRIMARY KEY,
    pizza_name VARCHAR(50) NOT NULL,
    quantity VARCHAR(5) NOT NULL,
    order_date DATETIME NOT NULL,
    order_time TIME NOT NULL,
    unit_price DECIMAL(10,2) NOT NULL,
    total_price DECIMAL(10,2) NOT NULL,
    pizza_size VARCHAR(5) NOT NULL,
    pizza_category VARCHAR(20) NOT NULL,
    pizza_ingredients VARCHAR(150) NOT NULL,
    pizza_name VARCHAR(15) NOT NULL,
   
);
```
