It is a method for implementing [[Feature Scaling]].
It is also known as Z-Score Normalization

Formula:
	![[Pasted image 20250227215351.png]]
	Where,
		 μ​ - Mean
		 σ - Standard Deviation

It changes the original distribution to [[normal distribution]] with **μ** = 0 and  **σ** = 1
It is useful for algorithms that use normally distributed data (like [[linear regression]], [[logistic regression]] etc.)

Output generally lies between $[-3,3]$, other than outliers (can be proved using **Empirical Rule**).

```
		from sklearn.preprocessing import StandardScaler
		sc = StandardScaler()
		X_train[:,3:] = sc.fit_transform(X_train[:,3:])
		X_test[:,3:] = sc.transform(X_test[:,3:])
```
			