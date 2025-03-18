It is a method wherein the regression coefficients are either shrinked or set to zero to prevent overfitting.

### Types of regularization

1. **L1 regularization (Lasso Regression)**: 
	- It aims to set some of the regression coefficients to zero by introducing a penalty term into the loss function.
	- It is beneficial in cases where we deal with high-dimensional datasets.
2. **L2 regularization (Ridge Regression):**
	- It aims to shrink the regression coefficients towards zero while still allowing them to be non zero by introducing a penalty term into the loss function.
	- It is beneficial in cases where we deal with [[multicollinearity]].
3. **Elastic Net Regularization**:
	- It is nothing but combining L1 and L2 regularization techniques.
