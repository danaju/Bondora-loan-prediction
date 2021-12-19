# Bondora-loan-prediction


## Introduction

Bondora offers different ways for investors to invest. The easiest way is to use Bondora's own 
built-in service or just set up your portfolio based on risk levels. For some investors these 
methods are great as they require minimal user input. However the downside is that the investor 
has no control over the loans that they receive. The solution would be to use Bondora's API as 
it provides investors full control over the loans they can purchase on the primary and secondary 
market. In order to know which loans are worth to invest in we first need to obtain the data, 
process it and train machine-learning models that are capable of predicting loan outcomes.

To clarify, the scope of this project is not to create an application that uses Bondora's 
API to automatically buy loans. Instead we will work with Bondora's publicly available dataset and create a 
model that is capable of accurately predicting loan outcomes and the model can later be used in 
such applications. 

In conclusion the goal is to create an interesting and a descriptive project that is 
also useful in a real-world scenario.

## Project description

The project consists of three worksheets:
1. Data preprocessing
2. Modeling
3. Validation

In the preprocessing step the data is downloaded, cleaned and filtered. A custom target variable
is created to distinguish the preferred loans from the non-preferred loans.

The modeling step is about training different machine learning models 
and finding suitable hyperparameters.

The last step is validation, where we evaluate the models' performance on unseen data and 
calculate different statistics at different classification thresholds in order to 
decide the best model.

## Results

With a sample size of over 30000 loans, an average annual ROI of at least 11% can be constantly
reached. The models are validated on a validation set which does not consist 
of any loans that are used in the training set.

Below is a table with top 5 results for the xgboost model with the roc_auc scoring function:

| Threshold | Total number of loans | Investments made <br/>(% of total number) | Precision | Average annual ROI |
|-----------|-----------------------|-------------------------------------------|-----------|--------------------|
| 0.800     | 31206                 | 0.949%                                    | 0.882     | 11.699%            |
| 0.750     | 31206                 | 1.779%                                    | 0.843     | 11.650%            |
| 0.775     | 31206                 | 1.311%                                    | 0.863     | 11.498%            |
| 0.725     | 31206                 | 2.317%                                    | 0.833     | 11.452%            |
| 0.700     | 31206                 | 2.961%                                    | 0.828     | 11.262%            |

The more extensive coverage of the results can be found in the "3-validation.ipynb" worksheet.

## Project status

The project is mostly complete and the models can be used for predicting loan outcomes.
I am still planning to tidy up some code and might even add some things from the list below:

1. Experiment with feature engineering.
2. Create a more sophisticated strategy, e.g. invest more into loans with higher thresholds and less into loans with lower thresholds.
3. Include loans from other countries besides EE.