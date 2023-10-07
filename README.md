# Used-Car-Price-Prediction

Dataset: [https://www.kaggle.com/datasets/tunguz/used-car-auction-prices]  
Real case: The dataset contains historical car auction sales prices, scraped from outside internet sources. The dataset was collected in 2015, and will not be updated.

## Summary  

### 1. Background (Fake scenario)  
This is an e-commerce company that specializes in the car marketplace. During the sales period, the company experienced quite extreme instability in sales trends. The main cause is that the prices set by sellers on the platform are not suitable for customers, thus affecting purchasing interest.  

### 2. Objectives
Increase car sales transactions by providing appropriate price recommendations for sellers   

### 3. Business Metrics    

- Click-Through Rate (CTR)  => Click-through rate is **the ratio of clicks** on a specific link (ML model after deployment) to see how this model can help the seller
- Price To Market => Price adjustments for different markets. Measuring PTM allows sellers to find opportunities to gain maximum profit by **measuring the value** (using model machine learning) of their vehicle.
- Gross Merchandise Value (GMV)  => GMV is considered an important metric to be able to measure company growth by calculating the growth of total transactions on our platform, as in the problems previously explained.  

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



### 5. Modelling  

| Model | MAE | RMSE | R2  |
| --- | --- | --- | --- |
| Linear Regression   | 2436 | 3291 | 0.81 |
| Lasso Regression    | 2436 | 3291 | 0.81 |
| Ridge Regression    | 2436 | 3291 | 0.81 |
| **Random Forest**       | **668** | **1206** | **0.97** |
| Cat Boost           | 925 | 1461 | 0.96 |
| XG Boost            | 1016 | 1589 | 0.95 | 
 

The best model is the **Random Forest** model because it has the highest R2 score and the smallest MAE and RMSE among the other models. 
Cross Validation: 97%, which means the model is best fit.


**New Selling Price Predicted**  

<img width="208" alt="image" src="https://github.com/Yunanouv/Used-Car-Price-Prediction/assets/146415555/d67ddc63-ca8d-41d2-a263-243b4dcf829a">




**Comparison Before-After Modelling**  
With the sample 20% of data (105,562) we can see the comparison of the average selling price before and after modeling to make the business recommendation.  

| Action | Total Transaction | Percentage | Avg.Selling Price|
| --- | --- | --- | --- |
| Original Data - Above MMR   | 50,374 | 48.69 |14,702 |
| Original Data - Below MMR  | 53,076 | 51.31 |12,422 | 
| After Modelling - Above MMR     | 53,466 | 51.68 |12,959 | 
| After Modelling - Below MMR     | 49,984 | 48.32 |13,468 | 


### 6. Conclusion and Business Recommendation  
1. With a sample of 20%, the price prediction made shows that the percentage of prices below MMR is 48.19%, where this figure shows a decrease of around 3% from the initial data, and prices above MMR also have an increase of 3% compared to the initial data.  

2. After modeling, the average price under MMR is 13468. If we compare the average price of cars sold under MMR from the original dataset which is 12422, we can conclude that the car price recommended for sale is $1046 (8.4%) higher, so sellers can get more profits.

3. The same thing goes for the average car above mmr is 12959 compared to the original dataset which is 14702. We recommend the seller to sell the car for $2041 (11.8%) lower so that the price is not too expensive.  

4. We can do Quality Control (QC) for the cars before the seller can sell them on our platform, just like the screening and approval. This business recommendation is important so the quality of car condition and spec can increase customer beliefs.
