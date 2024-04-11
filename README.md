# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First, we want to import numpy, then import sys, assume a variable.
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3. For that we want to make a range accorting to our program output.
4. Then print the program with correct form then the output will display 

## Program:
```
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: S.Krishna Prasad
RegisterNumber: 212223230108

```
```
import numpy as np
n = int(input())
a = np.zeros((n,n+1))
x = np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j] = int(input())
for i in range(n):
    if a[i][i] == 0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]
            
x[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    for j in range(i+1,n):
        x[i] = x[i] - a[i][j] * x[j]
    x[i] = x[i]/a[i][i]

for i in range(n):
    print('X%d = %0.2f' %(i,x[i]), end=' ')
    
```

## Output:
![image](https://github.com/KrishnaPrasad148/Gaussian/assets/147332763/525f9b5b-bec6-42e2-8f5a-1417654a29e2)

![image](https://github.com/KrishnaPrasad148/Gaussian/assets/147332763/0ed4a73d-6d35-42e3-aa12-bd3b282e1b35)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

