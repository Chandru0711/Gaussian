# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy module and sys module
2. Get input from the user for number of rows and add it by 1 for number of column
3. Using np.zeros() set the matrix as null matrix.
4. Using nested for loop find the ratio and perform the elementary row operations and find the final matrix.
5. print and end the program 

## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: CHANDRU SM
RegisterNumber: 212223230034
'''
import numpy as np
n= int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range (n+1):
         arr[i][j]=int((input)())
for i in range(n):
     for j in range(i+1,n):
         ratio=arr[j][i]/arr[i][i]
         for k in range (n+1):
             arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ")

*/
```

## Output:

![Screenshot 2024-05-08 233913](https://github.com/Chandru0711/Gaussian/assets/144979368/0f480e4c-9927-4a55-9205-a1b003d93a1d)

![Screenshot 2024-05-08 233927](https://github.com/Chandru0711/Gaussian/assets/144979368/8e286f42-a94c-4c59-8005-74e82cd2760d)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

