# Market-Basket-Analysis

Market basket analysis to analyse the purchase behaviour of individual customers to estimate with relative certainty, what items are more likely to be purchased individually or in combination with some other products.

Data Exploration and Cleaning :
- Imported all the required libraries into python
- Imported the 5 dataset into python : Customers, Orders, Order_Items, Payments, Products
- Looked for any null values in the dataframes and treated them
- Looked for Outliers in the dataset
- Dropped the columns which are not required for the analysis
- Merged the dataframes into a final dataframe with correct foreign key
- Filtered the data only with orders which have order status as delivered\


Data Visualization :
Visualized the data in tableau and identified the top product categories with highest orders and highest revenue

Market Basket Analysis :
Identified the product categories which are ordered more than 5 times and performed market basket analysis on the dataset in python to figure out which categories are most frequently ordered together


<img width="884" alt="image" src="https://github.com/Shrestha097/Market-Basket-Analysis/assets/78401805/1e6176a5-b952-4af2-abfc-c232619d1af9">

- Top 10 product categories are responsible for 90% of the revenue.
- “Toys” product category have the highest revenue as compared to all other product categories

<img width="556" alt="image" src="https://github.com/Shrestha097/Market-Basket-Analysis/assets/78401805/ba2d12f6-d2a9-4065-aa2c-05d282b48bf3">

- 79% payments were done using credit card and 18% by wallet

<img width="892" alt="image" src="https://github.com/Shrestha097/Market-Basket-Analysis/assets/78401805/53b7ac2d-3e84-4b7f-b786-541cd1366121">

- The number of orders and revenue generated have been increasing till 2018 but there is a dip in 2018 Q3 quarter

<img width="818" alt="image" src="https://github.com/Shrestha097/Market-Basket-Analysis/assets/78401805/8c84ee38-929d-4db4-8a19-bc562975d271">

- For Market Basket Analysis, dataframe was created by grouping order id and product category and taking the count of products. This gave the list of orders and numbers of products for that particular order for each and every product category.
- Since for the analysis, the number of orders is not needed but it is more important to know if a customer has ordered that particular product category or not. To know this, the output is encoded so that if any particular category is ordered in as order then it is 1 otherwise 0.
- Then, Apriori algorithm is applied to the data so that item sets are formed for different product categories and support is calculated for each product category.
- Using association rule of Apriori algorithm, the association between different product categories is measured.
- The dataframe with associations are filtered as lift >= 0.04 and confidence >= 0.05.
- After performing the market basket analysis, the top 10 associations formed which are ordered more are as given

