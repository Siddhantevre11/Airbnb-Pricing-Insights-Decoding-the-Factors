# Airbnb Pricing Insights: Decoding the Factors

[![Seattle](seattle.jpg)](https://mohamedirfansh.github.io/Airbnb-Data-Science-Project/)



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

## Conclusion

![image](https://github.com/user-attachments/assets/89e44393-ce77-4ab0-b3eb-d9a9d8cc8eab)
From all the analysis above, we can say a few things:

Type of room for the listing has a great influence in the price. Most hosts list their entire property. Moreover, entire property lisitings cost the most.

The type of property also influences price. Although the highest price is fetched by boat houses, there are very few of them. The most common properties are houses and apartments since these are the 2 types of properties that most hosts list and they do fetch a high price provided the entire property is listed as mentioned in (1).

The number of bedrooms in the listing also has a general trend with the price of the listing. The more rooms available, the higher the price of the listing.

Finally, there are certain ammenities such as: 'Dryer', 'Washer', 'Kid Friendly', 'Heating', 'Free Parking' etc. that most expensive listings also provide. The ammenities will be further explored in the machine learning parts of the project.

![image](https://github.com/user-attachments/assets/873157c2-f2f2-4fbc-b9db-08453a677a18)
By analyzing the number of listings and prices for each neighborhood, we can get a clearer understanding of which neighbourhoods have a lot of expensive listings. Looking at the analysis done so far, we can see that certain neighbourhoods are indeed more 'expensive' than others. However, some of those neighbourhoods do not have as many listings as other expensive neighbourhoods. Since our problem was to identify factors that make a listing more expensive, we can infer that these neighbourhoods tend to have more expensive listings. However, a more thorough inference would be to identify neighbourhoods that have both a higher number of listings and higher price as lower number of listings would mean fewer available listing for a customer to choose.

As such, neighbourhoods such as 'Belltown', 'West Queen Anne' are neighbourhoods that have a lot of expensive listings.

![image](https://github.com/user-attachments/assets/ad51c6e1-b5b6-43ee-b318-d5fbfba570c7)
From the graphs above, we can conlcude 3 things. First is that **most reviews do not have much negativity. Only a few reviews have a modicum of negativity**. Infact, most of the reviews have no negativity classified in the 0.0 negative sentiment. Second thing we can see is that there are **a lot of reviews with a reasonable amount of positivity**. However, the final thing we can conclude is that **most of the reviews have much neutrality**. **If most of the reviews have a lot of neutrality, we cannot infer much on positivity/negativity of comments with respect to price since the bulk of reviews all fall in the neutral category**. So we can conclude that most reviews are written with a neutral sentiment although there is a very slight tilt to positive sentiments.

![image](https://github.com/user-attachments/assets/7a378d4f-44a4-4f0c-918e-a1cc0c56728c)
From the above correlation matrix, we can clearly see that number of reviews and the price of a listing has a very weak negative correlation. Hence we can conclude that the number of reviews a listing receives does not have much of an impact on the price.
From all the textual data analysis we have done, we can see that the reviews a listing gets and the number of reviews a listing gets does not have much of an impact on the price of a listing. However, having certain keywords like: 'view', 'modern', 'walk' does put your listing in the same bracket as those listings with higher prices.








