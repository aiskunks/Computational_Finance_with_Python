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

## Annualized Returns

Annualized return is a method used to express an investment's return (usually a portfolio's return) on an annual basis, taking compounding into account. It provides a clearer picture of the return over time, especially for holding periods that are not one year.

### Annualized Return Formula:

For investments held over multiple years, the annualized return can be calculated using the formula:

\[ \text{Annualized Return} = \left(1 + \text{HPR}\right)^{\frac{1}{n}} - 1 \]

Where:
- \( \text{HPR} \) is the total holding period return.
- \( n \) is the number of years of the holding period.

### Interpretation:

- The annualized return provides an average yearly return rate, giving a better perspective of an investment's performance across time.
- This figure is especially useful when comparing investments of different durations.

### Example:

Suppose you have a holding period return (HPR) of 50% over a 2-year period. The annualized return would be:

\[ \text{Annualized Return} = \left(1 + 0.50\right)^{\frac{1}{2}} - 1 \approx 0.2245 \]

This translates to approximately 22.45% annual return, which means the investment grows on average by this rate each year for the given period.

### Note:

When evaluating investments, it's crucial to consider both the holding period return and the annualized return. The latter is particularly helpful in comparing the performance of investments held for different lengths of time. By annualizing returns, investors can determine which investments are more effective in generating profit on an annual basis.

## Log Returns (Continuously Compounded Returns)

Log returns, also known as continuously compounded returns, provide a way to measure returns that is particularly useful for mathematical and statistical analyses. They are typically used because of their nice properties when aggregating over time and when products of returns are involved.

### Log Return Formula:

The log return for a single period is calculated using the formula:

\[ r_t = \ln\left(\frac{P_t}{P_{t-1}}\right) \]

Where:
- \( r_t \) is the log return at time \( t \).
- \( P_t \) is the asset price at time \( t \).
- \( P_{t-1} \) is the asset price at the previous time (e.g., the previous day or month).

### Interpretation:

- Log returns can be additive across time, unlike simple returns. For instance, the cumulative log return over multiple periods is just the sum of the log returns over those periods.
- They transform the process of obtaining returns from a multiplicative one (as with simple returns) to an additive one, simplifying certain mathematical and statistical operations.

### Example:

Suppose an asset has a price of $100 on day 1 and $105 on day 2. The log return for day 2 would be:

\[ r_2 = \ln\left(\frac{105}{100}\right) \approx 0.04879 \]

This translates to a log return of approximately 4.879%.

### Note:

Log returns are commonly used in financial econometrics, time series analysis, and other areas of finance where mathematical tractability and consistency are needed. They are especially convenient when analyzing the returns of assets over a long period or when conducting multiperiod analyses.

## Annualized Log Returns (Continuously Compounded Annual Returns)

While log returns give the return of an asset over a specific period (like a day or month), it's often useful to know what the return would be over a standard time period, like a year. This helps in comparing returns across different assets or investments. Annualized log returns allow us to express returns on a standardized yearly basis.

### Annualized Log Return Formula:

Given a log return \( r \) over a period \( t \) and assuming \( n \) such periods make up a year, the annualized log return is calculated using:

\[ R_a = n \times r \]

Where:
- \( R_a \) is the annualized log return.
- \( r \) is the average log return for the given period.
- \( n \) is the number of periods in a year (e.g., if you're working with daily returns, and assuming 252 trading days in a year, \( n = 252 \)).

### Interpretation:

- Annualized log returns provide a way to compare the performance of assets over equivalent yearly periods.
- This method of annualizing assumes the return compounds in a continuously compounded manner over the course of the year.

### Example:

Assuming you have a daily log return (for a trading day) of 0.001 and there are 252 trading days in a year, the annualized log return would be:

\[ R_a = 252 \times 0.001 = 0.252 \]

This translates to an annualized log return of 25.2%.

### Note:

It's essential to use the correct number of periods for \( n \) depending on the data frequency (daily, monthly, quarterly, etc.) to get accurate annualized returns.




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
