# Used-Car-Price-Prediction

Dataset: [https://www.kaggle.com/datasets/tunguz/used-car-auction-prices]  
Real case: The dataset contains historical car auction sales prices, scraped from outside internet sources. The dataset was collected in 2015, and will not be updated.

## Summary  

### 1. Background (Fake scenario)  
This is an e-commerce company that specializes in the car marketplace. During the sales period, the company experienced quite extreme instability in sales trends. The main cause is that the prices set by sellers on the platform are not suitable for customers, thus affecting purchasing interest.  

### 2. Objectives
Increase car sales transactions by providing appropriate price recommendations for sellers   

### 3. Business Metrics    
**a.** Click-Through Rate (CTR)  => Click-through rate is **the ratio of clicks** on a specific link (ML model after deployment) to see how this model can help the seller  
**b.** Price To Market => Price adjustments for different markets. Measuring PTM allows sellers to find opportunities to gain maximum profit by **measuring the value** (using model machine learning) of their vehicle.  
**c.** Gross Merchandise Value (GMV)  => GMV is considered an important metric to be able to measure company growth by calculating the growth of total transactions on our platform, as in the problems previously explained.  

### 4. Business Insight  
#### a. MMR as the Target  
Because there is no reliable price reference, we refer to MMR (Manheim Market Report). MMR is the premier indicator of wholesale prices. Pricing calculations are based on over 10 million sales transactions for the previous 13 months with precise pricing unmatched by guidebooks.  
So, in this case, we tried to look at how sales are and divide the car data into 2 categories (based on MMR): Above MMR and Below MMR.  

<img width="583" alt="image" src="https://github.com/Yunanouv/Used-Car-Price-Prediction/assets/146415555/4f734e64-9269-4ea8-85a3-87f9ce552de8">  

According to calculations, more cars are sold below the MMR price than those above the MMR, namely 51.26%. This is quite bad because sellers don't even sell cars above the wholesale prices. 

#### b. The Growth of Transaction Amount and Number of Transactions  
The next step is to look at the company's sales trends both in terms of number of transactions and amount.  

<img width="607" alt="image" src="https://github.com/Yunanouv/Used-Car-Price-Prediction/assets/146415555/059e60eb-f368-4454-af96-cbf4a8d5012d">  

The graph above shows that February 2015 was the peak of transactions with a total of around 160k transactions and transaction amounts of around $2B. In contrast to January-February 2014 and also in April and July 2015 with the least transactions.

#### c. Top Brand  
Now it's time to take a look at the most sold car brands on the platform.   

<img width="402" alt="image" src="https://github.com/Yunanouv/Used-Car-Price-Prediction/assets/146415555/3b8ad888-63e0-4e19-8e9a-664cf42ed6ee">  


Ford is the most popular brand with total revenues of almost $1.4B, indicating that Ford has a strong market. Then there was a significant decline in the second popular car, Chevrolet. Meanwhile, Chevrolet, Nissan, Toyota, etc. show a constant difference or the gap is not too big.







