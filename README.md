# Portfolio Optimization

This repository contains the code and research findings related to a systematic portfolio optimization approach for German retail households. The research, based on the outlined sections of a thesis, follows the following key steps:

## Table of Contents

- [Research Overview](#research-overview)
  - [Introduction](#introduction)
  - [Methodology](#methodology)
  - [Numerical Simulation](#numerical-simulation)
  - [Portfolio Measures](#portfolio-measures)
  - [Additional Risk and Return Measures](#additional-risk-and-return-measures)
  - [Cash Inclusion](#cash-inclusion)
  - [Portfolio Optimization Steps](#portfolio-optimization-steps)
  - [Portfolio Types](#portfolio-types)
  - [Constraints](#constraints)
- [Data Collection](#data-collection)
- [Scaling Data](#scaling-data)
- [Optimization Results](#optimization-results)
- [Contact](#contact)

## Research Overview

### Introduction

This research focuses on optimizing the portfolios of German retail households, including the introduction of two alternative asset classes: buyout and venture capital (VC).

### Methodology

1. **Asset Opportunity Set Creation**: Construct an asset opportunity set reflecting typical investments made by German households.

2. **Historical Performance Analysis**: Analyze the historical performance of asset classes using various risk and return measures.

3. **Household Portfolio Analysis**: Assess the existing household portfolio to create a benchmark for later optimizations.

4. **Portfolio Optimization**: Optimize asset allocation to increase expected return while controlling risk.

5. **Evaluation of Alternative Assets**: Assess the impact of introducing buyout and VC to the household portfolio.

### Numerical Simulation

Optimize portfolios using historical performance data from 2001 to 2022, involving three stages:

1. **Fixed Cash + No Alternatives**: Optimization with fixed cash holdings and no alternative assets.

2. **Variable Cash + No Alternatives**: Optimization with variable cash levels while maintaining a minimum cash liquidity of 12%.

3. **Variable Cash + With Alternatives**: Introduction of alternative assets buyout and VC to the portfolio.

### Portfolio Measures

- **Expected Portfolio Return**: Computed by aggregating expected returns of constituent asset classes based on their weights.
- **Portfolio Variance**: Calculated as the weighted sum of covariances among asset pairs using historical return covariance values.
- **Portfolio Domination**: Identify portfolios offering superior risk-return trade-offs to form the efficient frontier.

### Additional Risk and Return Measures

- Compute various additional measures, including CVaR, skewness, kurtosis, median, geometric mean, Bayes-Stein, and illiquidity-penalized return for simulated portfolios.

### Cash Inclusion

Include cash as a financial asset in the optimization process to enhance expected return while mitigating increased risk through diversification.

### Portfolio Optimization Steps

The optimization is divided into three steps:

1. **Optimization on Existing Asset Set**: Optimize the household portfolio based on the existing asset opportunity set while keeping cash holdings constant.

2. **Optimization with Variable Cash**: The same optimization as step 1 but with variable cash levels.

3. **Introduction of Alternative Assets**: Include buyout and VC in the household asset pool to assess their marginal contribution to the previously optimized portfolio.

### Portfolio Types

During each simulation step, compute Markowitz Portfolios, Min-Variance Portfolio, Max-Sharpe Portfolio, and Optimal Risk-Matching Portfolio.

### Constraints

The optimization is performed from the perspective of a long-only retail investor with a maximum allocation constraint of 33% to individual assets.

## Data Collection

The data used in this research consists of 10 series of index and return data spanning from 2001 to 2022, representing various asset classes relevant to German household investments. The data sources and asset class proxies are detailed in the repository.

## Scaling Data

Since data series have varying granularities, the monthly series are scaled up to create a dataset with matching quarterly granularity. Return and standard deviation are annualized to better assess performance on a yearly scale.

## Optimization Results

The three-step portfolio simulation yields significant and nuanced insights into the general efficient performance dynamics and influence of venture and buyout on the portfolio. The efficient frontiers, derived from the 10 million portfolio simulations per step, are presented, highlighting the minimum-variance (red star), max-Sharpe as tangent (green star), and retail (purple star) portfolio. All other portfolios are further colored according to their Sharpe ratios. The evolution of the portfolio composition across varying levels of risk along the efficient frontier is pictured next to them. The first two detailed simulation results can be found in the Appendix and will be incorporated and discussed in the line-over-line performance comparison. They are used to measure the impact that each optimization step has and isolate the impact of the inclusion of buyout and VC. The highlight of the portfolio simulations is the final step, where the alternative assets are incorporated, enlarging the asset opportunity set:


<div style="overflow-x: auto;">
  <table style="width: 80%;">
    <tr>
      <td style="width: 50%;"><img src="Results/Efficient%20Frontier_v3.png" alt="Efficient Frontier"></td>
      <td style="width: 50%;"><img src="Results/Efficient%20Frontier%20Composition_v3.png" alt="Efficient Frontier Composition" width="1600"></td>
    </tr>
  </table>
</div>

## Contact

For more details, please refer to the original thesis document.

This repository contains the code and materials used in this research to facilitate transparency, reproducibility, and further exploration of the portfolio optimization methodology and findings. For questions or collaboration opportunities, feel free to contact me.

