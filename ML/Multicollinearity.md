***Multi-Col-Linearity***

It is a phenomenon when **multiple predictor (independent) variables are correlated** (show linear relationship) to each other. 
For Ex. Lets say we are predicting house prices using features such as area, num of rooms, num of windows, total area of windows. Here, area and num of rooms are correlated to each other as more area generally means more num of rooms and similarly num of windows and total area of windows are correlated as more num of windows means larger total area.

### Problem with multicollinearity

Talking about regression:
1. **Unstability of regression coefficients** that may show large fluctuations in response to small changes in data
2. **Reduced interpretability** of model as it makes it hard to determine individual contribution of each predictor among the correlated ones, on dependent variable 
3. Risk of **overfitting**

### How to detect multicollinearity

1. Using **Variance Inflation Factor (VIF)**:
		$VIF=1/(1-R^2)$
			$R_i^2$ : The R-squared value of the regression model where **feature $X_i$​** is treated as the **target** and all other features are used as independent variables.
		![[Pasted image 20250318220130.png]]
2. **Correlation Matrix:**
	It is matrix representation of pairwise correlation of all the features.
	By computing correlation matrix, we can identify which features are correlated to each other and upto what extent.
3. **Plotting each pair of predictors using scatter plot**:
	This technique helps visually identify the correlated predictors but is often time consuming and not recommended when the number of independent features is large


### How to mitigate multicollinearity

1. By **removing or combining** correlated columns based on domain knowledge.
2. Using [[Regularization]] techniques
3. By using [[Principal Component Analysis (PCA)]]
