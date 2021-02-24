# Neural Networks Charity Analysis

## Overview
With machine learning and neural networks, we have used the features in our dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup thus helping the foundation predict where to make investments.

## Results: 

### Data Preprocessing
#### The target or y variable was the IS_SUCCESSFUL column 
#### The features for the model consist of APPLICATION TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT
#### Data that were neither targets nor features, and were removed from the input data were EIN, NAME, and STATUS.

### Compiling, Training, and Evaluating the Model
####  After trail and error I settled with the model having 10 neurons in the 1st layer, 8 neurons in the second and 4 in the 3rd using RElu activation in the hidden layers and simoid in the output layer.  The activation combination yield the highest accuracy.  The relatively low amount of neurons was based on performance and the fact that higher neuron counts did not improve accuracy. 
#### The highest performace we achieved was .7264, basically the same pre-optimization.  
#### Initially to improve performance I dropped the STATUS feature and ORGANIZATION feature.  That actually dramatically drop accuracy so I added back "ORGANIZATION".  I then iterated through activation combinations to identifiy the best performaning.  RElu was by far the best performing for the hidden layers.  I then added a 3rd hidden layer and both increased and decreased neurons. These last iterations had no impact on accuracy leading me to use fewer neurons to focus on calculation time. 

## Summary
The overall results of the deep learning model was below the accuracy threshold to be reliable despite many iterations between neuron count, activations and epochs. I recommend getting more data on the applicants and going through various compbinations of the wider data pull to try to get over .75 accuracy.
