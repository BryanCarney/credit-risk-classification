# credit-risk-classification

### Solved File

[credit_risk_classification](https://github.com/BryanCarney/credit-risk-classification/blob/main/credit_risk_classification.ipynb)

# Background Requirements

### Instructions

**The instructions for this Challenge are divided into the following subsections:**

• Split the Data into Training and Testing Sets

• Create a Logistic Regression Model with the Original Data

• Write a Credit Risk Analysis Report

### Split the Data into Training and Testing Sets

**Open the starter code notebook and use it to complete the following steps:**

1. Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

2. Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

> note - A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

3. Split the data into training and testing datasets by using train_test_split.

### Create a Logistic Regression Model with the Original Data

**Use your knowledge of logistic regression to complete the following steps:**

1. Fit a logistic regression model by using the training data (X_train and y_train).

2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

3. Evaluate the model’s performance by doing the following:

> • Generate a confusion matrix.

> • Print the classification report.

4. Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

### Write a Credit Risk Analysis Report

Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:

1. **An overview of the analysis:** Explain the purpose of this analysis.

2. **The results:** Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

3. **A summary:** Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.



# Credit Risk Analysis Report

### Overview of the Analysis
The purpose of this analysis is to evaluate the performance of a machine learning model in predicting credit risk, specifically in identifying high-risk loans. The goal is to determine whether the model can accurately classify loans as either "healthy" (class 0) or "high-risk" (class 1) based on various features related to the applicants. The model will be used by a financial institution, such as a bank, to help make informed decisions regarding loan approval and risk assessment. A robust model is crucial for minimizing financial losses due to defaults while also ensuring the institution doesn't miss out on legitimate loan opportunities.

### The Results

**Accuracy Score: 0.99**

The model achieved an overall accuracy of 99%, which indicates it correctly classified 99% of the loans.

**Precision for Class 0 (Healthy Loan): 1.00**

The precision for class 0 is perfect, meaning the model is able to predict healthy loans with 100% certainty, without incorrectly labeling any unhealthy loans as healthy.

**Recall for Class 0 (Healthy Loan): 0.99**

The recall for class 0 is 99%, meaning the model correctly identified 99% of the actual healthy loans, with a very small number of false negatives.

**Precision for Class 1 (High-Risk Loan): 0.84**

The precision for class 1 is 84%, meaning when the model predicts a loan as high-risk, 84% of the time it is correct, though 16% of high-risk predictions are false positives (healthy loans classified as high-risk).

**Recall for Class 1 (High-Risk Loan): 0.99**

The recall for class 1 is 99%, meaning the model correctly identifies 99% of the actual high-risk loans, making it very effective at catching high-risk loans and minimizing the chances of a false negative (missing a high-risk loan).

**F1-Score for Class 1 (High-Risk Loan): 0.91**

The F1-score for class 1 is 0.91, indicating a strong balance between precision and recall, though there's still room for improvement in precision.

### Summary

The machine learning model performs exceptionally well with an overall accuracy of 99%. It shows near-perfect performance in predicting healthy loans (class 0), with 100% precision and 99% recall, making it highly reliable for identifying loans that are low-risk. For high-risk loans (class 1), the model shows excellent recall (99%), meaning it catches most of the high-risk loans, but the precision (84%) is slightly lower, indicating that some healthy loans are misclassified as high-risk.

Given that missing a high-risk loan (false negative) can have serious financial consequences for the bank, the model’s high recall for class 1 is particularly important. While precision could be improved for high-risk loans, the high recall ensures that very few high-risk loans are missed. This is critical in minimizing financial losses due to defaults.

### Recommendation

I recommend deploying this model for use by the company. The high recall for class 1 means the model is effective at identifying high-risk loans, which is crucial for risk mitigation in a financial institution. While precision for high-risk loans can be improved, the model’s overall performance—especially in terms of recall—makes it a reliable tool for preventing high-risk loans from being approved.

If precision for class 1 becomes a priority, further tuning (such as adjusting the decision threshold or using additional techniques like cost-sensitive learning or rebalancing the dataset) can be explored. However, given the current performance, this model is well-suited for real-world deployment in loan risk assessment.
