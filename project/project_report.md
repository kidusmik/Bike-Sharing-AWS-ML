# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### KIDUS MICHAEL WORKU

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
DONE: I realized that the count predictions were of float64 values and have decimal values. And this wasn't a realistic prediction for counting number of bikes, therefore I had to convert the float64 dtype to int64 dtype and also rounding the prediction values.

### What was the top ranked model that performed?
DONE: The hpo model (Hyper Parameter Optimized) model performed best. And the WeightedEnsemble_L3 trained model was the top ranked in all 3 models.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
DONE: The datetime column can be further divided into month, day and hour and these can be added as additional features. And since the season and weather columns are just numeric representation of categories, they can be converted to a category dtype.

### How much better did your model preform after adding additional features and why do you think that is?
DONE: The model performed 62.91% better and it is because the model can better understand the datetime column when it is separated to month, day and hour.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
DONE: The model performed 6.41% better when the hyperparameters are tuned.

### If you were given more time with this dataset, where do you think you would spend more time?
DONE: I would spend more time on tuning the hyperparameters to improve my model.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|time_limit|problem_type|eval_metric|score|
|--|--|--|--|--|
|initial|600|None|None|1.79151|
|add_features|600|None|None|0.66433|
|hpo|600|regression|median_absolute_error|0.62172|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

DONE: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

DONE: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
DONE: The model shows improvment when there are more features especially features that can be simplified to smaller units such as year, month, day and hour. Hyperparameters tuning also improves the model since there is more control on the parameters such as which evaluation metric to use. Overall the best model was the hpo model and the top ranking model trained is WeightedEnsemble_L3 in all 3 models.
