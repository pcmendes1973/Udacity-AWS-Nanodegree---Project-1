# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Paulo Mendes

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
The initial model (without optimization) provided predictions that were much inferior than those posted earlier in the Kaggle competition. Extant Kaggle scores
were several times lower than those provided by the initial model.

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

### Create a table with the models you ran, the hyperparameters modified, and the Kaggle score.
|model|Time limit|Presets|Custom hpo|score|
|--|--|--|--|--|
|initial|600|Best quality|No|1.80506|
|add_features|600|Best quality|No|2.14682|
|hpo|600|Best quality|Yes|1.50047|



### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
Training models is a complex undertaking because of the wide variety of available models and the complexity of each model.
To obtain optimal predictions, modelers must expend considerable effort in choosing and fine-tuning several models.
