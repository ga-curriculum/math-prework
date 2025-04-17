<h1>
  <span class="headline">Math Prework</span>
  <span class="subhead">Central Limit Theorem</span>
</h1>

## Central Limit Theorem ( 45 min )

*author: [Matt Brems](https://www.linkedin.com/in/matthewbrems/) : Lead Instructor, Data Science Immersive, Washington, D.C.*

----
<br>

The central limit theorem (CLT) is at the core of making inferences about large data sets — a primary part of the job of a data scientist. In this lesson, you’ll explore how CLT helps us explore and understand what’s happening under the hood: the story behind the data.

## Topics

- Central Limit Theorem
- Distributions

### **Learning Objectives**

By the end of this lesson, you'll be able to:

- Explore the statistical implications of the central limit theorem.
- Identify how and why you would sample a population.

## Symbols To Look Out For

During this lesson, you'll see some new and unusual mathmatical symbols, but never fear! GA is here to help...

**Symbol Key**

- Data: $X$

- Sample mean: $\overline{x}$

- All possible sample means: $\overline{X}$
 
- Variable: $n$

- Mean of first sample: $\overline{x}_1$

- Mean of second sample: $\overline{x}_2$

- Mean of third sample: $\overline{x}_3$


## Inferential Statistics

Let’s say you work for a polling company. You’re interested in understanding the landscape of voters for an upcoming election.

It’s not exactly efficient to survey the preferences of the entire U.S. population, so you choose to collect data from a group of 100 people.

Does that data tell the whole story of all voters? No, not really. But you, being the savvy data scientist that you are, can make an *inference* based on the data you do have.

Enter **inferential statistics**, where we focus on generalizing results from a sample to a larger population.

## Populations

To start determining voter trends and preferences, you may want to get to know your target audience, such as all individuals who will vote in an upcoming election.

That group of people? That’s your group of interest — your **population**.

<img src="./assets/pop.png" width="700" />

<br>


### Samples

Now, let’s say you want to take a closer look at this population to see which individuals tend to respond to questions about their voting preferences.

That’s your **sample** — a subset of the population.

<img src="./assets/sample.png" width="700" />

<br>

Using the mean of this sample, or the **sample mean**, implies that you can use that smaller sample to draw conclusions about the larger population.

When we calculate a sample mean ($\overline{x}$), we treat it as one observation from the distribution of all possible sample means ($\overline{X}$).

## Normal Distribution

Lots of real-world phenomena follow a **normal distribution**: data near the mean occurring more frequently than data that is further from the mean.

If we know that $\overline{X}$ follows a normal distribution, we can then rely on this when conducting inference on a sample mean.

Take a look at this figure reflecting **three normal distributions**. It highlights how normal distributions typically appear — symmetrical around their mean, denser in the center, and less dense around the tails.

1. **Green (left) distribution**: Has a mean of **-3** and a standard deviation of **0.5**.
2. **Red (middle) distribution**: Has a mean of **0** and a standard deviation of **1**.
3. **Black (right) distribution**: Has a mean of **2** and a standard deviation of **3**.

<img src="./assets/normal.png" width="500" />

<br>

### Central Limit Theorem

How can we be sure that an assumption of normal distribution is accurate?

We turn to the **central limit theorem**.

The central limit theorem ensures the data ($X$) is accurate, whether or not the sample size distribution of data is normal and regardless of the distribution of the original data.

As the sample size increases, the margin of error decreases — no matter the shape of the population distribution. This is especially true for sample sizes of more than 30. The more samples you take, especially large ones, the more your graph of the sample means will look like a normal distribution.

## Sampling Distribution

Suppose we take a sample of $n$ observations from a population and record the mean of this sample.

We then replace all observations, pull another sample of $n$ observations from the same population, and record the mean of *that* sample.

Now, say we do this over and over again until we’ve recorded the mean of every possible sample of size $n$ from the population. This is known as the **sampling distribution** of $\overline{X}$.

### Central Limit Theorem in Practice

Let’s take a closer look at the central limit theorem and sampling distribution.

In the example below, we can see that as the sample size gets larger, the graph approaches a more normal distribution.

If $n$ is larger than $30$, then $\overline{X}$ is sufficiently close to normal. The larger the value of $n$, the better basis you’ll have for decision-making.

<img src="./assets/clt.png" width="550" />

<br>

## Visualizing the Central Limit Theorem

Take a look at these four histograms and what they represent:

- **One die**: Distribution of the sample mean for all possible samples of size $1$.
- **Two dice**: Distribution for samples of size $2$.
- **Three dice**: Distribution for samples of size $3$.
- **Four dice**: Distribution for samples of size $4$.

Notice that, as $n$ increases, the distribution becomes more normal.

<img src="./assets/dice.png" width="700" />

<br>

## Exploring the Central Limit Theorem

Let’s look at another example:

Suppose you roll a six-sided die. You roll it once and get a 5.

If you were to calculate the average of that roll, that average would be 5. We’d indicate this with $\overline{x}1=5$, saying that the mean of our sample is 5.

You decide to roll again, and this time you get a 3.

The mean of this second sample ($\overline{x_2}$) is **3**.

## Exploring the Central Limit Theorem (Cont.)

Let’s do this again, but instead use sample size $n=2$. In this case, we’ll roll the die twice and find the average:

$$Sample\ 1:\{1,1\}⟹ \overline{x_1}=1\\
Sample\ 2: \{1,2\}⟹ \overline{x_2}=1.5\\
Sample\ 3: \{1,3\}⟹ \overline{x_3}=2\\
...\\
Sample\ 36 :\{6,6\}⟹ \overline{x_{36}}=6$$


## More on the Central Limit Theorem

What if we were to do this for every possible sample of size 1? That would mean rolling a 1, 2, 3, 4, 5, and 6 exactly once each.

We’d use the random variable ($\overline{X}$) to represent all possible values of the sampling distribution ($\overline{x}$), along with how frequently we observe the sample mean of those values.

If we were to visualize this with a histogram, we get a flat chart in which values 1 through 6 are all equally likely.

<img src="./assets/hist.png" width="550" />

<br>

### Experimental Design

What would you do to ensure that your means of data collection, or your experiment, has been handled in the right manner?

**Experimental design** is concerned with validity, reliability, and replicability. It ensures that:

1. The question the experiment is trying to answer is clearly defined.

2. Sources of variability in the experiment are identified.

3. Descriptions exist of how participants were allocated — i.e., if they were randomly chosen or other methods were used.

## Experimental Design IRL

In data science, **sample protocol** is an important part of dealing with survey data (or *experiments*). Statistical significance should always be used when making decisions based on data, but it’s also important to consider *the types of questions being asked* and *who is answering them*.

For example, customers with bad experiences may be more likely to write reviews on a website than those with good experiences. Therefore, this does not necessarily mean that users are having more negative experiences than positive ones! Instead, it suggests that the results are biased toward dissatisfied customers.

If you know your data set contains biased answers, it’s up to you to decide how to deal with the data so that you can still get meaningful results.

---
# Central Limit Theorem (CLT) Overview

The Central Limit Theorem (CLT) is one of the most fundamental concepts in stastics. 

It states that:

*When we take sufficiently large random samples from any population (regardless of its original distribution), the sampling distribution of the sample mean will approximate a normal distribution, even if the original dataset is not normally distributed.*

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


## Wrap up

We’ve reviewed how to calculate, visualize, and analyze data using the central limit theorem. As you move throughout the course using sample data sets to estimate characteristics about large populations, recalling the central limit theorem will come in handy.

## Up Next...

After some knowledge checks we will look at Rules of Probability.
