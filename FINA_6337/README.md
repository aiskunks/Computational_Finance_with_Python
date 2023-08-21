# Computational Finance with Python

## Simple Returns (Arithmetic Returns)

Simple returns, often referred to as arithmetic returns or simply returns, represent the percentage change in a financial asset's price over a specific period. They are the most straightforward method to calculate the return on an investment.

### Simple Return Formula:

For a single-period simple return, the formula is:

\[ R_t = \frac{P_t - P_{t-1}}{P_{t-1}} \]

Where:
- \( R_t \) is the simple return at time \( t \).
- \( P_t \) is the asset price at time \( t \).
- \( P_{t-1} \) is the asset price at the previous time, \( t-1 \).

This formula calculates the return between two consecutive time periods. To find the total return over multiple periods, you can sum the single-period returns.

### Interpretation:

If \( R_t \) is positive, it indicates a profit, whereas a negative \( R_t \) suggests a loss for that period. The value is often multiplied by 100 to get a percentage. For instance, a value of 0.05 or 5% means the asset increased in value by 5% from \( t-1 \) to \( t \).

### Example:

Let's say you bought a stock at a price of $100 (\( P_{t-1} \)) and sold it later at $110 (\( P_t \)). The simple return would be:

\[ R_t = \frac{110 - 100}{100} = \frac{10}{100} = 0.10 \]

Which is equivalent to a 10% return on the investment.

### Note:

Simple returns are particularly useful when dealing with assets that do not produce cash flows between the beginning and ending period, such as stocks without dividends. For assets that provide interim cash flows, like bonds with coupon payments, the total return (accounting for both price change and interim cash flows) would be more appropriate.

## Holding Period Returns (HPR)

The Holding Period Return (HPR) represents the total return on an investment over a given period, accounting for all cash flows and capital gains or losses. The holding period can range from a single day to several years, depending on the context.

### Holding Period Return Formula:

The formula for the holding period return is:

\[ HPR = \frac{P_t + D - P_{t-1}}{P_{t-1}} \]

Where:
- \( HPR \) is the holding period return.
- \( P_t \) is the ending price of the asset.
- \( P_{t-1} \) is the beginning (or purchase) price of the asset.
- \( D \) is the cash dividend or cash flow received during the holding period.

### Interpretation:

- If the \( HPR \) is positive, it indicates a profit over the holding period.
- If the \( HPR \) is negative, it suggests a loss over the holding period.
- The value is often expressed as a percentage to show the percentage gain or loss. For instance, a value of 0.07 or 7% means the asset's total return (including dividends or cash flows) was 7% over the holding period.

### Example:

Let's say you bought a stock at a price of $100 (\( P_{t-1} \)), received a dividend of $5 (\( D \)), and sold it later at $110 (\( P_t \)). The holding period return would be:

\[ HPR = \frac{110 + 5 - 100}{100} = \frac{15}{100} = 0.15 \]

Which represents a 15% return on the investment over the holding period.

### Note:

Holding period returns are valuable for assessing the performance of an investment over a specified time frame, taking into account both capital appreciation and any additional income or cash flows. It provides a comprehensive view of the investment's performance.


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
