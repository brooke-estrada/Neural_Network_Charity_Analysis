# Neural Networks
### Overview of the analysis: 
Our team has been tasked with helping a non-profit, Alphabet Soup, create a model to accurately predict which organizations are worth donating to and which are high risk. Their company donates funds to organizations that are striving to improve individuals' well-being and unite the world.

### Results: 
Using bulleted lists and images to support your answers, address the following questions.

#### Data Preprocessing
* The target variable is the "IS_SUCCESSFUL" column. 
![](https://i.imgur.com/TT5VABt.png)

* The feature variables are the following columns:`"APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "INCOME_AMT", and "SPECIAL_CONSIDERATIONS"`.
*  We decided to remove columns: `"EIN"` and `"NAME"` as their information was not necessary for the analysis.
![](https://i.imgur.com/41Ankp3.png)

#### Compiling, Training, and Evaluating the Model
* In this model, there are # neurons and two hidden layers. We used the RELU activation functions to process the hidden layers and the sigmoid function to process the output layers. We decided to use the RELU function as we did not have any negative inputs. For the hidden layers, we found that two were necessary, and keeping them similar in size helped increase the accuracy.
* Unfortunately, we were not able to meet our target performance. We were able to achieve 69% accuracy.
* We attempted to increase the accuracy in three different ways.
    1. Created more bins for both the APPLICATION and CLASSIFICATION columns.
    2. Added a second layer and assigned it five hidden nodes.
    3. Changed the activation functions for the hidden layers from RELU to TANH.
![](https://i.imgur.com/jMtegjT.png)


### Summary:
The neural network model was not able to reach the optimal performance of 75% accuracy. We were able to adjust the bins, which increased the accuracy from 66% to 69%. However, our two other attempts did not increase the accuracy. For further analysis, we recommend considering changing the randomization state, removing more columns, or adding the number of epochs to the training regimen. For example,  "SPECIAL_CONSIDERATIONS" only have two types of values, and the "CLASSIFICATION" has 71 unique values, which could be weighing the model down and skewing the data.
