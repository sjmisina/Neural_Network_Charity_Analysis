# Alphabet Soup Charity Analysis
Analyst: <code><i> Stanley Misina, Columbia University Data Analytics Bootcamp</i></code><br />
Systems Used: <i><code> Python 3.8.11, TensorFlow 2.6.0, Jupyter Notebook 6.4.3 </i> </code> <br />
Data Source Provided: <i><code>charity_data.csv</code></i>

-----
## Overview
#### Abstract
From Alphabet Soup’s business team, we received a CSV containing more than 34,000 organizations that have received funding from the charity over the years. The question from the charity is: is there a predictable determination of success for these organizations with the support of the charity. Using neural network solutions, we have been tasked to see if there is a better than 75% chance of success based on Alphabet Soup's investment.

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
