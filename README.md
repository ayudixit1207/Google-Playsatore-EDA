
Google Play Store — Exploratory Data Analysis & Feature Engineering


Analyzed 10,841 apps across 33 categories to uncover what makes an app successful on Google Play Store.

GAME category dominates with 35+ Billion installs while 93%+ apps are Free.


Problem Statement
Today, 1.85 million different apps are available for users to download. Android users have even more to choose from, with 2.56 million apps available through the Google Play Store.
Objective:

Most popular app categories by installs
Apps with largest number of installs
Relationship between app features and ratings
Key business insights for app developers


Dataset Information
PropertyDetailsSourceGoogle Play Store DatasetRows10,841Columns13Missing ValuesYes (Rating, Type, Size, etc.)Duplicates1,181 duplicate apps removed
Features:
ColumnDescriptionAppName of the appCategoryCategory of the appRatingApp rating (0–5)ReviewsNumber of user reviewsSizeSize of the appInstallsNumber of installsTypeFree or PaidPricePrice of the appContent RatingTarget audienceGenresGenre of the appLast UpdatedLast update dateCurrent VerCurrent versionAndroid VerMinimum Android version required

Steps Performed
1. Data Cleaning
StepActionReviewsDropped invalid row, converted to intSizeConverted M/k suffixes to KB, filled nulls with medianInstallsRemoved + and comma, converted to intPriceRemoved $, converted to floatLast UpdatedExtracted Day, Month, YearDuplicatesRemoved 1,181 duplicate apps
2. Exploratory Data Analysis
AnalysisDetailsUnivariateKDE plots for numerical, countplots for categoricalCategoriesMost popular by app count and installsTop AppsTop 5 most installed apps per categoryRatingsApps with perfect 5-star ratingOutliersDetection using boxplotsComparisonFree vs Paid app analysis
3. Feature Engineering
StepDetailsLabel EncodingType column — Free=0, Paid=1Log TransformationReviews, Installs, Price (right-skewed)CorrelationHeatmap of all numerical featuresDrop ColumnsApp, Last Updated, Current Ver, Android Ver, Genres

Key Business Insights
#Insight1GAME category dominates with 35+ Billion installs293%+ apps are Free — freemium model is the standard3FAMILY has most apps (18%) but GAME has most installs4Reviews and Installs are highly correlated (r=0.64)5Paid apps have slightly higher ratings6Reviews, Installs, Price are right-skewed — log transform needed7BEAUTY and COMICS are least crowded — niche opportunity

Tech Stack
ToolPurposePythonCore programmingPandasData cleaning and analysisNumPyNumerical operationsMatplotlibBase plottingSeabornStatistical visualizations

How to Run
bashgit clone https://github.com/ayudixit1207/google-playstore-eda.git
cd google-playstore-eda
pip install pandas numpy matplotlib seaborn
jupyter notebook PlayStore_Merged.ipynb

Project Structure
google-playstore-eda/
│
├── PlayStore_Merged.ipynb
├── googleplaystore.csv
├── google_cleaned.csv
└── README.md

Author
Aayush Dikshit
B.Tech CSE (Data Science) — ABES Engineering College, Ghaziabad
Show Image

Show Image

Future Scope
PlanBuild ML model to predict app ratingDeploy prediction app using StreamlitPerform sentiment analysis on user reviews
