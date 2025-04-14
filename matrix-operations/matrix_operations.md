## **Introduction to Matrices**

### **What is a Matrix?**
A **matrix** is a rectangular array of numbers arranged in rows and columns. It is typically represented as:

\[
M = \begin{bmatrix}
m_{1,1} & m_{1,2} & \dots & m_{1,n} \\
m_{2,1} & m_{2,2} & \dots & m_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\
m_{m,1} & m_{m,2} & \dots & m_{m,n}
\end{bmatrix}
\]

where:
- \( M \) is an \( m \times n \) matrix with \( m \) rows and \( n \) columns.
- \( m_{i,j} \) represents the element in the \( i \)-th row and \( j \)-th column.

### **Use Cases of Matrices in Data Science**
Matrices play a fundamental role in data science and machine learning. Some key applications include:

1. **Dataset Representation**:
   - Datasets in machine learning are often stored as matrices, where **rows** represent samples and **columns** represent features.
   
2. **Linear Algebra Operations**:
   - Matrices allow operations such as transformations, rotations, and projections in high-dimensional space.
   
3. **Principal Component Analysis (PCA)**:
   - PCA uses matrix decompositions (such as eigenvalues and eigenvectors) to reduce dimensionality and improve efficiency.
   
4. **Linear Regression**:
   - The normal equation in **Ordinary Least Squares (OLS)** regression is solved using matrix operations:
   
   
   $\beta$ = (X^T X)^{-1} X^T y
   
   
5. **Neural Networks**:
   - Weights and activations in deep learning models are represented as matrices, and forward/backpropagation relies on matrix multiplications.
   
6. **Computer Vision**:
   - Images are stored as matrices of pixel values, enabling transformations like edge detection and convolutional filtering.
   
7. **Recommendation Systems**:
   - Matrices are used in collaborative filtering techniques like Singular Value Decomposition (SVD) to predict user preferences.

---

## Matrix Operations in Python

1. Creating a Matrix
```python
import numpy as np

M = np.array([[1, 2], [3, 4]])
print("Matrix M:\n", M)

```

2. Matrix Addition and Subtraction
```python
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

print("Matrix Addition:\n", A + B)
print("Matrix Subtraction:\n", A - B)


```

3. Scalar Multiplication: Multiply each element by a scalar
```python
scalar = 2
print("Scalar Multiplication:\n", scalar * A)

```

4. Matrix Multiplication

It is the dot product of matrices (not element-wise multiplication):

```python
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

C = np.dot(A, B)  # or A @ B
print(f"Matrix Multiplication:\n {C}")
```

5. Matrix Transpose

The transpose of a matrix swaps its rows and columns

```python
A = np.array([[1, 2, 3], [4, 5, 6]])
print(f"Transpose of A: {A.T}") # NumPy .T called on a matrix will transpose it

```