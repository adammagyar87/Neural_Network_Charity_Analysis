# Neural_Network_Charity_Analysis
Mod 19 challenge

## Overview of the analysis: Explain the purpose of this analysis.
We attempted to apply machine learning to a dataset with the intent on determining if an applicant would be successful if funded by Alphabet Soup based on previous data. 

## Data Preprocessing
### What variable(s) are considered the target(s) for your model?
The target is our "Is_Successful" column. We created a binary data set to indicate if an applicant was successful or not.

### What variable(s) are considered to be the features for your model?
Every column besides "Is_Successful", "EIN", and "Name" as the first was our Target and we dropped the latter two.

### What variable(s) are neither targets nor features, and should be removed from the input data?
As stated above, we removed the "EIN" and "Name" columns as they were neither targets nor variables. In one optimization attempt (attempt 3) I decided to remove the "Affiliation" column, which ultimately led to a decrease in the models predictability. 

## Compiling, Training, and Evaluating the Model

### How many neurons, layers, and activation functions did you select for your neural network model, and why?
I initially started with 2 layers. The first layer had 100 neurons while the second layer had 40 neurons. We had 44 columns and 100 neurons seemed like a reasonable starting point. The second layer I arbitrarily chose 40 as it was fewer than the first. 

### Were you able to achieve the target model performance?
We aimed for 75% accuracy and the first attempt did not get there. The model kept flirting with 74% but was unable to get higher. The attempts to optimize are listed below. 

### What steps did you take to try and increase model performance?
The first optimization attempt was to change the amount of neurons in layer to from 40 to 60, then also add a third layer with 40 neurons. This had essentially no effect on the accuracy.

In the second attempt I added a fourth layer with 20 neurons, and it seemingly had no effect again.

For the third attempt I decided to move back to the data pre processing section and removed the affiliation column as an input. I set the layers/neurons to be the same as the first optimization attempt. This led to a drastic decrease in the accuracy, down in the 65% range.

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
