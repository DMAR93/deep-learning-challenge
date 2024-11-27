# deep-learning-challenge
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures
# **Report in the Neural Model for Alphabear Soup** #

## Overview##
The propouse of this analysis is to develope and evaluate a deep learning model to predict the success of the charitable donation for Alphabet Soup. By analyzing past donation data.

## Results ##
### Target Variable ###
 the target variable for the model is **IS_SUSSESSFUL**, which indicate whether a funding request was successful.
## Feature Vairables: ##
 This iclude columns like **APPLICATION_TYPE**, **CLASSIFICATION** and **ASK_AMT** were columns importatn for the accuracy of the model but needed some adjust to improve the aim ot the model.

 ## Removed Variables: ## 
 after analizing the different columns and how it affects accuracy we found that apart of **NAME and EIN** also **STATUS** beacuse of its low variance and **SPECIAL_CONSIDERATIONS ** because it doesnt impact the model it was better to drop those columns.

 ## Compiling, training and Evaluating the model##
### Neuron Layers
- Layer 1: 254 Neurons with Relu activation function
- Layer 2: 128 Neurons with tanh activation function
- Layer 3: 65 Neurons with Relu activation function
- the output layer consist of 1 neuron with a Sigmoid activation to predict binary outcomes.
-  The Relu and tanh function were selected for hdden layers to address potential issues, while sigmoid were used for the output layer to handle the binary calssiffication task.

## Target model perfomrance:
- Despite efforts, Dropping different columns, using Relu, tahn and also Leakly function, using different hidden layers, using different epocs, activations and others the model did no achieve the target performance of 75%. The final accuracy was approximately 73%. 1% better than the startet code.

## Steps taken to improve Model Performance:
- Experimented with different numbers of neurons and layers to optimized the model architecture.
- Used relu and tanh function to imprvve gradient flow and mitigate vanishing gradient problem.
- Standarized the Feature data usinf **StandardScaler** to ensure consistent scalling
- Applied SMOTE to address class imbalance in the target variable, creating a more balanced dataset.
- tried early stopping to prevent overfitting by monitoring validations loss during training
- Increase the number of Epochs and experimented with different Batch size.

## Summary:
the deep learning model successfully identified patterns but it fells short in the desired accuracy. 

### recomendation:
- use an alternative model. 
- Identify and collect more data. 
- Engineer more features to capture relationship between vaibales.
