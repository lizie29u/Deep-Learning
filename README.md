# Deep-Learning

In this project, we used deep learning recurrent neural networks to create two  models to predict bitcoin closing prices. One model used the FNG indicators the other model will use a window of closing prices to predict the nth closing price.

The initial model was run using various differnt window size. In the end we chose to use a rolling  10 day window to predict the 11th day closing price.  For comparative purposes, this will be the same for both models

## Data Preparation
* (1) Load csv files into separate pandas dataframes 
* (2) Join both dataframes to create a single dataframe. 
* (3) Split data into training (70%) and testing (30%)
* (4) Scale data using MinMax Scalar
* (5) Reshape data.

## Build and Train the LSTM RNN
Using Tensorflow we built the model using 3 layers, 30 neurons in each layer and a 20% dropout between each layer. The optimizer used was "adam" and loss was measured using "mean_squared_error". 
We trained the model using 10 epochs and a batch size of 1

## Model evaluation

The model with the lower loss was the model using the closing prices to predict


![loss](images/loss.PNG)


As per below plot, the closing prices model, tracks the actual values better over time.

![predictions](images/fng.PNG)

![predictions](images/closing_prices.PNG)

We experimented with window sizes of 5, 6, 8 and 10.  The window size of 10 seemed to give the best performance.
.




