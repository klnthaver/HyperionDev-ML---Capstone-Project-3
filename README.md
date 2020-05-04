# HyperionDev-ML---Capstone-Project-3
A machine learning project developing sentiment analysis on the imdb dataset.

The IMDB dataset is a popular dataset for use in introductory Sentiment Analysis exercises and development. This project aims to build a Recursive Neural Network in order to perform sentiment analysis with the IMDB dataset. 

The required packages for this python project are numpy, matplotlib and tensorflow. There are a number of variables that are configured for the model such as maximum review length and vocabulary limits as well as neural network specific parameters such as solvers and loss functions. The data was imported and interpreted in order to understand the nature of the data being used. Each review is represented by a list of numbers that are mapped to letters by a dictionary. One of the tasks performed in the project is to create functions that can convert the list back to a review and vice versa.

The data is then converted to an array and padded or truncated to a length of 500. The model architecture itself is only 4 layers; an embedding layer (to allow the neural network to work with text input as integers), a recursive LSTM layer, a regular LSTM layer and the Dense output layer. The model is then compiled and trained on the training data and validated on the testing data. Three epochs were enough to get reasonable results from the predictions on the model (extending the epochs to ten made no observable difference to the performance of the model).

The model was then evaluated on the test dataset and the Loss was 0.404 and the Accuracy was 84.77%. The final test of the model is using it to take new reviews and evaluate the sentiment of those reviews. Short examples were used as short reviews are more difficult to evaluate due to lower amounts of data and this will allow the easier identification of weak points in the neural network.

The model gives reasonably good understanding of the sentiment of the chosen reviews even though the reviews were deliberately chosen to be difficult to interpret (but with simple language). The main issue with the prediction of the model is that negatives are not handled consistently 'not good' is correctly identified as negative however 'not bad' is not identified as positive and 'not great' is not identified as negative.
