# Neural_Network_Charity_Analysis

## Overview of Analysis

Via use of machine learning and neural networks, use the features in the dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.  This will be accomplished by preprocessing data for a neural network model, compiling, training, and evaluating the model, and optimizing the model.

## Results of Analysis

[AlphabetSoupCharity.ipynb](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb)

[AlphabetSoupCharity.h5](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.h5)

[AlphabetSoupCharity_Optimization.ipynb](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity-Optimization.ipynb)

[AlphabetSoupCharity_Optimization.h5](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimization.h5)

### Data Preprocessing

- What variable(s) are considered the target for the model?

    The target of the model is the "IS_SUCCESSFUL" variable as it indicates whether the charitable donation was used effectively or not.
    
- What variable(s) are considered to be the features of the model?

    The features of the model include 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'.
    
- What variable(s) are neither targets nor features, and should be removed from the input data?

    The EIN and Name variables are not beneficial to the model as it is identification information and should be removed from the input data.  In the additional tests ORGANIZATION was removed.

### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation function were selected for the neural network model and why?

    80/30 neurons were originally used and later modified to 100/50/10 in order expand the ability of each layer to transform the data.  2 layers were originally used and later increased to three in order to enhance the model to potentially capture more complex input-output relationships.  The output activation selected was sigmoid given the outcome we were looking for was to predict the probability of a outcome.  The hidden layers used relu for activation for all layers until test where the third layer was changed to tahn.  Relu was selected to have negative variables set to zero to avoid those variables impacting the outcome and changed to tahn for the final test in case any negative variables should be considered.
    
- Were the model able to achieve the target model performance?

    The model was unable to meet the target performance accuracy of 75%.  Additional steps performed did not result in the crossing the 75% accuracy threshold.  The accuracy achieved was 72.8%.
    
- What steps were taken to try to increase model performance?

    First step was to apply the bucketing feature to the ASK_AMT data to condense into 6 unique values based on a range of ask amounts.  The accuracy achieve was 72.4%.
   
    ![Test1.1](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/Resources/Test1_Variable_Removed.png)!
    
    ![Test1.2](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/Resources/Test1_Ask_Amount1.png)!
    
    ![Test1.3](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/Resources/Test1_Ask_Amount2.png)!
        
    Second step was to add a third layer with 10 neurons.  The accuracy achieve was 72.82%.
    
    ![Test2.1](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/Resources/Test2_layer.png)!
    
    Third step was to increase the number of epochs to the training regimen.  The accuracy achieve was 72.77%.
    
    ![Test3.1](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/Resources/Test3_activation.png)!
    
    ![Test3.2](https://github.com/nkinsler/Neural_Network_Charity_Analysis/blob/main/Resources/Test3_epochs.png)!

## Summary of Analysis

### Summary of Results

Overall the models and subsequent changes to the models all failed to reach an accuracy of 75%.  None of the changes to the models resulted in significant variation to the overall accuracy score.

### Recommendation

Recommend using the random forest classifier model for the following reasons:
- The data set is tabular in nature
- The model is robust and scalable
- Output and feature selection is easy to interpret
- Builds on smaller models to form a robust and accurate model
