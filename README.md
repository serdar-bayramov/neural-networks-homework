# Neural-networks-homework

## Background

The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. With the knowledge of machine learning and neural networks, using the features in the provided dataset it is anticipated to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

### Step 1: Preprocess the data

Using the `StandardScaler()`, preprocess the dataset in order to compile, train, and evaluate the neural network model
1. Read in the charity_data.csv to a Pandas DataFrame, and identify the following in your dataset:
  * What variable(s) are considered the target(s) for your model?
  * What variable(s) are considered the feature(s) for your model?
2. Drop the `EIN` and `NAME` columns.
3. Determine the number of unique values for each column.
4. For those columns that have more than 10 unique values, determine the number of data points for each unique value.
6. Use the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, `Other`, and then check if the binning was successful.
7. Use `pd.get_dummies()` to encode categorical variables

### Step 2: Compile, Train, and Evaluate the Model

Design a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup funded organization will be successful based on the features in the dataset. Identify how many inputs there are before determining the number of neurons and layers in your model.
 
1. Once completed that step, compile, train, and evaluate the binary classification model to calculate the model's loss and accuracy.
2. Create a neural network model by assigning the number of 
input features and nodes for each layer using Tensorflow Keras.
3. Create the first hidden layer and choose an appropriate activation function.
4. If necessary, add a second hidden layer with an appropriate activation function.
5. Create an output layer with an appropriate activation function.
6. Check the structure of the model.
7. Compile and train the model.
8. Create a callback that saves the model's weights every 5 epochs.
9. Evaluate the model using the test data to determine the loss and accuracy.
10. Save and export your results to an HDF5 file, and name it `AlphabetSoupCharity.h5`.

### Step 3: Optimize the Model

Optimize your model in order to achieve a target predictive accuracy higher than 75%. If you can't achieve an accuracy higher than 75%, make at least three attempts to do so.

Optimize the model in order to achieve a target predictive accuracy higher than 75% by using any or all of the following:

* Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as:
  * Dropping more or fewer columns.	
  * Creating more bins for rare occurrences in columns.
  * Increasing or decreasing the number of values for each bin.
* Adding more neurons to a hidden layer.
* Adding more hidden layers.
* Using different activation functions for the hidden layers.
* Adding or reducing the number of epochs to the training regimen.
