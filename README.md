# Alphabet Soup Charity Analysis
Analyst: <code><i> Stanley Misina, Columbia University Data Analytics Bootcamp</i></code><br />
Systems Used: <i><code> Python 3.8.11, TensorFlow 2.6.0, Jupyter Notebook 6.4.3 </i> </code> <br />
Data Source Provided: <i><code>charity_data.csv</code></i>

-----
## Overview
#### Abstract
From Alphabet Soup’s business team, we received a CSV containing more than 34,000 organizations that have received funding from the charity over the years. The question posed is: can success of the project be predicted with better than 75% accuracy with the charity's investment?

#### Method
The received data is imported by Python as a Pandas dataframe. The data is prepared for neural network processing, and output is generated from a multi-layered machine learning model that will produce an accuracy result reflecting the success rate of companies with whom Alphabet Soup has invested.

## Results
* Data Preprocessing
    * The data provided shows a column for 'IS_SUCCESSFUL,' and will be the targeted data point for these predictions.
    * There are many data points (features) that will be used as input for the models. Included are:
        - AFFILIATION
        - APPLICATION_TYPE
        - ASK_AMT
        - CLASSIFICATION
        - INCOME_AMT
        - ORGANIZATION
        - SPECIAL_CONSIDERATIONS
        - STATUS
        - USE_CASE
    * The columns for "NAME" and "EIN" have no direct effect on the success/falure rate, and have been excluded from processing.

* Compiling, Training, and Evaluating the Model
    * Initial preparation for the Sequential Neural Network specified 43 input features, into three processing layers that began with 80 neurons and decreased to 30 and 15, and a single output layer.
    * The target performance of 75% accuracy was not met (72.75%).
    * Further testing was done with three dynamic tuned models that statically and dynamically selected inputs, layers, neurons, and activations. These attempts yeilded accuracy results of:
        - First Model: 73.49%
        - Second Model: 73.17%
        - Third Model: 73.51%
    * Although accuracy was only improved marginally, the total loss of the dynamic deep learning models did offer an excellent decrease in the Loss factor.

## Summary
The initial model showed that there was a 72.74% chance of success when Alphabet Soup invested with an organization.
![Test0Result](https://user-images.githubusercontent.com/84740997/138523902-ba350b3d-085c-41af-ad70-c1736aba04bb.jpg)


Further testing involved tuned models in an attempt to improve prediction accuracy. Three efforts were made:<br />

<b>Test</b> 1 *(added activation options on hidden layers)*
![Test1Results](https://user-images.githubusercontent.com/84740997/138524116-538cfdb0-612d-48e5-88e2-7f7df0969e67.jpg)

<b>Test 2</b> *(non-sigmoid activation options on all layers, hidden layers randomized from 5 to 10, 'CLASSIFICATION' <4000 and 'APPLICATION_TYPE' < 1000 are grouped into 'Other', changed compile options)*
![Test2Results](https://user-images.githubusercontent.com/84740997/138524146-9581afc9-8916-4699-8be8-e2cff0a2ec29.jpg)

<b>Test 3</b> *(added activation options on hidden layers, input is randomized from 10 to maximum total features)*
![Test3Results](https://user-images.githubusercontent.com/84740997/138524162-408f2797-e219-46e4-917b-9f42c5f99055.jpg)

To further investigate these tests we recommend alternative, non-sequential hyperparameter models considered. Another means of improving accuracy is to have more datapoints. Although we did not boost success rate to 75%, we have minimized loss using these tuned models.
