# Energy_forecasting_LSTM

Energy forecasting model that uses renewable energy data from 6 years to forecast and predict. 
Uses Long Short term Memory Neural Network model
Impleneted using Pytorch

## Base Model
The base model we use to evaluate and understand the different post-processing techniques is an LSTM-RNN, which stands for Long Short Term Memory Recurrent Neural Network. It is commonly employed in renewable energy forecasting, as the field requires data to be considered from not just recent occurrences but also past occurrences. 
These models are highly effective for data forecasting due to their ability to capture complex time-based dependencies in sequential data. In the context of forecasting, LSTM RNNs are typically trained on historical time series data, where each data point is associated with a timestamp. During training, the network learns to analyse the sequential patterns and correlations present in the data, encoding them into the memory cells of the LSTM units. These memory cells have mechanisms, such as input, output, and forget gates, which enable them to selectively retain or discard information over time. Multiple studies have used LSTM models to predict time-based data sequences, as follows. 

Our LSTM model consists of one hidden layer and a dense output layer, and initially, we trained it on a sigmoid activation function with an AdaM (Adaptive Moment Estimation) optimizer. The data was scaled for faster processing, and the GHI was limited to values above 150,  to track readable values of irradiance only and reduce the variance. 

The LSTM file shows the initial version of the model used for preliminary results, the RNN_LSTM file shows the final version of the model, which is used to track daily avg GHI values of a 50 day ahead cycle. It also uses Model output Statistics to quantify the reuslts and a scatterplot for better visual representation. 

Our training data consists of 10 years of hourly measured Solar energy data, including the Global horizontal irradiance (GHI) and 2m Temperature, which records the temperature just 2m above the sensor. 


