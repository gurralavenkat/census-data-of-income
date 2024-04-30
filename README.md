# census-data-of-income
first import all tthe libraries 
pandas , numpy , matplotlib, sklearn, 
imblearn ( handle imbalanced dataset )

next load the data set read.csv 

next handle the missing values 
replace ? with nan whether the ? are present in the data are replaced 

next preprocessing 
 categorical variables are encoded into numerical so we use LABEL ENCODER 
from sklearn preprocessing the data of categorical columns are fitted and tranformed to label encoder 

next 
split the data into x and y where x is features and y is target 
x contains all colums except income 
y contain only income 

handle the class imbalance with oversampling 
technique: RANDOM OVER SAMPLER  from imblern 
used to balance the class distribution 
It generates samples for the minority class (in this case, individuals earning '>50K') to match the number of samples in the majority class


split resampled data into train and test sets 
the oversampled data - x and y is split into training (x-train and  y-train )
and testing (x-test and y-test ) using (train test split   from sklearn )

scale features 
x train and y tarin are scaled using standard scaler from the sklearn preprocessing 
step standardizes the data to have zero mean and unit variance, which can improve model performance, especially for algorithms sensitive to feature scaling

model - training 
 Random Forest
 XGBoost ( pip install xgboost ) 
 Naive Bayes
 Logistic Regression
 Decision Tree
 K-Nearest Neighbors
 Support Vector Machine
defined and trained using the scaled training data (X-train scaled, y-train). Each trained model is evaluated on the scaled test data (X-test-scaled, y-test) using accuracy score

visualisation 
seaborn and matplotlib
 
distribution of income  we made a plot using seaborn to distinguish the salary >50k and <=50k
second plot (heatmap) shows how different features in our data are related to each other.



