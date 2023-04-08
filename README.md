customer churn analysis 
The churn rate is an important metric for e-commerce businesses because it can significantly impact their revenue and profitability. High churn rates can indicate issues 
with customer service, product quality, or pricing. To combat churn, e-commerce businesses often implement retention strategies, such as targeted marketing campaigns,loyalty programs, and personalized recommendations, to keep customers engaged and satisfied.

dataset overview:_
The data set belongs to a leading online E-Commerce company. An online retail (E commerce) company 
wants to know the customers who are going to churn, so accordingly they can approach customer to 
offer some promos.

File Structure:_

CustomerID: Unique customer ID

Churn Churn: Flag

Tenure: Tenure of customer in organization

PreferredLoginDevice: Preferred login device of customer

CityTier: City tier

WarehouseToHome: Distance in between warehouse to home of customer

PreferredPaymentMode: Preferred payment method of customer

Gender: Gender of customer

HourSpendOnApp: Number of hours spend on mobile application or website

NumberOfDeviceRegistered: Total number of deceives is registered on particular customer

PreferedOrderCat: Preferred order category of customer in last month

SatisfactionScore: Satisfactory score of customer on service

MaritalStatus: Marital status of customer

NumberOfAddress:Total number of added added on 

particular customer: Complain Any complaint has been raised in last month

OrderAmountHikeFromlastYear: Percentage increases in order from last year

CouponUsed: Total number of coupon has been used in last month

OrderCount: Total number of orders has been places in last month

DaySinceLastOrder: Day Since last order by customer

CashbackAmount: Average cashback in last month


steps:_
this project was performed usong power bi tool, first i performed some data cleaning and validation steps as 
  -removing duplicates 
  -handling outliers
  -filling null values 
  all these steps peformed in power query editor, a great tool to manipulate your data!
then getting this data into the data model and used the suitable visulaizatons, through this step i created measures with DAX language to help me through calculations 
these measures were:
-total number of customers:
#of customers = COUNT('E Commerce Dataset'[CustomerID])

-number of churns:
 number of churns = CALCULATE ( COUNT ( 'E Commerce Dataset'[Churn] ),FILTER ( 'E Commerce Dataset', [Churn] ="1" ))

-churn rate:
churn rate = ('E Commerce Dataset'[number of churns]/'E Commerce Dataset'[#of customers])*100

-maximum number of days since last order:
max days since last order = MAX('E Commerce Dataset'[DaySinceLastOrder])

after finishing the previous steps i started to gnerate the required dashboards:_

#EDA dashboard
![EDA dasboard](https://user-images.githubusercontent.com/92961262/230742882-d3fe3273-0843-404a-a679-9b1c751d9419.PNG)



#days since last order and gender infographics
![days since last order](https://user-images.githubusercontent.com/92961262/230742970-04e1cb5c-a331-4500-a778-66d70a6f0c62.PNG)



#Churn indicators
![new churn indicators](https://user-images.githubusercontent.com/92961262/230743981-af8443ea-c347-49f8-a3cd-6b6257c3772d.PNG)




#Complains 
![image](https://user-images.githubusercontent.com/92961262/230743062-cc5bc831-6929-404c-bf4a-f31598dd3bdf.png)



Explanation:
what does these dashboards tell us?
 
 well, lets start with the first one:_
 -total number of customers = 17k
 -total number of churned customers = 2844
 -total number of not churned customers = 14k
 -the majority of customers are male and married customers.
 -customers prefer logging on with pc more than the mobile phone.
 -debit card is the preferd payment methods for our customers.
 -the most demanding products are laptops and accessory.
 -number of customers by each tenure.
 
 
 
 -
 



  
