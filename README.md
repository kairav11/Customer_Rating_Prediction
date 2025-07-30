# Customer Rating Prediction
This project focuses on analyzing and predicting customer feedback using data from a Brazilian e-commerce platform. The goal is to help businesses gain actionable insights to improve customer experience, increase retention, and guide strategic decisions in operations and marketing.

## Objective
1. Categorize customer feedback into Bad, Neutral, and Good.
2. Identify key factors influencing customer satisfaction.
3. Predict feedback category using machine learning models.

## Dataset
Source: Brazilian E-Commerce Public Dataset by Olist
- Multiple datasets (orders, customers, reviews, products, etc.) were merged and cleaned.
- Irrelevant columns (e.g., IDs, timestamps) were removed.
- Missing values were minimal and removed directly.

## Workflow
- Data Preparation: Merging relevant tables, filtering columns, cleaning missing values.
- Feature Engineering: Creating delivery delay, categorizing feedback, etc.
- Exploratory Data Analysis (EDA): Boxplots and histograms to examine the relationship between delivery time, price, freight cost, number of items, and review scores.
- Data Preprocessing:
1. Label encoding categorical features.
2. Standard scaling of numerical features.
- Created custom feedback labels:
1-2 → Bad, 3 → Neutral, 4-5 → Good

## Model Training & Evaluation:
- Used XGBoost and Random Forest Classifier.
- Evaluated model performance based on classification metrics.

## Key Insights
- Delivery Time: Longer delivery delays are linked to poor feedback.
- Freight Cost: No strong correlation with feedback; reliability may matter more.
- Order Size: More items per order often lead to lower satisfaction (possibly due to missing/damaged items).
- Regional Trends: Some regions consistently showed lower ratings.
- Top Features: Delivery delay and delivery time had the highest importance in predicting feedback.

## Limitations
- Did not analyze textual reviews. Sentiment analysis could add more value.
- Some feedback categories had lower representation, impacting model balance.

## Future Improvements
- Include sentiment analysis using NLP techniques on textual reviews.
- Use techniques like SMOTE to address class imbalance in the dataset.
- Explore deeper feature interactions and advanced model tuning.
