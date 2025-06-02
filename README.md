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

## Feature Selection
Based on hypothesis testing with Spearman and Pearson, the results show that there are three variables that correlate with calorie value, namely Duration (length of activity), Heart_Rate and Body_Temp. So these three variables will be used as predict variables, while caloric value will be used as the target variable.

## Model Selection
Of the two models built, namely Linear Regression and Random Forest Regression, I chose to use the Random Forest Regression Model to predict the test data. This is because the model evaluation results show that Random Forest Regression has a better model evaluation value even though from the scatter plot results Linear Regression is more fit than Random Forest Regression. This is because my main focus is to get prediction results that are closer to the train data. The MSE is lower (0.03256 vs. 0.04982), which means the prediction is more accurate and closer to the actual data. The R-squared is also higher in Random Forest (0.9674 vs. 0.9502), indicating this model is able to explain more of the data variance.

# Contact
LinkedIn: http://www.linkedin.com/in/retnoanggraeni/
Email: cc:@retnoagraeni@gmail.com




