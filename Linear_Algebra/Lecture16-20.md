Linear Algebra
===
Lecture 16-20

-------------------
Lecture 16
---
Projection Matrix P
$Pb$ project b onto a space, then $(I-P)b$ project b onto a $\bot$ space.

#### Least Square
Find the best line that error is smallest.
![Lease Square][1]

$Ax=b \Rightarrow \begin{bmatrix}1&1 \\ 1&2 \\ 1&3\end{bmatrix}\begin{bmatrix}C\\D\end{bmatrix}=\begin{bmatrix}1 \\ 2 \\ 3\end{bmatrix}$

minimize $\begin{Vmatrix} Ax-b\end{Vmatrix}^2=\begin{Vmatrix} e\end{Vmatrix}^2=\begin{Vmatrix} e_1\end{Vmatrix}^2+\begin{Vmatrix} e_2\end{Vmatrix}^2+\begin{Vmatrix} e_3\end{Vmatrix}^2$


Find $\widehat x = \begin{bmatrix} C\\D \end{bmatrix} $
$A^TA\widehat x=A^Tb$ --- normal equations. we get $C=1/2, D=2/3$
so, the best line is $y= {1\over 2} + {2\over 3}t$

property of $e$:

1. $p+e=b$
2. $p \cdot e = 0$


If A has independent columns then $A^TA$ is invertible.
Suppose $A^TAx=0$, 
then $x^TA^TAx=0 \Rightarrow (Ax)^TAx=0 \Rightarrow Ax=0 \Rightarrow x=0$ 
$ \Rightarrow A^TA$ is invertible 

#### Orthonormal vectors
Columns definitely independent if they are **perpendicular unit vectors**, that is orthonormal vectors.



\begin{bmatrix} \end{bmatrix}
\begin{Vmatrix} \end{Vmatrix}

--------------------
Lecture 17
---




  [1]:https://raw.githubusercontent.com/JefferyFan/notebook/master/Linear_Algebra/assets/least_square.jpg