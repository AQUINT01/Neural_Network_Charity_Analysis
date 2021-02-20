# Neural Network Charity Analysis
## Overview :

Alphabet Soup is a privately funded, philanthropic organization whose goal is to raise money to assist organizations that protect the environment, improve people’s well-being, and unify the world. For the past 20 years, it has raised and donated over $10 billion to recipients worthy of its mission.

Unfortunately not every donation the company makes is impactful. In some cases, an organization will take the money and disappear. As a result, we were required to create a mathematical data-driven solution that can predict which organizations are worth donating to and which to avoid.




## Results: 

Using the Python TensorFlow library, I designed, tested, and  trained a deep neural network model to evaluate a data file with over 34,000 organizations that have received funding from Alphabet Soup over the year to produce a clear result.  



- ### Data Preprocessing 

What variable(s) are considered the target(s) for your model?
- The targeted variable for this model is the *IS_SUCCESSFUL* column because it indicates whether the money received by an organization was used effectively.

What variable(s) are considered to be the features for your model?
- The feature variables of this model are;
        -   APPLICATION_TYPE
        -   AFFILIATION
        -   CLASSIFICATION
        -   USE_CASE
        -   ORGANIZATION
        -   STATUS
        -   INCOME_AMT
        -   SPECIAL_CONSIDERATIONS
        -   ASK_AMT
    

What variable(s) are neither targets nor features, and should be removed from the input data?
- The   *EIN* & *NAME* columns were dropped  because these variables had too many unique values, `EIN = 34299` & `NAME = 19568` , with no significant impact on the result. 



- ### Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
-  After many attempts of reconfiguring the number of neurons, hidden-layers, and activation functions, The model with 4 hidden-layers yielded the best accuracy rate of **72.43%**, *refer to attached screenshot below*.
<img width="1118" src="https://github.com/AQUINT01/Neural_Network_Charity_Analysis/blob/main/images/model4.png">


Were you able to achieve the target model performance?
-  Unfortunately, this model's accuracy rate of 72.43% fell short in achieving the target model's performance rate of 75% or higher.  


What steps did you take to try and increase model performance?
- The original model started with two hidden-layers and 80 and 30 neurons, yielding a **72.18%** accuracy rate, as green-highlighted below.

<img width="1118" src="https://github.com/AQUINT01/Neural_Network_Charity_Analysis/blob/main/images/model1.png">

- A total of four attempts were made to optimize the model to meet the set target performance, including adding additional hidden-layers, trying different neuron combos, and changing the activation types to get better results.  After many redesigns, the model with 4 hidden-layers produced the closest  accuracy rate to the target performance rate.
<img width="1118" src="https://github.com/AQUINT01/Neural_Network_Charity_Analysis/blob/main/images/model4L.png">




## Summary: 

After careful reviewing the four models created, the model with 4 hidden-layers slightly performed better than the other models.  When comparing the accuracy rates of the  4 hidden-layer model, *72.43%*, with the 2 hidden-layer model,*72.18%*, the rate differences are within range of each other.  A case can be made to suggest that perhaps the 2 hidden-layer model with an accuracy rate of **72.18%** is respectable enough for the model's predictive result.  However, it's worth noting that even if the 2 hidden-layer model is "acceptable", all models created failed to achieved the target model performance and thus all models would be rejected.

Further optimization is recommended to achieve the desired performance.  For starters, it would be wise to re-examine the dataset in hopes of finding other feature variables that may be negatively impacting the model. As an example, how useful is the inclusion of the 'ASK_AMT' variable?  This information has no merit on the use of  funds and may be overly weighted within the model.  

An alternate solution would be to test a different machine learning technique such as the Random Forest. The Random Forest algorithm creates decision trees on randomly selected data samples, gets prediction from each trees and selects the best solution by means of voting. It has a variety of applications and can be used to classify corrupt organizations.

