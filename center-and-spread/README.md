<h1>
  <span class="headline">Math Prework</span>
  <span class="subhead">Measures of Center and Spread</span>
</h1>

## Measures of Center and Spread ( 50 min )

*author: [Matt Brems](https://www.linkedin.com/in/matthewbrems/) : Lead Instructor, Data Science Immersive, Washington, D.C.*

----
<br>

Goldilocks wanted a bed that was not too hard, or too soft, or too hot, or too cold. Like Goldilocks, you might want to find that value that’s right in the middle. But when you’re dealing with a large, complex data set, that can be more complicated than it sounds. In this lesson, we’ll dive into the statistics that will help you see the range of options and find where “center” actually is.

## Topics

- Descriptive and Inferential Statistics
- Measures of Center and Spread
- Standard Deviation and Range
- Outliers

### **Learning Objectives**

By the end of this lesson, you'll be able to:

- Identify the difference between descriptive and inferential statistics.
- Explore calculating basic measures of spread.

## Descriptive Statistics

*“Most people check their phones 58 times a day.”*

*“Customers who switch to our insurance save &#36;200 a year on average.”*

*“This was the coldest winter on record.”*

How would you begin to make sense of this data?

The reality is that you’ve been given bits of information in the form of descriptive statistics your entire life, but you may not have thought about it in those exact terms.

**Descriptive statistics** focus on summarizing, describing, and understanding the data we observe.

## Descriptive Statistics IRL

Let’s say you’re a marketing analyst for [Etsy](https://www.etsy.com/), a website where people can purchase artisanal products.

You have data detailing how many purchases have been made per hour over the past six months.

Your manager is eager to hear how shopping numbers have been, so you want to share the data you’ve collected. You could recite every hourly total and come to a fuzzy conclusion about what purchasing habits *generally* look like. But your manager doesn’t have time for you to list out all of those numbers.

Instead, you could describe your data with certain kinds of numbers that will quickly get your point across: **measures of center** and **measures of spread**.

First, we’ll talk about measures of center.

## What Are Measures of Center?

Measures of center are exactly what it sounds like: Ways to describe the middle (i.e., measure the center) of your data.

It turns out that there are a few different ways to describe the middle of your data. We’ll cover the three most common here: **mean**, **median**, and **mode**.

## Measures of Center

<a href="https://generalassembly.wistia.com/medias/qr0cpm0v1i"><img src="https://embed-ssl.wistia.com/deliveries/af56ae7e5a709fb7ab6105fa1dc37819.jpg?image_crop_resized=900x506&image_play_button=true&image_play_button_size=2x&image_play_button_color=222222e0" alt="center" width="450" height="253" /></a>


### Measures Of Spread

You’ve now navigated measures of center by calculating the most common ways to describe the middle of your data set: mean, median, and mode. Congrats! 🎉

But does this tell the whole story? Not quite.

It’s as if you read the plot summary of a movie on Wikipedia. You’d know a lot about the movie, but not *everything*. We’re doing something similar here — taking our full data set (the movie) and condensing it down to a summary (the Wikipedia post).

We can get a more complete picture of the story if we calculate our measures of center along with **measures of spread**.

## Visualizing Measures of Spread

Think back on our Etsy scenario — examining how many purchases have been made every hour over the past six months. It’s not enough to just share the mean or median, because those numbers don’t tell the whole story!

For example, both of these histograms have a mean and median that are exactly 14:

<img src="./assets/spread.png" width="700" />

<br>

Your manager, when faced with these data sets, might make different decisions about how to proceed. We want more information than just the measures of center.

**Measures of spread** — range, standard deviation, and variance — can help us understand how dispersed (spread out) our data is.


### Range

**Range** is an easy way to measure the spread of your data.

We find the largest and smallest values in our data, then calculate the difference between the two.

Let’s use Histogram 1 as an example:

<img src="./assets/range.png" width="500" />

<br>

If we wanted to calculate the range here, 21 (the largest value) - 7 (the smallest value) = **14** (the range).

## Standard Deviation

Another way to measure the dispersion in our data is to calculate the **standard deviation**. Standard deviation, denoted σ (“sigma”), is approximately the average distance of every data point from the mean.

Two factors to keep in mind when determining standard deviation:

- **Low standard deviation**: The mean is close to zero and the data isn’t very spread out.
- **High standard deviation**: The mean is far from zero, and there is a lot of spread in our data.

<img src="./assets/std.png" width="700" />

<br>

In Scenario 1, our standard deviation is exactly zero! The behavior of our shoppers doesn’t deviate at all; each hour has the exact same results.

In Scenario 2, different hours reflect different shopping patterns. Our data is more spread out than in the first scenario, which helps us better understand our data.

### Walk-Through: Calculating Standard Deviation

The formula for the standard deviation of a data sample is:

$$\sigma = \sqrt{\frac{\sum\limits_{i=1}^{n} \left(x_{i} - \bar{x}\right)^{2}} {n-1}}$$

Let’s walk through the steps of this formula to find the standard deviation for the data set [3, 4, 5].

1. Calculate the mean.
2. Take the difference of each observation and the mean.
3. Square each result from Step 2.
4. Sum each result from Step 3.
5. Divide the result of the previous Step by $(n−1)$, where $n$ is the number of observations.
6. Take the square root of this result.

Before scrolling down, try to calculate these totals yourself!

## Calculating Standard Deviation — Solved!

Here are our results:

1. Calculate the mean. **The mean is 4**.
2. Take the difference of each observation and the mean. **The differences are -1, 0, and 1**.
3. Square each result from Step 2. **The squared results are 1, 0, and 1**.
4. Sum each result from Step 3. **The sum is 2**.
5. Divide the result of the previous step by $(n−1)$, where $n$ is the number of observations. **2 / (3-1) = 2/2 = 1**.
6. Take the square root of this result. **The square root of 1 is 1**.


The standard deviation of the data set [3, 4, 5] is **1**.

Our mean value is **4** and our lowercase sigma represents **one standard deviation** to the right or left of the mean.

<img src="./assets/stds.png" width="700" />

<br>

### Variance

Fun fact: Had we stopped at Step 5, we would have found the **variance**: 
a rough idea of how spread out our data is.

So, in our walk-through example...

1. Calculate the mean.
2. Take the difference of each observation and the mean.
3. Square each result from Step 2.
4. Sum each result from Step 3.
5. Divide the result of the previous step by $(n−1)$, where 
$n$ is the number of observations. **2 / (3-1) = 2/2 = 1 (the variance)**.

Variance is very similar to standard deviation and is seen frequently throughout data science. The smallest a variance gets is zero, but it can be infinite with numbers in the millions or billions (and beyond).

However, one downside of using variance is that our units are squared! In our example above, the number 2/3 here means 2/3 visitors squared. That doesn’t mean anything in the real world!

## Outliers

Measures of center and spread aren’t just used to quickly communicate important information about your data.

They can also be used to identify extreme points that fall far outside the pattern of your data.

For example, suppose we have this data set, reflecting the number of purchases made each hour:

    [11, 12, 13, 13, 14, 14, 14, 15, 15, 16, 17] 
    
Suppose that, in the next hour, the number 41 was added to this data set, indicating that 41 purchases had been made.

We might refer to the value of 41 as an **outlier**.

## Navigating Outliers

**Outliers** are numbers that fall beyond the pattern of our data.

It may be important for us to consider outliers because they can have severe implications on business decisions!

For example...

- If there were 41 purchases in an hour, do we need to order more product sooner than we thought?
- Was our marketing team doing something differently that we should continue doing?
- Is it possible that 41 was simply a typo, and it actually meant 14 people?

While there’s no one prescribed way to identify and handle outliers, there is one common way to spot potential outliers that involves the mean and standard deviation.

### How to Identify Outliers

One way to identify potential outliers involves calculating the mean and the standard deviation.

Take our data from earlier:

    [11, 12, 13, 13, 14, 14, 14, 15, 15, 16, 17, 41]
    
The mean of this data is **16.25** and the standard deviation is about **7.6**.

Any points that fall below the mean minus three times the standard deviation or any points that fall above the mean plus three times the standard deviation may be considered outliers.

$16.25 - 3 * 7.6 = -6.55$

$16.25 + 3 * 7.6 = 39.05$

Any points below -6.55 or above 39.05 may warrant further investigation, as they may be outliers!

---
# Measures of Central Tendency: See it in Python!

---

## Getting Set up

Go ahead and open a new notebook in [Google Colab](https://colab.research.google.com/) and run the following Python code.

*Note: It is recommended to type out the code provided throughout the pre-work. It will help develop some muscle memory and get you prepared for the Bootcamp!*

Execute the code in the colab cell by either clicking the little "Play" button or hitting Shift+Enter.

```python
import pandas as pd
import matplotlib.pyplot as plt
```

A refresher about imports. Often times we'll need to use code that's already been developed. These **libraries** provide pre-written code for common tasks, saving us time and effort.

We're starting off importing [Pandas](https://pandas.pydata.org/), one of the most widely used libraries in Python for data analysis.

Additionally, we're also importing [Matplotlib](https://matplotlib.org/), a commonly used data visualization library.

We will dive much, much deeper into these libraries during the Data Science Bootcamp!

---

## Reading in the Diamonds Dataset

We're going to create a variable called `diamonds`. This is a well-known dataset for getting acquainted with data analysis.

*(It's okay if you want to copy and paste this code, don't worry about typing out the link.)*

```python
diamonds = pd.read_csv('https://raw.githubusercontent.com/pycaret/pycaret/refs/heads/master/datasets/diamond.csv')

```

The `diamonds` variable is what's called a [Pandas DataFrame](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html)

To make this exercise simpler, we're only going to use the numeric columns in the data set and limit ourselves to 100 rows. 

We'll do this with the following code:

```python
diamonds = diamonds.loc[:99, ['Carat Weight', 'Price']].copy(deep = True)

```

and then inspect the first 5 rows with `.head()`

```python
diamonds.head()
```

If you're seeing the first five rows of the data set and only columns for `Carat Weight` and `Price`, then you're good to go!

---

## Mean or Average

The Mean or Average is calculated by summing all the values, then dividing the sum by the number of values.

We will manually calculate this for the `Price` column in our `diamonds` data and then use Pandas to check our work.

```python
price_sum = 0 # create an incrementor variable to keep track

for i in diamonds['Price']: # accessing all the values in the Price col
    price_sum += i # incrementing price_sum by each value

price_sum # Seeing what value we got for the price_sum
```

```python
price_mean = price_sum / len(diamonds['Price'])

price_mean
```

Now let's compare to Pandas
```python
diamonds['Price'].mean() # We can use the Pandas .mean() method directly on the Price column
```

And we should have the same numbers!

---

## Median

Median is another central tendency measure, but it is more commonly used when a dataset has a lot of outliers.

We calculate the median by sorting all of the data points from smallest to largest, then identifying the number in the middle of the ordered dataset.

If there is an odd number of values, the middle value is the median.

If there is an even number of values, the average of the two middle values is the median.

First, let's sort our `Price` column and then find the middle values

```python
sorted_prices = sorted(diamonds['Price']) # using built-in Python sorted function
```

We're only using 100 rows from the original dataset, so it's easy to find the middle values of it. 

We'll start by finding the middle value's index position:

```python
len(sorted_prices) / 2 # using built-in len (length) function and dividing by 2 to find middle value index

```

Unsurprisingly, we should get 50. Now let's find the middle two values.

```python
prices_sorted[49] # remember that Python is zero-indexing so we subtract 1 to get the left middle value

prices_sorted[50] # and use the other one as the right middle value
```

Then we average these two numbers together:

```python
(prices_sorted[49] + prices_sorted[50]) / 2

```

And check our work with Pandas `.median()` method!

```python
diamonds['Price'].median()
```

---

## Mode

The mode is the value that shows up most frequently. The way of doing this without Pandas is fairly tedious and beyond the scope of the pre-work, so we'll use Pandas `.mode()` method.

```python
diamonds['Price'].mode()
```

---

## Calculating Range

The range is given by the biggest number in the list of values, minus the smallest values.

The max and min values often of interest themselves, too!

```python
# Using the built-in max and min functions
max(diamonds['Price']) - min(diamonds['Price'])
```

---

## Variance and Standard Deviation

Variance and standard deviation are two important statistical measures that describe the spread or dispersion of data.

- **Variance** ($\sigma^2$ for population, $s^2$ for sample) measures how far each data point is from the mean. It is calculated as the average of the squared differences from the mean.
- **Standard Deviation** ($\sigma$ for population, $s$ for sample) is simply the square root of the variance. It tells us, on average, how much the values in a dataset differ from the mean in the same units as the data.

### Formulas

#### Population Variance

$$\sigma^2 = \frac{\sum (x_i - \mu)^2}{N}$$

#### Sample Variance

$$s^2 = \frac{\sum (x_i - \bar{x})^2}{n-1}$$

#### Population Standard Deviation

$$\sigma = \sqrt{\frac{\sum (x_i - \mu)^2}{N}}$$

#### Sample Standard Deviation

$$s = \sqrt{\frac{\sum (x_i - \bar{x})^2}{n-1}}$$

Where:
- $x_i$ represents each individual data point.
- $\mu$ is the population mean.
- $\bar{x}$ is the sample mean.
- $N$ is the total number of data points in the population.
- $n$ is the number of data points in the sample.

We will calculate these by hand and check our work with Pandas as usual.

First, let's calculate the mean of price (You can use the `price_mean` variable created earlier if you still have it defined).

```python
price_mean = diamonds['Price'].mean()

```

Pandas defaults to the *sample* variance, so we'll do that formula in the following steps:
- Subtract the mean price from each price
- Square that difference
- Sum up those numbers
- Divide them by the number of values (subtracted by 1 for sample variance)

This sounds like a lot of work, but we can actually do it in one line!

```python
# n-1 for sample variance in denominator
sum((diamonds['Price'] - price_mean)**2) / (len(diamonds['Price']) - 1)
```

Check our work with Pandas:

```python
diamonds['Price'].var()
```

What is nice about about calculating Standard Deviation, is that it's only taking the square root of the Variance!

```python
diamonds['Price'].var()**2
```

or use the Pandas `.std()` method.

```python
diamonds['Price'].std()
```

---

We've manually calculated some very useful measure of central tendency and spread. While knowing how these statistics are calculated, you'll never need to (and shouldn't) do things manually when we have functions that can do it for us. Pandas has a very helpful method called `.describe()` that will show us most of these statistics in a concise table. You can call it either for a single variable or the entire dataset.

```python
diamonds['Price'].describe()
```

You'll see the count, mean, standard deviation, minimum, maximum, 25th percentile, median (50th percentile), 75th percentile, and the max for your numeric variables in your dataset.

## Wrap up

Now we know the difference between measures of spread and measures of central tendency! These numbers are summaries that help us paint a fuller picture of our data’s story (and are particularly useful when making business decisions).

### Up Next...

After some knowledge checks we will look at Measures of Center and Spread.
