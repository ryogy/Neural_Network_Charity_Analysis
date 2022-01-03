# Neural Network Charity Analysis

## Overview of Analysis
The purpose of this analysis was to design and test a deep learning model to predict Charity donation application success rates.

## Results
### Data Preprocessing

* The target variables for the model, or the y values, was the IS_SUCCESSFUL column within the dataframe.  The data in this column was represented in binary format.

* The main features for the model were APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT.  All of these columns contained relevant predictive information that was encoded.

* The columns that were removed as features from the model were NAME, EIN, STATUS, and SPECIAL_CONSIDERATIONS.  All of these columns contained irrelevant information, or information that would of created confusion within the model.

* Buckets were created to organize the following columns: INCOME_AMT, CLASSIFICATION, ASK_AMT, and APPLICATION_TYPE.  This was used to narrow the distribution of information in these columns and eliminate outliers that could of confused the model.

### Compiling, Training, and Evaluating the Model

* For the optimized model, the architecture was as follows...
Number of Input Features: 36
First Hidden Layer: 60 Nodes with Relu activation function
Second Hidden Layer: 20 Nodes with Selu activation function
Third Hidden Layer: 7 Nodes with Selu activation function
Output Layer: 1 node with Sigmoid activation function

Used the Relu activation function for the broadness of the application and then used two Selu (Scaled Exponential Linear Unit) layers, because they are self normalizing and coul hopefully make better sense of the data once the Relu layer had done its work.

* I was not able to achieve target performance.  The model came in at 72.4% Accuracy with a test loss of 55.4%.

*   The main steps I took to oprimize performance were in trying to further clean the dataframe and adapt it to a deep learning model.  Removing unnecessary columns and bucketing and narrowing the distribution of values in some columns.  I tried quite few different strategies with the model, adding and removing layers, adding and removing nodes, and changing the activation functions.  All of this proved fruitless as I saw very little gains in accuracy.

## Summary
Over the three attempts for optimization, the models were unable to break 75%, and all models had an accuracy of around 72%.  In attempt for further optimization, I would recommend a rigourous statistical analysis of the dataframe so it would be easier to streamline the features for the model.
