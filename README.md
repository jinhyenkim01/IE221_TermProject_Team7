# IE221 Term Project - Optimal Staff Scheduling via Short-Term Demand Forecasting at Pulbit-Maru

**Using Machine Learning to perform demand forecasting** 

# Code
The code was run on Google Colab Python 3 CPU, 2025.10.

Given a training dataset, the model aims to learn the underlying patterns of each subsequent data point by referring to all previous data points and studying its features.

In doing so, the model learns short-term demand forecasting for the next time period given information about previous demand patterns.

# Model
The code uses Random Forest Regressor Model, chosen for its ability to handle non-linear demand patterns and sudden changes to the data, both of which are useful in studying real-life customer arrival pattern that is often stochastic and sudden.

# Dataset
There are a total of four different groupings for the dataset:
* Dataset A: Customer arrival during Lunchtime, Monday~Thursday
* Dataset B: Customer arrival during Lunchtime, Monday~Thursday
* Dataset C: Customer arrival during Dinnertime, Monday~Thursday
* Dataset D: Customer arrival during Dinnertime, Monday~Thursday

The code treats Monday \~ Thursday and Friday separately to account for the typical school day at KAIST, where the majority of the students have most of their lectures during Monday \~ Thursday.

For each group, the number 1~5 indicates the specific date of interest that the model aims to predict. For instance, a model training under dataset A_1 aims to learn the customer arrival patterns of a specific Monday lunchtime through studying the customer arrival data of Tuesday \~ Thursday lunchtime.

# Contents
### dataset
* data_processed: Contains the raw data used for demand forecasting
* data_test: Contains the raw data used for model testing
* data_train: Contains the raw data used for model training
### plot
* Contains 18 diagrams visualizing the model prediction compared to actual data
### result
* result.xlsx: Contains the summary of model, along with its performance metrics