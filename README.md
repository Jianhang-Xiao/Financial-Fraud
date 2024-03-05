# Financial-Fraud

i. Which insights did you gain from your EDA?

There are some fraud cases idenfified in the data. A lot of transaction are small amounts. The transaction amounts shows a range of common values and potential outliers. Cash out and transfer are identified as fraud. In terms of transaction amount by type, transfer has the average high amount than other four types of transactions. 

ii. How did you determine which columns to drop or keep? If your EDA
informed this process, explain which insights you used to determine
which columns were not needed.

selected = ["step", "nameOrig", "nameDest", "isFlaggedFraud"] #isFlaggedFraud is 0, so no need to include in the dataset. "nameOrig" and "namedest" just account number, so they are not important. "step" is not necessarily to include because we are doing randomized analysis. 


iii. Which hyperparameter tuning strategy did you use? Grid-search or
random-search? Why?

I used both grid-search and random-search. Grid search tries every combination of hyperparameters in the specified ranges and evaluates them using cross-validation. This model can explores all possible combinations of hyperparameter values. In contrast, random search selects random combinations of hyperparameters and evaluates them.



iv. How did your model's performance change after discovering optimal
hyperparameters?

Precision measures the accuracy of positive predictions.

Recall measures the ratio of correctly predicted positive observations to the all observations in actual class.

F1-score is the weighted average of precision and recall. It is a single metric that combines both precision and recall.

Support indicates the number of actual occurrences of each class in the specified dataset.

For the Gridserach and random-search, before and after hyperparameter tuning, the two model's performance did not change much after discovering the optimal hyperparameters.






v. What was your final F1 Score?

I used random forest classifier. The best model is to evaluate on a test set to calcuate F1 score. 

For the Gridserach, the final F1 score is 

Class 0: F1-score = 0.999766
Class 1: F1-score = 0.837209

For the Randomsearch, the final F1 score is 

Class 0: f1-score = 0.999733   
Class 1: F1-score = 0.809524