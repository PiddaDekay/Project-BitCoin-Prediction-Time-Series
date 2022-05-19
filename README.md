# Project-BitcoinPredict-TimeSeries
By Mingfei M. | 
05/18/2022
## What we're going to cover
* Get time series data (the historical price of Bitcoin)
  * Load in time series data using pandas/Python's CSV module
* Format data for a time series problem
  * Creating training and test sets (the wrong way)
  * Creating training and test sets (the right way)
  * Visualizing time series data
  * Turning time series data into a supervised learning problem (windowing)
  * Preparing univariate and multivariate (more than one variable) data
* Evaluating a time series forecasting model
* Setting up a series of deep learning modelling experiments
  * Dense (fully-connected) networks
  * Sequence models (LSTM and 1D CNN)
  * Ensembling (combining multiple models together)
  * Multivariate models
  * Replicating the N-BEATS algorithm using TensorFlow layer subclassing
* Creating a modelling checkpoint to save the best performing model during training
* Making predictions (forecasts) with a time series model
* Creating prediction intervals for time series model forecasts
* Discussing two different types of uncertainty in machine learning (data uncertainty and model uncertainty)
* Demonstrating why forecasting in an open system is BS (the turkey problem)

horizon = number of timesteps to predict into future

window = number of timesteps from past used to predict horizon

 Naive model (baseline)
* 1 Dense model, horizon =1, window =7
* 2 Same as 1, horizon =1, window =30
* 3 Same as 1, horizon =7, window =30
* 4 Conv1D, horizon =1, window =7
* 5 LSTM, horizon =1, window =7
* 6 Same as 1 (but with multivariate data) , horizon =1, window =7
* 7 N-BEATs Algorithm , horizon =1, window =7
* 8 Ensemble (multiple models optimized on different functions), horizon =1, window =7
* 9 Future prediction model (model to predict future), horizon =1, window =7
* 10 Same as 1 (but with turkey data introduced), horizon =1, window =7
