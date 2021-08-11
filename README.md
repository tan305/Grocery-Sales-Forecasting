## Problem Statement
 
In this paper, we use a data set provided by Corporation Favorita which is a large grocery store chain in Ecuador. 
The dataset consists of several files containing information about the products, stores, and the change in sales per product over time. For each product, 
we have information like the family of the items to which it belongs, whether it was being promoted, whether it is perishable, etc. Also, for each store, 
we have the daily total transactions, geographical information, cluster type, etc.  From the plot of daily total unit sales in Fig 3.1, we can see there is a clear trend. 
Meager sales are recorded on 1st January possibly because stores are closed or very few people came to shop. 
In our paper, we will try to build models that can help us to capture these trends. Due to the hierarchical structure of our data, 
it would be difficult to directly use this data and perform simple time-series based forecasting. 
So, we will aggregate this data and perform feature engineering to make it suitable for feeding it to our models. We plan to do the prediction by treating this problem as a 
time-series based as well as a static supervised learning problem. For both the approach, we will make use of Artificial Neural Networks to forecast the unit sales. 
Additionally, we will also make use of the price of oil for prediction as the Ecuadorian economy is heavily dependent on it. Finally, we will compare different approaches and 
discuss their pros and cons. 
