# Source:
1. BLOCKCHAIN_PRICE_URL = "https://api.blockchain.info/charts/market-price?timespan=all" (Bitcoin Historical Price)
2. Yfinance (Gold)
---
## Bitcoin Historical Price Chart
![[blockchain._9_0.png]]

y = m * x + b

price = m * day + b
when day is 0 -> price = b (initial value)
price = m * day + initial value

When initial value = 0 
price = m * day_since_the_first_day_of_the_innitial_value
price = m * (day_current - day_initial)

m = price / (day_current - day_initial)

# Analysis
## 1. Using Logarithmic rather than Linear scale

- Bitcoin has gone through many orders of magnitude within a few years -> Going through so many orders of magnitude is unusual for a financial instrument, and the linear chart of Bitcoin doesnt tell us much rather than Bitcoin is a risky investment due to its fluctuation.

- Any price swings close to the present are so large in magnitude compared to the price in the past, that past prices seem meaningless. However, to make sense of a long-term price trend, all past prices should have some importance. The reason for the above effect is that using a linear scale is inconvenient for anything that goes through so many orders of magnitude -> Applying Logarithmic to have a deeper insight.


y= m * x + b


### $Log_{10}(Price)$
![[blockchain._14_0.png]]

### $Log_{10}(Price) \text{ vs } Log_{10}(Time)$
![[blockchain._16_0.png]]

m = log_price / (log_(day_current) - log_(day_initial))

Linear Regression simply a mathematical equation that calculates the strength in a relationship 

y_1 = m * x + b
y_2 = m_2 * x_2 + b
y_3 = m_3 * x_3* + b
R^2


```
a = [[Days_Since_The_FIRST][Price],
[Days_Since_The_FIRST ][y1],
[x2][y3]]

b , x= [x1, x2]
relatsionhip between elements a 2
```



## 2. Applying Linear Regression
- Since both axes are already in $log_{10}$ scale, a linear regression on `log_days` vs `log_price` directly gives us the power law fit (a straight line in $log-log$ space = a **power law** in linear space).
- Since its linear, we have $y=mx+b$.
- We know that:
    1. $y$ = Price
    2. $m$ = SLOPE (Rate of Change)
    3. $x$ = Time (Days Since The Genesis)
    4. $b$ = Intercept (The minimum value of Bitcoin since the beginning )
- With this equation:
    - `Price` = `How fast the value grows` * `Time` + `Initial Value`
-------
#### Power Law Functin:

$$f(x) = a * x ^m$$

$$m = \text{ Rate of Change } \quad | \quad x = \text{time} \quad | \quad a = \text{Initial Value}$$
---
#### Bitcoin Power Law:

$$P(t) = A * t^n$$


$$n = \text{ Rate of Change } \quad | \quad t = \text{time} \quad | \quad A = \text{Initial Value}$$

---------------------
**Linear Regression function also produces:**
1.$$R^2 \newline \text{How close is the linear relationship}$$
2.$$P-\text{Value} \newline \text{The odd that the relationship was never real}$$
3.$$\text{Stdandard Error} \newline \text{Doubts in the relationship. Uncertainty}$$


| Statistic               | Value                  | Good / Bad | Interpretation                                       |
| ----------------------- | ---------------------- | ---------- | ---------------------------------------------------- |
| $R^2$                   | **95.99%**             | Good       | *Price* and *Time*. $R^2 = $ 96% compability         |
| $P\text{-Value}$        | **0**                  | Good       | Not Random, and value grows based on a stable system |
| $\text{Standard Error}$ | Close to 0; **0.0304** | Good       | Rate of Growth is Accurate                           |


---

**The growth of Bitcoin clearly follows the Power Law Theory**

$$y = mx + b$$

$$Log_{10}(Price) = \text{slope} * Log_{10}(Time) + \text{intercept}$$

---
-> Raise to the Power of 10 to get back the actual price

$$\text{Price} = 10^{intercept + slope \quad * \quad log_{10}(\text{time})}$$

-> Rewrite using Log Rules:

$$\text{Price} = 10^{Intercept} * \text{time}^{\text{Growth Exponent}}$$

----------------
$$\text{ Price} = 10^{-16.3265} * \text{days since the genesis}^{5.6377}$$

**The relationship between Price and Time $R^2$ improves as time passes**![[blockchain._24_0.png]]

### Graph The Regression Line
- Which is the predicted growth
![[blockchain._25_0.png]]

Parallel Shifting

$$log_{10}(Price) = slope × log_{10}(days) + (intercept + k)$$
$$Price = 10^{(intercept + k)} × days^{slope}$$

- Minimum Residuals: k = min(residuals)

- Maximum Residuals: k = max(residuals)

----------

PriceLowerBound = $$slope × log_{10}(days) + (\text{intercept + min(residuals)})$$

![[blockchain._27_0.png]]
 
 PriceUpperBound = $$slope × log_{10}(days) + (\text{intercept + max(residuals)})$$
![[Pasted image 20260506131853.png]]

Mid-band lines: halfway between each bound and the main regression

1. MidLower = $$slope × log_{10}(days) + (\text{intercept + min(residuals) / 2 })$$
2. MidUpper = $$slope × log_{10}(days) + (\text{intercept + max(residuals) / 2 })$$

![[blockchain._30_0.png]]
==Combine them together, we get **Bitcoin Ranbow Chart**==

![[blockchain._31_0.png]]


**The Power Law on the $log_{10}{Price} \text{ vs } Time$**
![[blockchain._32_0.png|697]]


Power Law in Gold?
![[blockchain._42_1.png]]


