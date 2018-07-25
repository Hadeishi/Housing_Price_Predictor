# Ames Housing Data and Kaggle Challenge

Problem: Predict the price of a house at sale in Ames, Iowa.

Solution: Use the highly detailed Ames Housing Dataset. Since the Ames Housing Dataset is so detailed, extensive exploratory data analysis conducted and features engineered. Linear regression and other regression models created, train-test split and cross-validated. Hyperparameters gridsearched and optimal solutions made. Models were double-checked using the Kaggle Competition site's test set. Solutions interated upon until best solutions arrived at.

## Dataset:

After signing up for a Kaggle account [here](https://www.kaggle.com/), we signed up for the Ames challenge and downloaded the dataset by going [here](https://www.kaggle.com/t/ef1b2451fd2c4efc9292b5d5821c1c7e)). The data set contained detailed information on 

The Kaggle site supplied us with a "train" dataset with which to create our models. Kaggle's "train" set had the actual values of the homes listed--- our target--- however, their "test" set did not. Our job was to develop a model that would predict these target values without being able to see them. I mention this because in the next section I will describe how we train-test split our train data, which means we split the data that Kaggle is referring to as our "train" dataset into two portions, our train set and our test set, in order to determine how accurate our models are with regard to the ever-present danger of over-fitting. An over-fit model is able to fit the values of the training data extremely well--- so well that it takes the data used to train the model too seriously, fitting outliers and rarely occuring oddities, thus fouling up the predictive value of these models (see below).

## Developing a Model

Looking at the data dictionary, the dataset is extremely well described, far beyond simple square footage and number of bedrooms/bathrooms, a mixture of continuous and categorical variables. As a crude first pass model, we decided to simply drop all non-numeric variables () and fit a linear regression model (see [Intro_to_Kaggle_Project_2.ipynb](https://github.com/Hadeishi/Housing_Price_Predictor/blob/master/notebooks/Project_2_Other_Model_Notebooks/Intro_to_Kaggle%2C_Project_2.ipynb) to give us a baseline upon which to iterate and improve. We also fit several other models, some involving significant feature engineering seeking to account for greater variance in housing price (see [here](https://github.com/Hadeishi/Housing_Price_Predictor/blob/master/notebooks/Project_2_Lasso_Only_Modified/1.%20Exploratory%20Data%20Analysis.ipynb) and others involving Lasso regularization to decrease the number of features and reduce overfitting (see [here](https://github.com/Hadeishi/Housing_Price_Predictor/blob/master/notebooks/Project_2_Lasso_Only_Modified/Project_2%2C_LR%2C_Train_Test_Split%2C_Lasso_to_Regularize%2C_YH%20-%20LA%20-%204.ipynb). Ridge and ElasticNet also tried, but resulted in inferior models (data not shown).

The train dataset has all of the columns we need to generate and refine our models. First we took just the The test dataset has all of these columns except for the target that we are trying to predict. To create our model, we train test split our train data as described above so we had an independent way to validate our models before submitting to Kaggle.

## Submission Checklist

We tested our models by submitting the Kaggle test set of properties along with our predicted prices for these properties at [this site](https://www.kaggle.com/c/dsi-us-4-project-2-regression-challenge). Once we submitted our predictions, we could see our scores [here](https://www.kaggle.com/c/dsi-us-4-project-2-regression-challenge/leaderboard).

The best model I was able to develop so far is located [here](https://github.com/Hadeishi/Housing_Price_Predictor/blob/master/notebooks/Project_2_Other_Model_Notebooks/Project_2%2C_LR%2C_Train_Test_Split%2C_Lasso_to_Regularize.ipynb). It had a public Kaggle sacore of 45819 with a private score of approximately 37000. This was simply using Lasso regularized regression. Future model building ideas include further feature engineering and dimensionality reduction using principal components analysis. I also plan to train test split my train data so that I can evaluate my models and iterate more quickly.