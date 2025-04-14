# Central Limit Theorem (CLT) Overview

The Central Limit Theorem (CLT) is one of the most fundamental concepts in stastics. 

It states that:

    When we take sufficiently large random samples from any population (regardless of its original distribution), the sampling distribution of the sample mean will approximate a normal distribution, even if the original dataset is not normally distributed.

## Why Does the CLT Matter?
1. Justifies the use of a Normal Distribution
    * Many stastical tests assume a normal distribution.
    * The CLT ensures that even if our data isn't normal, we can still use these tests assuming we have a large enough sample size.
2. Makes Inference Possible
    * We can invoke the CLT to make predictions about a population of interest using sample statistics, such as confidence intervals or hypothesis tests
3. Essential for Estimation
    * It is the reason why sample means tend to be reliable estimates of the population mean.

There are many useful properties of the Normal Distribution that make our lives as data scientists easier. By using the Central Limit Theorem, we can take advantage of these useful properties. 

*Note: A good rule of thumb for invoking the CLT is having a sample size of 30 or more observations. 

___

## Python Example of CLT

In [Google Colab](colab.research.google.com), run the following imports in a cell:

```python
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

[NumPy](https://numpy.org/) is an incredibly useful Python library for scientific computing, we'll use it to simulate some data.
[Seaborn](https://seaborn.pydata.org/) is another visualization library similar to Matplotlib.

Now, this next line of code is weird and confusing for beginners, and it is hard to explain in text, but it helps with reproducibility. All you need to know is that you should get similar numbers to me when running it and simulating our data in the same cell.

```python
np.random.seed(42)
```

In the same cell as the random seed, we're going to simulate a population. Thankfully, NumPy makes this very easy for us. We're going to simulate an [exponential distribution](https://en.wikipedia.org/wiki/Exponential_distribution). Do not worry about the properties of the exponential distribution at this moment. We only need it to showcase the CLT.

To create our population, write the following code:

```python
population = np.random.exponential(scale = 2, size = 10000)

```

Do not worry about what `scale=2` means, it was arbitrarily chosen.

Let's go ahead and plot our population:

```python
sns.histplot(population, bins=50, color='blue')
plt.title("Original Population Distribution (Exponential)")
plt.xlabel("Value")
plt.ylabel("Frequency")

```

This plot most definitely is **not** a normal distribution.

Now, let's see how we can sample our population and then compute the means of each of these samples.

```python
sample_size = 30 # Number of samples per draw
num_samples = 1000 # Number of sample draws
# calculate sample means
sample_means = [np.mean(np.random.choice(population, sample_size)) for i in range(num_samples)]
```

It is okay if you are struggling with how the `sample_means` variable was created. All you need to worry focus on is that we took 30 random samples of our population, caculated their mean, and then repeated that 1,000 times.

Now, in order to illustrate the CLT, let's plot our `sample_means`

```python
sns.histplot(sample_means, bins = 50, color = 'green')
plt.title(f'Sampling Distribution of Sample Means (n={sample_size})')
plt.xlabel('Sample Mean')
plt.ylabel('Frequency')
```

Our sample means are approximating a normal distribution!

---
## To Recap
Here's what we did:
* Simulated a population distrubted as an exponential distribution
* Sampled that distribution with a sample size of 30
* Took the mean of that sample
* Repeated that a bunch of times
* Plotted the distribution of our sample means
