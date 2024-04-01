# Airbnb Pricing Insights: Decoding the Factors

[![Seattle](seattle.jpg)](https://mohamedirfansh.github.io/Airbnb-Data-Science-Project/)

*Here is a quick overview of the project. The full analysis and findings can be viewed [here](https://mohamedirfansh.github.io/Airbnb-Data-Science-Project/).*

## 📖 Overview
### What are the factors and features of a listing that make an Airbnb listing in Seattle more expensive?  
  
That is the question this project aims to answer. We started of by collecting data of listings in Seattle from [Kaggle](https://www.kaggle.com/airbnb/seattle). Then, we cleaned the data to a useful format for data analysis. We then did Exploratory Analysis on the data by focusing on 3 sub-problems:

1. What are the features/facilities/ammenities of a property that affect its price?
2. Are there particular locations in Seattle where Airbnb listings fetch higher prices?
3. Does textual data in the summary and sentiments of reviews affect price?

Afterwards, we did Machine Learning on the data by adopting 6 different **Regression** models for our regression problem. They were:

1. Linear Regression
2. Random Forrest Regression
3. XGBoost
4. CatBoost
5. Ridge Regression
6. Lasso Regression

We partitioned the data into train and test sets and evaluated the models on their prediction accuracy. Once we found the most accurate prediction model, we used that model in a library called **TreeInterpreter** which decomposed the prediction into a sum of contributions from each feature: `Prediction = Bias + Feature1 x Contribution1 + … + FeatureN x ContributionN`. We used this to find the most important features that affected the price of a listing.




