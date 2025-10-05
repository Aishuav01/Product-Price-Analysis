# Product-Price-Analysis
This project involves loading and cleaning a dataset of Walmart product listings. The data was then used to analyze price trends over time for different product models and manufacturers, including visualizing these trends using line plots. The project also attempted to use the Gemini API to analyze the price trends and identify patterns or anomalies.

Steps Performed:
1. **Data Loading**: The project started by loading the Walmart product listing dataset from Kaggle Hub into a pandas DataFrame using kagglehub.dataset_load.
2. **Data Cleaning and Preparation**: Several steps were taken to clean and prepare the data for analysis:
Column names were renamed for better readability.
The insert_ts column was converted to datetime objects to extract the month and year.
Missing values in the star rating columns (five_star, four_star, etc.) and monthly_price were filled with 0.
The monthly_price and insert_year columns were dropped.
Missing values in the price column were filled with 0, and missing model_name values were filled with 'Unknown'.
3. **Data Analysis and Visualization**:
A new DataFrame product_df was created with relevant columns for price analysis (id, title, insert_ts, insert_month, sku, manufacturer, model_id, price, stock). New columns insert_dateid and insert_date were created for time-based analysis.
The average price trend was calculated by grouping the data by month, date, and model ID (model_price_trend).
Price trends for individual model IDs were visualized using line plots.
Price trends were also analyzed by grouping by month, date, model ID, and manufacturer (sku_price_trend).
Price trends for the top models (based on frequency) were compared using line plots.
4. **Gen AI (Attempted)**: An attempt was made to use the Gemini API to analyze the model_price_trend data to identify trends, anomalies, and price ranges


