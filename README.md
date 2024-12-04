# Monte-carlo

## Overview

This project explores advanced numerical integration techniques, including:

- **Monte Carlo methods**
- **Quasi-Monte Carlo approaches**, such as Sobol sequences and Latin Hypercube Sampling
- **Haber's Estimators** for stratified integration
- Preliminary experiments with **Importance Sampling**

## Goals

- Estimate the integral of a complex function using different methods.
- Compare these methods based on precision, stability, and computational efficiency.

## Methods

### Monte Carlo Integration

- Uniformly samples random points over \([0,1]^d\).
- Approximates the integral as the mean of function evaluations.

### Quasi-Monte Carlo Integration

- Uses low-discrepancy sequences (e.g., Sobol, Latin Hypercube Sampling).
- Provides better space coverage than standard Monte Carlo methods.

### Haber’s Estimators

1. **First-order estimator**:
    - Stratifies \([0,1]^d\) into \(k^d\) hypercubes.
    - Convergence rate: \(n^{-\frac{1}{2} - \frac{1}{d}}\) for \(C^1\) functions.

2. **Second-order estimator**:
    - Similar to the first-order estimator but provides higher accuracy by using more evaluations.
    - Convergence rate: \(n^{-\frac{1}{2} - \frac{2}{d}}\) for \(C^2\) functions.

### Importance Sampling

- Samples points based on a distribution tailored to the function.
- In this project, a multivariate Gaussian distribution was tested.

## Results

- **Accuracy**: Haber’s Estimators and Quasi-Monte Carlo methods achieved the best precision.
- **Stability**: Haber’s second-order estimator and Quasi-Monte Carlo methods had the least variance.
- **Efficiency**: Monte Carlo is the fastest method; Importance Sampling showed potential but requires improved sampling distributions.

## Conclusion

This project demonstrates the strengths of Quasi-Monte Carlo methods and Haber’s Estimators in providing accuracy and stability. Importance Sampling shows potential but requires careful selection of sampling distributions. These methods offer valuable tools for advanced numerical integration.
