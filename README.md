# PROGRAMING ASSIGNMENT 2
NUMERICAL PYTHON (NUMPY)

---

**NAME:** SILVERIO, Jamille Anne &emsp;&emsp;&emsp;&emsp; **DATE SUBMITTED:** Sept. 3, 2025  
**SECTION:** 2ECEB  

---

## I. Intended Learning Outcomes:
1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a Numpy library

---

## II. Instructions:
Write a Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter
notebook in the dedicated submission bin.

---

### NORMALIZATION PROBLEM
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. Mathematically, normalization can be
expressed as:

<p align="center">
$$
Z = \frac{X - \bar{x}}{\sigma}
$$
</p>

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and
.std() calls.

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy

**Implementation (My Work):**
```python
#IMPORT NUMPY LIBRARY
import numpy as np

#CREATE A RANDOM 5x5 NDARRAY
X = np.random.random((5,5))
#NORMALIZE X USING NORMALIZATION EQUATION
X_normalized = ((X - X.mean()) / (X.std()))

#PRINTS OUTPUT
print(X_normalized)

#SAVE NDARRAY
np.save("X_normalized.npy", X_normalized)
```
**Code Walkthrough:**
```python
import numpy as np
```
* I imported the NumPy Library, which I refer to as ```np``` throughout the code. It provides necessary functions for creating and implementing arrays.
```python
X = np.random.random((5,5))
```
* I used ```np.random.random()``` to create an array shape ```5x5```. Each element floating-point number.
```python
X_normalized = ((X - X.mean()) / (X.std()))
```
* I then normalized X using the normalization equation.
```python
print(X_normalized)
```
* I used the ```print()``` function to display the normalized array, with ```X_normalized``` as the parameter.
```python
np.save("X_normalized.npy", X_normalized)
```
* Finally, the normalized array is saved to a file named ```X_normalized.npy```. It can be retrieved later on using ```np.load```.
  
**Conclusion:**  
The program **successfully** displayed the normalized 5x5 array of ```X```.

---

### DIVISIBLE BY 3 PROBLEM
Create the following 10 x 10 ndarray.

<p align="center">
$$
A =
\begin{bmatrix}
1 & 4 & \cdots & 81 & 100 \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
8281 & 8464 & \cdots & 9801 & 10000
\end{bmatrix}
$$
</p>

which are the squares of the first 100 positive integers.

From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

**Implementation (My Work):**
```python
#IMPORT NUMPY LIBRARY
import numpy as np

#CREATE A 10x10 ARRAY WITH THE SQUARES OF THE FIRST 100 NUMBERS
sqrt = np.arange (1, 101) ** 2
arr = sqrt.reshape (10,10)

#PRINTS OUTPUT
print("10x10 array of squares:\n", arr)

#DISPLAYS ALL THE ELEMENTS DIVISIBLE BY 3
div_by_3 = arr[arr % 3 == 0]

#PRINTS OUTPUT
print("\nSquares divisible by 3:\n", div_by_3)

#SAVE NDARRAY
np.save("div_by_3.npy", div_by_3)
```
**Code Walkthrough:**
```python
import numpy as np
```
* I imported the NumPy Library, which I refer to as ```np``` throughout the code. It provides necessary functions for creating and implementing arrays.
```python
sqrt = np.arange(1, 101) ** 2
arr = sqrt.reshape(10,10)
```
* I used ```np.arange()``` to generate the first 100 integers, with ```(1, 101)``` being the parameter.
* Each element is squared using the operator ```**2```.
* The resulting array is then reshaped into a 10x10 array using ```.reshape(10, 10)```.
```python
print("10x10 array of squares:\n", arr)
```
* I used the ```print()``` function to display the 10x10 array of the squares of the first 100 positive integers, with ```arr``` as the parameter.
```python
div_by_3 = arr[arr % 3 == 0]
```
* I applied the modulo operator ```arr % 3 == 0``` to extract the values divisible by 3.
```python
print("\nSquares divisible by 3:\n", div_by_3)
```
* I used the ```print()``` function to display the squares that are divisible by 3, with ```div_by_3``` as the parameter.
```python
np.save("div_by_3.npy", div_by_3)
```
* Finally, the results is saved to a file named ```div_by_3.npy```. It can be retrieved later on using ```np.load```.

**Conclusion:**  
The program **successfully** displayed a 10x10 array with the squares of the first 100 positive integers, then filtering out those that are divisible by 3.

---

**Click here to see my Jupyter Notebook:**  [SILVERIO_2ECEB_PA2.ipynb](https://github.com/JamSilverio1114/ECE2112_PAssignment2_SILVERIO_2ECEB/blob/main/SILVERIO_2ECEB_PA2.ipynb)  
**DATE DUE:** Sept. 3, 2025  

---
