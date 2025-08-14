# Diabetes Detection using Machine Learning
Dataset source: You can access the dataset [here](https://drive.google.com/file/d/13G9yJZok2Z6pvBsaktHmO8hU7qFSpb7Z/view?usp=sharing)  
Pdf version: You can access the pdf [here](https://drive.google.com/file/d/13zSOIeyq_8DlUfpyRoYEhFbnfJHPEOBa/view?usp=sharing)

## Problem Statement
Diabetes cases in Indonesia have surged by 167% over the past decade, with projections reaching 28.57 million by 2045. This rapid growth poses a significant public health challenge, as late diagnosis often leads to severe complications and increased mortality. Traditional methods struggle to keep pace with the rising demand for early and accurate detection. Leveraging machine learning can transform this landscape by enabling scalable, data-driven solutions to identify high-risk individuals earlier.

Data source: https://databoks.katadata.co.id/layanan-konsumen-kesehatan/statistik/8380d72a010b4f0/jumlah-penderita-diabetes-di-indonesia-diproyeksikan-capai-2857-juta-pada-2045

## Data Overview
The dataset consists of 100,000 entries and 9 features, all of which are fully populated with no missing values. It includes a mix of numerical, binary, and categorical data types, providing comprehensive information relevant to diabetes detection

## Feature Engineering
The selected features for the model include gender, age, hypertension, heart disease, smoking history, BMI, HbA1c level, and blood glucose level (X). The target variable (Y), diabetes, was selected to train the model for classification purposes. The dataset was split into training and testing sets to evaluate the performance of the machine learning models effectively. Using an 80-20 split, 80% of the data was allocated for training, and the remaining 20% was reserved for testing.

## Modelling Overview
Three models are utilized for comparison in this analysis: Random Forest, XGBoost, and K-Nearest Neighbors (KNN). The following is a comparison of accuracy, precision, recall, and F1-score results for each model.
|Models|Accuracy|Precision|Recall|F1-Score|
|---|---|---|---|---|
|Random Forest |96.2% |97% |99% |75% |
|XGBoost |96.5% |97% |99% |77% |
|KNN |95.8% |96% |99% |73% |

## Conclusion
1. All three models (Random Forest, XGBoost, and KNN) demonstrate high accuracy, with XGBoost achieving the highest accuracy at 96.55%, followed by Random Forest at 96.22%, and KNN at 95.86%. These results show that all models are effective for diabetes classification.
2. While all models show high precision for the non-diabetic class, there is a notable tradeoff in recall for the diabetic class. XGBoost provides the best balance, with a precision of 0.93 and recall of 0.66, leading to a higher F1-score of 0.77 compared to the other models.
3. KNN has the lowest recall for diabetic cases (0.62), which suggests that it struggles more in identifying diabetes, despite performing well with non-diabetic cases. This may indicate that KNN is less suitable for imbalanced classification tasks like diabetes detection.
4. The choice of features and model selection plays a critical role in performance. XGBoost and Random Forest models, which are both ensemble-based methods, tend to outperform KNN, especially in handling complex, imbalanced datasets.
5. While all models provide strong accuracy, further tuning, such as adjusting hyperparameters or using techniques like oversampling or under-sampling for class imbalance, could improve recall for the diabetic class, especially for the KNN model.















