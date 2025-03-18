It is a dimensionality reduction technique, which reduces the number of features while keeping as much important information as possible.

It combines related features into new variables (called **Principal Components**), ensuring these new variables capture the **maximum variance** (important patterns) in the data.

### Steps
1. **Standardization**:
    - Since different features may have different scales (e.g., height in cm, weight in kg), PCA starts by standardizing the data so all features are on the same scale.
2. **Finding Directions of Maximum Variance**:
    - PCA identifies new axes (called **principal components**) that point in the directions where the data varies the most.
    - These new axes are uncorrelated (independent) and ordered by how much variance they capture.
3. **Projecting the Data**:
    - The original data points are then projected onto these new axes (principal components).
    - The first principal component captures the most variance, the second one captures the second most, and so on.
4. **Dimensionality Reduction**:
    - We can now drop the less significant components (the ones that capture very little variance), effectively reducing the number of features.

**Note:** It prioritizes the directions where the data varies the most (because more variation = more useful information.

Related: [[Multicollinearity]]
