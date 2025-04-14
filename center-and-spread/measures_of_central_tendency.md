# Measures of Central Tendency

---

## Getting Setup

Go ahead and open a new notebook in [Google Colab](https://colab.research.google.com/) and run the following Python code.

*Note: It is recommended to type out the code provided throughout the pre-work. It will help develop some muscle memory and get you prepared for the Bootcamp!*

You can execute the code in the cell by either clicking the little "Play" button or hitting Shift+Enter.

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

- **Variance** (\(\sigma^2\) for population, \(s^2\) for sample) measures how far each data point is from the mean. It is calculated as the average of the squared differences from the mean.
- **Standard Deviation** (\(\sigma\) for population, \(s\) for sample) is simply the square root of the variance. It tells us, on average, how much the values in a dataset differ from the mean in the same units as the data.

### Formulas

#### Population Variance
```math
\sigma^2 = \frac{\sum (x_i - \mu)^2}{N}
```

#### Sample Variance
```math
s^2 = \frac{\sum (x_i - \bar{x})^2}{n-1}
```

#### Population Standard Deviation
```math
\sigma = \sqrt{\frac{\sum (x_i - \mu)^2}{N}}
```

#### Sample Standard Deviation
```math
s = \sqrt{\frac{\sum (x_i - \bar{x})^2}{n-1}}
```

Where:
- \(x_i\) represents each individual data point.
- \(\mu\) is the population mean.
- \(\bar{x}\) is the sample mean.
- \(N\) is the total number of data points in the population.
- \(n\) is the number of data points in the sample.

We will calculate these by hand and check our work with Pandas as usual.

First, let's calculate the mean of price (You can use the `price_mean` variable created earlier if you still have it defined).

```python
price_mean = diamonds['Price'].mean()

```

Pandas defaults to the *sample* variance, so we'll do that formula in the following steps:
    * Subtract the mean price from each price
    * Square that difference
    * Sum up those numbers
    * Divide them by the number of values (subtracted by 1 for sample variance)

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