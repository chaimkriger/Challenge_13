# Venture Funding With Deep Learning
   
   In this application, I will apply my knowledge of deep learning models to predict whether an employee is likely to depart from a company.
  
Talent retention has always challenged companies. Today, the global opportunities that remote work offers employees have compounded this challenge. Losing employees can carry a great financial cost for companies. Some studies have found that replacing a full-time employee costs a company six to nine months of salary, on average. So, human resources teams that develop talent retention strategies are now including machine learning predictions to better tackle this problem.

In this application, I have been asked to generate a deep learning model. The model should predict whether an employee is likely to depart from the company within the next two years, given their current employee profile.

---

## Overview

   *Preprocessing The Data*
   
To start, I read the applicants.csv file from the Resources folder and create a DataFrame. I review the resulting DataFrame, and check the data type associated with each column to identify categorical and non-categorical variables. I create a list of the categorical variables, and use the OneHotEncoder module from scikit-learn to encode the dataset's categorical variables. I then create a new DataFrame that contains the encoded categorical variables and the numerical variables from the original dataset. 
   I use this DataFrame to create the features (X) and target (y) sets. With the features and targets now in place, I can create the training and testing sets using the train_test_split function from scikit-learn, and use scikit-learn’s StandardScaler to standardize the numerical features.
   
   *Compile and Evaluate a Binary Classification Model Using a Neural Network*
   
I create a deep neural network by assigning the number of input features, the number of layers, and the number of neurons on each layer using Tensorflow's Keras. I compile and fit the model using the "binary_crossentropy" loss functon, the "adam" optimizer, and the "accuracy" evaluation metric. I then evaluate the model using the test data to determine the model's loss and accuracy, and save and exportthe model to an HDF5 file, and name it "AlphabetSoup.h5". 
 
   *Optimize the Neural Network Model*
   
In my first model, I used an input number of 116 features, along with 58 hidden nodes in my first layer, and 29 hidden nodes in my second layer. I also used 50 epochs. The results were an accuracy score of 68%. I knew I had to optimize the neural network model to perform better, and so I created two new models.
In my second model, I kept my input features the same, but only used one hidden layer of 58 nodes, and used 100 epochs. This model gave me an accuracy score of 73%, conisderably better than my original model. For my third model, I also kept the imput features the same, but used three hidden layers, with 58, 29, and 15 nodes respectively. I also used 150 epochs. This model gave me a similer accuracy score to my second model: 72.8%.
In conclusion, I would recommend my second model to be used to predict which startups will be successful or not.


![screenshot of model 1 loss and accuracy plots](https://github.com/chaimkriger/Challenge_13/blob/main/Starter_Code/Screenshot%20(43).png)

![screenshot of model 2 loss and accuracy plots](https://github.com/chaimkriger/Challenge_13/blob/main/Starter_Code/Screenshot%20(44).png)



---

## Technologies

This project leverages Python 3.7.

---

## Installation Guide

Before running this application, Python must be installed.

---

## Usage

Simply run the code to view the three different models I have created. You can change any of the models to your preference, to see if you can get a higher accuracy score.

---

## Contributors

Just me, and a little bit of help from module 13

## License

No license, feel free to copy the code any time.











