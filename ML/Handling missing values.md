It is among the initial steps of [[Data Pre-Processing]], wherein we take care of missing values in the training data.

It is also known as **Imputing missing values**.

#### Types of Missing Values

1. **Missing Completely at Random (MCAR)**: In this type of missing data, the probability of a data point being missing ***is entirely random and does not depend on values of other variables or the characteristics of the same variable***.
   Ex. A hospital records datasets where weights of some patients are missing due to the random malfunction of weighing machine.
2. **Missing at Random (MAR)**: In this type of missing data, the missing probability of a data point entirely ***depends on the value of other variables, but does not depend on the missing variable itself.*** 
   Ex. In a survey, women are less likely to report their weight. So, if we know the gender of the person, we can predict the probability of missing weight.
3. **Missing Not at Random (MNAR)**: In this type of missing data, the missing probability is ***completely dependent on the missing variable itself***.
   Ex. In an insurance fraud detection dataset, fraudulent claims may have missing data points (like invoice details) on purpose, as fraudsters intentionally omit information.

#### Methods of handling missing values

1. Removing the rows with missing values
	```
	    df= df.dropna()
	```
2. **Forward and Backward Fill**: Replacing the missing values with preceding or next non missing values
	```
	    forward_fill = df['Marks'].fillna(method='ffill')
		backward_fill = df['Marks'].fillna(method='bfill')
	```
3. **Mean Median Mode Imputation**: Replacing the missing values with mean or median or mode of the non missing values of the feature
	```
	    from sklearn.impute import SimpleImputer
		imputer = SimpleImputer(missing_values=np.nan, strategy='mean')
		imputer.fit(df[:, 1:3])
		df[:, 1:3] = imputer.transform(df[:, 1:3])
	```
4. **Interpolation Techniques**: This technique uses linear or quadratic interpolation to predict the missing values. This is only useful when the data points can be reasonably assumed to follow a linear or quadratic pattern
```
	    linear_interpolation = df['Marks'].interpolate(method='linear')
		quadratic_interpolation = df['Marks'].interpolate(method='quadratic')
```
