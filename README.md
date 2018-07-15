# ML Lab Projects


This is the project file of CSE476 (Machine Learning Lab). Here We are tackling two problems:

1. Apartment Price Prediction
2. Document Categorization


# Apartment Price Prediction

Problem category :

This is a regression problem where the input is a set of features of a house or apartment and the output or prediction is a continuous value representing the price of the house or apartment.

Dataset : 

The dataset we have used here is the kc_house_data. In the dataset there are 21 columns. First we analyzed the dataset and realized that some features are not making any impact on price prediction and they are 'id' and 'date'. Then we separated the 'price' column as this is our target and assigned to another array. After that we saw that different features are in different range. So we had to scale all the features with min-max scaling. The transformation is :

X_std = (X - X.min(axis=0)) / (X.max(axis=0) - X.min(axis=0))
X_scaled = X_std * (max - min) + min

where min, max = feature_range

We defined min=0, max=1 and as a result all the feature values were in the same range of 0 to 1. 

These are all the preprocesses we did with the data. 

Training :

In the 'Apartment Price Prediction' folder there are 2 notebook one is for training the dataset in neural network using tensorflow and the other one is for training the dataset in different Regression algorithm of Scikit-learn. We used Linear Regressor, Gradient Boosting Regression, Random Forest Regressor, Decision Tree Regressor and Support Vector Regressor. All the accuracy are:

Linear Regressor : 68.7%

Gradient Boosting Regression : 90.2%

Random Forest Regressor : 86.1%

Decision Tree Regressor : 68.4%

Support Vector Regressor : 33.8%

For the neural network we get the mean squared error(mse) of test data :0.000395173






# Document Categorization

Problem Category :

This is a classification problem where the input is a stream of strings and the output or prediction is a discrete value representing a category. 

Dataset :  

The dataset has 12 folders representing 12 different category and in each folder there are a bunch of .txt files. Each .txt file represents one data and that is a single news of that category. The news is in Bangla Language. We counted the occurrences of different words and mapped each unique word to an integer number and made a dictionary. Then we use the dictionary as our input data.

Training :

In the 'Document Categorization' folder there are 2 notebook one is for training the dataset in neural network using tensorflow and the other one is for training the dataset in different Classification algorithm of Scikit-learn. We used Multinomial Naive bayes Classifier, Decision Tree Classifier and Support Vector Classifier. All the accuracy are:

Multinomial Naive Bayes : 49.4%
 
Decision Tree Classifier : 57.9%

Support Vector Classifier : 67.9%  

Neural network (loss) : 0.277781004   


As this in Bangla we couldn't preproccess the data properly like stemming and removing articles and as a result the accuracy isn’t good. 




