# Machine Learning Homework - Exoplanet Exploration

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

# Summary

Four models were built to represent the data using the target value of 3 (CANDIDATE, CONFIRMED, and FALSE POSITIVE). Later an assumption was used to group target into two categories. CANDIDATE and CONFIRMED were grouped together as 0 and FALSE POSITIVE was set to 1.

The Decision Tree feature_importance_ was used to select the features for all models. While this may favor Random Forrest, I verified this by using all 40 features in the Neural Network and Deep Learning with no gain in accuracy but there was an improvement in Loss by approximately 0.06. The same 16 features were used for all 4 models with accuracy ranging between 0.84 to 90. 

Of the 4 models Random Forrest performed slightly better than Neural network. Because of the potential to overfit Random Forrest was not chosen. I did not perform hyperparameter tuning on Random Forest and Neural Network but did evaluate several parameters as discussed in the respective section below.


## Prediction and Further Improvement

The Neural Network model was determined to be the best model even though Random Forest and Deep Learning had similar accuracy results. The model does a very good job predicting False Candidates with an accuracy of almost 99%. The trouble the model has is determining the difference between a CANDIDATE and CONFIRMED and this is understandable since they could be one in the same. That is it is highly likely that some CANDIDATE data will become CONFIRMED planets eventually.

To improve this model, I would investigate hyperparameter tuning both Neural Network and Deep Learning models. Time did not permit the research and evaluation, but the below link is one option:

https://www.tensorflow.org/tutorials/keras/keras_tuner

# Evaluation of 4 Models Using Target of 3


## Neural Network/Deep Learning  (Loss: 0.298, Accuracy: 0.89)

The Neural Network (epochs = 1,000) was about the same as Deep Learning model (epochs = 400) with an accuracy of 0.89. Multiple ‘Dense’ were tried but was finally determined to set at 30, also tried 40 and 50. The Deep Neural Network had 3 layers, unit Density at 30, 30 and 3.

MinMax scaling was better than Scaler. Lower Epochs appeared to perform better in deep learning compared to Neural Network. 


## Random Forrest   (Accuracy 0.90)

This was the model I did the most intensive hyperparameter tuning on and is one of the reasons it is performing the best. Scaling was not done on this model because this is a decision tree model and assumed scaling would not affect the results because each feature is considered separate. 


## Logistic Regression (Accuracy 0.85)

I had some concerns that this was a good model to use because Logistic regression is a binary comparison and I was concerned how this function is being used since we have a target value of three. 


## K Nearest Neighbor  (Accuracy: 0.84)

Of the four models we created, KNN had the lowest accuracy score but not by much. I also found that scaling using Scaler was better than using MinMax. Most likely the score could be increased if we added more features back in. 


# With Target of 2

Assuming CANDIDATE and CONFIRMED are the same, as an experiment they were grouped together as 0 and FALSE POSITIVE was set to 1 in Logistics Regression. I tried this with Logistic Regression and the accuracy was 0.99. This was a big assumption and was not pursued further. 

# The Process

## Preprocess the Data

* Preprocess the dataset prior to fitting the model.
* Perform feature selection and remove unnecessary features.
* Use `MinMaxScaler` or ‘StandardScaler’ to scale the numerical data.
* Separate the data into training and testing data.

## Tune Model Parameters

* `GridSearch` was used to tune model parameters for Logistic and KNN.
* Tune and compare four different classifiers.


## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)


