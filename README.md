# Algorithm for QR Decomposition

# NAME : SHREEJA R S
# REF.NO : 25017561

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
![Screenshot_27-3-2026_215227_lms2 ai saveetha in](https://github.com/user-attachments/assets/4487d548-961f-4041-8d36-ce493e2f20f1)

<img width="1180" height="763" alt="Screenshot 2026-03-27 215528" src="https://github.com/user-attachments/assets/e6c45ad2-d1b6-4a63-9206-b4494f19682f" />

<img width="1186" height="300" alt="Screenshot 2026-03-27 215536" src="https://github.com/user-attachments/assets/71f4c84a-9b53-416b-b455-f623a40f37a9" />

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
















































































































































































































































































































































































































































































































..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
..
.
..................................






.

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

.

.
.
.

.
.
.

.



.


.
.
.

.
.

..

.


.
..
..
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
