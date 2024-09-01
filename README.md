# cancer-prediction
This project involves building and evaluating models to predict cancer diagnoses based on a dataset of 1,500 patients. The dataset includes various medical and lifestyle factors, such as genetic risk, cancer history, smoking habits, and more. The project explores both k-nearest neighbor (KNN) and logistic regression models, analyzing the impact of different features on the model's accuracy.

## Data

### Features

The dataset contains the following features:

- **Age**
- **Gender**
- **Body Mass Index (BMI)**
- **Genetic Risk**
- **Physical Activity**
- **Alcohol Intake**
- **Smoking Habits**
- **Cancer History**

### Target

- **Diagnosis**: The target variable indicating whether the patient was diagnosed with cancer.

## Methods

### Data Preprocessing

- **Feature Scaling**: Standard scaling and min-max scaling was applied to normalize the features, as applicable to each type of model.
- **Train-Test Split**: The dataset was split into 80% training and 20% validation sets.

### Model Selection

- **K-Nearest Neighbors (KNN)**: The KNN model was trained using different combinations of features. The model with k=35 yielded the best accuracy of 0.77. However, the model's inability to directly compute feature importance led to the exploration of logistic regression.
- **Logistic Regression**: Several logistic regression models were tested using different combinations of features to determine their importance. The best accuracy achieved was 0.80, with the most significant features identified as Cancer History, Genetic Risk, Gender, Smoking Habits, and Alcohol Intake.

### Feature Importance and Model Interpretation

- **KNN**: Initially, a combination of Age, Physical Activity, and Smoking Habits was used. After testing different feature sets, the combination of Genetic Risk, Alcohol Intake, and Cancer History provided better results.
- **Logistic Regression**: Feature importance was evaluated by examining the coefficients of the logistic regression model. The final model included Genetic Risk, Cancer History, Smoking, Gender, and Alcohol Intake as the most significant features.

## Results

- **Best Model**: The Logistic Regression model using Genetic Risk, Cancer History, Smoking, Gender, and Alcohol Intake achieved the highest accuracy of 0.80.
- **Feature Ranking**:
    1. Cancer History
    2. Genetic Risk
    3. Gender
    4. Smoking Habits
    5. Alcohol Intake

## Conclusion

This project demonstrates the effectiveness of both KNN and logistic regression models in predicting cancer diagnoses. Logistic regression provided better interpretability and slightly higher accuracy, making it the preferred model for this task. The analysis highlights the critical role of Cancer History and Genetic Risk in predicting cancer, along with the importance of careful feature selection.

