# Report

## Background

The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. With the knowledge of machine learning and neural networks, using the features in the provided dataset it is anticipated to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.


## Data pre-processing

1. The first step in building the project is to import all necessary dependancies needed. The imported dependencies are:

* sklearn
* pandas
* tensorflow
* keras_tuner

2. Read the csv file - charity_data.csv and drop unnecessary columns 'EIN','NAME'.
3. Determine the number of unique values in each categorical column
4. The column 'APPLICATION_TYPE' contains 17 distinct values. We chose a cut-off value of 250 and replaced all value counts below that to 'Others' category, thus distinct values dropped to 9
5. The column 'CLASSIFICATION' contains 71 distinct values. We chose a cut-off value of 1000 and replaced all value counts below that to 'Others' category, thus distinct values dropped to 6
6. Using get_dummies function, converted all categorical data to numeric

## Building the model

1. Split preprocessed data into features and target arrays. y = 'IS_SUCCESSFUL', X = all other columns except y
2. Split the preprocessed data into a training and testing dataset
3. Create a StandardScaler instances
4. Fit the StandardScaler and scale the data
5. Compile, Train and Evaluate the Model
6. Use deep neural network model and initialise the Sequential class
7. Add two hidden layers using activation 'relu' and adding 44 and 30 neurons in each layer respectively
8. Define output layer using sigmoid activation function
9. Compile the model using loss="binary_crossentropy", optimizer="adam", metrics=["accuracy"]
10. Train the model and create a callback that saves the model's weights every 5 epochs
11. Evaluate the model using the test data. The results were as follows:
Loss: 0.5516025424003601, Accuracy: 0.7264139652252197
12. Export the model to HDF5 file

## Model optimisation

In Jupyter notebook 'AlphabetSoupCharity_Optimization' there are 3 additional models created attempting to optimise the model accuracy. The optimisation was targeted making the following amendments to the original model:

* Reduced the number of features in 'CLASSIFICATION' column to 4, assigning the values below 3000 to others. 
* Increased and decreased number of hidden layers 
* Increased and decreased number of neurons
* Changed activation functions
  

## Results and conclusion

The accuracy achieved was around 73%. Unfortunately, the model accuracy has not increased substantially following the optimisation. The tuning of the model by adjusting the neuron size and hidden layers are not contributing to the overall accuracy improvement. Most likely, a significant reduction of dataset might help to achieve the accuracy, however the reduction of dataset also leads to losing some important information. Otherwise, it is suggested to try to use different classification models, for example, RF classifier as an alternative.


