# Sales-Forecasting-for-Walmart
# Executive Overview

The project involves developing a sales forecasting model for Walmart, aiming to predict daily sales over the next 28 days. We developed a sophisticated forecasting model that synergistically used the strengths of Long Short-Term Memory (LSTM). This initiative aimed to revolutionize inventory management, optimize resource allocation, and significantly enhance customer satisfaction with accurate predictions of sales demand. The culmination of this effort is detailed in this report, which outlines the journey of analysis, the strategic insights obtained, and the resulting impact on Walmart's business operations. The data encompasses multiple stores across different states, categories, and includes variables like promotions (SNAP), seasonality, and special events. The initial scope included data from 3,049 products across 10 stores in 3 categories and 3 states. This was narrowed down to 2,260 products from 3 stores in one category (Hobbies) in California.

# Exploratory Data Analysis (EDA) Insights:
The EDA phase was instrumental in uncovering critical insights that informed our predictive models:

Seasonality and Peak Sales: A consistent pattern was discovered across various categories, where peak sales months remained steady, highlighting the significant role of seasonality in sales trends.

Event-Driven Sales Variability: Our analysis observed a substantial increase in sales during sports and cultural events, pinpointing these as major drivers of consumer spending. In contrast, sales volume decreased on national or religious holidays, suggesting store closures impact sales performance.

SNAP Days and Weekends: Further insights revealed increased sales activity on SNAP benefit days and weekends, indicating the critical times for heightened sales focus in our forecasting models.

# Data Preprocessing and Preparation:
A comprehensive data preprocessing and preparation strategy was crucial for ensuring the accuracy of our predictive models:

Handling Null Values and Outliers: We tackled null values innovatively by labeling them as "None" in the calendar data, while capping outliers above the 75th percentile to mitigate data skewness. Negative sales values were adjusted to zero to maintain data consistency.

Feature Engineering: The construction of dummy variables for SNAP days and the transformation of weekdays and months into cyclical features were pivotal in reflecting sales patterns. Normalizing sales data within the range of 0 to 1 further stabilized model input.

Lag Features and Transposition: Integrating lag features accounted for the sales increase observed 1-2 days before events. We also transposed the dataset, ensuring that each row represented a day's sales for all 2,260 products, facilitating a more effective forecasting process.

# Predictive Modeling:
Sequence Data Preparation: By analyzing the sales data of the previous 28 days, we created sequences to forecast sales for the 29th day, effectively capturing the temporal dependencies in the sales data.

Modeling Approaches: Our team explored two modeling strategies—one that disregarded the sales increase before event days and one that included it. This comparative approach was vital in assessing the impact of anticipatory buying behavior on forecast accuracy.

Multiple models were trained, evaluated, and refined:

Model Architectures: Explored combinations of LSTM and CNN layers, adjusting for hyperparameters to optimize performance.

Performance Metrics: Models were rigorously evaluated using MAPE and RMSE, guiding iterative improvements towards the optimal model.

# Results
The project culminated in the development of a highly effective sales forecasting model:

Best-Performing Model: A blend of CNN (64 filters) and LSTM layers emerged as the most accurate, achieving a desirable balance between computational efficiency and forecasting precision.

Accuracy Metrics: The leading model attained a MAPE of 54.207% and an RMSE of 0.934, setting a benchmark for future enhancements.
