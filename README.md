#### <ins> Regression analysis </ins>

#### Having an introduction to regression analysis using the StatsModels library and Scikit-Learn, we decided to create a regression analysis project. This roject was really intuitive because our skills were to be put to test using this housing data.

#### As a good practise for any project, we had to come up up with a detailed but brief business objective to give a synopsis of what we were to do. We came up with three obectives which are:
* Buid a regression model with a good accuracy score as well as an RMSE score closer to 0. This would finally become the metric for choosing the best model for which we were to use.
* Extract insights from the data especially the main factors impacting the prices both positively and negatively.
* Investigate the predictor features/independent features impact on the prices of houses.

#### The task at hand involved analysis of the King County Housing data and extracting meaningfull insights that may impact on the prices of houses. Thereafter we built a model using various models specifically linear models. This involves alot of feature engineering as well as clustering to generate new features that may have a direct correlation with house pricing. A Domain and basic knowledge  was of essence in this project so as to know what new features to generate may have an imapct on the house prices. A brief knowledge about Real Estate came in handy throughout this project. 

#### Before any analysis it is important to understand your data and have a good overview of what each column represents so as to have a smooth landing. It is also good practise to import all the necessary libraries required for any data analysis assignment. Armed with a description file for all the column names, it was a little bit easier to manoevre through the whole project. 

#### <ins> Data Cleaning </ins>
#### Conducting a proper data cleaning is the first step before data analysis. This ensures no wrong insights are extracted from unclean data. Unclean data in most may lead to wrong conclusions. Data cleaning involves either imputing/dropping missing values as well as ensuring the columns are in their correct formart especially datetime columns which were really necessary in engineering new features. It also involves creating new categories for missing data in the categorical variables rather than filling them with te mode or median values. This generally depends on the task at hand and before dropping off any data, we esnured we checked it's missing values percentage. 

#### <ins> Data Analysis </ins>
#### This stage involves creating visualizations with the aim of examining the patterns in data, whether they follow common trends or whether they are scattered or not. The visualization libraries such as Matplotlib and Seaborn were very crucial in this phase. We checked for the distributiion in every ppredictors in relation to the target variable.Most of the data seemed to have wide ranges such as the house price which had the lowest price at 78,000 and a maximum of baout 7,000,000. But such is the nature of Real Estate where very many factors are involved in determing the prices of houses. This stage involved plotting Histograms, scatter plots, distribution plots as well as line plots. This was necessary in ensuring the data being dealt with assumes the Linear regression assumption of normality. Suppose the data doesn't meet the normality assumption, it is always necessary to log transform the data or even scale the data. Log transformations shouls be however done with  caution as this alters the correlations which may have an impact on the model's accuracy score as well as RMSE scores. 

#### <ins> Feature Engineering </ins>
#### This has to be the most important step on any data being prepared for the modelling process. With housing data, domain knowledge tells us that house sales always have a season and there are certain times of the year when house prices boom and there are also other seasons where sales drop significantly. Most house sales and prices are therefore faced with the concept of seasonality. Domain knowledge also dictates the age of any house determines the price at which it will be sold. Mapping and encoding of categorcal variables is also always necessary in this phase because the model works with numeric features and these features are very important in helping us find a good correlation with the price. The new features play an important role in ensuring a good model score.

#### <ins> Data Modelling </ins>
#### Here data is now very ready for the modelling process. It is good practise to split your dta into training and test sets so as to get a good measure of ho the model may perform on unseen data. We used four models naely StatsModels, Scikit-Learn, RandomForest Regressor, XGBoost and LightGBM. Both XGBoost and LightGBM are gradient boosting algorithms and as such they have great speeds in getting the scores on testing data and predicted values. They also have good accuracies with options for tuning to even push the accuracy scores higher. The mian disadvantage with them is that they may easily overfit the data and give  aflase sense of a good model. However, with the help of cross validation, overfitting is greatly minimized as it takes care of the random state of numbers. We also used the ration 8:2 in the splitting of train and test sets. 
#### XGBoost algorithm was the best with an accuracy score of about 86.5 and a normalized RMSE of about 0.0172.

#### <ins> Objectives </ins>
#### To answer our objectives, we used the Partial Dependency Plots so as to have a better understanding of how the model works. These plots give more clear insights than the feature importance plots that come embedded with the gradient boosting models. All our objectives were answered by these plots and even more insights were extractred from these plots. 

#### <ins> Challenges </ins>
#### Some columns which were very importantt had missing values and would have really helped in developing good models. 
#### Most of the data was also skewed and as such conflicted on whether to log transform some or use it as it is.

#### There was alot of learning of the Real Estate Domain from the insights generated. We learned alot from each other especially when we were feature engineering new features. 

