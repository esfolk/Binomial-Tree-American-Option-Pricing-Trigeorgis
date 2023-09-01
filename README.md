# Binomial-Tree-American-Option-Pricing-Trigeorgis

Trigeorgis pricing is an enhanced binomial options pricing model developed by Lenos Trigeorgis in 1991. Some key features:

- It is an extension of the Cox-Ross-Rubinstein (CRR) binomial model.

- The standard CRR model matches the first 2 moments of the binomial distribution to the lognormal distribution.

- Trigeorgis pricing matches the first 4 moments of the binomial to the lognormal.

- This provides greater accuracy in approximating the continuous lognormal distribution.

- It uses a general probability p for the up move instead of 50% probability.

- The up/down movements and probability p are numerically calibrated to match the first 4 moments.

- This is done by solving a system of 4 equations relating the binomial and lognormal moments.

- The extra calibration provides higher accuracy in pricing options compared to CRR.

- It retains the flexibility of binomial trees to allow early exercise of American options.

- Overall, it improves the precision of the binomial model while keeping the implementation tractable.

The Trigeorgis model is widely used in practice when needing higher accuracy than CRR, but also needing to handle American options where closed-form Black-Scholes is not applicable. The four moment matching bridges the gap between discrete binomial and continuous lognormal.
