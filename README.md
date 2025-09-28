# predict_calorie_expenditure
kaggle_competition

# Introduction
## Project Description
This is a data science competition project organized by kaggle. Predict calorie expenditure is the process of estimating the number of calories burned by the body during certain activities or under resting conditions. For those of you who want to see how other participants completed this competition, just access the kaggle competition page via the following link: https://www.kaggle.com/competitions/playground-series-s5e5/data

## Purpose Project
Tujuan dari project ini adalah untuk membangun model machine learning yang paling akurat untuk memprediksi pengeluaran kalori berdasarkan data aktivitas fisik dan fitur terkait lainnya. Project ini dapat membantu mengukur kebutuhan energi seseorang dan merancang program diet atau latihan secara optimal. 

# Dataset
Dataset yang digunakan untuk membangun model machine learning berformat csv ('train.csv') dan untuk dataset yang digunakan memprediksi model bernama ('test.csv'). Kedua file bisa didapatkan di halaman kaggle yang dapat diakses melalui link berikut:
https://www.kaggle.com/competitions/playground-series-s5e5/data

# Methode
## Data Preprocessing
### 1. Data Cleaning
This dataset does not have any empty data, so this stage can be skipped. This dataset has no duplicate data, and this stage can also be skipped. This dataset has some outliers, but I choose not to handle the outliers because in this case, the outliers are the values that determine the prediction output.

### 2. Transformasi Data
Standardize the numerical data after separating the train and test data to have an equal scale and to maintain the index data. This is done because the data to be predicted has a continuous index of train data and test data, so the separation of train data and test data is done earlier than data standardization.  

### 3. Encoding
The data was collected on a single categorical variable, namely the ‘Sex’ feature, which has two unique values: ‘Male’ and ‘Female’. 

## Feature Selection
Based on hypothesis testing with Spearman and Pearson, the results show that there are three variables that correlate with calorie value, called Duration (length of activity), Heart_Rate and Body_Temp. So these three variables will be used as predict variables, while caloric value will be used as the target variable. And last but not least, although the correlation cannot be measured between calorie and 'Sex', according to several sources, gender differences can affect a person's calorie requirements and expenditure.

## Model Selection
From the results of the Linear Regression model evaluation, a fairly good r2_square was obtained. Each of these values is the R2 obtained by the model on each different fold (data division). It can be seen that all of them are very high, approaching 0.95. The average R2 of all folds is 0.95, which is very consistent with the R2 of 0.95 obtained from the previous train_test_split. This shows that the model performs very well on average across various data subsets. 

Standard Deviation R2: 0.00. This is a very strong point. A standard deviation of zero (or very close to zero when rounded) indicates that the R2 generated in each cross-validation fold is very stable and consistent. The model provides nearly identical performance regardless of which data subset is used to train and evaluate it. This is a key indicator of the model's high stability and robustness.

These cross-validation results provide strong evidence that the Machine Learning model is highly stable, robust, and has exceptional predictive performance. Performance stability (R2 and RMSE) remains virtually unchanged across different data splits. In terms of robustness, the model is not overly sensitive to small variations in the training data. 


# Contact
LinkedIn: http://www.linkedin.com/in/retnoanggraeni/
Email: cc:@retnoagraeni@gmail.com




