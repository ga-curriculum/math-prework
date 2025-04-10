[TODO] in general need the popups for incorrect responses as well.

## Raandom Variables

### Knowledge Check

Which of the following is an example of a continuous value?

Select the best answer.

- Incorrect: The number of home runs hit by Babe Ruth.

- Correct : The volume of water in all the earth's oceans.

- Incorrect: The number of employees in a company.

- Incorrect : The number of grains of sand on earth.

Correct: Because volume is a measurement, the volume of water in all the earth's oceans is indeed a continuous value.  We can always increase the decimal place to which the volume is measured to improve its accuracy.

### Knowledge Check

Which of the following random variables are correctly labeled as “CONTINUOUS” or “DISCRETE”?

Select all that apply.

[TODO]

Correct: That’s right! All of these are labeled correctly except for, “The length of a shadow cast by a willow tree.” This is a continuous variable, as we can always increase the decimal place to which the length is measured to improve its accuracy.

### Knowledge Check

Which of the following is an example of a discrete variable?

Select the best answer.

[TODO]

### Knowledge Check

What is the expected value of $x$?

[TODO]- image

Select the best answer.

- Incorrect: 0.35
- Incorrect: 0.75
- Incorrect: 1.5
- Correct: 1.1  The expected value of $x$ is 0+1(0.35)+2(0.15)+3(0.15) = 1.1

### Knowledge Check

Continuous data comes from quantities that can be ____________.

Select the best answer.

- Correct: Measured.  Continuous variables can be measured, while discreet variables can be counted
- Incorrect: Counted
- Incorrect: Both

### Knowledge Check

Which of the following is *not* an example of continuous data?

Select the best answer.

[TODO]

### Knowledge Check

You decide to collect several bottles of water and measure the volume of water each contains. Let $x$ be the number of milliliters of water in each bottle. What type of variable is $x$?

Select the best answer.

[TODO]

## Measures of Center and Spread

### Knowledge Check

What is the mean of the following values:

[13, 18, 13, 14, 13, 16, 14, 21, 13]

Select the best answer.

- Incorrect: 18
- Incorrect: 14
- Correct: 15
- Incorrect: 13

Correct:
(13+ 18+ 13+ 14+ 13+ 16+ 14+ 21+ 13)/ 9 = 15

### Knowledge Check

What’s the median in this set?

        [13, 13, 13, 13, 14, 14, 16, 18, 21]
Select the best answer.

- 14 (Correct)
- 13
- 18
- 21

Correct: If we line up these values from smallest to largest, we find the middle-most value is 14.

### Knowledge Check

What’s the mode in this set?

       [13, 18, 13, 14, 13, 16, 14, 21, 13]                       
Select the best answer.

- 14
- 16
- 13
- 21 (correct)

Correct: The value we see most often is the 13.

### Knowledge Check

What are the data types of `+42`, `1`, `False`, and `float(False)`, respectively?

- int, bool, bool, float
- int, int, bool, bool
- int, float, bool, bool
- int, int, bool, float (correct)

The built in float() function converts the value passed in into a float. Note that 1 by itself is an int, even though True is internally represented as 1.

### Knowledge Check

What is the variance of the values [4, 10, 16]?

Select the best answer.

[TODO]

### Knowledge Check

Suppose that we had **3** purchases at 9:00 this morning, **4** purchases at 10:00, and **5** purchases at 11:00.

This makes a data set of [3, 4, 5]. We want to calculate the standard deviation for this data.

If we want to find the distance from each data point to the mean, we first have to calculate the mean. Which of these options represents the mean?

Select the best answer.

- Correct: 4
- Incorrect: 2
- Incorrect: 7

### Knowledge Check

Given the following data set:

[11, 12, 13, 13, 14, 14, 14, 15, 15, 16, 17]

Mean = 14

Standard deviation = 1.65

Which points (if any) warrant further investigation as potential outliers?

Select the best answer.

[TODO]

## Central Limit Theorem

### Knowledge Check

Suppose you have the following variables:

- $X$ = A random variable representing the blood pressure of everyone in one country.
- A sample size of 50 individuals.
- $\overline{X}$ = The mean of this sample’s blood pressure.

If we know that blood pressure ($X$) follows a normal distribution, then we know that the sampling distribution of $\overline{X}$ follows a normal distribution as well.

If we **don’t** know that blood pressure ($X$) follows a normal distribution, can we assume that the sampling distribution of 
$\overline{X}$ is approximately normally distributed?

Select the best answer.

- yes: correct
- no: incorrect

correct: Yes we can!  If we don't know that blood pressure $X$ follows a normal distribution, we can assume that the sampling distribution of $\overline{X}$ is approximately normally distributed, because our sample size is greater than 30.  We can apply the central limit theorem here.

### Knowledge Check

We want to estimate the average age among our coworkers. We sample 25 individuals and ask them their age. We don’t know if the population of age would follow a normal distribution.

Which of the following statements is true?

Select the best answer.

[TODO]

### Knowledge Check

If we visualize the distribution of rolling a die six times and getting 1, 2, 3, 4, 5, and 6 exactly once, the histogram would be...

Select the best answer.

- Normally distributed
- Round on the sides but flat on top
- Flat (correct)
- Skewed to the right

Correct: If we were to roll a die six times and get each number exactly once, the histogram will be flat.  As we increase the number of rolls, the shape of the distribution will become more normal and eventually reach the central limit theorem.

### Knowledge Check

We want to test if 66 inches is a reasonable guess for the average height of employees at our company. We know that the employees' heights follow a normal distribution and we sample 15 people for the test.

Which of the following statements is **true**?

Select the best answer.

- We do not need to apply the central limit theorem (correct)
- We need to apply the central limit theorem


