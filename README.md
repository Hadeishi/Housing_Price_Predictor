# Ames Housing Data and Kaggle Challenge

Problem: Predict the price of a house at sale in Ames, Iowa.

Solution: Use the highly detailed Ames Housing Dataset. Since the Ames Housing Dataset is so detailed, extensive exploratory data analysis conducted and features engineered. Linear regression and other regression models created, train-test split and cross-validated. Hyperparameters gridsearched and optimal solutions made. Models were double-checked using the Kaggle Competition site's test set. Solutions interated upon until best solutions arrived at.

## Dataset:

After signing up for a Kaggle account [here](https://www.kaggle.com/), we signed up for the Ames challenge and downloaded the dataset by going [here](https://www.kaggle.com/t/ef1b2451fd2c4efc9292b5d5821c1c7e)). The data set contained detailed information on 

The Kaggle site supplied us with a "train" dataset with which to create our models. Kaggle's "train" set had the actual values of the homes listed--- our target--- however, their "test" set did not. Our job was to develop a model that would predict these target values without being able to see them. I mention this because in the next section I will describe how we train-test split our train data, which means we split the data that Kaggle is referring to as our "train" dataset into two portions, our train set and our test set, in order to determine how accurate our models are with regard to the ever-present danger of over-fitting. An over-fit model is able to fit the values of the training data extremely well--- so well that it takes the data used to train the model too seriously, fitting outliers and rarely occuring oddities, thus fouling up the predictive value of these models (see below).

## Developing a Model

Looking at the data dictionary, the dataset is extremely well described. As a crude first pass model, we decided to simply drop all non-numeric variables and fitting a linear regression model (see [Intro_to_Kaggle_Project_2.ipynb](). Before train-test splitting our data, we first constructed an ultra-simplified model by simply dropping all non-numeric 
The train dataset has all of the columns we need to generate and refine our models. First we took just the The test dataset has all of these columns except for the target that we are trying to predict. To create our model, we train test split our train data as describec above. We used the same train-test split for all of our models, Generate your regression model using the training data. We expect that within this process, you'll be making use of:
    - train-test split
    - cross-validation / grid searching for hyperparameters
    - strong exploratory data analysis to question correlation and relationship across predictive variables
    - code that reproducibly and consistently applies feature transformation (such as the preprocessing library)
3. Predict the values for your target column in the test dataset and submit your predictions to Kaggle to see how your model does against unknown data.
    - **Note**: Kaggle expects to see your submissions in a specific format. Check the challenge's page to make sure you are formatting your files correctly!

## Submission Checklist

We expect the following to be submitted by end of day on the due date.

1. Your code for the regression model, including your exploratory data analysis. Add your (well organized!) notebooks to this repository and submit a pull request.
2. At least one successful prediction submission on [DSI-US-4 Regression Challenge](https://www.kaggle.com/c/dsi-us-4-project-2-regression-challenge) --  you should see your name in the "[Leaderboard](https://www.kaggle.com/c/dsi-us-4-project-2-regression-challenge/leaderboard)" tab.
3. Check the Project Feedback + Evaluation section (below) to ensure that you know what will factor into the evaluation of your work.

## Project Feedback + Evaluation

For all projects, students will be evaluated on a simple 4 point scale (0-3 inclusive). Instructors will use this rubric when scoring student performance on each of the core project requirements:

Score | Expectations
----- | ------------
**0** | _Does not meet expectations. Try again._
**1** | _Approaching expectations. Getting there..._
**2** | _Meets expecations. Great job._
**3** | _Surpasses expectations. Brilliant!_

For Project 2 the evaluation categories are as follows:

- **Organization**:	Clearly commented, annotated and sectioned Jupyter notebook or Python script.  Comments and annotations add clarity, explanation and intent to the work.  Notebook is well-structured with title, author and sections. Assumptions are stated and justified.
- **Presentation**: The goal, methodology and results of your work are presented in a clear, concise and thorough manner.  The presentation is appropriate for the specified audience, and includes relevant and enlightening visual aides as appropriate. 
- **Data Structures**: Python data structures including lists, dictionaries and imported structures (e.g. DataFrames), are created and used correctly.  The appropriate data structures are used in context.  Data structures are created and accessed using appropriate mechanisms such as comprehensions, slices, filters and copies.
- **Python Syntax and Control Flow**: Python code is written correctly and follows standard style guidelines and best practices.  There are no runtime errors.  The code is expressive while being reasonably concise.
- **Modeling**: Data is appropriately prepared for modeling.  Model choice matches the context of the data and the analysis.  Model hyperparameters are optimized.  Model evaluation is robust.  Model results are extracted and explained either visually, numerically or narratively.
- **Regression Challenge Submission**: Student has made at least one successful submission to the [DSI-US-4 Regression Challenge](https://www.kaggle.com/c/dsi-us-4-project-2-regression-challenge)

Your final assessment ("grade" if you will) will be calculated based on a [topical rubric](https://docs.google.com/spreadsheets/d/1V6OzSHPXCJEe_sVT7B1vE7sT-jqNMNo-NrmZHtafMXY/edit?usp=sharing). For each category, you will receive a score of 0-3. From the [rubric](https://docs.google.com/spreadsheets/d/1V6OzSHPXCJEe_sVT7B1vE7sT-jqNMNo-NrmZHtafMXY/edit?usp=sharing) you can see descriptions of each score and what is needed to attain those scores.
# Housing_Price_Predictor
# Housing_Price_Predictor
