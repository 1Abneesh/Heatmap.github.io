# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Abneesh Kumar

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Since I am working on my local environment, I realized that the provided code snippet needed some changes to make it compatible with my local setup. Specifically, the code seemed to be written for a specific execution environment, and I had to make adjustments to ensure it could run properly in my local development environment.

Additionally, in order to understand and utilize the various hyperparameters of the AutoGluon library effectively, I referred to the documentation. This allowed me to gain a better understanding of the library's capabilities and make the necessary modifications to the code. As a result, I was able to successfully code and run the prediction process in my local environment.

### What was the top ranked model that performed?
The top-ranked model was the (add features) model named WeightedEnsemble_L3, with a validation RMSE score of 31.894198 and the best Kaggle score of 0.48693 (on test dataset).

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The exploratory analysis helped me discover several insights that guided my feature engineering process. Firstly, I found that the variables "season" and "weather" had integer values ranging from 1 to 4. Recognizing that these values represented categorical information, I converted them into categorical variables to improve the model's understanding of their impact on the target variable.

Additionally, I observed that the "datetime" column contained information about the year, month, day, and hour. Recognizing the importance of these temporal components, I split the "datetime" column into separate columns for year, month, day, and hour. This allowed the model to capture more granular temporal patterns and significantly enhanced its performance. Specifically, the model's performance improved from an initial score of 1.76 to a much lower score of 0.49.

By leveraging these additional features derived from the exploratory analysis, the model was able to capture important categorical and temporal patterns in the dataset, resulting in a substantial improvement in its predictive performance.

### How much better did your model preform after adding additional features and why do you think that is?
The model's performance significantly improved after adding additional features. The best performing model with the added features achieved a RMSE of 31.894198, compared to the previous RMSE of 51.300820. This indicates a substantial increase in performance, with approximately 37.9% improvement.

The improvement can be attributed to the additional features that were incorporated into the model. By splitting certain features and extracting more granular information, the model was able to capture more detailed patterns and relationships within the data. This increased level of feature engineering provided the model with a richer representation of the underlying patterns, leading to improved predictive accuracy.

Overall, the inclusion of additional features allowed the model to better understand the complexities of the dataset, resulting in a significant 37.9% boost in performance compared to the earlier version of the model.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
After experimenting with different hyperparameters, the model showed improvement compared to its initial state. However, the performance fell slightly short of the gains achieved through feature engineering alone. Fine-tuning hyperparameters requires more in-depth understanding and experimentation to achieve optimal results. Despite this, hyperparameter optimization contributed to enhancing the model's performance, complementing the gains achieved through feature engineering. Combining optimized hyperparameters with well-engineered features can further improve the model's predictive capabilities.

### If you were given more time with this dataset, where do you think you would spend more time?
If given more time with the dataset, I would focus on extensive hyperparameter tuning to identify the optimal model configuration. This would involve exploring different combinations of hyperparameters, conducting cross-validation, and utilizing advanced techniques such as Bayesian optimization or genetic algorithms. Additionally, I would invest time in feature selection and extraction techniques to further enhance the model's performance.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|best-quality|intial_config|intial_config|1.75981|
|add_features|best-quality|problem_type = regression|intial_config0.48693|
|hpo|best-quality|tabular autogluon|dropout_prob = 0-0.7,learning rate = 10|0.60202|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
During this project, I successfully applied the concepts learned in the course to develop a regression model using the autogluon framework. By analyzing the features and conducting EDA, I gained valuable insights that improved the model's performance. Considering factors like working hours and seasonal variations, I was able to achieve competitive results with a kaggle score close to experienced professionals.
