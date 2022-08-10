# Bondora-loan-prediction


## Introduction

Bondora offers different ways for investors to invest. The easiest way is to use Bondora's own 
built-in service or just set up your portfolio based on risk levels. For some investors these 
methods are great as they require minimal user input. However the downside is that the investor 
has no control over the loans that they receive. The solution would be to use Bondora's API as 
it provides investors full control over the loans they can purchase on the primary and secondary 
market. In order to know which loans are worth to invest in we first need to obtain the data, 
process it and train machine-learning models that are capable of predicting loan outcomes.

To clarify, the scope of this project isn't to create an application that uses Bondora's 
API to automatically buy loans. Instead we will work with Bondora's publicly available dataset and create a 
model that is capable of accurately predicting loan outcomes and the model can later be used in 
such applications. 

In conclusion the goal is to create an interesting and a descriptive project that is 
also useful in a real-world scenario.

## Project description

The project consists of three main steps:
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

With a sample size of almost 30000 loans, an average annual ROI of over 10% can be constantly
reached. When further optimizing the investing strategy by only investing into loans which have at least 20% interest, then a maximum annual ROI of 15% was achieved.
The models are validated on a validation set which doesn't consist 
of any loans that are used in the training set.

Below is a table with the top 5 results which are also included in the worksheet. The threshold varies because the table contains different models. 
More extensive coverage of the results can be found in the worksheet.

| Threshold | Total number of loans | Investments made <br/>(% of total number) | Precision | Average annual ROI |
|-----------|-----------------------|-------------------------------------------|-----------|--------------------|
| 0.850	    | 29178                 | 1.049%                                    | 0.781	    | 15.002%            |
| 0.625     | 29178                 | 1.069%                                    | 0.744	    | 14.783%            |
| 0.825     | 29178                 | 1.494%                                    | 0.727	    | 14.177%            |
| 0.800     | 29178                 | 2.032%                                    | 0.710	    | 14.039%            |
| 0.525     | 29178                 | 1.265%                                    | 0.762	    | 13.945%            |


## Project status

I'm not currently planning to working on this project anymore, but here are a few ideas that might be worth looking into.

1. Experiment with feature engineering.
2. Create a more sophisticated strategy, e.g. invest higher amounts into loans with higher thresholds and less into loans with lower thresholds.
3. Try to find more optimal hyperparameters and/or use other hyperparameter optimization algorithms.