# Group-9-Traffic-Volume-Prediction-Using-regression
1-Aditya Kanaujiya(202401100300015)
2-Aanjneya Nayak(202401100300001)
3-Anushka Rajput(202401100300059)
4-Arpit(202401100300065)
5-Ankit Singh Yadav(202401100300050)

Predicting Metro Interstate Traffic Volume Using Weather and Time Data

1. Problem Statement
The goal of this project is to build a machine learning model that can accurately predict the volume of traffic on the Metro Interstate based on weather conditions and time-related features. Accurate traffic prediction can help city planners, commuters, and authorities make informed decisions, manage congestion, and improve road safety.

2. Dataset Overview
Source: Kaggle: Metro Interstate Traffic Volume

Key Columns:

date_time: Timestamp of the observation

traffic_volume: Number of cars passing by the station in an hour

Weather-related columns: temp, rain_1h, snow_1h, clouds_all, weather_main, weather_description

holiday: Indicates if the day is a holiday

3. Methodology
A. Data Preparation and Feature Engineering
Datetime Conversion:
The date_time column is converted to a datetime object to extract time-based features.

Feature Extraction:
New columns are created for year, month, day, hour, and weekday, capturing temporal patterns in traffic.

One-Hot Encoding:
Categorical features (weather_main, weather_description, holiday) are converted into numeric format using one-hot encoding.

Feature Selection:
All relevant features except date_time and traffic_volume are used as inputs (X), while traffic_volume is the target (y).

B. Model Building
Algorithm Used:
Random Forest Regression is chosen for its ability to handle non-linear relationships and interactions between features.

Data Splitting:
The dataset is split into training (80%) and testing (20%) sets to evaluate model performance on unseen data.

Model Training:
The Random Forest model is trained on the training set.

C. Model Evaluation
Predictions:
The trained model predicts traffic volume for the test set.

Metrics:

Mean Squared Error (MSE): Measures the average squared difference between actual and predicted values (lower is better).

R-squared (R²): Indicates the proportion of variance in the target explained by the model (closer to 1 is better).

4. Visualizations and Output Interpretation
A. Actual vs. Predicted Traffic Volume
Description:
A scatter plot shows how closely the model’s predictions match the actual traffic volumes. The dashed line represents perfect predictions.

Interpretation:
Points near the line indicate accurate predictions. A tight cluster around the line means the model is performing well.

B. Residual Plot
Description:
This plot shows the difference (residuals) between actual and predicted values against the predicted values.

Interpretation:
If residuals are randomly scattered around zero, the model does not have systematic errors and fits the data well.

C. Distribution of Predicted Values
Description:
A histogram with a density curve and rug plot shows the distribution of predicted traffic volumes.

Interpretation:
This helps identify if the predictions are reasonable, if there are outliers, or if the model is biased toward certain values.

D. Heatmap of Average Traffic Volume by Hour and Weekday
Description:
A heatmap visualizes average traffic volume for each hour of the day and each day of the week.

Interpretation:
This reveals traffic patterns, such as rush hours on weekdays, lower traffic on weekends, or specific hours with heavy congestion.

5. Output Example
Suppose your model outputs:

text
Mean Squared Error: 141795.73
R-squared: 0.96
