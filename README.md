Problem Statement
Today, 1.85 million different apps are available for users to download. Android users have even more to choose from, with 2.56 million apps available through the Google Play Store.
Objective — Analyze the Play Store dataset to find the most popular app categories, apps with largest installs, relationship between features and ratings, and key business insights for app developers.

Dataset Information
PropertyDetailsSourceGoogle Play Store DatasetRows10,841Columns13Missing ValuesYes — Rating, Type, SizeDuplicates Removed1,181
ColumnDescriptionAppName of the appCategoryCategory of the appRatingApp rating 0 to 5ReviewsNumber of user reviewsSizeSize of the appInstallsNumber of installsTypeFree or PaidPricePrice of the appContent RatingTarget audienceGenresGenre of the appLast UpdatedLast update dateCurrent VerCurrent versionAndroid VerMinimum Android version required

Steps Performed
Data Cleaning
StepActionReviewsDropped invalid row, converted to intSizeConverted M and k suffixes to KB, filled nulls with medianInstallsRemoved plus and comma symbols, converted to intPriceRemoved dollar sign, converted to floatLast UpdatedExtracted Day, Month, Year as new columnsDuplicatesRemoved 1,181 duplicate apps
Exploratory Data Analysis
AnalysisDetailsUnivariateKDE plots for numerical, countplots for categoricalCategoriesMost popular by app count and by installsTop AppsTop 5 most installed apps per categoryRatingsApps with perfect 5 star ratingOutliersDetection using boxplots for all numerical featuresComparisonFree vs Paid app rating and install analysis
Feature Engineering
StepDetailsLabel EncodingType column — Free=0, Paid=1Log TransformationApplied on Reviews, Installs, PriceCorrelation HeatmapBetween all numerical featuresDropped ColumnsApp, Last Updated, Current Ver, Android Ver, Genres

Key Business Insights
NoInsight1GAME category dominates with 35+ Billion installs — highest user engagement293 percent apps are Free — freemium model is the industry standard3FAMILY has most apps 18 percent but GAME has most installs — quantity does not equal popularity4Reviews and Installs are highly correlated r=0.64 — more installs means more reviews5Paid apps have slightly higher ratings — quality focus from paid developers6Reviews, Installs and Price are right skewed — log transformation needed before ML7BEAUTY and COMICS are least crowded — lower competition, potential niche opportunity

Tech Stack
ToolPurposePythonCore programmingPandasData cleaning and analysisNumPyNumerical operationsMatplotlibBase plottingSeabornStatistical visualizations
