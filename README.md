# 📘 PA 2 – Programming Assignment

👨‍💻 Author: Jasper F. Ancheta <br>
📅 Date: September 14, 2024 <br>
📚 Course: ECE2112 – Programming Assignment

# 📌 Version History

V1.0 (09-14-24) – Initial Release and Submission of GitHub Link

V1.1 (09-14-24) – Added README Documentation for Problems

V1.2 (09-14-24) – Added Code Snippets and Outputs in README

# 📌 Problem 1: Normalization Problem

This problem performs normalization on a 5×5 array. Normalization ensures that the dataset has a mean of 0 and a standard deviation of 1, which is useful in machine learning and data preprocessing.

Steps:
1. Create a 5×5 random array using np.random.rand(). 
2. Compute the mean using .mean() and standard deviation using .std().
3.Apply normalization using the formula:

X_norm = (X - mean) / std

4. Save the normalized array in a file named X_normalized.npy.

5. Load and print the results to confirm correctness.

# ✅ Input:
```
# PA 2 – Problem 1: NORMALIZATION PROBLEM

import numpy as np

# Create a random 5x5 array
X = np.random.rand(5, 5)

# Calculate the average value of all elements in X
X_mean = X.mean()

# Calculate the standard deviation of all elements in X
X_std = X.std()

# Standardize X by subtracting the mean and dividing by the standard deviation
X_norm = (X - X_mean) / X_std  

# Store the standardized array into a file called 'X_normalized.npy'
np.save('X_normalized.npy', X_norm)

# Display the original data
print("Original Array (X):\n", X)

# Display the standardized data
print("\nNormalized Array (X_normalized):\n", X_norm)

```


# ✅ Output:
```
Original Array (X):
 [[0.18656705 0.11395633 0.40811811 0.87967991 0.72698425]
 [0.60238104 0.41042394 0.82998272 0.07099728 0.56558024]
 [0.99051996 0.21877149 0.81878237 0.1437136  0.81659381]
 [0.41530096 0.13635563 0.64409431 0.6068243  0.15848987]
 [0.08016197 0.72855342 0.28406314 0.7305026  0.77704527]]

Normalized Array (X_normalized):
 [[-1.05799334 -1.30805514 -0.29500054  1.32899648  0.80313262]
 [ 0.37401552 -0.28705957  1.15784587 -1.45600048  0.24727839]
 [ 1.71071508 -0.94708548  1.11927332 -1.20557503  1.11173622]
 [-0.27026376 -1.23091489  0.51767055  0.38931752 -1.15468749]
 [-1.42443849  0.80853666 -0.72222961  0.81524937  0.97553623]]
```

# 📌 Problem 2: Divisible by 3 Problem

This problem generates the squares of the first 100 positive integers, reshapes them into a 10×10 array, and filters values that are divisible by 3.

Steps:

Create an array of numbers from 1 to 100 using np.arange().

Square the array values.

Reshape the squared numbers into a 10×10 array.

Use modulo % to find numbers divisible by 3.

Save the result as div_by_3.npy.

# ✅ Input:
```
# Create an array of integers from 1 to 100
num = np.arange(1, 101)

# Square each element in the array
squares = num ** 2

# Reshape the squared numbers into a 10x10 matrix
A = squares.reshape((10, 10))

# Extract only the elements that are divisible by 3
div_by_3 = A[A % 3 == 0]

# Save the filtered elements into a file named 'div_by_3.npy'
np.save('div_by_3.npy', div_by_3)

# Print a label for clarity
print('Original 10x10 Array:\n')

# Display the contents of the array A
print(A)

# Print a label to describe what will be shown
print('Array of Squares Divisible by 3:\n')

# Display the elements from array A that are divisible by 3
print(div_by_3)
```

# ✅ Output:
```
Original 10x10 Array:

[[    1     4     9    16    25    36    49    64    81   100]
 [  121   144   169   196   225   256   289   324   361   400]
 [  441   484   529   576   625   676   729   784   841   900]
 [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]
 [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]
 [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]
 [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]
 [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]
 [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]
 [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]]

Array of Squares Divisible by 3:

[   9   36   81  144  225  324  441  576  729  900 1089 1296 1521 1764
 2025 2304 2601 2916 3249 3600 3969 4356 4761 5184 5625 6084 6561 7056
 7569 8100 8649 9216 9801]

```
# 🛠 Software(s) Used
<p align="left"> <img src="https://www.python.org/static/community_logos/python-logo.png" alt="Python Logo" width="120"/> <img src="https://jupyter.org/assets/homepage/main-logo.svg" alt="Jupyter Logo" width="90"/> </p>
📂 Repository Information

# Languages Used:

Python (100%)
