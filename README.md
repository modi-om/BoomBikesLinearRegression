# Boombikes - Linear Regression Model 
> Multiple Linear Regression performed on the Boombikes bike rental dataset


## Table of Contents
* [Problem Statement](#problem-statement)
* [Business Goal](#business-goal)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)

## **Problem Statement**

A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.


A US bike-sharing provider **BoomBikes** has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 


In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.


They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

- Which variables are significant in predicting the demand for shared bikes.
- How well those variables describe the bike demands

Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors. 


## **Business Goal**
We are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 

## Conclusions

- The major steps included in the python notebook are data interpretation, data visualisation, data pre-processing, model training, feature selection, residual analysis, model evaluation on the test set. 
- Analysis is carried out using a Mixed Feature Selection Approach. **15 features are selected algorithmically using Recursive Feature Elimination.** Further selection is done manually by looking at multicollinearity and statistical significance of features and overall fit of the model. The **10 most significant features to understand demand have been reported.**

- The R-squared value of the train set is 83.2% whereas the test set has a value of 82.6% which suggests that our model broadly explains the variance quite accurately on the test set and thus we can conclude that it is a good model.

- Our developed model's mean squared error is ~0 on both the training and testing datasets which suggests that the variance is accurately predicted on the test set. The p-values and VIF were used to select the significant variables. RFE was also conducted for automated selection of variables.


- Concepts such as EDA, p-value, VIF, RFE were used and model building was done using statsmodels library.

- Model is stable at 82%(+/-13%) coefficient of determination at 95% Confidence level, ascertained through cross validation.

#### **The Equation for best fitted line -** 
- **cnt** = 0.131488 + (**temp** × 0.453612) + (**yr** × 0.240374) - (**weekday_Sat** × 0.071721) - (**mnth_Nov** × 0.099894) - (**mnth_Dec** × 0.067850) + (**workingday** × 0.054807) + (**season_Winter** × 0.115089) - (**season_Spring** × 0.125942) - (**weathersit_Light Snow + Rain** × 0.280320) - (**weathersit_Mist + Cloudy** × 0.077951)




#### **Business Suggestions -**

- **Temparature is the major driver** and should be given maximum attention to increase bike rental number.
- **Focus should be more on Winter Season and Working Days** since the have positive influence on the bike rentals and boost the rentals.
- We can see **Spring season has negative coefficients** and negatively correlated to bike rentals. So we can **give some offers** there to increase the demand.
- Also we see **negative coefficients for Light Snow , Rain and Misty weather , for this we can also introduce some offers/discounts.**
- Special Schemes can be launched for **Months of Nov and Dec** since they have negative coefficients.


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- pandas
- seaborn
- matplotlib
- statsmodels
- sci-kit learn
- numpy

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

