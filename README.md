## Experiment 1: Exploring NumPy and Pandas

## Aim

To understand the use of NumPy and Pandas for performing basic data manipulation and analysis in Python.

## Algorithm

Import the NumPy library for matrix and numerical operations.

Define a two-dimensional square matrix A and a vector b.

Compute the transpose of matrix A to interchange rows and columns.

Calculate the inverse of matrix A using np.linalg.inv(A) (ensure A is non-singular).

Solve the linear equation A × x = b using np.linalg.solve(A, b).

Perform eigen decomposition to find eigenvalues and eigenvectors using np.linalg.eig(A).

Display the results for the matrix, transpose, inverse, solution vector, and eigenvalues.

End the program.

## Formulas / Theory

Transpose: Aᵀ --- interchange rows and columns.

Inverse: A⁻¹ = adj(A) / |A|, provided det(A) ≠ 0.

Linear system: A × x = b  ⇒  x = A⁻¹b.

Eigen decomposition: A v = λ v, where λ is an eigenvalue and v is an eigenvector.

## Program


```

import numpy as np
import pandas as pd

arr1=np.array([10,20,30,40,50])
arr2=np.array([5,10,15,20,25])
print("Array 1:", arr1)
print("Array 2:", arr2)

print("Addition:", arr1+arr2)
print("Subtraction:", arr1-arr2)
print("Multiplication:", arr1*arr2)
print("Division:", arr1/arr2)


student={
    'Name':["John","Alice","Bob","Daisy"],
    'Age':[25,30,22,20],
    'Salary':[40000,50000,32000,45000]
}
df = pd.DataFrame(student)

print("\nDataset:")
print(df)


print("\nStatistical Summary: ")
print(df.describe())
print("\nDataset Info:")
print(df.info())

```


## Output



```


Array 1: [10 20 30 40 50]
Array 2: [ 5 10 15 20 25]

Addition: [15 30 45 60 75]
Subtraction: [ 5 10 15 20 25]
Multiplication: [ 50 200 450 800 1250]
Division: [2. 2. 2. 2. 2.]

Dataset:
    Name  Age  Salary
0   John   25   40000
1  Alice   30   50000
2    Bob   22   32000
3  Daisy   20   45000

Statistical Summary:
             Age        Salary
count   4.000000      4.000000
mean   24.250000  41750.000000
std     4.349329   7505.553499
min    20.000000  32000.000000
25%    21.500000  38000.000000
50%    23.500000  42500.000000
75%    26.250000  46250.000000
max    30.000000  50000.000000

Dataset Info:
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 4 entries, 0 to 3
Data columns (total 3 columns):
 #   Column  Non-Null Count  Dtype
---  ------  --------------  -----
 0   Name    4 non-null      object
 1   Age     4 non-null      int64
 2   Salary  4 non-null      int64
dtypes: int64(2), object(1)
memory usage: 228.0+ bytes

```

## Result


Thus, the basic operations of NumPy and Pandas were successfully performed using Python. Arithmetic operations such as addition, subtraction, multiplication, and division were carried out using NumPy arrays. A Pandas DataFrame was created to store student details, and descriptive statistics and dataset information were obtained successfully.

