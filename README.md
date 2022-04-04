# Deep_Learning_Challenge

The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. With my knowledge of machine learning and neural networks, I used the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
I received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:


EIN and NAME—Identification columns

APPLICATION_TYPE—Alphabet Soup application type

AFFILIATION—Affiliated sector of industry

CLASSIFICATION—Government organization classification

USE_CASE—Use case for funding

ORGANIZATION—Organization type

STATUS—Active status

INCOME_AMT—Income classification

SPECIAL_CONSIDERATIONS—Special consideration for application

ASK_AMT—Funding amount requested

IS_SUCCESSFUL—Was the money used effectively


## Step 1: Preprocess the data

I used Pandas and the Scikit-Learn’s StandardScaler() to preprocess the dataset in order to compile, train, and evaluate the neural network model later in Step 2. 


I read in the charity_data.csv to a Pandas DataFrame, and identified the following from the dataset:


What variable(s) are considered the target(s) for your model?
What variable(s) are considered the feature(s) for your model?


I dropped the EIN and NAME columns and determined the number of unique values for each column. For the columns that have more than 10 unique values, I determined the number of data points for each unique value. Using the number of data points for each unique value, I picked a cutoff point to bin "rare" categorical variables together in a new value, Other, and then checked if the binning was successful.

Finally, I useed pd.get_dummies() to encode categorical variables

## Step 2: Compile, Train, and Evaluate the Model

I used TensorFlow to design a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. I compiled, trained, and evaluated my binary classification model to calculate the model’s loss and accuracy.

I saved and exported my results to an HDF5 file called AlphabetSoupCharity.h5.


## Step 3: Optimize the Model

I created a new Jupyter Notebook file and name it AlphabetSoupCharity_Optimzation.ipynb and used TensorFlow again to optimize my model in order to achieve a target predictive accuracy higher than 75%. I optimized my model in order to achieve a target predictive accuracy higher than 75% by Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the mode such as:
-dropping more or fewer columns.
-creating more bins for rare occurrences in columns.
-increasing or decreasing the number of values for each bin.


## Step 4: Write a Report on the Neural Network Model

I provide a written report of my findings that answer the following inquiries:


What variable(s) are considered the target(s) for your model?
What variable(s) are considered to be the features for your model?
What variable(s) are neither targets nor features, and should be removed from the input data?

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take to try and increase model performance?

