# ![Airline Logo](https://example.com/airline_logo.png) **Air Passenger Modeling and Forecasting**  <span style="color: #007BFF;">✈️</span>

## Introduction
Time series data are ubiquitous across various fields, including finance, meteorology, and healthcare. Understanding underlying patterns and anticipating future trends in these time series is crucial for informed decision-making. This project aims to explore several time series modeling and forecasting techniques using the dataset on the number of air passengers.

## Project Objectives
The main objective of this project is to investigate the use of time series forecasting models. More specifically, we aim to:

- <span style="color: #28A745;">Evaluate the effectiveness of Artificial Neural Networks (ANN)</span>, which can learn complex patterns and dynamically adapt to time-related data.
- <span style="color: #17A2B8;">Examine the effectiveness of LSTMs</span> for handling long temporal sequences, capturing long-term dependencies.
- <span style="color: #FFC107;">Compare the performance of ARIMA, ANN, and LSTM models</span> to determine which is best suited for our dataset.

## Exploratory Analysis
Before proceeding with modeling, an exploratory data analysis was conducted. This involved initial statistical examination and visualizations to understand the trends, seasons, and variations present in the dataset. These steps are essential for preparing the data for modeling.

## Modeling with ARIMA
### Introduction to ARIMA
The ARIMA (AutoRegressive Integrated Moving Average) model is used to model time series by capturing trends and seasonal patterns. The ARIMA approach consists of three components: the autoregressive term (AR), the integration term (I), and the moving average term (MA).

### Methodology
1. **Baseline Model:** A persistence model was used as a reference.
2. **Component Identification:** Identification of \( p \), \( d \), and \( q \) values using ACF and PACF.
3. **Model Estimation:** Grid Search method was employed to determine optimal orders.
4. **Validation and Predictions:** Display of forecasts against actual data.

### Results
After execution, the best identified model was ARIMA(12, 1, 3) with an RMSE of **16.496**. Illustrative charts show how ARIMA forecasts compare to actual data.

## Modeling with ANN
### Introduction to ANN
Artificial Neural Networks (ANN) are powerful tools for capturing nonlinear relationships in data. They learn from the data and can generalize to new information.

### Methodology
1. **Baseline Model:** A baseline ANN model was developed to evaluate performance.
2. **Model Estimation:** Grid Search method was used to determine optimal parameters, such as the number of hidden layers and neurons.
3. **Validation and Predictions:** Forecasts were evaluated against actual data.

### Results
The best ANN model was determined with **4 hidden layers** and **50 neurons**, achieving an RMSE of **22.79**. Charts illustrate the model's predictions compared to actual data.

## Modeling with LSTM
### Introduction to LSTM
Long Short-Term Memory (LSTM) networks are a variant of ANN specially designed to handle sequences of data. They can capture long-term dependencies due to their unique architecture.

### Methodology
1. **Baseline Model:** Development of a baseline LSTM model to evaluate performance.
2. **Model Estimation:** Grid Search method was used to explore different configurations.
3. **Validation and Predictions:** LSTM forecasts were validated against actual data.

### Results
The LSTM model achieved an RMSE of **26.82**, with the best parameters being **150 neurons**. Results are visualized to compare LSTM predictions with actual data.

## Model Comparison
The comparison of model performances revealed that:

- **ARIMA:** Best model with an RMSE of **16.496**, indicating strong predictive capability for time series.
- **ANN:** Although it has a higher RMSE of **22.79**, it remains significantly better than the persistence model.
- **LSTM:** Showed improvement over persistence, but with an RMSE of **26.82**, it performed overall less impressively than ARIMA.

## Conclusion
This project explored various methods for time series forecasting, highlighting the strengths and weaknesses of each. ARIMA proved to be the most effective model for our dataset, providing accurate forecasts suited to the prevailing linear trend. The results underscore the importance of choosing a modeling method that matches the specific characteristics of the data. This project paves the way for promising future applications in fields where understanding temporal trends is essential.

---

