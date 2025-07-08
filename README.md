# 🛍️ Churn Analysis Using Customer Segmentation in E-Commerce 

## Problem Statement
In the e-commerce sector, customer churn represents a critical challenge that can significantly impact business sustainability and profitability. Understanding the factors leading to customer churn is essential for developing effective retention strategies. This project aims to analyze an e-commerce dataset to identify patterns and characteristics associated with customer churn, and to develop segmentation models that can help target at-risk customers and optimize marketing efforts.

**Dataset**: Ecommerce Customer Churn Analysis and Prediction [[source]](https://www.kaggle.com/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction)

## Goals 
**Reduce Customer Churn:** by identifing and targeting high-risk customers to improve retention and increase customer lifetime value, leading to enhanced revenue stability.

**Optimize Marketing Spend:** Use segmentation insights to allocate marketing resources more effectively, boosting ROI and driving higher engagement and conversions.


## Libraries Used
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Numerical operations and data manipulation.
- **Matplotlib**: Plotting and visualization.
- **Seaborn**: Statistical data visualization.
- **Scikit-learn**: Machine learning algorithms and preprocessing.



## Dataset Understanding 

| **Attribute** | **Data Type** | **Description** |
| --- | --- | --- |
| CustomerID | Integer | Customer ID |
| Churn | Integer | 1 means customer leave and 0 means customer uses the service |
| Tenure | Float | Tenure of customer in organization |
| PreferredLoginDevice | Object | Preferred login device of customer like laptop or phone |
| CityTier | Integer | City tier(1,2,3) |
| WarehouseToHome | Float | Distance in between warehouse to home of customer |
| PreferredPaymentMode | Object | Preferred payment method of customer |
| Gender | Object | Gender of customer |
| HourSpendOnApp | Float | Number of hours spend on mobile application or website |
| NumberOfDeviceRegistered | Integer | Total number of deceives is registered on particular customer |
| PreferedOrderCat | Object | Preferred order category of customer in last month |
| SatisfactionScore | Integer | Satisfactory score of customer on service |
| MaritalStatus | Object | Marital status of customer |
| NumberOfAddress | Integer | Total number of added added on particular customer |
| Complain | Integer | Any complaint has been raised in last month |
| OrderAmountHikeFromlastYear | Float | Percentage increases in order from last year |
| CouponUsed | Float | Total number of coupon has been used in last month |
| OrderCount | Float | Total number of orders has been places in last month |
| DaySinceLastOrder | Float | Day Since last order by customer |
| CashbackAmount | Float | Average cashback in last month |

<br>

## Project Outline
### 3.1 Data Collection and Preparation
- **Data Collection**: Obtain the e-commerce dataset containing customer attributes, transaction details, and churn status.
- **Data Cleaning**: Handle missing values, outliers, and inconsistencies using appropriate imputation methods.
- **Feature Selection**: Identify relevant features and remove redundant columns.

### 3.2 Exploratory Data Analysis (EDA) and Visualization
- **Descriptive Statistics**: Compute summary statistics for numerical and categorical features.
- **Correlation Analysis**: Use correlation tests to explore relationships between variables.
- **Visualizations**: Create plots to visualize data distributions and relationships (e.g., histograms, count plots).

### 3.3 Customer Segmentation
- **RFM Segmentation**: Segmenting done by Recency, frequency, and monetary value of transactions per customer  
- **K-Means**: Dividing customers into clusters based on their behavioral data.

### 3.4 Business Insights and Recommendations

## EDA Insights
* This dataset has 5630 observations and 20 variables with 15 numerical variables, 5 categorical variables and 2 target variable.
* From the data visualization, it is obtained that the churn ratio has a correlation with tenure, complaints, cashback Amount, & preferred order cat.
* Male customers (10.7%) churn more on e-commerce than female customers (6.2%). The assumption is because male users will churn after finding the item they are looking for.
* Customers who churn more have a Satisfaction Score of 3 (5.1%). However, there are also those who have a customer satisfaction score of 5 but still churn, at 4.7%. This shows that customer satisfaction does not affect customers to churn.
* Customers who file more complaints (9.0%) have a greater potential to churn than those who do not file complaints (7.8%). This is possible because customers who file complaints feel dissatisfied with the existing service.
* Customers who are still single tend to churn by 8.2%. The assumption is that because they are still single, so they don't buy many necessities.
* Customers who churn more choose to buy mobile phones by 9.6%. The assumption is because of the need to buy mobile phones every year. Even so, mobile phone purchases tend to be one-time or one-time purchases so there is no need for a second and third purchase at relatively the same time.
* Customers who churn by 11% tend to log in using a mobile phone rather than a computer. This can be made into a strategy to retain customers by providing discount coupons if they log in using a mobile phone.
* It can be concluded that customers who tend to churn are male, satisfaction score 3, more complaints, more purchases of mobile phones and login using mobile phones.

## Modeling Insights
1. **Best Customers:**
- This segment consists of 176 customers
- Customers can be said to be Best Customers who have made recent transactions, often make transactions, and have the highest total transactions.
- In this segment, the average total transaction for each customer is around \\$231 with an average transaction frequency of 8 times, and an average last purchase time of around 2.6 days.
- Customers in this segment give an average review score of 3.1
- In this segment, customers mostly buy the Fashion category with credit card payment methods.
- The treatments provided are loyalty programs/reward points, new product recommendations, and exclusive product offers. (Cross/Up Selling Strategy)

2. **Loyal:**
- This segment consists of 501 customers
- Customers who make the most frequent transactions.
- In this segment, the average total transaction for each customer is around \\$158 with an average transaction frequency of 5 times, and an average last purchase time of around 4.8 days.
- Customers in this segment gave an average review score of 2.9
- In this segment, customers mostly buy the Laptop & Accessory category with credit card payment method.
- The treatment given is loyalty program/reward point and exclusive goods offer (Cross/Up Selling Strategy).

3. **Big Spender:**
- This segment consists of 712 customers
- Customers who have the highest total transactions.
- In this segment, the average total transaction for each customer is around \\$245 with an average transaction frequency of 3 times, and an average last purchase time of around 3 days.
- Customers in this segment gave an average review score of 3
- In this segment, customers mostly buy the Fashion category with credit card payment method.
- The treatment that can be given is exclusive goods recommendation, partnership/membership offer (B2B), and purchase offer at wholesale price (Cross/Up Selling Strategy)

4. **New:**
- This segment consists of 888 customers
- Customers who have recently made a transaction and have only made one transaction.
- In this segment, the average total transaction for each customer is around \\$138 with an average transaction frequency of 1 time, and an average last purchase time of around 1 day.
- Customers in this segment give an average review score of 3.1
- In this segment, customers mostly buy the Mobile Phone category with the credit card payment method.
- Treatments that can be given are welcome emails to build relationships, loyalty program/reward point offers, and discount vouchers (Cross/Up Selling Strategy)

5. **Promising:**
- This segment consists of 1336 customers
- Customers who have recently made transactions, and their transaction frequency and total are above the average of other customers.
- In this segment, the average total transaction for each customer is around \\$153 with an average transaction frequency of 2 times, and an average last purchase time of around 2 days.
- Customers in this segment give an average review score of 3.1
- In this segment, customers mostly buy the Mobile Phone category with the credit card payment method.
- Treatments that can be given are regular limited offers, discount vouchers and cashback via e-mail (Retention Strategy)

6. **Lost Potential:**
- This segment consists of 1671 customers
- Customers who have not made a transaction for a long time, but the frequency and total transactions are above the average of other customers.
- In this segment, the average total transaction for each customer is around \\$195 with an average transaction frequency of 4 times, and an average last purchase time of around 8.4 days.
- Customers in this segment give an average review score of 3.1
- In this segment, customers mostly buy the Laptop & Accessory category with the credit card payment method.
- Treatments that can be given are regular limited offers, discount vouchers and cashback via e-mail (Retention & Reactivate Strategies)

7. **Lost:**
- This segment consists of 346 customers
- Customers who have not made a transaction for a long time, have only made one transaction, and the total transaction is small.
- In this segment, the average total transaction for each customer is around \\$141 with an average transaction frequency of 1 time, and an average last purchase time of around 6 days.
- Customers in this segment give an average review score of 3.1
- In this segment, customers mostly buy the Laptop & Accessory category with the credit card payment method.
- Treatments that can be given are campaigns via e-mail and asking for feedback. (Reactivation Strategy)


## Business Recommendation
  
| RFM Segment | Strategy | Description |
|-------------|----------|-------------|
| Best        | Loyalty program/reward points, new product recommendations, and exclusive product offers (Cross / Up Selling Strategy) | Customers who have recently made transactions, frequently make transactions, and have the highest total transactions. |
| Loyal       | Loyalty program/reward points and exclusive product offers (Cross / Up Selling Strategy) | Customers who make the most frequent transactions. |
| Big Spender | Exclusive product recommendations, partnership/membership (B2B) offers, and wholesale purchase offers (Cross / Up Selling Strategy) | Customers who have the highest total transactions. |
| New         | Welcome email to build relationships, loyalty program/reward points offers, and discount vouchers (Cross / Up Selling Strategy) | Customers who have recently made transactions and have only made one transaction. |
| Promising   | Regular limited offers, discount vouchers and cashback via e-mail (Retention Strategy) | Customers who have recently made transactions, and whose transaction frequency and total are above the average of other customers. |
| Lost Potential | Regular limited offers, discount vouchers and cashback via e-mail (Retention & Reactivate Strategies) | Customers who have not made a transaction for a long time, but the frequency and total transactions are above the average of other customers. |
| Lost        | Campaign via e-mail and asking for feedback. (Reactivation Strategy) | Customers who have not made a transaction for a long time, have only made one transaction, and the total transaction is small. |
