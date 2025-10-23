# What are hyperparameters ?

Hyperparameters in machine learning are configuration settings that are external to the model and whose values cannot be estimated from the data. They are set by the data scientist before the training process begins and are
used to control the learning process itself.

## ⚙️ The Role and Contrast with Parameters

|Feature |Hyperparameter| Parameter (Model Parameter)|
|--------|---|---|
|Set By | The Data Scientist/User|The Learning Algorithm (during training)|
|Learned From Data | No (External to the model)| Yes (Internal to the model)|
|Controls | The learning process or the model's structure.|The predictions or output of the model.|
|Example|"Learning Rate K in K-means, max_depth in Decision Trees."|"Weights, Biases in Neural Networks, coefficients in Linear Regression."|

## 🧠 Examples in Common Algorithms
The choice of hyperparameters significantly affects the model's performance and training time.

1. K-Means Clustering
   * $K$ (Number of Clusters): The most critical hyperparameter, which must be chosen before training starts (e.g., using the Elbow Method or Silhouette Score).
2. DBSCAN Clustering
   * Epsilon ($\boldsymbol{\epsilon}$/eps): The radius defining the neighborhood of a point.
   * MinPts (Minimum Samples): The minimum number of points required to form a dense region (a Core Point).
3. Hierarchical Clustering
   * Linkage Method: The rule used to calculate the distance between clusters (e.g., Single, Complete, Ward).
4. Machine Learning (General)
   * Learning Rate: Controls how much the model's weights are updated in response to the estimated error each time the model parameters are updated.
   * Number of Iterations/Epochs: The number of passes through the entire training dataset.

## 🛠️ Hyperparameter Tuning
Since hyperparameters cannot be learned, they must be manually chosen or optimized through a process called Hyperparameter Tuning or Optimization. Common techniques include:
  * Grid Search: Exhaustively searches over a manually specified subset of the hyperparameter space.
  * Random Search: Selects random combinations of hyperparameters, often more efficient than Grid Search.
  * Bayesian Optimization: Uses a probabilistic model to select the most promising hyperparameter settings to evaluate in the next iteration.

