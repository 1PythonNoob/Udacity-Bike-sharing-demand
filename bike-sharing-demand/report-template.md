# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Lukas Klockenhoff

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Before being able to submit my Predictions I had to
change all of the Outputs that were Negative into Zeroes.
### What was the top ranked model that performed?
The 3rd model with optimized Hyperparameters and added features performed best for me. After no quantitive change happened between the 1st and 2nd I was relieved that the 3rd model performed better. 
The Model had 3600s time to train, the problem was spezified as "regression" and the the **kwargs were "bayesopt" 

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I found that splitting the datetime up was helpful to the predictivness of the model. While my initial seperat "month" column had no real effect on the models performance I later added a "Hour" column for the 3rd model by defining a new column in the train.csv that used the dt method in pandas to isolate the Hour of the datetime object. 

### How much better did your model preform after adding additional features and why do you think that is?
I thought my 2nd model would perform better with the additional "Month" column would improve performance due to (Probably) not much bike sharing in winter months. But when there was no change (maybe due to another error) i added the "Hour" feature for the 3rd Model, because there will be hours where there is no bike sharing demand (10pm - 4am?) so features and targets are directly related 

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
Surprisingly the time i trained the model for did not have as much effect on the performance as I thought (at least that was true for this model with my hyperparameters) with one second training time the 3rd model archieved a 0
.5 Score, just like the model trained for 1 hour. I cant say much to that due to my very limited knowledge of the topic but as I progress in this course i will find out the reason for this and the exact effect of certain Params.
### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|?|?|?|?|
|add_features|?|?|?|?|
|hpo|?|?|?|?|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation
