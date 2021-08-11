## Summary
Performed sales forecasting in Python for an Ecuadorian grocery store chain using multi-step time series data.
Leveraged beautiful soup and pandas to accomplish feature engineering by web scraping geographic data.
Utilized bottom-up, univariate aggregation, multivariate aggregation, and static supervised learning techniques.
Implemented Feed Forward Neural Networks, LSTM, GRU and SVM using PyTorch and scikit-learn to predict sales.
Static supervised learning approach gave us the best predictions.

## Problem Statement
Sales forecasting can play a major role in the success of an organization. Accurate sales forecasts allow organizations to make informed decisions while setting organizational goals, hiring, and budgeting among other profit impacting factors. Accurate predictions are essential for brick and mortar grocery stores as an overestimation of demand can lead to overstocked perishable goods and an underestimation of demand can lead to popular items selling out which can lead to a loss of potential revenue and customer dissatisfaction.

An Artificial Neural Network is a collection of connected nodes that are modeled after the neurons in a biological brain. Neural Networks models such as FeedForward Neural Networks with Backpropagation can be used to perform time series forecasting. Recurrent Neural Networks have also been found to be effective in solving problems involving sequential data such as time series forecasting and Natural Language Processing. The vanishing gradient problem can be mitigated by using the Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU) models which are designed to handle long term dependencies in sequential data. 
This repository presents the use of Artificial Neural Networks for time series forecasting. As this is a regression problem, we compare our methods in terms of the prediction performance using Mean Squared Error (MSE) as the evaluation metric.
 
## Dataset
We have used a data set provided by Corporation Favorita which is a large grocery store chain in Ecuador. 
The dataset consists of several files containing information about the products, stores, and the change in sales per product over time. For each product, 
we have information like the family of the items to which it belongs, whether it was being promoted, whether it is perishable, etc. Also, for each store, 
we have the daily total transactions, geographical information, cluster type, etc. 

We will try to build models that can help us to capture the trends. Due to the hierarchical structure of our data, it would be difficult to directly use this data and perform simple time-series based forecasting. 
So, we will aggregate this data and perform feature engineering to make it suitable for feeding it to our models. We plan to do the prediction by treating this problem as a 
time-series based as well as a static supervised learning problem. For both the approach, we will make use of Artificial Neural Networks to forecast the unit sales. 
Additionally, we will also make use of the price of oil for prediction as the Ecuadorian economy is heavily dependent on it. Finally, we will compare different approaches and 
discuss their pros and cons. 

## Different Approaches for Forecasting

* Bottom-up Approach
* Single Model Approach
* Static Supervised Learning Approach
* SVM

## Conclusion
For the bottom-up approach, we found that bidirectional LSTMs using Multivariate data produce the best results in terms of Mean Squared Error. However, it requires greater computational effort to execute. Nevertheless, since the results have improved by an entire order of magnitude, we believe that this is the best model available to us. 

For the single model approach, we found that a simple plain backpropagation model with one hidden layer produces the best results. Overall, the static supervised learning approach produced the best results.

## Future Scope

For further experimentation, we can consider using the top-down approach where we run a model at the highest level of the hierarchy and use inference to deduce the sales at the lower levels. Another possibility is to make longer-term predictions using Encoders and Decoders and Attention Models. Convolutional Neural Networks can also be applied to the data.

Finally, all of the experimentation can be done at the original level of granularity, i.e. at the item and store level.

## Notebooks
Exploratory Data Analysis: CIS731: Exploratory Data Analysis and Data Preparation.ipynb
Bottom-up Approach: Bottom Up.ipynb
Single Model Approach: Multivariate Aggregate.ipynb, Univariate Model.ipynb, Recurrent Neural Networks.ipynb
Support Vector Machines: Support Vector Machines.ipynb
Static Supervised Learning Approach: Data_Aggregation.ipynb, Combine_Embeddings.ipynb, Final_Model.ipynb, Items_Model.ipynb, Stores_Model.ipynb

