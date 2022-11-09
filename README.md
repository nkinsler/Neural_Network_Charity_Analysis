# Neural_Network_Charity_Analysis

## Overview of Analysis

Via use of machine learning and neural networks, use the featueres in the dataset to create a binary classifer that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.  This will be accomplished by preprocessing data for a neural network model, compiling, training, and evaluating the model, and optimizing the model.

## Results of Analysis

### Data Preprocessing

- What variable(s) are considered the target for the model?
    The target of the model is the "Is_SUCCESSFUL" variable as it indicates whether the charitiable donation was used effectively or not.
- What variable(s) are considered to be the features of the model?
    The feautres of the model include 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'.
- What variable(s) are neither targets nor features, and should be removed from the input data?
    The EIN and Name variables are not beneficial to the model as it is identification inforamtion and should be removed from the input data.

### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation function were selected for the neural network model and why?
- Were the model able to achieve the target model performance?
    The model was unable to meet the target performance accuracy of 75%.  Additional steps performed did not result in the crossing the 75% accuracy thrsehold.  The accuracy achieved was 72.85%.
- What steps were taken to try to increase model performance?
    First step was to apply the bucketing feature to the ASK_AMT data to condense into 6 unique values based on a rnage of ask amounts.  The accuracy achieve was 72.79%.
    Second step was to add a third layer with 10 neurons.  The accuracy achieve was 72.82%.
    Thirs step was to increase the number of epochs to the training regimen.  The accuracy achieve was 72.77%.

## Summary of Analysis

### Summary of Results

### Recommendation

Recommend using the ________ model and the following reasons:
