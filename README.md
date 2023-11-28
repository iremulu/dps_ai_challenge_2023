# dps_ai_challenge_2023
Digital Product School Batch #21 AI Challenge

This is the Digital Product School AI Challenge, forecasting the number of accidents in January 2021 using Facebook's model Prophet. Some other popular forecasting models (LSTM, ARIMA, SARIMAX) are also used but the Prophet worked a lot better with this type of time series (or I couldn't manage to predict with the rest :)). 

**Dependencies with Recommended Versions**

Versions:
- pandas == 1.1.3
- numpy == 1.24.4
- matplotlib == 3.3.2
- sns == 0.11.0
- optuna == 3.4.0
- prophet == 1.1.5
  
I also imported Optuna to optimize hyperparameters, but I did not use it with this model, I believe I optimized it with experiments. You may use it, I like how it optimizes parameters. 

Note: You may need to update your numpy after you install Prophet.

**Visualizations and Descriptions**
The given data should be filtered before plotting. I filtered it to use only the needed columns and limited the year info until the end of 2020. 

The given figure is a bar plot that illustrates 'Number of Accidents by Categories Over Years':

<img width="464" alt="image" src="https://github.com/iremulu/dps_ai_challenge_2023/assets/78342399/f747bee8-0e36-4445-88f2-35bc689a9252">

The given month and year information is transformed to a better date version as 2000-01-01, I filtered the data again with the specific prediction options. 

The figure shows the time series data of the desired (to be predicted) accident category and type:
<img width="482" alt="image" src="https://github.com/iremulu/dps_ai_challenge_2023/assets/78342399/0f7f90bd-b207-4353-851d-fde863685a03">

I optimized the model parameters by experiment but I recommended an optimization method in the 'Dependencies with Recommended Versions' section. Prophet by Facebook is used in this project, it predicts the seasonality and trend of this data perfectly. I tried forecasting using other models too but I couldn't catch the trend of the data. (Especially with the LSTM versions, I may complicated the problem so much that I couldn't solve it.)

The following figure represents the forecast using the Prophet:

<img width="369" alt="image" src="https://github.com/iremulu/dps_ai_challenge_2023/assets/78342399/a2e29390-eadb-4fa0-8eda-a17d36e2e58d">

Finally, the actual data and the predicted one is given in the figure below:

<img width="363" alt="image" src="https://github.com/iremulu/dps_ai_challenge_2023/assets/78342399/d5e568ce-f3a1-48ec-9e61-1855de727ab6">

