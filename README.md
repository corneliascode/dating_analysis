# Analysis of a dataset using Random Forest
### 'Like' or 'intelligence' matter the most?

![Importance Plot](random_forest.PNG?raw=true "Importance Plot")

#### Introduction
- For this project I use speeddating dataset available in the reference section  to analyse what are the most important attributes for this kind of dating, using random forest. At the end of the analysis for the both models I take a look at the feature importance of each variable


#### Installation

- The libraries can be installed using the requirement file with the following code:  
```pip install -r requirements.txt```

#### Usage

- The analysis code can be used with any other dataset (by changing it accordingly) for cleaning and analysing categorical and numerical variables and implement the model.

#### Analysis Details

- First of all I take a look at the data.
- I split all this variables into 2 categories: numerical and categorical and do some cleaning.
- I also include a recode part in which I tranform some values (e.g. reading > 10 into 10) because their interest in these activities can only be measured in the interval [1-10] acoording to the article.
- I drop only one variable beacause it has a lot of NaN
- In the original variables, I replace the NaN values with the median
- I use min max scalling in order to plot all the numerical variables into a single graphic
- I analyse and clean the categorical variables and I use One Hot Encoder to be able to perform the Random Forest model

#### Random Forest

1. I divide the data into what will be used for training the model, the features, and what we want to predict, the label
2. Instantiate model with 100 decision trees and train the model on training data
3. I use the forest's predict method on the test data
4. I compare some of predicted values with the actual values to see how accurate the result are
5. Evaluate performance of algorithm with the Mean Absolute Error, Mean Squared Error and Root Mean Squared Error
6. In the end I create a feature importance plot

#### Results:

- The results indicades that liking is the most important attribute folow by a similar attribute: if the partner is attractive.
Other attributes like intelligence, ambition and even age are not so important according to this analysis

#### Contributing
Third-Party Libraries:

- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- xgboost

#### References
Database: https://www.openml.org/search?type=data&sort=runs&id=40536&status=active  
Article: https://doi.org/10.1162/qjec.2006.121.2.673
