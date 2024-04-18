# Alphabet Soup Charity Report

## Overview of the Analysis

The purpose of this analysis was to to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. 

## Processing the Data

* The target feature for the model is 'IS_SUCCESSFUL'

* Feature Variables Used:

    * APPLICATION_TYPE — Alphabet Soup application type

    * AFFILIATION — Affiliated sector of industry

    * CLASSIFICATION — Government organization classification

    * USE_CASE — Use case for funding

    * ORGANIZATION — Organization type

    * STATUS — Active status

    * INCOME_AMT — Income classification

    * SPECIAL_CONSIDERATIONS — Special considerations for application

    * ASK_AMT — Funding amount requested

    * IS_SUCCESSFUL — Was the money used effectively

* Removed Variables:

    * EIN - Identification Column

    * NAME - Identification Column

# First Attempt Results

* Layers
    * Layer1 had 75 hidden nodes and "relu" activation
    * Layer2 had 50 hidden nodes and "relu" activation
    * Output Layer used "sigmoid" activation

* Model Training
    * 100 epochs

* Results
    * Accuracy: 0.7295626997947693

# Second Attempt Results

* Layers
    * Layer1 had 100 hidden nodes and "relu" activation
    * Layer2 had 50 hidden nodes and "relu" activation
    * Output Layer used "sigmoid" activation

* Model Training
    * 100 epochs

* Results
    * Accuracy: 0.7301457524299622 (Improvement from previous result)

# Third Attempt Results
* Layers
    * Layer1 had 50 hidden nodes and "relu" activation
        * I added a Dropout of 0.325
    * Layer2 had 45 hidden nodes and "relu" activation
        * Dropout of 0.325
    * Layer3 had 30 hidden nodes and "relu" activation
        * Dropout of 0.325
    * Output Layer used "sigmoid" activation

* Model Training
    * 75 epochs
    * Added a Validation_split of 0.155

* Results
    * Accuracy: 0.7292128205299377 (worse from both previous result)

# Third Attempt Results
* Layers
    * Layer1 had 50 hidden nodes and "relu" activation
        * I added a Dropout of 0.325
    * Layer2 had 45 hidden nodes and "relu" activation
        * Dropout of 0.325
    * Output Layer used "SGD" activation with a learning rate of 0.01

* Model Training
    * 75 epochs
    * Added a Validation_split of 0.155
    * Added Batch size of 32

* Results
    * Accuracy: 0.7306122183799744 (Overall Improvement)

## Summary

I did many tests with many different variables but was only able to get a max accuracy of 0.7306. This did not meet the 0.75 requirement. I would reccomend trying different activations to test new models because changing from "sigmoid" to "SGD" gave me the highest accuracy, although a small improvement.
