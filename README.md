# clustering US Stock market data based on Monthly-returns:
* The dataset contains 20 years data (2000 to 2020)

### Problem 1 - Examine the daily Volume data:
* Identifying the Optimal number of Clusters for daily-Volume data
  * using Elbow plot, Optimum clusters is identified to be 4
  * Clustering is done using k-means algorithm (scikit learn package)
* Got Silhouette score of 51% which means that the clusters are not well separated, but it is a decent score.

### Problem 2 - Examine the daily open, close, and volume data:
* Computing the Fractional Differencing values for (1) Opening price, (2) Closing price, (3) Volume of stocks traded daily.
* Clustering the above 3 parameters
   * optimum no:of clusters is found to be 5

### Problem 3 - Compute Monthly returns
* The monthly dates are extracted using pandas modules such as USFederalHolidayCalendar, CustomBusinessMonthBegin, CustomBusinessMonthEnd.
* Mean of Monthly returns of 20 years (2000-2020) is calculated.

### Problem 4 - Use DECISION TREE to classify if investing in any month can be a profitable strategy:(Business statement)
* Calculating the Month based profit/loss (Decision tree Regression model predictions)
* Comparing Actual-value VS Decision-tree model predicted-values
* finally, using Decision tree classifier to classify month based profit/loss
* Evaluating the model: (Error metrics)
    * Confusion matrix
    * Classification report
    * AUC-ROC curve
    * overall accuracy score score is 71%
* Plotting the decision tree
* using Hyper-parameter tuning
