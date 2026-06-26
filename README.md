# Google-Playsatore-EDA
*Problem Statement
Today, 1.85 million different apps are available for users to download. Android users have even more to choose from, with 2.56 million apps available through the Google Play Store.
Objective: Analyze the Play Store dataset to find:

*Most popular app categories by installs
Apps with largest number of installs
Relationship between app features and ratings
Key business insights for app developers


*Dataset Information
PropertyDetailsSourceGoogle Play Store DatasetRows10,841Columns13Missing ValuesYes (Rating, Type, Size, etc.)Duplicates1,181 duplicate apps removed
Features

*App — Name of the app
Category — Category of the app
Rating — App rating (0–5)
Reviews — Number of user reviews
Size — Size of the app
Installs — Number of installs
Type — Free or Paid
Price — Price of the app
Content Rating — Target audience
Genres — Genre of the app
Last Updated — Last update date
Current Ver — Current version
Android Ver — Minimum Android version required


*Steps Performed
1. Data Cleaning

Fixed Reviews — dropped invalid row, converted to int
Fixed Size — converted M/k suffixes to numeric (KB), filled nulls with median
Cleaned Installs — removed + and ,, converted to int
Cleaned Price — removed $, converted to float
Extracted Day, Month, Year from Last Updated
Removed 1,181 duplicate apps

2. Exploratory Data Analysis

Univariate analysis — KDE plots + countplots
Most popular categories by app count and installs
Top 5 most installed apps per category
Apps with perfect 5-star rating
Outlier detection using boxplots
Free vs Paid app comparison

3. Feature Engineering

Label Encoding — Type (Free=0, Paid=1)
Log Transformation — Reviews, Installs, Price
Correlation Heatmap
Dropped unnecessary columns


*Key Business Insights

1.GAME category dominates with 35+ Billion installs — highest user engagement
2.93%+ apps are Free — freemium model is the industry standard
3.FAMILY has most apps (18%) but GAME has most installs — quantity does not equal popularity
4.Reviews and Installs are highly correlated (r=0.64) — more installs = more reviews
5.Paid apps have slightly higher ratings — quality focus from paid developers
6.Reviews, Installs, Price are right-skewed — log transformation needed before ML
7.BEAUTY and COMICS are least crowded — lower competition, potential niche opportunity


*Tech Stack
Python | Pandas | NumPy | Matplotlib | Seaborn

*How to Run
bashgit clone https://github.com/ayudixit1207/google-playstore-eda.git
cd google-playstore-eda
pip install pandas numpy matplotlib seaborn
jupyter notebook PlayStore_Merged.ipynb

*Project Structure
google-playstore-eda/
│
├── PlayStore_Merged.ipynb      # Main notebook
├── googleplaystore.csv         # Raw dataset
├── google_cleaned.csv          # Cleaned dataset
└── README.md

Author
Aayush Dikshit

B.Tech CSE (Data Science) — ABES Engineering College, Ghaziabad
Show Image

Show Image

Future Scope

Build ML model to predict app rating
Deploy prediction app using Streamlit
Perform sentiment analysis on user reviews
