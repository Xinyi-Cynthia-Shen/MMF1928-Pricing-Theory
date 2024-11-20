# Project 1: American Option Pricing

Related Files

- [Project 1 Code Vectorized](https://github.com/Xinyi-Cynthia-Shen/MMF1928-Pricing-Theory/blob/main/Project%201%20Code%20Vectorized.ipynb)
- [Project 1 Code](https://github.com/Xinyi-Cynthia-Shen/MMF1928-Pricing-Theory/blob/main/Project%201%20Code.ipynb)
- [Project 1 Report](https://github.com/Xinyi-Cynthia-Shen/MMF1928-Pricing-Theory/blob/main/Project%201%20Report.pdf)

## Overview

This project explores the pricing of American put options using a variation of the **Cox-Ross-Rubinstein (CRR)** model. The study derives branching probabilities under the **risk-neutral measure**, evaluates the exercise boundary of the American put option, and simulates stock price paths to analyze the option’s performance. Additionally, the project investigates hedging strategies, profit and loss (P&L) distributions, and stopping time behavior under varying market conditions.

The project is divided into two main sections:
1. **Pricing and Exercise Boundary Analysis** 
2. **Profit and Loss Analysis**

## Pricing and Exercise Boundary Analysis

### Implementation and Analysis
1. **Derive Branching Probabilities:**
   - Compute the probabilities of upward and downward movements of the stock price under the risk-neutral measure.
   - Ensure that the discounted stock price process remains a martingale.

2. **Exercise Boundary Plot:**
   - Determine the optimal exercise boundary for the American put option.
   - Plot the exercise boundary as a function of time \( t \) for different volatility (\( \sigma \)) and risk-free rate (\( r \)) values.

3. **Simulated Stock Paths:**
   - Generate two sample paths:
     - Path 1: The option is **exercised early**.
     - Path 2: The option is **not exercised** until maturity.
   - Simulate stock price movements using the derived branching probabilities and plot the paths relative to the exercise boundary.

4. **Hedging Strategy:**
   - Implement **delta hedging**, a dynamic strategy that minimizes the risk associated with small changes in the underlying stock price.
   - Plot the hedging strategy as a function of time for both sample paths.

5. **Sensitivity Analysis:**
   - Illustrate how the results (exercise boundary, sample paths, and hedging strategies) vary with changes in volatility (\( \sigma = 10\%, 20\%, 30\% \)) and risk-free rate (\( r = 0\%, 2\%, 4\% \)).

### Profit and Loss Analysis: Simulation and Analysis
1. **P&L and Stopping Time Distributions:**
   - Simulate 10,000 stock price paths.
   - Compute and analyze the distributions of:
     - **Profit and Loss (P&L):** Accounting for early and non-exercised options.
     - **Stopping Times:** The time points when the option is exercised early.
   - Record the **probability of exercise** to account for paths where the option is exercised early.

2. **Parameter Sensitivity:**
   - Repeat the P&L and stopping time analysis for various combinations of \( \sigma \) and \( r \).

3. **Realized vs. Assumed Volatility:**
   - Analyze scenarios where the **realized volatility** (\( \sigma = 10\%, 15\%, 20\%, 25\%, 30\% \)) differs from the **assumed volatility** (\( \sigma = 20\% \)) used for pricing the option.
   - Evaluate the impact on P&L and stopping time distributions when using a fixed exercise boundary.

## Key Findings

1. **Exercise Boundary:**
   - Higher volatility results in smoother and lower exercise boundaries at earlier time points, encouraging delayed exercise.
   - Higher interest rates lead to steeper boundaries, incentivizing earlier exercise due to the opportunity cost of holding the option.

2. **Simulated Paths:**
   - Early exercised paths cross the exercise boundary earlier, while non-exercised paths remain above the boundary until maturity.

3. **Hedging Strategy:**
   - Delta hedging varies significantly along the stock paths, with larger adjustments required for more volatile paths.

4. **Profit and Loss:**
   - Higher volatility increases the range of possible outcomes, leading to a broader P&L distribution.
   - Higher interest rates shift the P&L distribution toward lower values, reducing profitability due to discounting effects.

5. **Stopping Times:**
   - Higher volatility delays exercise times, while higher interest rates result in earlier exercises.

## Implementation Details

The project relies on Python and incorporates the following key functionalities:
- **Risk-neutral measure derivation:** Using mathematical modeling to derive probabilities for stock price movements.
- **Binomial tree construction:** For stock price and option value calculations.
- **Simulation:** Generating stock paths and evaluating exercise strategies.
- **Delta hedging:** Computing and visualizing dynamic hedging strategies.
- **Parameter analysis:** Exploring the effect of volatility and interest rate changes.

## Conclusion

This project provides comprehensive insights into the pricing and behavior of American put options. By incorporating sensitivity analyses, it highlights the significant impact of market parameters like volatility and interest rates on optimal exercise strategies, P&L outcomes, and hedging behavior.

For more detailed implementation, refer to the associated Python notebooks and report.
