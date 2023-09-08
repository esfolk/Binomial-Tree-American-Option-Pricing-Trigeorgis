
---

# American Option Pricing and Greeks using Binomial Trees

This repository provides a Python implementation for pricing American options (both Call and Put) and computing their Greeks (Delta, Gamma, Theta, Vega, and Rho) using binomial tree methods. The implementation is based on the scientific paper titled "Computation of Greeks Using Binomial Tree" by Yoshifumi Muroi and Shintaro Suda.

## Overview

The binomial tree model is a discrete-time method used for option pricing. In this implementation, we've used the Trigeorgis method, which is a variant of the binomial tree, to price American options and compute their Greeks.

## Features

1. **American Option Pricing**: Calculate the price of American Call and Put options using the Trigeorgis binomial tree method.
2. **Greeks Computation**: Compute the following Greeks for American options:
   - **Delta**: Measures the rate of change of the option price with respect to changes in the underlying asset's price.
   - **Gamma**: Measures the rate of change in Delta with respect to changes in the underlying asset's price.
   - **Theta**: Represents the rate of change of the option price with respect to time.
   - **Vega**: Measures the sensitivity of the option price to changes in volatility.
   - **Rho**: Represents the rate of change of the option price with respect to the interest rate.

## Usage

To use the provided code, initialize the `AmericanOption` class with the desired parameters (stock price, strike price, interest rate, volatility, time to maturity, and number of steps). Then, set the pricing strategy to `TrigeorgisPricing` and call the `price()` method to get the option price. To compute the Greeks, call the `greeks()` method.

```python
# Example
call_option = AmericanOption(S0=100, K=100, r=0.05, sigma=0.2, T=1, N=100, option_type='C')
call_option.set_pricing_strategy(trigeorgis_pricing)
price = call_option.price()
delta, gamma, theta, vega, rho = call_option.greeks()
```

## References

- Muroi, Yoshifumi, and Shintaro Suda. "Computation of Greeks Using Binomial Tree." [Link to Paper](https://pdfs.semanticscholar.org/6361/964cbcf2576ec3dbb3641eb2d4dde9c4c1d0.pdf)

---

This README provides a concise summary of the work done, the features of the code, a brief usage example, and references the scientific paper. 

