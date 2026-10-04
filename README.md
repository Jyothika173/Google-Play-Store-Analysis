# Google Play Store Analysis

## Objective
Perform a comprehensive analysis of the Google Play Store: clean messy real-world data, explore app categories, analyse ratings and pricing trends, and run sentiment analysis on user reviews.

## Datasets
- `googleplaystore.csv`: 10,841 apps, 13 columns
- `googleplaystore_user_reviews.csv`: 64,295 user reviews, 5 columns

After cleaning, 7,027 apps remain for analysis.

## Tools
Python, pandas, numpy, matplotlib, seaborn, VADER (vaderSentiment), plotly, Jupyter Notebook

## What I did
- [x] Loaded both datasets separately
- [x] Cleaned the data: converted Installs, Price, Reviews and Size to numbers, removed duplicates, handled nulls and dropped one corrupted row
- [x] Category analysis: bar chart of apps per category and the most saturated categories
- [x] Ratings analysis: rating distribution and average rating by category
- [x] Size vs installs: scatter plot and correlation
- [x] Pricing analysis: free vs paid, price distribution of paid apps and estimated revenue by category
- [x] Sentiment analysis of reviews with VADER (positive, negative, neutral)
- [x] Sentiment by category
- [x] Interactive plotly chart (app size vs installs)
- [x] Conclusion with 3 insights for a developer launching a new app

## Key findings
- FAMILY (1,512 apps), GAME (832) and TOOLS (626) are the most saturated categories.
- 92.3% of apps are free and 7.7% are paid.
- App size and installs have a weak positive correlation (about 0.13).
- LIFESTYLE has the highest estimated revenue from paid apps, followed by FAMILY and GAME.
- Most reviews are positive. AUTO_AND_VEHICLES has the highest share of positive reviews (about 82%), while VIDEO_PLAYERS (about 29%), SOCIAL (about 26%) and FINANCE (about 24%) have the highest share of negative reviews.

## Insights for a developer
1. Crowded categories (FAMILY, GAME, TOOLS) need unique features or a niche audience.
2. A free or freemium model fits the market, since most apps are free.
3. Categories with high negative sentiment point to unmet user needs, which a new app can solve with better usability and performance.

## Notes
- Revenue is estimated as Price x Installs, assuming every install is a paid purchase, so real revenue is likely lower. A few apps priced near $400 may inflate some category estimates.
- Apps with missing ratings and apps with "Varies with device" size were removed, so all counts and percentages come from the cleaned set.
- Categories with few reviews can show extreme sentiment percentages.

## Files
- `Google_Play_Store_Analysis.ipynb`: the notebook
- `googleplaystore.csv`, `googleplaystore_user_reviews.csv`: the data
