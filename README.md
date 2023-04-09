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




+after finishing the previous steps i started to gnerate the required dashboards:_



#EDA dashboard


![EDA dashboard new](https://user-images.githubusercontent.com/92961262/230744992-58412ecb-4670-4056-bcfd-64f02ddb858d.PNG)


**Explanation:**


#what does these dashboards tell us?

 
 ##well, lets start with the first one:_
 
 
 -total number of customers = 17k
 
 
 -total number of churned customers = 2844
 
 
 -total number of not churned customers = 14k
 
 
 -the majority of customers are male and married customers.
 
 
 -customers prefer logging on with pc more than the mobile phone.
 
 
 -debit card is the preferd payment methods for our customers.
 
 
 -the most demanding products are phones.
 
 
 -number of customers by each tenure.
 
 #Recommendations based on the information above:_
 
 
 +as we have the majority of our customers from male customers, we have to provide more male related products on our online store to keep the current male customers and attract more customers.
 
 
 +as the prefered login device is phones not PCs we have to make sure that the user experience with PCs not that bad and modify it if needed.
 
 
 +facilitate other payment methods.
 

 
 #days since last order and gender infographics
 
 
![days since last order](https://user-images.githubusercontent.com/92961262/230742970-04e1cb5c-a331-4500-a778-66d70a6f0c62.PNG)
 
 
 -the maximum days since last order = 46 days.
 
 
 -total number of males and females.
 
 
 -prefered items for both genders.
 
 
 -prefed payment methods for both genders.
 
 
 -number of customers and the days since last order they placed.
 
 
 -total number of orders for both genders and as mentioned above that we have more male customers than females, but the female customers we have are placing orders close to the number of male orders.
 
 
 -prefered login device for both genders.
 
 
 
 
#Churn indicators


![new churn indicators](https://user-images.githubusercontent.com/92961262/230743981-af8443ea-c347-49f8-a3cd-6b6257c3772d.PNG)

**Explanation**
 
 -total number of customers by city tier.
 
 
 -total number of churned and non churned customers.
 
 
 -average tenure for all customers.
 
 
 -churn rate.
 
 
 -number of customers by satisfaction score, satisfaction score if very important metric to track it is an indicator for the customers tending to churn.
 
 
 -churn rate by number of addresses, we can notice that more number of addresses the more the customer tend to churn hence this is also a very important metric to track.
 
 
 
 
 #Complains 
 
 
![image](https://user-images.githubusercontent.com/92961262/230743062-cc5bc831-6929-404c-bf4a-f31598dd3bdf.png)
 
 
 **Explanation**
 
 -total number of complains
 
 
 -number of customers by each order hike
 
 
 -number of customers by the number of times of using coupons
 
 
 -number of complains for each warehouse to home distance
 
 
 
 
 
 
 


 
 
 
 
 
 
 
 -
 
 
 
 
 
 
 



  
