# Covid-Affects
This project is based on Machine Learning classification of Data in-order to predict the death toll in each county on a daily basis.
To archive this we will be using Python's most popular libraries.
# Step One : Importing Libraries
1. We'll be importing the Numpy library (*for linear algebra*) and Pandas library (*for data processing*).
2. Import sklearn's model selection,which will apply in the later process when we split the data to Train and Test.
3. Import sklearn's linear_model,the purpose of this is to minimize the residual sum of squares between the target variables and the targets predicted by the linear.
# Step Two : Data Cleaning and Exploration
1. We use the DataFrame to read the excel file,which contains 10000 rows x 50 columns
2. From the continent column,we replace : 
- 'Asia' : 0
- 'Europe' : 1
- 'North America' : 2
- 'Africa' : 3
- 'South America' : 4 
- 'Oceania' : 5
3. We fill the null/missing values with mean values using the *fillna* function.
4. Before proceeding to model training,we drop all the unnecessary columns we not going to use.
# Step Three : Model Training
1. We set *df['total_death']* as our target variable (*as our main goal is to predict the number of death toll*)
2. Import the xgboost regressor,this is a decision-tree based supervised learning algorithm that uses a gradient boosting framework.
3. Training the model,we'll split test 20% of the data and set our *random_state=0*

# Prediction Results
After training our model,we got an accuracy score of 99% 
