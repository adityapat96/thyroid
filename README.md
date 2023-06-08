This project aims to make predictions on a thyroid dataset by performing data preprocessing and running machine learning algorithms. The primary objectives are to determine if patients are susceptible to thyroid surgery, hyperthyroidism, or hypothyroidism. The final results will be discussed, and possibilities for future work on the predictions will be explored.

Dataset:

The dataset used for this project can be found at: https://www.kaggle.com/datasets/emmanuelfwerr/thyroid-disease-data.

Data Preprocessing:

The following steps were performed for data preprocessing:
1. Imputed the Sex column, replacing "t" with "1" and "f" with "0." Rows with Sex as "-1" were dropped.
2. Imputed the binary columns, replacing "t" with "1" and "f" with "0."
3. Changed the data type of the binary columns to "int."
4. Replaced "?" with "0" in the blood test measurement columns.
5. Dropped rows with age less than 18 or greater than 98.
6. Cleaned the "target" column by mapping it to thyroid diagnosis and renamed it as "diagnosis_name."
7. Divided the data into age groups and calculated average values of the 5 blood tests for each group.

First Prediction: Thyroid Surgery

Models were run using Random Oversampling and Random Undersampling techniques. The following models were employed:

Random Oversample:
1. Logistic Regression
2. Random Forest
3. Cross Validation on Random Forest
4. Neural Networks

Random Undersample:
1. Logistic Regression
2. Random Forest
3. Neural Networks

The performance of oversampled models was generally better (around 98%) compared to undersampled models.

Second Prediction: Hyperthyroidism vs Hypothyroidism

The following models were run:
1. Decision Tree Classifier
2. Random Forest
3. Logistic Regression

For overall thyroid diagnosis, Decision Tree and Random Forest achieved around 99% accuracy, while Logistic Regression had slightly lower accuracy. Similarly, for hypothyroidism conditions, Decision Tree and Random Forest achieved around 99% accuracy, with Logistic Regression performing slightly lower.

Conclusion:
1. Oversampled models generally performed better than undersampled models due to the dataset's imbalanced nature.
2. The overall diagnosis prediction achieved high accuracy, while Logistic Regression had slightly lower performance compared to tree-based models.
3. The results may be influenced by the limited features in the original dataset and the prevalence of binary labels.
4. Future work can focus on additional features related to dates, more categorical features, patient-level data, and exploring the relationship between specific blood tests and hyperthyroidism/hypothyroidism.

Future Work/Research
1. Incorporate additional features related to dates for a more comprehensive analysis.
2. Introduce more categorical features rather than relying heavily on binary labels.
3. Shift the focus to patient-level data to gain deeper insights into individual cases.
4. Investigate the relationship between specific blood tests and their significance in machine learning models for predicting hyperthyroidism or hypothyroidism.
