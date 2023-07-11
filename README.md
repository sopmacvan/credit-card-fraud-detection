# Credit Card Fraud Detection
In this notebook project, we will be tackling the task of predicting fraudulent credit card transactions using a [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) dataset containing transactions made by European cardholders in September 2013. 

The primary goal is to develop a machine learning model that can accurately <u>classify transactions as either fraud or not fraud</u>, enabling credit card companies to identify and prevent unauthorized charges. 

The dataset presents a highly unbalanced distribution, with only 0.172% of the transactions labeled as fraud. It consists of numerical input variables resulting from a PCA transformation, with the exception of the 'Time' and 'Amount' features. The 'Time' feature represents the time elapsed in seconds between each transaction and the first transaction in the dataset, while the 'Amount' feature denotes the transaction amount. By leveraging these features and employing advanced machine learning techniques, we aim to build a robust model that can effectively detect fraudulent credit card activities.


# Conclusion

In conclusion, the <i>ExtraTreesClassifier</i>, an ensemble model, <u>emerged as the best-performing model for predicting fraudulent credit card transactions</u>. However, there are several limitations and areas for improvement to consider.

One limitation is that we only performed undersampling to address the class imbalance, using a 50:50 ratio. Undersampling can lead to information loss from the majority class and potentionally affect model performance. Exploring different ratios or alternative techniques, such as oversampling or SMOTE, coul be beneficial in mitigating the impact of class imbalance more effectively.

Additionally, the hyperparameter tuning process using RandomizedSearchCV with 10 iterations did not yield satisfactory results. It may be necessary to modify the hyperparameters to search from or increase the number of iterations to improve the tuning process. Exploring alternative techniques like GridSearchCV, although time-consuming, could also be considered for a more comprehensive hyperparameter search.

Furthermore, the <i>VotingClassifier</i>, which combines the predictions of multiple top-performing models, did not outperform the individual top model. This is understandable as the top models were not extensively tuned. In the future, it might be more efficient to focus on optimizing a single model, considering the time requirements associated with tuning multiple models.

Throughout our discussion, we have covered various aspects, including data preparation, exploratory analysis, dimensionality reduction, hyperparameter tuning, multiple model comparison, and model evaluation. Despite the challenges faced, this project has provided valuable insights into the detection of fraudulent credit card transactions and importance of addressing class imbalance.

To further improve the model, additional considerations could include feature engineering to capture more meaningful patterns. It would be beneficial to evaluate the model's predictions and analyze which features it considered the most influential during the decision-making process. This analysis can provide valuable insights and potentially lead to new ideas for feature engineering. By understanding the features that strongly contribute to the model's predictions, we can focus on enhancing those specific aspects of the dataset and potentially improve the model's performance in detecting fraudulent card transactions.

Overall the journey of developing a fraud detection model has highlighted the complexities involved and the need for iterative improvements and fine-tuning to achieve optimal performance.