# Computational Finance with Python


## Granger Causality

Granger causality is a statistical concept used to determine whether one time series can predict another time series. It was developed by Clive Granger, who was awarded the Nobel Prize in Economics in 2003 for his work. Despite the term "causality" in its name, Granger causality doesn't imply a causal relationship in the traditional sense, but rather a predictive one.

### Basic Breakdown:

1. **Two Time Series**: Granger causality typically deals with two time series, \(X\) and \(Y\).
2. **Prediction**: The fundamental question Granger causality asks is whether past values of \(X\) provide information that helps predict \(Y\), above and beyond the information provided by past values of \(Y\) itself.
3. **Lagged Values**: To determine this, a statistical model is used that includes lagged (i.e., past) values of \(X\) and \(Y\).
4. **Comparison**: The predictive power of a model that uses lagged values of both \(X\) and \(Y\) to predict \(Y\) is compared to a model that uses only lagged values of \(Y\).
5. **Result**: If the inclusion of lagged values of \(X\) significantly improves the prediction of \(Y\), then \(X\) is said to "Granger-cause" \(Y\).

### Key Points:

- **Not Causal in Traditional Sense**: Just because \(X\) Granger-causes \(Y\) doesn't mean \(X\) is the underlying cause of changes in \(Y\). It simply means there's a consistent pattern where changes in \(X\) precede changes in \(Y\).
- **Bi-directionality**: It's possible for \(X\) to Granger-cause \(Y\) and for \(Y\) to Granger-cause \(X\). This would indicate a bi-directional predictive relationship.
- **Limitations**: The concept is based on linear models, and the results might not hold in non-linear systems. Also, if the lag structure or model is misspecified, it could lead to incorrect conclusions.

Granger causality tests are widely used in econometrics, neuroscience, and other fields where time series data are available, and researchers are interested in understanding potential predictive relationships between variables.
