The ML models in general do not understand string as input. For training them, it is necessary to convert the textual data (i.e. categorical data) to numerical data.

The categorical data can be classified as:
1. **Nominal Data**: Categorical data without any intrinsic ranking (Ex. Gender)
2. **Ordinal Data**: Categorical data that have some sort of intrinsic ranking (Ex. Rank in a competition)

#### Methods of encoding
1. **Label Encoding**: It is a pretty straightforward technique wherein an integer is assigned to each category randomly. This type of encoding is used for ordinal data where order of categories is meaningful.
```
	    from sklearn.preprocessing import LabelEncoder
		le = LabelEncoder()
		y = le.fit_transform(y)
```
2. **One Hot Encoding**: In this technique, categorical data is converted into a binary matrix, where each category is represented by a binary vector.  This type of encoding is used for nominal data.
```
	    from sklearn.compose import ColumnTransformer
		from sklearn.preprocessing import OneHotEncoder
		ct = ColumnTransformer(transformers=[('encoder', OneHotEncoder(), [0])], remainder='passthrough')
		X = np.array(ct.fit_transform(X))
```
3. **Ordinal Encoder**: It is similar to label encoding but it ensures an order is preserved.
```
	    data = np.array(['low', 'medium', 'high', 'medium', 'low']).reshape(-1, 1)
		ordinal_encoder = OrdinalEncoder(categories=[['low', 'medium', 'high']])
		encoded_data = ordinal_encoder.fit_transform(data)
```


Related: [[Data Pre-Processing]]
