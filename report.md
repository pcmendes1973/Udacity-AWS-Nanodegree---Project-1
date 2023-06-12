# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Paulo Mendes

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
The initial model provided predictions that were mhcu inferior than those posted earlier in the Kaggle competition. Before Kaggle scores
were several 

### What was the top ranked model that performed?
The model with optimized hyperparameters performed best.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I attempted to add weekday as a separate feature because I recokned that demand could vary as a function of the week (e.g. lower
on business days and higher on weekends). But exploraroty analysis showed that this wasn't true--demand was uniform across weekdays.
The resulting model actually performed worse than the initial 'raw' model.

### How much better did your model preform after adding additional features and why do you think that is?
Performance worsened after I added the weekday as a separate feature. Since demand was constant across weekdays, it's possible that this
'dead' variable introduced more inexactitude across the models, thus impacting convergence and worsening the model characteristics.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
Hyperparameter tuning yielded the best results, with a roughly twofold improvement in my Kaggle score.

### If you were given more time with this dataset, where do you think you would spend more time?
Trying out other values and combinations of hyperparameters. Tweaking hyperparameters yielded the best results. Another
potential approach is adding new features, particularly splitting datetime into day, month and year.

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
