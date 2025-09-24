# Programming Assignment #2
This file contains the codes for Programming Assignment #1, which includes the following problems:
1. Normalization Problem
   - Create a random 5x5 ndarray and store it to variable X. Normalize X. Save your normalized ndarray as X_normalized.npy
   
2. Divisible by 3 Problem
   - Create a 10x10 ndarray which are the squares of the first 100 positive integers.
   - From this ndarray, determine all the elements that are divisble by 3. Save the result as div_by_3.npy

I. Intended Learning Outcomes:
1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a
Numpy library

# CODE AND EXPLANATION

## Normalization Problem
 
     ### CODE:
  
     x = np.random.random((5,5)) 
     x_normalized = (x-x.mean()) /np.std(x)
     np.save("x_normalized.npy", x_normalized)
     print ("Original x (5x5):\n",x)
     print ("\nNormalized x:\n", x_normalized)

  ### EXPLANATION:
  
  - np.random.random((5,5)) 
        - Creates a 5x5 matrix with random values between 0 and 1. 
        - Stores this matrix in the variable x.

  - x_normalized = (x-x.mean()) /np.std(x) - Applies the normalization formula: (x - mean)/std
                                         - x.mean() finds the average value of all elements in x.
                                         - np.std(x) calculates the standard deviation 

  - np.save("x_normalized.npy", x_normalized) - Saves in .npy format, which is NumPy.

  - print ("Original x (5x5):\n",x) - Prints the original matrix x.
  
  - print ("\nNormalized x:\n", x_normalized) - Prints the normalized version (x_normalized).

## Divisible by 3
     
     ### CODE:
     
     a = np.arange(1,101) ** 2
     a = a.reshape(10,10)
     div_by_3 = a[a%3==0]
     np.save("div_by_3.npy", div_by_3)
     print ("\n10x10 Array of Squares (a):\n",a)
     print ("\nElements Divisible by 3:\n",div_by_3)

   ### EXPLANATION:
     
   - a = np.arange(1,101) ** 2 - np.arrange(1,101) generates integers from 1 to 100
                               - Squaring them (**2) gives values from 1^2 up to 100^2.

   - a = a.reshape(10,10) - Converts into a 10x10 matrix

   - div_by_3 = a [a%3==0] - a%3 == 0 determines which elements are divisible by 3.

   - np.save("div_by_3.npy", div_by_3) - Saves those numbers into a file called div_by_3.npy
    
   - print ("\n10x10 Array of Squares (a):\n",a) - Prints the full 10x10 matrix of squares.
     
   - print ("\nElements Divisible by 3:\n",div_by_3) - Prints the extracted numbers that are divisible by 3.
     
  # SUMMARY

  - In the Normalization Problem, a 5x5 matrix is generated, then normalized using the formula provided
  - (x-mean)/std. Lastly, the result is saved in a file named x_normalized.npy

  - In the Divisible by 3 problem, the squares of numbers 1 to 100 are arranged into a 10x10 matrix.
  - Elements are extracted and saved in a file named div_by_3.npy.

