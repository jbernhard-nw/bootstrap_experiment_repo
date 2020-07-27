# Bootstrap Experiment Repository

This library creates a dataset related to a landing page clickthrough, conversion, and revenue funnel.  

The resulting plots are stored in `./results/`.

You can run and store the results by running:

```
ipython bootstrap_experiment.py
```

By updating the `main` function, you can increase the sample size for the original sample created.  In the current script, there are 10,000 samples in each variant.

Additionally, the probability of conversion can be changed in the `create_data` function by changing the lines associated with:

```
result_1 = np.random.binomial(1, 0.10, version_1_sample)
result_2 = np.random.binomial(1, 0.07, version_2_sample)
```
to use probabilities other than `0.10` and `0.07`.  

The revenue numbers are also in the `create_data` function in relation to the following lines:

```
product_prices = [20, 40, 60, 80, 100, 150]
odds_result_1 = [0.5, 0.2, 0.1, 0.1, 0.05, 0.05]
odds_result_2 = [0.3, 0.1, 0.1, 0.1, 0.2, 0.2]
```

Here you can simulate data associated with different prices by changing `product_prices` or with the odds of those prices occurring in the dataframe by updating either `odds_result_1` or `odds_result_2`.  
