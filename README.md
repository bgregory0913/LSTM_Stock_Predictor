<h3 align="center">Python: LSTM (Long Short-Term Memory) Stock Predictor</h3>
<p align="center">
  <a href="https://github.com/bgregory0913/LTSM_Stock_Predictor">
    <img src="btc.jpg" alt="bitcoin" align="center">
  </a>
</p>

## Project Overview:

LSTM (Long Short-Term Memory) is a recurrent neural network (RNN) used in deep learning. Unlike standard neural networks, LSTM has feedback connections and can process single data points as well as entire sequences of data (such as text, audio, images or video).

In this example, LSTM is applied to to make bitcoin market close price predictions; one model using historical close prices ad another model using the [Fear & Greed Index](https://alternative.me/crypto/fear-and-greed-index/)

* Steps:
    * Prepare the data by reading the csv files into Pandas DataFrames.
    * Preprocess the data.
    * Split the dataset into train and test datasets
        * In both models, 70% of the data is allocated for training and 30% of the data for testing.
    * Convert features into NumPy arrays
        * Reshape the arrays to be accepted by the LSTM model
    * Build the architecture for LSTM network
    * Compile the model and fit to the training data.
    * Evaluate the performance of model with the test data.


### Model Performance Observations:
* Which model had a lower loss?
    * The model evaluating closing prices and not FNG values had a significantly lower loss
* Which model tracks the actual values better over time?
    * If you fully expand the results DataFrame, you can see that the non-FNG script has the closest predicted values day-to-day.
* Which window size works best for the model?
    * To evaluate both models the same, the input parameters for both need to be the same. With 10 windows this allowed the closing price predictor model the best predictions but did not perform so well for FNG. If increased or decreased, both models performaed less efficiently.


## Built With:

* [Python](https://www.python.org/)
* [JupyterNotebook](https://jupyter.org/)
* [Pandas](https://pandas.pydata.org/)
* [NumPy](https://numpy.org/)
* [TensorFlow](https://www.tensorflow.org/)
* [SciKit-Learn](https://scikit-learn.org/stable/)


## Contact:
Blake Gregory - [LinkedIn](www.linkedin.com/in/blake-greg) - blake.gregory@tilineum.com