# Analysis Report

## Overview

Alphabet Soup’s business team, gave me a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset were a number of columns that capture metadata about each organization. The non-profit foundation Alphabet Soup wants to me to create an algorithm to predict whether or not applicants for funding will be successful.

My goal is to optimize my model in order to achieve a target predictive accuracy higher than 75%.

## Results

* Data Preprocessing

    Variables considered targets in my model:

  * "IS_SUCCESSFUL"

    Variables considered features in my model:

  * "APPLICATION_TYPE"
  * "AFFILIATION"
  * "CLASSIFICATION"
  * "USE_CASE"
  * "ORGANIZATION"
  * "INCOME_AMT"
  * "ASK_AMT"
  * IS_SUCCESSFUL

    Variables dropped from the dataset and are neither targets nor features of my model:

  * "EIN"
  * "NAME"
  * "STATUS"
  * "SPECIAL_CONSIDERATIONS"

* Compiling, Training, and Evaluating the Model

  * My deep-learning neural network model contained total of eight hidden layers with 10, 15, 20, 30, 40, 50, 60, and 70 neurons respectively. The output layer's neurons were 1 (binary_classification) due to the IS_SUCCESSFUL yes/no value. The optimizer is adam and loss metrics setting is binary_crossentropy.

  * I was unable to attain the target model performance threshold of 75%. I reached .728 in my final model version.

  * To improve my model over several iterations, I dropped several more non-essential columns, increased the number of values in each bin, increased the number of neurons and the number of hidden layers from my original 3 ![Image](https://github.com/pemenalo/charity_funding_predictor/blob/main/Images/layers.PNG "Hidden Layers & Input Features") to 8 ![Image](https://github.com/pemenalo/charity_funding_predictor/blob/main/Images/layers_8.PNG "Hidden Layers & Input Features"), and increased the number of epochs from my original 100 to 150. With al this done, my model's accuracy improved from around 70% upto it's highest of 72.99% ![Image](https://github.com/pemenalo/charity_funding_predictor/blob/main/Images/accuracy_score.PNG "Model Accuracy") and down back to 72.82% ![Image](https://github.com/pemenalo/charity_funding_predictor/blob/main/Images/accuracy_score_8layers.PNG "Model Accuracy"). Overal my model iterations di not significantly improve.

## Summary

Further research is required on the model type chosen and the various levels of restriction I chose to use for my model. I would recommend taking learning rate and regularization rate into account in further iterations of the model as well as other activation types.
