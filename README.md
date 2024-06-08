# Sales-Forecasting-for-Walmart
# Situation
Walmart needed a robust sales forecasting system to optimize inventory management and marketing strategies across multiple stores. The objective was to predict daily sales for the next 28 days for products in the "Hobbies" category across stores in California, incorporating influences like promotions, seasonal trends, and special events.

# Task
The task was to develop and implement a machine learning model that could accurately forecast sales using historical sales data and calendar information, such as special events and SNAP promotions. The model needed to handle the complexities of varying sales patterns and provide actionable insights to improve business decisions.

# Action
# Data Preparation and Feature Engineering:

Data Collection: Sales and calendar data were collected, with sales data spanning from 2011 to 2016. Initial data exploration was conducted to understand key trends and anomalies.

Data Cleaning and Preparation: The calendar data was cleaned, and missing values were filled. Sales data was filtered to focus only on relevant products, stores, and years. The dataset was then transformed to align sales with calendar features.

Outlier Handling: Sales data outliers were capped at the 75th percentile to reduce the impact of extreme values.
Normalization: Data was normalized to aid in the model's learning process.

Cyclical Features: Day of the week and month were encoded using sine and cosine transformations to capture their cyclical nature, essential for modeling seasonal trends in sales.

Categorical Encoding: Event types were one-hot encoded to transform nominal categorical data into a format suitable for modeling.

# Model Development and Evaluation:
Model Architecture: Various LSTM models, including simple and bidirectional configurations, were evaluated to determine the best fit for the forecasting task. Bidirectional LSTMs were particularly focused on for their ability to capture temporal dependencies both forwards and backwards in time.

Training and Validation: The models were trained on a sequence of sales data prepared as 28-day blocks to predict sales for the subsequent day, simulating the real-world forecasting scenario. Model performance was validated using a split of training and test data.

Performance Metrics: Models were assessed using Mean Absolute Percentage Error (MAPE) and Root Mean Squared Error (RMSE) to evaluate accuracy and reliability.
Result

Model Performance: The best-performing models achieved an RMSE as low as 0.92 and a MAPE around 18%, indicating a moderately high accuracy in the context of retail sales forecasting, which typically deals with high variability.

Visualization and Analysis: Predictions were visualized against actual sales to demonstrate the model's effectiveness, providing clear insights into the model's predictive accuracy and areas for improvement.

# Conclusion
The Walmart Sales Forecasting project successfully implemented a sophisticated LSTM-based model capable of handling complex patterns in sales data influenced by promotions, seasonal trends, and events. The model provided actionable insights, enabling better inventory and marketing decisions, thereby aligning with Walmart's strategic business objectives. Future enhancements are focused on scalability and ongoing refinement to maintain relevance and accuracy in a changing retail environment.
