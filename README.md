# Auto-mobile-sales-Insight

### Overview 
This repository contains an in-depth analysis of a car sales dataset using SQL for data manipulation and Power BI for visualization. The project aims to derive insights from the data, identify trends, and provide actionable recommendations for sales strategies.

## Data Sources
The dataset used in this analysis comprises detailed records of car sales over a specified period. Key attributes of the dataset include:
- Date: The date when the sale was made.
- Car_Model: The model of the car sold.
- Company: The manufacturer of the car.
- Price: The sale price of the car.
- Quantity_Sold: The number of cars sold.
- Customer_Gender: Gender of the customer.
- Sales_Region: The geographical region where the sale was made.

## Tools
Dax queries, Excel - Data cleaning.
Power BI - Data transformation and visualization.

## Data Cleaning/Preparation
This data required a lot of data cleaning as the raw data set wasn't workable with out critical modifications and cleaning.
In the initial data preparation phase, we performed the following tasks:
- Data loading and inspection: this involves a quick scroll through the data while marking necessary changes and modifications to be done on excel.
- Data cleaning and formatting: empty column and duplicates were deleted 

## Exploratory Data Analysis(EDA)
- In power bi we used the transform data provision to extract the month from the date using 'MonthName = FORMAT('Table'[DateColumn], "MMMM")', then sorted it by the month number column.
- Most columns were adjusted to remove decimal places, as there were no significant numbers after the decimal point.
- the different data columns were set to the corresponding data types like currency, whole numbers and date.
- Using SQL queries I got the revenue per month
- '''  --SELECT THE TOTAL REVENUE PER MONTH
SELECT MONTH(DATE) AS sale_month,
SUM(price) AS REVENUE_PER_MONTH
FROM Analysis.dbo.CAR_SALES
GROUP BY MONTH(DATE)
ORDER BY REVENUE_PER_MONTH;'''
- And the average price per model using
- '''--THE AVERAGE PRICE PER CAR MODEL
SELECT MODEL, AVG(price) AS AVG_PER_MODEL
FROM Analysis.dbo.CAR_SALES
GROUP BY MODEL'''
- The rest of the queries was shown in the file uploaded.
- 6 different dashboards were created: The general overview of the data, regional overview, different dashboards for the top 3 car dealers and the last one created to select different regions and car dealerships to view the insights.

## Observations 
- At $99,266,059, Dec had the highest Revenue and was 380.85% higher than Febuary, which had the lowest revenue at $20,643,945.External Debt Analysis: At $98,335,333,958.00, 2022 had the highest External debt stocks and was 193.90% higher than 1990, which had the lowest Average of External debt stocks at 33,458,483,418.00.
- ﻿Dec accounted for 14.78% of Sum of Price.﻿Dec accounted for 14.78% of Sum of Price.
- ﻿﻿Across all 10 Model, Sum of Price ranged from $9,097,717 to $14,263,424.
- Progressive car dealership was the best performing dealership with revenue at $37m and 1000 sales.

## Conclusion
Through the comprehensive analysis of the car sales dataset using SQL for data manipulation and Power BI for visualization, we have gained valuable insights into various aspects of the sales process.
- Trends and Patterns: We identified trends in car sales over time, observed seasonal variations, and discerned patterns in sales across different regions and customer demographics.
- Performance Metrics: By evaluating key performance metrics such as total sales revenue, average selling price, and sales quantity, we gained a deeper understanding of the effectiveness of sales strategies and customer preferences.
- Recommendations: Based on the analysis, we recommend targeted marketing efforts tailored to specific customer segments and regions, pricing adjustments to maximize revenue, and inventory management strategies to optimize stock levels.
Overall, this analysis provides actionable insights that can guide decision-making processes to enhance the efficiency and profitability of car sales operations. Continuing to leverage data-driven approaches will be crucial for staying competitive and meeting the evolving needs of the market.
