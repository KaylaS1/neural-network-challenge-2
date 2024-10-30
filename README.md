# Week 19 Kala Neural Network Challenge 2 - Predict Employee Attrition and Department

### Step 1: Preprocessing of data
* Read the input CSV file.
* Target columns are "Attrition" and "Department".
* Picked 12 columns for X dataframe and converted "Overtime" feature into numeric.
* Split input data into train and test.
* Used Standard Scalar to scale data.
* Used OneHotEncoder to encode target columns.

### Step 2: Create the model
* Create a branched neural network using TensorFlow's Keras.
* Model has 2 shared hidden layers and an additional hidden layer for each output layer.
* Model was compiled and fit with training data using 100 epochs.
* Model was evaluated using the testing data.
* Model returned an accuracy score of 81.2% for Attrition and 51.9% for Department.

### Step 4 Questions and Answers:
1. **Is accuracy the best metric to use on this data? Why or why not?**
* I think accuracy is a good metric to start with for this data, because we are predicting classification for Department and Attrition. But because the input data is skewed (see #3 below), other metrics like F1-Score, Precision, Recall, MultiClassConfusionMatrixPlot, etc. may also be useful.

2. **What activation functions did you choose for your output layers, and why?**
* I chose "softmax" activation function for Department output layer, because there were 3 values for Department - (a) Research & Development, (b) Sales, and (c) Human Resources. I chose "sigmoid" activation function for Attrition output layer, because there were only 2 possible values for Attrition - a binary classification of Yes or No.

3. **Can you name a few ways that this model might be improved?**
* Obtain additional data that would help predict Department better, for example, college major, professional certifications, etc. Also input data was very skewed with respect to Department, only 63 rows or 4% of data was for Department Human Resources, 446 rows or 30% for Sales, and remaining 66% of rows were Department R&D. The model might predict better with more data rows for HR and Sales Departments.
 
### Sources of code
* Most of my code is based on code provided in starter code file and in exercises by the AI Bootcamp.