Correct: We do not need to apply the central limit theorem because our original data is normally distributed, and the sampling distribution will be approximately normally distributed, regardless of sample size.


## Rules of Probability

### Knowledge Check

Does `my_set_1.union(my_set_2)` yield the same result as `my_set_2.union(my_set_1)` ?

Select the best answer.

- Yes, it does! (correct)
- No, it doesn't!

Correct: Set union is order-invariant (symmetric).

### Knowledge Check

Does `my_set_1.intersection(my_set_2)` yield the same result as `my_set_2.intersection(my_set_1)` ?

Select the best answer.

- Yes, it does! (correct)
- No, it doesn't!

Correct: Set intersection is order-invariant (symmetric).

## Knowledge Check

Which of the following are *true* about the rules of probability?

Select all that apply.

- Correct: An event's probability must be greater than or equal to zero.
- Incorrect: The total probability of an outcome must be greater than one.
- Correct: The probability of a union of two mutually exclusive events is the sum of the probabilities of the individual events.
- Incorrect: The probability of a union of two mutually exclusive events is the product of the probabilities of the individual events.

Correct: There are three axioms of probability:

1. The probability of an event cannot be negative.
2. The probability of an outcome occurring in the sample space is one.
3. The probability of a union of two events is the sum of the probabilities of the individual events.

## Knowledge Check

What is the marginal probability that you will be selected for a bag search (and risk losing your jar of peanut butter)?

Select the best answer.

- 5.7% (correct)
- 8.6%
- 17.1%
- 2.9%

Correct: From our sample group of 35 people, two were searched, so we'd have 2/35 = 0.057

## Knowledge Check

What is joint probability?

Select the best answer.

- The likelihood of a single random event occurring.
- The likelihood of a single non-random event occurring.
- The likelihood of two random events occurring together. (correct)
- The likelihood of two non-random events occurring together.

correct: great job!

## Knowledge Check

Repeat the burger joint example, but find the conditional probability that a customer who orders a veggie wrap (🌯) will also order fries (🍟):

![](./probability/assets/knowledge-check.png)

Select the best answer.

- 28.6%
- 33.3% (correct)
- 66.7%
- 71.4%

correct: P(fries|veggiewrap) = 0.1/0.3

## Vectors in Python

### Knowledge Check

Select all of the following that are **vectors**.

Select all that apply.

[TODO]]

Correct: Scalars are single numbers with magnitude but no direction, while vectors are an ordered list of scalars. The elephant's weight is a single number without direction. The pool ball is a vector because it has a magnitude and a direction. An accelerating or decelerating object's direction is indicated by a positive or negative number respectively. The car is a vector because it has multiple values.

### Knowledge Check

Suppose we have the following data points representing plant measurements. Which rule might be useful for classifying each plant as the species versicolor or iris?

- Versicolor: $(0.1,1.7,3.9).$

- Versicolor: $(0.3,1.9,4.0).$

- Versicolor: $(0.2,2.5,4.1).$

- Iris: $(0.4,2.2,3.4).$

- Iris: $(0.2,1.6,3.5).$

Select the best answer.

[TODO]

### Knowledge Check

What is the magnitude of the vector $x$?

$x=(−1,1,3,5)$

Select the best answer.

- $\sqrt{8}$
- 6 (correct)
- 36
- $\sqrt{34}$

correct: The magnitude is the square root of the sum of each component squared, so $\sqrt{(-1^2)+1^2+3^2+5^2+} = \sqrt{36} = 6$

### Knowledge Check

Normalize the vector $v=(3,4)$

Select the best answer.

- (3,4)
- (3/7, 4/7)
- (3/5, 4/5) (correct)
- (0.7, 0.3)

Correct: [TODO]

## Knowledge Check

Which of the following vectors has the largest magnitude?

Select the best answer.

- (-2, 2, 3)
- (0, -5, 0)
- (4, 4, 3) (correct)
- (-2, -3, -4)

correct: [TODO]

## Knowledge Check

Which of the following computes a vector containing the mean of each component pair of mathbf{x} and mathbf{y}?

- $mathbf{x} =(1,3)$.
- $mathbf{y} =(4,2)$.

Select all that apply.

correct: $0.5(x+y)$
correct: $x/2+y/2$
incorrect: $x+y$

Correct: The mean value of the first component pair is $(1+4)/2$, and the mean of the second component pair is $(3+2)/2$. Together, our final vector should be $(2.5,2.5)$. There are two ways to achieve this: We could sum the vectors and multiply the resulting vector by 0.5, or we could divide each vector by 2 and then sum them. The first two choices both result in the desired $(2.5,2.5)$.


## Matrix Operations in Python

### Knowledge Check

How many total elements would a matrix with 13 rows and 10 columns have?

Select the best answer.

- 65
- 130 (correct)
- 13

correct: For each row there are 10 elements, because there are 13 rows, there are 10\*13= 130 elements.

### Knowledge Check

Suppose we find the dot product of a vector, $x$, with itself — the sum of the element-wise products.

What is the result?

Select the best answer.

[TODO]

### Knowledge Check

What is the result of the following equation? (These matrices are written as nested lists, just as you’d write them in NumPy. So, the first nested list is the first row.)

0.5 \* [[8, 10],[2, 2]]- [[5, 2][1, -3]]

Select the best answer.

[TODO]

correct: [TODO]

### Knowledge Check

The following is of the form $\mathbf{AX}=\mathbf{B}$. What are possible values for the $x$ vector that would make this equation valid?

[TODO]

Select all that apply.

[TODO]

### Knowledge Check

How might the equations $y_1=5x+3$ and $y_2=−2x−7$, evaluated at the points $x=4$ and $x=0$, be represented as **AX** (where **X** includes values for the constant coefficients)?

Select the best answer.

[TODO]
