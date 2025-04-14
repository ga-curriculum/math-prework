What is a Vector?
A vector is a mathematical object that has both magnitude (size) and direction. In simple terms, it’s an ordered list of numbers (components), which can represent a point in space, movement, or quantities with multiple dimensions.

Vectors are commonly written as:

    𝑣 = [𝑣1, 𝑣2, 𝑣3,...,𝑣𝑛]

where 𝑣1, 𝑣2,…, 𝑣𝑛 are the components of the vector.

## How are Vectors Used in Data Science?

Vectors play a crucial role in data science and machine learning. A common application include Feature Representation. Data points in a dataset are often represented as vectors. For example, a dataset of houses might have features like [size, price, bedrooms], which can be written as a vector.

---

## Python Examples

1. Creating a Vector

```python
import numpy as np
# Creating a 1-dimensional vector (array)
v = np.array([3, 4])

print(f"Vector v: {v}")
```

2. Vector Addition and Subtraction

```python
v1 = np.array([1, 2, 3])
v2 = np.array([4, 5, 6])

sum_vector = v1 + v2
diff_vector = v1 - v2

print(f"Vector Addition: {sum_vector}")
print(f"Vector Subtraction: {diff_vector}")
```

3. Scalar Multiplication (Scaling a Vector)

```python
scaled_vector = 2*v1
print(f"Scalar multiplication: {scaled_vector}")
```

4. Vector Magnitude (Norm)

The **norm** (or magnitude) of a vector represents its length. Given a vector:

\[
\mathbf{v} = [v_1, v_2, \dots, v_n]
\]

The **Euclidean norm** (also called the **L2 norm**) is calculated as:

\[
\|\mathbf{v}\| = \sqrt{v_1^2 + v_2^2 + \dots + v_n^2}
\]

In NumPy, you can compute this using:

```python
v = np.array([3, 4])
magnitude = np.linalg.norm(v)
print(f"Magnitude of v: {magnitude}")
```

5. Dot Product of Two Vectors

The **dot product** of two vectors \( \mathbf{v_1} \) and \( \mathbf{v_2} \) is defined as:

\[
\mathbf{v_1} \cdot \mathbf{v_2} = v_{1,1} v_{2,1} + v_{1,2} v_{2,2} + \dots + v_{1,n} v_{2,n}
\]

For example, given two vectors:

\[
\mathbf{v_1} = [a, b, c], \quad \mathbf{v_2} = [x, y, z]
\]

Their dot product is:

\[
\mathbf{v_1} \cdot \mathbf{v_2} = ax + by + cz
\]

```python
v1 = np.array([1, 2, 3])
v2 = np.array([4, 5, 6])

dot_product = np.dot(v1, v2)
print(f"Dot Product of v1 and v2: {dot_product}")
```

