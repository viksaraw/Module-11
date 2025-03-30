# Module-11 What drives the price of a car?
In this Module I am analyzing a data set to understand what are the parameters which impact the pricing of used cars

# OVERVIEW

A dataset is provided, it contains info for about 3 Million used cars. Goal is to understand the factors which determine the price of used cars. I need to provide recommendations to the client "a used car dealership" as what factors drive the price of used cars

# Approach
To understand the factors - I will take this is as a Machine Learning Challenge and approach it with these steps

Data Quality
	• Missing Data
	• Duplicate data
	• Outlier Analysis
	• Wrong data values - NaN, Wrong Price Values, Inf values
	• Data Type Conversion
	
EDA- Exploratory Data Analysis
	• Univariate
		○ Focus on one column at a time
	• Bivariate
		○ Relationship between columns
		○ Price should be the main focus columns
	• Correlations

Pre-processing
	• Standardization
	• Filling in the missing values

Feature Engineering
	• Year can be used to calculate the age
	• Feature Selection

Modelling                                                                                
	• Linear Regression
	• Ridge Regression
	• Lasso Regression
	
Dataset combination
	• Step 1 Numerical
	• Step 2 Numerical + Simple Categorical (one-hot encoding)
	• Step 3: Step 2 + Non-trivial categories - ordinal encoding
	
Hyperparameter Tuning
	• Alpha values for Ridge and Lasso + CV
	

