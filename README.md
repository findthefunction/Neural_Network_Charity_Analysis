# Neural Network Charity Analysis

## Overview
The purpose of this analysis is to use TensorFlow to create, train and evaluate the accuracy of a model designed to determine who should recieve loans from Alphabet Soup. We have been provided a dataset with 34000 organizations that have recieved funding over time.  We will be creating a binary classifier to determine which applicants will be successful.

## Results

### Dara Preprocessing

We select the target variable of IS_SUCCESSFUL and removed the EIN and NAME columns to eliminate their effect on the determinations of the model. We used the other columns as features with more relevant data to process.

![image](https://user-images.githubusercontent.com/31022640/125217836-7c0a4c00-e276-11eb-8bc0-e498d1b71219.png)

First attempt with 60 and 30 nodes on the first and second layer respectively, utilizing Relu activations for these layers and sigmoid for the output layer.

![image](https://user-images.githubusercontent.com/31022640/125218037-df947980-e276-11eb-9302-6a2e3441dc19.png)

This gave us a total trainable parameter cout of 8881.

After training the model the loss and accuracy factors were0.9244967940805953 for loss and 0.6570262312889099 for accuracy.

![image](https://user-images.githubusercontent.com/31022640/125218176-35692180-e277-11eb-940d-6ec23c04f5e8.png)

### Numerous Iterations

During the optimization experimentation the model experienced overfitting and would not generate a more accurate score beyond ~ 0.5126 for several iterations regardless of the adjustments in activation type including Gradient Descent (SGD) and tanh.  After restarting google colab notebook the model would generate different values and then fall into the same cycle of over fitting.

The final attempt involved adding another hidden layer and adjustijng the node sizes to 100, 50 and 25 respectively. This had a negative impact on the loss factor and resulted in a slightly lower score.

![image](https://user-images.githubusercontent.com/31022640/125219483-a9a4c480-e279-11eb-8394-537ba6464357.png)

The final attempt resulted in a lower score than the first model with a loss of 1.2403262853622437 and accuracy of 0.650845468044281

![image](https://user-images.githubusercontent.com/31022640/125219092-12d80800-e279-11eb-9030-2f8c3fdfe55c.png)


## Summary

The models were very instructive and showed some of their limitations based on the input layers and the features selected for analysis. Increasing the layer count and number of nodes had varying affect, but there seemed to be an issues with the model starting fresh after iterations.  Further review would include trying diffrent feature combinations to see how they perform, experimenting with advanced activation and taking more time to analyse and fit the data.  Having powerful machine to process the models is a distinct advantage as running numerous iterations takes time.  Understading the underlying math behind the activations is very important.



