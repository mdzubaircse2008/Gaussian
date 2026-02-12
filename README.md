# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Read input and construct matrices using numpy.array() and numpy.reshape().
2. Separate coefficient matrix A and constant vector B using slicing.
3. Compute the solution using numpy.linalg.solve(A, B).
4. Display the solution vector using print() function.

## Program:
```
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Mohammed Zubair R
RegisterNumber: 212225040252(25017722)

import numpy as np
import sys 
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0:
        sys.exit("Divide by zero")
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print("X%d = %0.2f"%(i,x[i]),end=" ")
```

## Output:

<img width="1134" height="587" alt="image" src="https://github.com/user-attachments/assets/8e2b7489-22c7-4494-8b09-40cb60522a80" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

