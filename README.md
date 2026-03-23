# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method
```
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
A=np.array(eval(input()))
n,m=A.shape
Q=np.empty((m,n))
R=np.zeros((m,n))
for i in range(n):
    v=A[:,i]
    for j in range(i):
        R[j,i]=np.dot(Q[:,j],A[:,i])
        v=v-R[j,i]*Q[:,j]
    R[i,i]=np.linalg.norm(v)
    Q[:,i]=v/R[i,i]
print("The Q Matrix is\n",Q)
print("The R Matrix is\n",R)

```

## Output

![Screenshot_24-3-2026_04520_lms2 ai saveetha in](https://github.com/user-attachments/assets/6fb3673b-8b3d-4556-a2bd-969758bacbd7)


## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.





.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
.
.
.
.
..
.
.
.
.
..
.
.
.
.

..
.
