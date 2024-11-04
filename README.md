# Boom Bikes - Linear Regression analysis
> BoomBikes, a US bike-sharing service, is facing a decline in revenue due to the Covid-19 pandemic. To prepare for a post-quarantine market, the company seeks to understand the demand dynamics for shared bikes by investigating the factors influencing demand. The goal is to create a model that can predict bike rental demand based on various factors in order to inform management strategies.


## General Information
- The objective is to develop a multiple linear regression model using available independent variables to predict the demand for shared bikes. This model will help BoomBikes tailor their business strategy to meet customer needs and navigate the new market conditions effectively.
- The dataset comprises 730 rows and 16 columns, primarily numerical except for a date column.
Cleaning processes included handling missing values, dropping irrelevant columns (e.g., 'instant', 'dteday', 'casual', and 'registered'), and converting certain numerical columns into meaningful categorical strings.
Outliers in the wind speed variable were identified and removed, reducing the dataset to 717 rows.


## Approach
- Box plots and pair plots were used to explore relationships between categorical variables and bike rental counts. Key observations indicated:
	Higher bike rentals occur in clear weather and peak during specific seasons (fall and summer) and months (July and September).
	Positive correlations were noted between temperature and bike rentals, while humidity and wind speed had weak negative correlations.
- A stepwise approach was taken to build the linear regression model:
	The target variable, 'cnt' (total bike rentals), was isolated from independent variables.
	Multiple model iterations were conducted by adding significant variables and assessing their impact on R-squared values and coefficients.
	Variance Inflation Factor (VIF) analysis was employed to identify multicollinearity among features, leading to a streamlined selection of relevant predictors.

## Final Model
- The final model included the independent variables: yr, temp, windspeed, season_spring, season_winter, mnth_sept, weathersit_mist, and weathersit_rain. This model displayed a satisfactory R-squared value of 0.81, indicating a good fit.

## Technologies Used
- library - python pandas, Seaborn, Numpy, matplotlib, sklearn, statsmodel
- Jupiter notebook

