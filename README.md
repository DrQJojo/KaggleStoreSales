Kaggle project: Store Sales - Time Series Forecasting.

You can find all the information and dataset here: https://www.kaggle.com/competitions/store-sales-time-series-forecasting

I implemented EDA on the data, built a bunch of untuned catboost models to predict sales for each products family then concatenate them together.

At the very beginning I think this would be a good practice for time series prediction as the title implies, however I found it hard to convert this structured data from long format to wide format, as the wide format table has too many features, so I just treat it as a non-time series task. However, as it's shown in the code, I created 'year', 'month', 'week', 'day' features for the sake of time series, and it worked just fine.

For the sake of precision, I build models for each type of product then store them in a dict. Since most of the features are categorical, I use catboost as the basic model.

Now it got rank 165/781. I believe there are lots to do in the future for this model, as the basic models are almost not tuned because I'm not familiar with catboost:(, and the information of holidays and locations is not fully leveraged.

