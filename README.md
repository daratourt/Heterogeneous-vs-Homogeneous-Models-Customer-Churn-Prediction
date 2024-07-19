# Evaluating the Effectiveness of Heterogeneous Ensemble Models Versus Homogeneous Models in Bank Customer Churn Prediction
## Problem Definition
The primary objective of the Bank Customer Churn Prediction project is to analyze the demographics and financial information of bank customers, including factors such as age, gender, credit score, country, balance, and more, to predict whether a customer will leave the bank. Customer churn, the decision of customers to leave a bank, can significantly impact the bank's business and profitability. By accurately predicting customer churn, the bank can take proactive measures to retain valuable customers and enhance customer satisfaction.

This project will compare the performance of heterogeneous ensemble models with single models in predicting bank customer churn. By leveraging the strengths of different algorithms, heterogeneous ensemble models aim to provide more robust and accurate predictions, which can help the bank implement effective retention strategies.

## About the Dataset
The dataset used in this project is sourced from [Kaggle](https://www.kaggle.com/datasets/mathchi/churn-for-bank-customers?datasetId=797699&sortBy=voteCount) and comprises 10,000 rows and 14 columns. The dataset's primary objective is to predict whether a customer will churn (leave the bank) based on their demographics and financial information.

The dataset contains several independent variables, which are potential factors that may influence a customer's decision to leave the bank. These variables include customer-specific information such as:

- Credit Score: A numerical representation of the customer's creditworthiness.
Country (Geography): The country where the customer resides.
- Age: The age of the customer.
- Tenure: The number of years the customer has been with the bank.
- Bank Balance: The balance maintained by the customer in their bank account.
- Number of Products (NumOfProducts): The number of bank products the customer uses.
- Has Credit Card (HasCrCard): Indicates whether the customer holds a credit card (1 if they do, 0 if they do not).
- Is Active Member (IsActiveMember): Indicates whether the customer is an active member with the bank (1 if they are active, 0 if they are not).

The target variable, also known as the dependent variable, is labeled "Exited" and is represented by a binary flag: 1 if the customer closed their account with the bank and 0 if the customer is retained. This dataset will be used to evaluate the effectiveness of heterogeneous ensemble models versus single models in predicting bank customer churn.

## Methodology
### Data Preprocessing
The dataset was first loaded and unnecessary columns such as 'RowNumber', 'CustomerId', and 'Surname' were dropped to focus on relevant features. Categorical variables like 'Geography' and 'Gender' were converted into numerical values using one-hot encoding. Binary variables like 'HasCrCard' and 'IsActiveMember' were also converted to integers. The dataset was then split into training and testing sets with an 80-20 split. Features were scaled using StandardScaler to ensure that all features contribute equally to the model.

### Model Training and Evaluation
The models were trained and evaluated using several performance metrics including accuracy, precision, recall, F1 score, and ROC AUC. Confusion matrices and ROC curves were plotted for better visualization.

### Homogeneous Models
A Random Forest classifier was trained on the training data and predictions were made on the test data. Performance metrics were calculated and the confusion matrix and ROC curve were plotted. Similarly, a Decision Tree classifier and a Support Vector Classifier (SVC) were trained and evaluated using the same process.

### Heterogeneous Ensemble Model
A Voting Classifier was created by combining Random Forest, Decision Tree, and SVC. The voting method was set to 'soft' to use the predicted probabilities for voting. The ensemble model was trained on the training data and predictions were made on the test data. Performance metrics were calculated and the confusion matrix and ROC curve were plotted.

## Results
The Random Forest model achieved an accuracy of 0.8645, precision of 0.7480, recall of 0.4682, F1 score of 0.5759, and ROC AUC of 0.8566. The Decision Tree model achieved an accuracy of 0.8540, precision of 0.7264, recall of 0.4545, F1 score of 0.5588, and ROC AUC of 0.8410. The SVC model achieved an accuracy of 0.8620, precision of 0.7411, recall of 0.4618, F1 score of 0.5745, and ROC AUC of 0.8542. The heterogeneous ensemble model achieved an accuracy of 0.8565, precision of 0.7103, recall of 0.4555, F1 score of 0.5550, and ROC AUC of 0.8419.
| Model                     | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|---------------------------|----------|-----------|--------|----------|---------|
| Random Forest             | 0.8645   | 0.7480    | 0.4682 | 0.5759   | 0.8566  |
| Decision Tree             | 0.8540   | 0.7264    | 0.4545 | 0.5588   | 0.8410  |
| SVC                       | 0.8620   | 0.7411    | 0.4618 | 0.5745   | 0.8542  |
| Heterogeneous Ensemble    | 0.8565   | 0.7103    | 0.4555 | 0.5550   | 0.8419  |

## Conclusion
The study compared the effectiveness of heterogeneous ensemble models versus homogeneous models in predicting bank customer churn. While the heterogeneous ensemble model did not significantly outperform the homogeneous models in terms of accuracy, precision, recall, and F1 score, the Random Forest model stood out with slightly better overall performance metrics. These findings indicate that while heterogeneous ensemble models can provide robust predictions, homogeneous models like Random Forest may still offer strong predictive power for bank customer churn. Future research could explore additional ensemble techniques and more complex models to further enhance prediction accuracy.








