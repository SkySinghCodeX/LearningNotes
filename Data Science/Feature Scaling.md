Feature scaling is a step of [[Data Pre-Processing]] to make sure all our **data is on similar scale**, so that no single feature dominates other

Think of it as mixing different ingredients in a recipe, if one ingredient is much bigger , it can overpower the mixture.

Feature scaling is always **applied on a column level** and not on row level.

Common scaling methods:
1. [[Normalization]]
2. [[Standardization]]

Feature scaling **should be done after test train split**, because feature scaling calculates mean and standard deviation which ideally should not include testing data as testing data should be a fresh set. This is also called **information leakage** to test set from train set. Hence to prevent this, feature scaling should always be done after splitting data into test and train.

Importance of feature scaling can be understood with an example of [[multiple linear regression]], where each feature is multiplied with a coefficient. So although if the coefficient value after regression comes out to be less but it will be countered by the large values of variable itself.

We need **not apply feature scaling to categorical variables** (after [[OneHotEncoding]]) as they are already either 1 or 0, and may loose interpretation if scaled to different values. For example a feature named Gender having two distinct values "Male" and "Female" may result in (0,1) and (1,0) after One Hot encoding. But if we apply Feature Scaling on it, it may get transformed to values say, (0.2,0.86) and (0.74, 0.5) which will lead to loss of interpretability as to which combination belonged to what category. Also, feature scaling categorical variable won't improve results.

