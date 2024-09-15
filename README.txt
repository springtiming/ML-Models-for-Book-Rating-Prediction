############
Run the main program directly to obtain the same results as the report.
#############
This section outlines the methods and procedures used in our analysis. We aim to determine users’ location and recommended books accordingly.

We employ machine learning techniques, including regressing and decision tree models. Our study processes user data to understand geographic distribution and reading preferences.

Data Collection: 
Data for this study was obtained from three primary sources. These datasets were sourced from publicly available data repositories.
Books: Details about books, including titles and genres
Ratings: User rating for books
Users: Demographic information about users, including their location

Data Preparation and cleaning: 
Data preparation involved several crucial steps to ensure accuracy and reliability of the analysis:
Handling missing values: Missing data in user demographics and ratings were identified and imputed where appropriate, or removed if necessary to maintain data integrity
Text Normalization: Special Characters and irregular spacing in location names were removed or standardized to ensure consistency across the data set
Categorical Data Handling: Locations and book genres, being categorical, were encoded using ‘OneHotEncoder’ and ‘TargetEncoder’ to transform them into a format suitable for machine learning models. 
We have removed the data under attributes that appear too infrequently.

Feature Engineering: 
Feature engineering was conducted to enhance model performance
Geographic Aggregation: User States with low frequency were grouped into an ‘other’ category to avoid model overfitting on sparse data 
Derived Metrics: New features such as average user ratings per book and per location were calculated to aid in understanding user preferences linked to geographic areas 
We calculated the average rating and number of ratings for each user by merging the user and rating datasets.

Data Splitting: 
The dataset was randomly split into a training set (80%) and a test set (20%).
This split was chosen to provide a robust set of training the models while leaving out a representative proportion of the data for final evaluation to assess the model’s predictive performance. 
Splitting our data also gave us an opportunity to test the validity of our machine learning model, without having to source more data

Model Development and training: 
2 types of models were developed. Ecah mode was trained using the training dataset, with parameters turned to optimize accuracy and minimize overfitting
Decision Tree Regressor: Implemented to analyze the decision paths and criteria most significant in prediction user locations and preferences
Linear Regression: Served as a baseline for comparing model performance 

Model Evaluation: 
Models were evaluated based on their Mean Squared Error (MSE) and R-squared values: 
Cross-validation: 5-fold cross-validation was employed
Performance Metrics: Both in-sample and out-of-sample performance metrics were recorded to assess and compare the effectiveness of each model in predicting user location sand suitable book recommendations

Summary: This methodology enables a comprehensive analysis of user data to address the research question effectively. Bty preparing, engineering and modeling the data, we ensured that the recommendation and predictions are both accurate and applicable in real-world scenarios 
