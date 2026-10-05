# custmer churn
Machine Learning project for predicting customer churn using the Telco Customer Churn dataset. The project includes data preprocessing, feature encoding, train/test splitting, scaling, and Logistic Regression classification. Model performance is evaluated using Accuracy, Precision, Recall, and F1-score, with predictions made for new customers.
Customer Churn Prediction

This project predicts whether a customer is likely to leave a service.

I used the Telco Customer Churn dataset for this project.

I started by loading the data and checking its columns and data types.

Before training the model, I inspected the dataset for missing values.

I also found that some numerical values were stored as text.

I converted those columns into proper numerical values.

After that, I checked the missing values again and handled them.

I removed the customer ID because it doesn’t provide useful information for prediction.

The target column was Churn, which contains Yes and No values.

I converted these values into 1 and 0 so the model could use them.

The dataset also contained many categorical features.

I encoded these features into numerical values.

After preprocessing, I separated the input features from the target.

Then I split the data into training and testing sets.

I used stratification so the class distribution stayed similar in both sets.

I also scaled the features before training the model.

For the first model, I used Logistic Regression.

I chose it because it is simple, fast, and works well as a classification baseline.

After training, I generated predictions for the test data.

I evaluated the model using Accuracy, Precision, Recall, and F1-score.

I wanted to look beyond accuracy because missing actual churners can be important.

The confusion matrix also helped me understand the model’s mistakes.

During the project, I checked each preprocessing step instead of training directly on the raw dataset.

This helped me understand how data preparation affects classification.

The project gave me practical experience with binary classification.

It also helped me understand why different evaluation metrics are useful for different problems.

what i used

Python, Pandas, NumPy, Matplotlib, and Scikit-learn.

Future Improvements

I would like to test Random Forest and Gradient Boosting, add ROC-AUC analysis, tune the classification threshold, and deploy the model.
