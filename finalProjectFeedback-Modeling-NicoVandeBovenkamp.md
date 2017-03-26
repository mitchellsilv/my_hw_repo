### ***Final Project - Modeling & Exploratory Analysis Feedback***

***Nico Van de Bovenkamp***
***

**Overall** Good work on your Python skills there! You navigated all of those regular expressions, loops, and Pandas methods very well in the end. This is a great start (your first linear models look good)! When you are evaluating these model, remember to evaluate on your test set (in the Train/Test Split) and set aside a metric to evaluate. With Regression problems, you want to plot predicted values, predicted KDEs, residuals, and (typically) MSE across features or parameters. See below for more.

*Also, you made some very nice visualizations, which will help you understand what kind of transformations or feature engineering to do. Quick note: try and keep your notebooks a bit cleaner as you go (or make multiple notebooks where each one is there for a particular task). Doing so will help readers AND help you recall where you wrote code blocks.*

**Some thoughts**
* **Dropping Null Values:** You can drop null values, but recall you do have some methods/techniques for dealing with missing data (imputing 0's to indicate/encode if data is missing in categorical cases, imputing the mean/median)
* **Scaling and Data Transformations** Check out the [Standard Scaler](http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html) package. The Standard Scaler will scale all numerical data, which will allow for some easier computation and more efficient computation. This part can actually be quite critical for Regularization. In addition to, or in replace of depending on how everything shakes out, Scaling your data, you should think about doing some data transformations. [Check out this quick guide!](https://www.isixsigma.com/tools-templates/normality/tips-recognizing-and-transforming-non-normal-data/). [This one is also quite good](https://www.isixsigma.com/tools-templates/normality/making-data-normal-using-box-cox-power-transformation/). Also, check out 'Data preprocessing' in Lesson 11 where we made use of some of these techniques.
* **Binning Continuous Features** In many cases, models will benefit from having features that are discrete (kind of like dummified) rather than continuous. Check out this walkthrough of Stacking (a really cool modeling architecture you may want to implement) because it also makes use of [binning data](https://www.kaggle.com/arthurtok/titanic/introduction-to-ensembling-stacking-in-python).

***A Table of Key Evaluation Metrics and Visuals:***

*Throwing this in here too! Below is a brief set of many ways you can communicate/measure results that will be useful for your final project. Please let me know if you have any questions!*

| Metrics | |
|--- | --- |
| *Classification* | Accuracy, Precision, Recall, AUC Score, Lift, F-Score, Log-Loss, Gini, Entropy/Information Gain, Statistical Significance (p-value) |
| *Regression* | Mean Squared Error, Mean Absolute Error, Log-Likelihood Estimation, Statistical Significance (p-value) |

| Visualizations | |
|--- | --- |
| *Model Tuning* | Learning Curves, Regularization Learning Paths with an Error Metric, Model Error stepwise increasing feature set size |
| *Classification* | ROC Curve, Feature Importance Charts, Lift Curves, Expected Value Plots |
| *Regression* | Residual plots(!), KDE and KDE of Predicted Values, Expected Value |
