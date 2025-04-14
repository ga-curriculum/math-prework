## Random Variables and Expected Value

### **Random Variables**
A **random variable** is a numerical outcome of a random process. It can take different values based on some probability distribution.

There are two main types:
- **Discrete Random Variables**: Can take only specific, countable values (e.g., the number of heads when flipping a coin).
- **Continuous Random Variables**: Can take any value within a range (e.g., the time it takes to run a marathon).

### **Expected Value (Mean)**
The **expected value (EV)** of a random variable is the long-term average of its values when repeated many times. It's computed as:

\[
E[X] = \sum (x_i \cdot P(x_i))
\]

where \( x_i \) are the possible values and \( P(x_i) \) is their probability.

#### **Example: Discrete Random Variable**
For a **fair die**, each number (1–6) has an equal probability of \( 1/6 \), so:

\[
E[X] = (1 \times \frac{1}{6}) + (2 \times \frac{1}{6}) + \dots + (6 \times \frac{1}{6}) = 3.5
\]

#### **Example: Biased Coin Toss**
For a **biased coin** where heads (\(X=1\)) occurs with probability 0.7 and tails (\(X=0\)) with probability 0.3, the expected value is:

\[
E[X] = (1 \times 0.7) + (0 \times 0.3) = 0.7
\]

---

### **Continuous Random Variables**
A **continuous random variable** can take infinitely many values within a given range. Instead of summing probabilities like in the discrete case, we compute the expected value using an integral:

\[
E[X] = \int x \cdot f(x) \, dx
\]

where \( f(x) \) is the probability density function (PDF) of \( X \).

#### **Example: Uniform Distribution**
Suppose a random variable \( X \) follows a **continuous uniform distribution** between \( a = 0 \) and \( b = 10 \). The PDF is:

\[
f(x) = \frac{1}{b - a}, \quad \text{for } 0 \leq x \leq 10
\]

The expected value is:

\[
E[X] = \frac{a + b}{2} = \frac{0 + 10}{2} = 5
\]

#### **Example: Exponential Distribution**
Another common **continuous random variable** is the **exponential distribution**, which models waiting times (e.g., time between customer arrivals at a store).

The PDF is:

\[
f(x) = \lambda e^{-\lambda x}, \quad x \geq 0
\]

where \( \lambda \) (lambda) is the rate parameter.

The expected value of an **Exponential(\(\lambda\))** distribution is:

\[
E[X] = \frac{1}{\lambda}
\]

---

### **Key Takeaways**
- **Discrete Random Variables**: Expected value is a weighted sum.
- **Continuous Random Variables**: Expected value is an integral of \( x \cdot f(x) \).
- **Uniform Distribution**: \( E[X] = \frac{a + b}{2} \).
- **Exponential Distribution**: \( E[X] = \frac{1}{\lambda} \).

---

## Python Example

Let's compute the expected value of rolling a fair die.

```python
outcomes = [1, 2, 3, 4, 5, 6] #all the possible numbers we can roll
probabilities = [1/6]*6 # Each outcome has equal probability
```
Then compute the expected value
```python
expected_value = sum(x * p for x, p in zip(outcomes, probabilities))

print(f"Expected Value of rolling a fair die: {expected_value}")
```

It's okay if you have not seen the built-in Python `zip()` function yet. Think of it as a "zipper" that allows you to loop through multiple iterables at once.
