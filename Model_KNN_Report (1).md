# Évaluation du Modèle de Régression Logistique

## Reasoning

To evaluate the quality of the logistic regression model, I need to
split the data into training and testing sets, train the model, make
predictions, and then calculate and display evaluation metrics such as
the confusion matrix, classification report, and ROC AUC score.

------------------------------------------------------------------------

# Prepare Data for Modeling

## Subtask

Separate features (`X`) from the target (`y`).\
Split the data into training and testing sets, ensuring stratification
on the `'defaut'` column.\
Apply `StandardScaler` to the features, fitting it on the training data
and transforming both the training and test sets.

------------------------------------------------------------------------

# Train and Optimize KNN Model

## Subtask

-   Train a simple KNN model (`K=5`) on the scaled data.\
-   Define a pipeline combining `StandardScaler` and
    `KNeighborsClassifier`.\
-   Implement `GridSearchCV` to optimize the `K` hyperparameter (1--20),
    using recall as scoring metric with 5-fold cross-validation.\
-   Display the best parameters and best recall score.

------------------------------------------------------------------------

# Evaluate Model Performance and Calculate ROI

## Performance Metrics

-   Recall (default class): **58%**
-   Precision: **75%**
-   F1-score: **65%**
-   ROC AUC: **0.78**
-   Accuracy: **94%**

### Confusion Matrix

-   TN: 263\
-   FP: 6\
-   FN: 13\
-   TP: 18

------------------------------------------------------------------------

# Return on Investment (ROI)

## Business Assumptions

-   Cost of False Positive: €1,000\
-   Cost of False Negative: €250,000

## Financial Results

-   Total Model Cost: €3,256,000\
-   Potential Loss Without Model: €7,750,000\
-   Savings: €4,494,000\
-   ROI: **138.02%**

------------------------------------------------------------------------

# Final Recommendation

-   ✅ Deploy the KNN model (`K=1`)\
-   🔍 Focus on reducing False Negatives\
-   🔄 Monitor and retrain regularly\
-   📊 Align threshold decisions with financial risk strategy
