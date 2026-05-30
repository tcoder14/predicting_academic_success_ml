# Academic Success Prediction Using Machine Learning

## Project Overview

This project builds a machine learning model to predict the academic status of students using an academic success dataset.

The model predicts whether a student will be:

- Graduate
- Dropout
- Enrolled

This type of model can help educational institutions identify students who may be at risk of dropping out and provide support early.

---

## Dataset Description

The dataset contains student-related information such as academic background, admission details, demographic information, and economic indicators.

These features are used to predict the final academic status of a student.

## Target Variable

The target column is:

```text
Target
```

It contains three classes:

| Class | Description |
|---|---|
| Graduate | The student successfully completed the program |
| Dropout | The student left the program before completion |
| Enrolled | The student is still continuing the program |

---

## Problem Type

This is a multi-class classification problem.

That means the model predicts one class from multiple possible categories.

In this project, the model predicts one of these three classes:

```text
Graduate, Dropout, Enrolled
```

---

## Project Workflow

The machine learning workflow follows these steps:

1. Load the dataset
2. Clean unnecessary columns
3. Handle missing values
4. Separate features and target variable
5. Encode categorical values
6. Scale numerical features
7. Split the dataset into training and testing sets
8. Train multiple machine learning models
9. Compare model performance
10. Select the best model
11. Save the trained model

---

## Data Preprocessing

Before training the model, the dataset was cleaned and prepared.

The preprocessing steps were:

- Removed unnecessary unnamed columns
- Removed rows where the target value was missing
- Filled missing numerical values using the median
- Filled missing categorical values using the most frequent value
- Converted categorical columns using one-hot encoding
- Scaled numerical columns using standard scaling

These steps help the machine learning models understand the dataset properly.

---

## Models Used

Several machine learning models were tested.

The models used in this project are:

- Logistic Regression
- Linear Support Vector Machine
- Random Forest Classifier
- Gradient Boosting Classifier
- Decision Tree Classifier

---

## Model Evaluation

The models were evaluated using common classification metrics.

| Metric | Meaning |
|---|---|
| Accuracy | Measures how many total predictions were correct |
| Precision | Measures how many predicted results were actually correct |
| Recall | Measures how many actual results were correctly found |
| F1 Score | Balance between precision and recall |
| Macro F1 Score | Average F1 score across all classes |

Macro F1 Score was important because this is a multi-class classification problem.

---

## Best Model

After comparing multiple models, the best-performing model was:

```text
Linear Support Vector Machine
```

## Performance

| Model | Accuracy | Macro F1 Score |
|---|---:|---:|
| Linear SVM | 61.76% | 55.45% |

The Linear SVM model gave the best overall performance among the tested models.

---

## Result Discussion

The model achieved moderate performance.

It performed better for clearer classes such as Graduate and Dropout. However, the Enrolled class was more difficult to predict.

This is because enrolled students are still continuing their studies, so their final outcome may not be fully clear. Because of this, the model may confuse Enrolled students with Graduate or Dropout students.

---

## Conclusion

This project successfully built a machine learning model for predicting student academic success.

The dataset was cleaned, processed, and used to train multiple classification models. Among the tested models, Linear SVM achieved the best result with 61.76% accuracy and 55.45% Macro F1 Score.

The model can be used as a basic academic risk prediction system. However, the result can be improved further using better feature engineering, class balancing, hyperparameter tuning, and advanced machine learning models.

---

## Future Improvements

Possible future improvements include:

- Convert the problem into binary classification: Dropout vs Graduate
- Handle the Enrolled class separately
- Apply class balancing techniques
- Use hyperparameter tuning
- Try advanced models such as XGBoost or LightGBM
- Add more visualizations
- Build a simple web interface for prediction
