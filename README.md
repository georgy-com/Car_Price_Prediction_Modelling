This project developed and evaluated machine learning models to predict the selling price of used cars using a dataset containing 301 vehicle records with features such as car brand, manufacturing year, current market price, mileage (driven kilometers), fuel type, transmission type, selling type, and ownership history. The objective was to understand the factors influencing used-car prices and build an accurate predictive model.

The analysis followed a complete machine learning workflow, including data cleaning, exploratory data analysis (EDA), feature engineering, categorical variable encoding, model training, evaluation, and prediction. Two regression algorithms—Linear Regression and Random Forest Regression—were compared using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and the Coefficient of Determination (R² Score).

The results showed that the Random Forest Regressor outperformed the Linear Regression model, achieving a lower prediction error and a higher explanatory power. Feature importance analysis further revealed that the current market price (Present_Price) is by far the strongest determinant of a vehicle's resale value.
Detailed Analysis
1. Dataset Overview

The dataset contains 301 observations and 9 variables, including both numerical and categorical features.
2. Data Quality Assessment

The data quality assessment indicated:

No missing values in any variable.
No duplicate observations after data cleaning.
Appropriate data types for all variables.
Interpretation

The dataset was clean and complete, requiring minimal preprocessing before model development. This improves the reliability of the analysis and reduces the risk of biased model predictions.

3. Descriptive Statistics

The statistical summary provides several insights:

Average selling price: 4.66
Average current market price: 7.63
Average manufacturing year: 2013
Average distance travelled: 36,947 km
Most vehicles had no previous owners

The selling prices range from 0.1 to 35.0, indicating substantial variation in vehicle values.

Interpretation

The wide range of prices suggests the dataset includes both economy and premium vehicles. Similarly, the large variation in mileage indicates differences in vehicle usage, which is expected to influence resale prices.

4. Distribution of Selling Prices

The histogram of selling prices indicates that most vehicles are concentrated within the lower price range, while only a few high-value vehicles exist.

Interpretation

The distribution is positively skewed, meaning:

Most cars have relatively low selling prices.
Luxury vehicles form a small proportion of the dataset.
The presence of high-priced vehicles introduces some outliers, which can influence regression models.
5. Correlation Analysis

The correlation heatmap illustrates the relationships among variables.

The strongest positive relationship exists between:

Present Price and Selling Price

Other variables such as:

Manufacturing Year
Driven Kilometers

also show meaningful relationships with the target variable.

Interpretation

Current market value is the most influential predictor because resale prices are naturally derived from the vehicle's original or present value. Newer vehicles generally retain higher resale values, while higher mileage tends to reduce vehicle prices.

6. Relationship Between Mileage and Selling Price

The scatter plot of Driven Kilometers versus Selling Price reveals a downward trend.

Interpretation

Cars with higher mileage generally have lower resale values due to increased wear and tear, higher maintenance requirements, and reduced remaining lifespan.

However, some vehicles with relatively high mileage still maintain higher prices because of strong brand reputation or premium vehicle categories.

7. Relationship Between Present Price and Selling Price

The scatter plot demonstrates a strong positive linear relationship.

Interpretation

As the present market price increases, the selling price also increases. This confirms that current market value is the strongest predictor of resale price.

Luxury vehicles naturally maintain higher resale prices even after depreciation.

8. Fuel Type Distribution

The majority of vehicles in the dataset use:

Petrol
Diesel

Only a small proportion use alternative fuel types.

Interpretation

The dominance of petrol and diesel vehicles reflects prevailing market trends. Fuel type influences resale value because operating costs, fuel efficiency, maintenance, and consumer preferences differ across fuel categories.

9. Transmission Type

The dataset contains more manually operated vehicles than automatic vehicles.

Interpretation

Manual transmission remains more common in many developing markets due to lower purchase costs and maintenance expenses. However, automatic vehicles may command higher resale values depending on consumer demand.

10. Selling Type

Most vehicles were sold through dealerships rather than directly by individual owners.

Interpretation

Dealer sales typically involve vehicle inspections, servicing, and warranties, increasing buyer confidence and potentially influencing selling prices.

11. Machine Learning Model Performance

Two regression models were evaluated.

Linear Regression

Performance metrics:

MAE: 2.62
RMSE: 4.13
R² Score: 0.339
Interpretation

The Linear Regression model explains approximately 34% of the variation in selling prices.

Although it provides a useful baseline model, its relatively low R² score indicates that it cannot adequately capture the complex relationships among the variables.

Random Forest Regression

Performance metrics:

MAE: 1.45
RMSE: 3.55
R² Score: 0.510
Interpretation

The Random Forest model explains approximately 51% of the variation in vehicle prices.

Compared with Linear Regression:

Prediction errors are substantially lower.
Model accuracy is higher.
Non-linear relationships are captured more effectively.
Feature Importance Analysis

The Random Forest model identified the most influential predictors.

Top features include:

Present Price (88.56%)
Year (7.03%)
Land Cruiser Brand
Driven Kilometers
Transmission Type
Corolla Altis
Selling Type
Innova
City
Fuel Type
Interpretation

The overwhelming importance of Present Price indicates that the current market value is the dominant determinant of resale price.

Vehicle age also plays a substantial role because depreciation increases over time.

Brand-specific features demonstrate that consumer trust, reliability, and brand reputation influence resale values beyond physical vehicle characteristics.
Actual vs Predicted Prices

The scatter plot comparing actual and predicted prices illustrates the predictive capability of the Random Forest model.

Interpretation

Although predictions generally follow the actual prices, some dispersion remains.

This indicates that while the model performs reasonably well, additional variables not included in the dataset—such as accident history, maintenance records, engine condition, location, and market demand—could further improve prediction accuracy.

Sample Prediction

The Random Forest model predicted a selling price of 3.65 for the sample vehicle, compared with the actual selling price of 3.35.

The Random Forest model was therefore selected as the best-performing model.
