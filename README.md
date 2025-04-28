# Task-3
1. Data Loading and Preprocessing
I began by loading the Walmart Sales dataset using the Kaggle API and ensuring the dataset was properly preprocessed for further analysis. The key preprocessing step involved converting the 'Date' column from a string format into a datetime object. This was important for accurately handling date-related features in future analysis.
Additionally, I ensured that the 'Date' column, which was in the DD-MM-YYYY format, was parsed correctly by specifying the dayfirst=True argument in the datetime conversion. This ensured that dates were interpreted correctly as day-month-year.

2. Exploratory Data Analysis (EDA): Correlation Heatmap
After preprocessing the dataset, I performed an exploratory data analysis (EDA) to understand the relationships between the numerical features in the dataset. Specifically, I created a correlation heatmap to visualize the strength and direction of correlations between features like Temperature, Fuel_Price, CPI, Unemployment, and the target variable Weekly_Sales.
This helped me identify which variables had strong relationships with the target variable. It also provided insights into potential issues like multicollinearity among features, which could impact model performance.

3. Feature Selection and Train-Test Split
In this step, I selected the most relevant features for predicting weekly sales. I chose the following features based on their potential impact on sales:
Temperatur
Fuel_Price
CPI (Consumer Price Index)
Unemployment
Holiday_Flag
The target variable, Weekly_Sales, was set as the output variable. I then split the dataset into training and testing sets using an 80-20 split, where 80% of the data was used for training the model, and the remaining 20% was held back for testing. This ensured that I could evaluate the model’s performance on unseen data.

4. Model Training: Simple Linear Regression
I proceeded to train a Linear Regression model to predict the weekly sales. Linear Regression was chosen for its simplicity and effectiveness in capturing the linear relationship between the input features and the target variable.
Using the training set, the model learned the patterns and relationships between the selected features and the weekly sales data. This model can now be used to predict future sales based on the same features.

6. Model Evaluation: Cross-Validation
To evaluate the performance of the model, I employed K-Fold Cross-Validation with 5 folds. This method splits the data into 5 parts, trains the model on 4 parts, and tests it on the remaining part. The process is repeated 5 times, with each fold used as the test set once.
The advantage of cross-validation is that it provides a more reliable estimate of the model’s performance, as it tests the model on multiple data splits. The results showed that the model performed consistently across different data subsets, confirming that it is stable and not overfitting to any particular split of the data.

Conclusion
Through this process, I gained valuable insights into the relationships between the features and weekly sales. The correlation heatmap provided a visual understanding of how different variables are interrelated, while the cross-validation results ensured the model’s robustness and generalizability.
The model, once trained and validated, is ready to be used for predictions. These steps laid a solid foundation for further enhancements, such as incorporating feature engineering or trying advanced models.
