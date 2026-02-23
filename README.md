# Sales-Data-Analysis using MS Excel
This is a sales data analysis revealing actionable insights into revenue trends, product performance, customer behavior, and sales team efficiency, allowing business to optimize strategies for higher profitability. 

# Calculated Quarter- Over-Quarter (QoQ) Revenue Growth
QoQ growth filters out seasonal noise by comparing a quarter to the the previous quarter. 
Using a Pivot Table 
1.	Added Quarters(Sales_Date), Years (Sales_Date)  to the Columns and Product_Category to the Rows of your Pivot Table.
2.	Right-clicked in the table → Show Values As → % Difference From....
3.	Set Base Field to Quarters(Sales_Date) and Base Item to (previous). This instantly replaced raw numbers with QoQ growth percentages.
Identifying Peak Sales & Seasonality
To find recurring patterns I used the Seasonal Index method to compare a specific period to the annual average. 
•	Step 1: Calculated Period Averages. Used a Pivot Table to group the sales by Quarter across multiple years. Set the Value Field to Average instead of Sum.
•	Step 2: Calculated the Seasonal Index. Divided the average for a specific Quarter by the overall Quarterly average for the entire year.
Key Observations:
Inserted a Line Chart to plot these indices which clearly shows cyclical "peaks" and "troughs" in this business cycle. For example- Qtr1 has been a strong quarter for clothing while Qtr2 has been a weak quarter.

# Identifying Best-Sellers 
•	Ranked by Volume: Used a Pivot Table with Product_Category
in Rows and Sum of Quantity_Sold in Values.
•	Ranked by Revenue: Added Sum of Sales_Amountto the same Pivot Table.
Key Observations:
            The "Winner" Category: Identified “Clothing” item as the “Core” product which is high in both volume and revenue and should never go out of stock.
Calculating Profit Margins:
Total Cost Price = Unit_Cost * Quantity_Sold 
Total Sales Price = Unit_Price * Quantity_Sold
Gross Profit = Total Sales Price - Total Cost Price

•	Using a Pivot Table, calculated Gross Profit Margin (%): = Gross Profit / Total Sales Price
•	Added Quantity_Sold(Sum), Gross Profit Margin (Sum) to the Columns and Product_Category to the Rows of the Pivot Table.
                Strategic Insight:
•	High Volume / Low Margin: “Clothing” is "Loss Leaders." They can be used to get customers in the door, but can’t be over-invested in their storage.
•	Low Volume / High Margin: “Food” is “Specialty" items where every sale is a major win.
Product-Level Demand
Using Pivot Table:
•	Calculated total revenue per product.
•	Sorted by Revenue (Highest to Lowest).
•	Calculated a % of Total Sales Price(Sum) of the total revenue.

# Forecast
This image shows a time-series line graph depicting historical data and future forecasts for a product, specifically identified as Product_ID. The chart is generated using Microsoft Excel's "Forecast Sheet" feature, which utilizes Exponential Smoothing (ETS) to predict future values based on historical trends. 
Chart Breakdown
The graph is divided into two main sections:
•	Historical Data (Blue Line): This represents the actual recorded values for Product_ID from January 1, 2023, to approximately December 27, 2023. The values fluctuate primarily between 1000 and 1100.
•	Forecast (Orange Lines): Starting from January 2024, the chart projects future values:
o	Central Forecast (Thick Orange Line): Shows a relatively flat, stable prediction continuing at roughly 1065.
o	Upper and Lower Confidence Bounds (Thin Orange Lines): These represent the 95% confidence interval, indicating the range where future values are likely to fall. As the forecast period extends toward March 2024, the "cone of uncertainty" widens. 
Key Observations:
•	Identifying the Peak Demand Value:
The Upper Confidence Bound line shows a clear upward trajectory. By the end of the forecast period (26-03-2024), the value reaches approximately 1135. This value (1135) is the "Safety Ceiling" for inventory levels or capacity planning.
•	Planning Strategy: The "cone of uncertainty" widens as we move further into 2024. This indicates that while the average demand is expected to remain stable, the volatility (potential for spikes) increases over time. Hence, increasing the Safety Stock levels starting from January 2024 is required to account for this widening risk.
•	Infrastructure: To ensure the storage or production capacity can handle a sustained 
level of 1100–1135 units, even though the "expected" demand is lower.
