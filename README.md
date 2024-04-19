### SC1015-Team-8

# ABOUT <br>
This is a Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence). We focused on the USA for our project, utilising the 2020 Behavioral Risk Factor Surveillance System (BRFSS) Survey Data. We also referred to the LLCP 2020 Codebook Report for a detailed description of the dataset.

# PROBLEM DEFINITION  <br>
With the prevalence of diabetes, our project's problem definition focuses on utilising machine learning methods to forecast the causal factors contributing to the rise in diabetes. By doing so, we aim to empower health professionals, government entities, and individuals with the knowledge needed to proactively prevent diabetes onset. 

# EXPLORATORY DATA ANALYSIS <br>
For exploratory data analysis, we plotted bar charts for visual representation and calculated various coefficients to determine which variables are to be used in our machine learning models. 
- Point-Biserial Correlation was used to measure correlation of numerical variables with DIABETES. 
- Rank-Biserial Correlation was used to measure correlation of ordinal variables with DIABETES. 
- Phi Coefficient was used to measure the correlation of dichotomous variables with DIABETES.

# MACHINE LEARNING MODELS USED <br>
- Random forest <br>
- Support vector machine (SVM) <br>
- Logistic regression <br>

We also performed Synthetic Minority Over-sampling Technique (SMOTE) to address the class imbalance problem when using these models. <br>

# CONCLUSION <br>
- We recommend using random forest. 
In general, this model aggregates the outputs of multiple decision trees to make predictions, making it robust to outliers, suitable for non-linear data, and less prone to overfitting. It also performs efficiently on large datasets and often achieves higher accuracy as opposed to other classification algorithms.

This is evident when comparing it to other algorithms like Support Vector Machine (SVM) and Logistic Regression, as it consistently achieves higher scores for accuracy, mean AUC, and mean F1 score. This indicates that it is the best-performing model among the three, striking a balance between precision and recall.

One issue we found with our random forest model was its high false negative rate of 0.40 and an accuracy of around 70%. We suspect this may be due to our use of SMOTE (Synthetic Minority Over-sampling Technique) to address the under-represented minority class. We believe this contributed to a low F1 score in our initial random forest model without using SMOTE. While SMOTE is intended to balance the class distribution, it may not have perfectly over-sampled the minority class.

To remedy the limited effectiveness of the current model, perhaps future implementations can try to use other methods when handling the under-represented classes such as by under-sampling the majority class instead.


# WHAT DID WE LEARN FROM THIS PROJECT? <br>
- How and when to calculate the Point-Biserial Correlation, Rank-Biserial Correlation, and Phi Coefficients
- How to deal with an imbalanced dataset using SMOTE
- How to use grid search to tune the hyperparameters
- How to evaluate its performance by conducting 5-fold cross-validation
- How to implement machine learning models such as random forest, SVM, and logistic regression


# INDIVIDUAL CONTRIBUTIONS <br>
Data cleaning - Group <br>
EDA - bar-plotting - Timothy <br>
EDA - rank-biserial correlation, point-biserial correlation, phi coefficient calculations - Ziying <br>
ML - random forest & SMOTE - Angelina <br>
ML - SVM - Ziying <br>
ML - logistic regression - Timothy <br>
Slides, video production, script - Group <br>



# REFERENCES <br>
Emre, A. (2022, January 4). BRFSS 2020 survey data. Kaggle. https://www.kaggle.com/datasets/aemreusta/brfss-2020-survey-data <br>

Behavioral Risk Factor Surveillance System. (2021, August 6). LLCP 2020 Codebook Report. https://www.cdc.gov/brfss/annual_data/2020/pdf/codebook20_llcp-v2-508.pdf <br>

Saeedi, P., Petersohn, I., Salpea, P., Malanda, B., Karuranga, S., Unwin, N., Colagiuri, S., Guariguata, L., Motala, A. A., Ogurtsova, K., Shaw, J. E., Bright, D., Williams, R., & IDF Diabetes Atlas Committee. (n.d.). Global and regional diabetes prevalence estimates for 2019 and projections for 2030 and 2045: Results from the International Diabetes Federation Diabetes Atlas, 9th edition. Diabetes research and clinical practice. https://pubmed.ncbi.nlm.nih.gov/31518657/ <br>

