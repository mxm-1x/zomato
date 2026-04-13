# Restaurant Success Factor Analysis (Zomato Dataset)

## Project Overview
This project performs a deep dive into restaurant performance data to identify the key drivers of high ratings and customer engagement. By analyzing factors such as pricing, online ordering capabilities, and table booking services, we provide actionable insights for restaurant owners and stakeholders.

## Key Features
- **Robust Data Pipeline**: Cleaning and feature engineering of raw Zomato data (handling non-numeric ratings, currency formatting, and missing value imputation).
- **Feature Engineering**: Creation of new metrics like `cost_per_person` and binary service indicators.
- **Interactive Visualizations**: High-quality plots using `Seaborn` and `Matplotlib`.
- **Business Intelligence**: Correlation analysis and comparative studies of service offerings.

## Data Pipeline & Cleaning
1.  **Rating Normalization**: Converted '4.1/5' strings to float and handled 'NEW' or '-' as null values.
2.  **Cost Formatting**: Cleaned the `approx_cost(for two people)` column by removing commas and handling nulls.
3.  **Service Indicators**: Created binary flags for `online_order` and `book_table` to enable correlation analysis.

## Visualizations & Insights

### 1. Distribution of Restaurant Ratings
- **Chart**: Histogram with KDE.
- **Insight**: The average restaurant rating is **3.63**. Most restaurants are clustered between 3.5 and 4.2, indicating a competitive market where 'good' is the standard.

### 2. Relationship Between Cost and Rating
- **Chart**: Regression Plot.
- **Insight**: There is a **0.28 correlation** between cost and rating. While expensive restaurants tend to have higher ratings, price is not a guaranteed proxy for quality.

### 3. Impact of Services on Ratings
- **Chart**: Side-by-side Boxplots.
- **Insight**: **Online ordering** significantly boosts satisfaction. Restaurants with online ordering average a **3.86 rating** vs. **3.49** for those without. Table booking shows a similar positive trend.

### 4. Correlation Matrix of Success Factors
- **Chart**: Heatmap.
- **Insight**: Customer engagement (**Votes**) shows the strongest correlation with ratings (**0.49**), suggesting that popular restaurants are generally rated higher by the community.

## Summary of Business Insights
- **Online Delivery is Essential**: Providing online ordering is the single most consistent factor associated with higher customer ratings.
- **Engagement Drives Perception**: High vote counts strongly correlate with high ratings; encouraging reviews is vital for brand perception.
- **Niche Performance**: The 'other' category (unique dining types) tends to have the highest average customer ratings compared to standard cafes or buffets.

## Technologies Used
- **Python** (Pandas, NumPy)
- **Data Visualization** (Matplotlib, Seaborn)
- **Environment** (Google Colab / Jupyter Notebook)