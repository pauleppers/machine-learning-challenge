# Machine Learning Homework - Exoplanet Exploration

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

## Summary

Three models were built to represent the data using the target value of 3 CANDIDATE, CONFIRMED, and FALSE POSITIVE. Later an assumption was used to group target into two categories. CANDIDATE and CONFIRMED were grouped together as 0 and FALSE POSITIVE was set to 1.


with Target of 3
## Logistic Regression (0.8072)

{'C': 10, 'max_iter': 1000, 'penalty': 'l1', 'solver': 'liblinear'}
Best Score: 0.8071687685109046

### Classification Report

            precision    recall  f1-score   support

           0       0.59      0.60      0.60       411
           1       0.67      0.68      0.67       484
           2       0.98      0.97      0.97       853

    accuracy                           0.80      1748
   macro avg       0.75      0.75      0.75      1748
weighted avg       0.80      0.80      0.80      1748



## Logistic Regression with Target of 2

{'C': 0.01, 'max_iter': 1000, 'penalty': 'l1', 'solver': 'liblinear'}
Best Score: 0.9782559180317131

### Classification Report

              precision    recall  f1-score   support

           0       0.97      0.98      0.98       895
           1       0.98      0.97      0.97       853

    accuracy                           0.98      1748
   macro avg       0.98      0.98      0.98      1748
weighted avg       0.98      0.98      0.98      1748

## Random Forrest 



## K Nearest Neighbor  (Best Score: 0.8104)


{'algorithm': 'auto', 'leaf_size': 5, 'n_neighbors': 20, 'weights': 'distance'}
Best Score: 0.8104115879172458
['CANDIDATE' 'CONFIRMED' 'FALSE POSITIVE']
                precision    recall  f1-score   support

     CANDIDATE       0.57      0.62      0.59       411
     CONFIRMED       0.66      0.62      0.64       484
FALSE POSITIVE       0.98      0.97      0.97       853

      accuracy                           0.79      1748
     macro avg       0.74      0.74      0.74      1748
  weighted avg       0.79      0.79      0.79      1748



## Nueral Network  (Loss: 0.3108, Accuracy: 0.8535)




### Preprocess the Data

* Preprocess the dataset prior to fitting the model.
* Perform feature selection and remove unnecessary features.
* Use `MinMaxScaler` to scale the numerical data.
* Separate the data into training and testing data.

### Tune Model Parameters

* Use `GridSearch` to tune model parameters.
* Tune and compare at least two different classifiers.

### Reporting

* Create a README that reports a comparison of each model's performance as well as a summary about your findings and any assumptions you can make based on your model (is your model good enough to predict new exoplanets? Why or why not? What would make your model be better at predicting new exoplanets?).

- - -

## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)

- - -

## Hints and Considerations

* Start by cleaning the data, removing unnecessary columns, and scaling the data.

* Not all variables are significant be sure to remove any insignificant variables.

* Make sure your `sklearn` package is up to date.

* Try a simple model first, and then tune the model using `GridSearch`.

- - -

## Submission

* Create a Jupyter Notebook for each model and host the notebooks on GitHub.

* Create a file for your best model and push to GitHub

* Include a README.md file that summarizes your assumptions and findings.

* Submit the link to your GitHub project to Bootcamp Spot.

* Ensure your repository has regular commits (i.e. 20+ commits) and a thorough README.md file

##### © 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.


