# Online-Retail-Store-Sales-and-Customer-Analysis
The primary objective of this project is to analyze sales and customer behaviour of an online retail store to provide insights that will enable the management team make informed business decisions and enhance marketing strategies.

The data set is a sales transaction data set for a UK-based e-commerce store selling gifts and homewares, covering 2 years (2022 and 2023). Their customers come from the United Kingdom and other Countries.

## Tools

Microsoft Excel (Xlookup, Pivot tables and Charts)  
Link to Microsoft Excel files: [Sales Analysis](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2FChinwesarah%2FOnline-Retail-Store-Sales-Analysis%2Fmain%2FOnline%2520retail%2520store_sales%2520analysis.xlsb&wdOrigin=BROWSELINK) and [Customer Analysis](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2FChinwesarah%2FOnline-Retail-Store-Sales-Analysis%2Fmain%2FOnline%2520retail%2520store_customer%2520analysis.xlsb&wdOrigin=BROWSELINK)

## Data Sources

This data was sourced from [Kaggle](https://www.kaggle.com/datasets/shivan118/big-mart-sales-prediction-datasets)

## Data Cleaning

1. A new column, 'total amount' was included, derived from the product of the columns 'unit price' and 'quantity'.
2. All rows with the country 'EIRE' were replaced with 'Ireland' for better understanding.
3. The column headers and columns were formatted for better allignment and presentation.
4. The' invoice date' column which included a date and time was formatted to include date only as the time was not needed for this purpose.

## Data Analysis

**1. Sales Analysis**

**a. Total sales per Country and a Pareto analysis** to establish the countries accounting for about 90% of total sales.  

**Steps taken to achieve this include:**  

-A pivot table is created with the Invoice date in years as columns and Country as row, the sum of Total amount is dragged to Values.  

-A new column called 'Cummulative %' is added to the pivot table and this is populated by a formula that calculates the running total of percentages and shows the progressive total as you move down the list. This will help us understand how each counry contributes incrementally to the total sum.  

-A second table is extracted from the pivot table showing the countries that make up a cummulative percentage of 90%.  

-This extracted table is then used for the Pareto chart.

   
**b. Sales trend overtime.**  

**Steps taken to achieve this include:**   

-A pivot table is created with the Invoice date as years and months dragged to Rows, Total amount is dragged to Values and changed to Total Sales (GBP).  

-A line chart to show the sales trend over time is created with the pivot table. The chart has  Year (segmented in months) as the x-axis and total sales as the Y-axis.


**2. Customer Analysis**

**a. Exclusive discounts** given to top customers on their next purchase, the percentage of discount given is based on their total purchase amount in 2022 and 2023, the higher the total purchase amount, the higher the discount. This was achieved using Pivot table and XLOOKUP.

**Steps taken to achieve this include:**    

-A pivot table created to list top customers (customers with total purchase amount of at least £5000) with their total purchase amounts.  

-A discount table created beside the pivot table, on the same sheet, containing a list of discount percentages and the corresponding minimum purchase amounts.  

-A third column '% discount on next purchase'is added to the pivot table and XLOOKUP is used to search for the appropriate discount based on the customer's total purchase amount.  

-The XLOOKUP formula is then copied down to populate the '% discount on next purchase' column on the pivot table.  

-The 'blank' row indicates all customers that do not have customer ID, this could be as result of checking out as guests.


**b.Identifying one time customers and their purchase date.**  

**Steps taken to achieve this include:**  

-A pivot table is created with 'customerID' and 'Invoice Date' as rows, then 'Number of Purchases' is dragged to Values.  

-Value filter is set to 'number of purchases equals 1' to filter customers that have made just one purchase.

## Results

1. The Pareto Analysis established that most customers are from the United Kingdom, followed by Netherlands and Ireland. These countires together account for 100% of the sales that make up the top 90% of the total sales. The United Kingdom alone accounts for the vast majority (94%). 

2. The sales trend overall shows that sales seem relatively stable, it fluctuates a little but does not show long-term upward or downward trend. There are occasional sharp increases or decreases, this might be indicative of some specific events like promotions and discount offer.
   
3. 263 registered customers with total purchase amount of £5000 and over were identified and given exclusive discounts. The 'blank' row indicates all customers that do not have customer ID, this could be as result of checking out as guests.

4. 79 one-time customers were identified with their date of purchase.

## Recomendations

1. Target Key Markets: Given that the United Kingdom, Netherlands, and Ireland account for 90% of total sales, marketing efforts can be localised and tailored specifically for different countries to encourage patronage from existing and new customers in these countries.

2. Exclusive Discounts for top Customers: Continue to nurture the relationship with high-value customers by offering  personalized offers and loyalty programs, this will foster and encourage them to make more purchases.

3. Convert One-Time Customers: Using personalized follow-up emails and offering discounts for their next purchase. New products could be highlighted in such emails and products relating to their previous purchase could also be flagged to spark their interest.

4. Encourage guest customers to register: This could be achieved by offering membership exclusive discounts and other offers such as free deliveries and/or returns.
