Machine Learning Predictions for Thyroid Data Analysis

Project Goal:

Make predictions on a thyroid dataset, which includes data preprocessing and running machine learning algorithms.
Understand if patients are susceptible to a thyroid surgery, hyperthyroidism, or hypothyroidism.
Conclude the final results and discuss possibilities of future work for the predictions.
Project Details:

Dataset: https://www.kaggle.com/datasets/emmanuelfwerr/thyroid-disease-data
Data Preprocessing
First Prediction: Predict if patients will be undergoing thyroid surgery based on their blood work
Second Prediction: Predict if patients could be diagnosed with a hyperthyroid or hypothyroid condition
Background: Thyroid:

The thyroid is a small butterfly-shaped gland located in the front of the neck. This gland creates and produces hormones that control the way the body uses energy, especially metabolism. When the thyroid gland doesn't work properly, it can impact the the entire body. If the body makes too much thyroid hormone, one can develop a condition called hyperthyroidism. If the body makes too little thyroid hormone, then the condition is called hypothyroidism.

The 5 Blood Tests:

TSH: This blood test measures the Thyroid Stimulating Hormone (TSH). Having problems with the thyroid gland is dependent on whether the TSH levels are too high or low.
T3: This blood test measures the active form of Triiodothyronine (T3), a hormone that regulates metabolism and ensures the body can perform essential functions properly. Usually T3 is bound to protein in the bloodstream, but some of this is unbound or free.
TT4: The thyroxine (TT4), also known as T4, is a hormone produced by the thyroid gland. This hormone plays a role in several of the body’s functions, including growth and metabolism.
FTI: The free T4 index (FTI) is used to diagnose thyroid disorders. In this blood test, a calculation from the TT4 results and the T3 uptake test is performed to understand the evaluation of the thyroid function. It checks only for the “free” form which is the form not bonded with any protein.
TBG: Thyroxine Binding Globulin (TBG) is a protein that’s measures to check how much it moves the thyroid hormone throughout the body.
Data Preprocessing:

Imputed the Sex column to have “t” to “1” and “f’ to “0.” Dropped rows where Sex was “-1.”
Imputed the binary columns to have “t” be “1” and “f” be “0.”
Changed the datatype for the binary columns to “int.”
For the blood tests measurement columns, wherever there was a “?,” this was changed to represent them as “0.”
Since the age range focus is between 18-98, any rows that had age of less than 18 and more than 98 were dropped.
Cleaned the “target” column to map this based on thyroid diagnosis and changed the column name to “diagnosis_name.” More on this for the second prediction.
Divided each age group based on age ranges. This will showcase the average values of the 5 blood tests based on each age group.
First Prediction:

Models run on Random Oversample:

Logistic Regression
Random Forest
Cross Validation on Random Forest
Neural Networks
Models run on Random Undersample:

Logistic Regression
Random Forest
Neural Networks
Second Prediction:

Models run:

Decision Tree Classifier
Random Forest
Logistic Regression
Models run on hypothyroidism:

Decision Tree Classifier
Random Forest
Logistic Regression
Conclusion:

First prediction:

While Logistic Regression, Random Forest, and Neural Networks was conducted straightforwardly, the Cross Validation of Random Forest was done using the KFolds method.
While the oversample had a better performance across most models (around 98%), the undersample performances were much lower compared to the oversample.
Second Prediction:

For the overall thyroid diagnosis, while Decision Tree and Random Forest come to about 99%, Logistic Regression is a little lower compared to the two.
Similar to the overall diagnosis focus, for the hypothyroidism conditions, while Decision Tree and Random Forest also come to about 99%, Logistic Regression is a little lower compared to the two.
Overall, because this dataset was mostly imbalanced, the model results may be a bit misleading due to not having enough features in the original data set. In addition, because most of the columns were binary labels from the beginning, this could also play a factor in the results of the models.

Future work/Research

Additional features pertaining to dates
Having more categorical features vs binary
Focus more on patient level data
Understand the relationship of certain blood tests with hyperthyroidism or hypothyroidism and how that plays a significant role in machine learning
