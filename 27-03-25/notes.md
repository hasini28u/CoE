Ensemble Learning:
	-1.BAgging 
	-2.Boosting
-(Bootstrap Aggregation) Bagging is used for overfitting, reducing variance without affecting bias.
-Boosting is used for underfitting and reducing bias without affecting variance.
-low bias->good model.
-----Boosting is an ensemble learning technique that improves the performance of weak learners (usually decision trees) by combining them into a 	   strong learner. It works by training models sequentially, where each new model focuses on correcting the mistakes of the previous ones.
	----How Boosting Works:
	A weak model (e.g., a small decision tree) is trained on the dataset.
	The model’s errors are identified, and higher weights are assigned to misclassified instances.
	A new model is trained, giving more importance to these hard-to-classify instances.
	This process is repeated multiple times, with each new model improving upon the previous ones.
	The final prediction is made by combining all weak models (weighted sum or voting).
	----Advantages:
		✅ Improves accuracy by focusing on difficult cases
		✅ Reduces bias compared to bagging methods
		✅ Works well with both structured and unstructured data

	---Popular Boosting Algorithms:
		AdaBoost (Adaptive Boosting)
		Gradient Boosting (GBM)
		XGBoost (Extreme Gradient Boosting)
/////1. AdaBoost (Adaptive Boosting)
The first boosting algorithm ever developed.
Works by training weak models sequentially, where each new model focuses on fixing mistakes made by the previous one.
Gives higher weights to misclassified data points so that the next model learns from them.
Uses decision stumps (single-level decision trees) as weak learners.
✅ Simple and effective for small datasets
❌ Sensitive to noise and outliers
🔹 Example use case: Face detection, spam filtering

//////2. Gradient Boosting (GBM)
Uses gradient descent to minimize errors while training models sequentially.
Instead of reweighting data like AdaBoost, it builds trees based on residual errors (difference between actual and predicted values).
More flexible and works well with complex data.
✅ High accuracy compared to AdaBoost
❌ Computationally expensive (slower training)
🔹 Example use case: Predicting house prices, fraud detection

/////3. XGBoost (Extreme Gradient Boosting)
An optimized, faster version of Gradient Boosting.
Uses regularization (L1 & L2) to reduce overfitting.
Handles missing values and large datasets efficiently.
Parallel processing makes it much faster than traditional GBM.
✅ Fast and scalable (best for large datasets)
❌ Requires tuning for optimal performance
🔹 Example use case: Kaggle competitions, recommendation systems