Project Summary: Time Series Forecasting
This project analyzes seasonality data from the "whse_retail_Data.csv" dataset using various time series and machine learning models to forecast sales for 'BEER', 'LIQUOR', and 'WINE' item types.

Tech Stack 
Python: The primary programming language used.

Libraries
pandas: For data loading, manipulation, and preprocessing.

numpy: For numerical operations.

matplotlib and seaborn: For data visualization (ACF and PACF plots).

Prophet: A time series forecasting model developed by Facebook.

statsmodels: For implementing ARIMA and SARIMA models.

sklearn: For data splitting, scaling (MinMaxScaler), and evaluation metrics (Mean Absolute Error, Mean Squared Error). Also used for Random Forest and GridSearchCV.

tensorflow and keras: For building and training the LSTM model.

xgboost: For implementing the XGBoost model.

Code Summary Steps
Data Loading and Preparation: Loaded the whse_retail_Data.csv file, created a datetime column (ds), and combined sales and transfers into a target variable (y).

Prophet Model (Original Data): Trained and evaluated a Prophet model on the original dataset to establish a baseline.

Error Analysis: Analyzed large errors from the initial Prophet model, focusing on identifying contributing data points in the 'WINE' category.

Prophet Model (Filtered Data): Created a filtered dataset by excluding identified outliers and trained and evaluated a Prophet model on this filtered data.
Time Series Model Comparison (ARIMA, SARIMA, LSTM): Prepared data for ARIMA, SARIMA, and LSTM models, trained them, and evaluated their performance, comparing the metrics. Data was resampled to a monthly frequency for these models.

Machine Learning Model Comparison (Random Forest, XGBoost): Prepared data for Random Forest and XGBoost by creating time-based and lagged features, trained these models, and evaluated their performance.

Hyperparameter Tuning: Performed hyperparameter tuning using GridSearchCV for Random Forest and XGBoost models to find optimal parameters.
Model Evaluation and Comparison: Calculated and compared the Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) for all trained models (Prophet on original and filtered data, ARIMA, SARIMA, LSTM, initial Random Forest, initial XGBoost, tuned Random Forest, and tuned XGBoost).

Best Model Scores
Based on the Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) metrics evaluated in this analysis, the Prophet model trained on the original, unfiltered data demonstrated the best performance.

Prophet (Original Data) Mean Absolute Error (MAE): 65.20
Prophet (Original Data) Root Mean Squared Error (RMSE): 269.34
These results indicate that the Prophet model was most effective in capturing the patterns and seasonality in the overall dataset for forecasting the combined sales of 'BEER', 'LIQUOR', and 'WINE'.
