# 1. Decision Tree Classifier / Regressor

| Hyperparameter (sklearn name) | Objective | Description |
| :--- | :--- | :--- |
| **`criterion`** | **Splitting Quality** | Measures the quality of a split. For classification, options are **'gini'** (Gini impurity) or **'entropy'** (Information Gain). For regression, options are **'mse'** (Mean Squared Error), **'friedman_mse'**, or **'mae'** (Mean Absolute Error). |
| **`max_depth`** | **Tree Complexity/Overfitting** | Controls the maximum depth of the tree. A larger value increases complexity and risk of overfitting. Often the most critical parameter to tune. |
| **`min_samples_split`** | **Node Size for Splitting** | The minimum number of samples required to split an internal node. Increasing this value prevents the tree from creating splits that are too specific to small pockets of data. |
| **`min_samples_leaf`** | **Leaf Size Constraint** | The minimum number of samples required to be at a leaf node. Similar to `min_samples_split`, it ensures that leaf nodes are not based on too few observations. |
| **`max_features`** | **Feature Randomness** | The number of features to consider when looking for the best split. Can be an integer, float, or a named option like **'sqrt'** (or **'auto'**) or **'log2'**. Essential for Random Forests, but can be used here too. |
| **`max_leaf_nodes`** | **Tree Size/Complexity** | Grow a tree with `max_leaf_nodes` in a best-first fashion. If this value is not $\text{None}$, `max_depth` is ignored. Restricts the tree size indirectly. |
| **`min_impurity_decrease`** | **Split Threshold** | A node will be split if the split results in a decrease of the impurity greater than or equal to this value. Used to prune splits that provide negligible information gain. |

# 2. Random Forest Classifier / Regressor

| Hyperparameter | Type | Explanation |  Explanation |
| :--- | :--- | :--- | :--- |
| **`n_estimators`** | Model Structure | The **number of decision trees** in the forest. Generally, higher is better, but it increases training time and may lead to diminishing returns. | \text{Number of decision trees} |
| **`max_depth`** | Tree Structure | The maximum **depth** of each individual tree. Limiting this helps control overfitting. | \text{Maximum depth of each tree} |
| **`min_samples_split`** | Split Control | The minimum number of samples required to **split an internal node**. Higher values prevent a tree from learning relationships specific to small subsets of the data. | \text{Min samples needed to split node} |
| **`min_samples_leaf`** | Split Control | The minimum number of samples required to be at a **leaf node**. Similar to `min\_samples\_split`, it smooths the model, particularly in regression. | \text{Min samples required at leaf node} |
| **`max_features`** | Feature Sampling | The number of features to consider when looking for the best split. For classification, the default is $\sqrt{n\_features}$; for regression, it's $n\_features$. | \text{Number of features for best split} |
| **`bootstrap`** | Data Sampling | Whether **bootstrap samples** (sampling with replacement) are used when building trees. If `False`, the entire dataset is used for each tree. | $\in \{\text{True}, \text{False}\}$ (Boolean) |

# 3. 
