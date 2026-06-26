Ye README acchi hai but thodi generic hai — isme tera naam, college, actual numbers (10,841 rows, 1,181 duplicates) nahi hain. Isko personalize karke de raha hoon:

📱 Google Play Store EDA
This project focuses on Exploratory Data Analysis (EDA) and Data Cleaning using the Google Play Store dataset. The notebook covers the complete preprocessing workflow and explores different insights through visualizations and statistical analysis.

📂 Project Overview
The main objective of this project is to:

Clean the raw Play Store dataset (10,841 rows, 13 columns)
Handle missing values across Rating, Size, Type columns
Remove 1,181 duplicate records
Convert data into appropriate data types
Perform exploratory data analysis
Visualize important patterns and relationships in the data


📊 Analysis Performed

✔️ Data Cleaning
✔️ Handling Missing Values
✔️ Removing Duplicates
✔️ Feature Engineering
✔️ Univariate Analysis
✔️ Bivariate Analysis
✔️ Correlation Analysis
✔️ Category-wise Analysis
✔️ App Rating Analysis
✔️ Reviews and Installs Analysis
✔️ Free vs Paid App Comparison
✔️ Outlier Detection
✔️ Distribution Plots and Heatmaps


🛠️ Libraries Used

Pandas
NumPy
Matplotlib
Seaborn


📁 Files
PlayStore_Merged.ipynb     # Complete EDA Notebook
googleplaystore.csv        # Raw Dataset
google_cleaned.csv         # Cleaned Dataset
README.md                  # Project Documentation

📌 Key Insights

GAME category dominates with 35+ Billion installs — highest user engagement
93%+ apps are Free — freemium model is the industry standard
FAMILY has most apps (18%) but GAME has most installs — quantity does not equal popularity
Reviews and Installs are highly correlated (r=0.64)
Paid apps have slightly higher ratings than Free apps
Ratings for most apps are concentrated between 4.0 and 4.5
BEAUTY and COMICS categories are least crowded — potential niche opportunity


🚀 How to Run

Clone this repository

bashgit clone https://github.com/ayudixit1207/google-playstore-eda.git

Install the required libraries

bashpip install pandas numpy matplotlib seaborn

Open the notebook

bashjupyter notebook PlayStore_Merged.ipynb

📸 Output
The notebook includes:

Cleaned dataset
Visualizations
Statistical summaries
Correlation Heatmap
Category Analysis
Rating Distribution
Install and Review Analysis
Outlier Detection Plots
Free vs Paid Comparison


📚 Learning Outcomes
This project helped me practice:

Data Cleaning on real-world messy data
Exploratory Data Analysis (EDA)
Data Visualization
Feature Engineering (Label Encoding, Log Transformation)
Working with real-world datasets using Pandas and Seaborn
