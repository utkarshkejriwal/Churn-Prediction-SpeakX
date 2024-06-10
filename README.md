## Churn-Prediction-SpeakX

### Data Collection and Preprocessing:
Data was collected from the Kaggle data repository
Link of dataset - https://www.kaggle.com/datasets/blastchar/telco-customer-churn
Dataset Summary -
  1. 7043 records
  2. 21 columns (4 numeric, 17 categorical)
  3. 11 missing values in column 'TotalCharges'
  4. Missing values deleted. Reason - Negligible amount of missing records
  5. Column 'CustomerID' deleted as it was irrelevant

### Exploratory Data Analysis
The following insights were obtained from this analysis
  1. The dataset was divided into 1 discrete and 3 continuous numeric columns and 16  categorical columns
  2. High correlation was found between Tenure and TotalCharges as well as MonthlyCharges and TotalCharges
  3. The ratio between the Churn class 'Yes':'No' was around 3:1.
  4. All the categorical variables had moderate to low correlation between each other.

### Feature Engineering
The dataset was divided into training and testing data at in the ratio 80 to 20.

### Model Building
XGBoost was used as the prediction model in this project with GridSearchCV used for fine tuning the Machine Learning Model.
A total of 720 (144*5) fits were checked to provide the best parameters for this model and dataset.

### Model Evaluation
A confusion matrix is created to better understand the output received using this Machine Learning model.

Accuracy - 80.74%
Recall - 51.33%
Precision - 68.68%
F1-Score - 58.75%
ROC-AUC Score - 71.4%

### Results
A moderately high value of accuracy is achieved. However the low scores of recall and precision can be blamed upon the imbalance found in the data.
The model can be further improved by augmenting the dataset by using techniques such as Oversampling and Undersampling or by augmenting the ML model furthermore by using methods such as Cost-Sensitive Learning.
