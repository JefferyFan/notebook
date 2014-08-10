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




--------------------
Lecture 17
---
#### Orthonomal vectors
$q_i^T q_j = \begin{cases}0 & \text {if } i \neq j \\ 1 &  \text {if } i=j \end{cases}$

$Q=\begin{bmatrix} q_1 & \cdots & q_n \end{bmatrix}$ then $Q^TQ=I$

> **Note:** Q is orthonormal matrix.

If Q is square then $Q^TQ=I$ tells us $Q^T=Q^{-1}$.

**Project** onto its column space
$P = Q(Q^TQ)^{-1}Q^T = QQ^T$

1. symmetric
2. $PP=QQ^TQQ^T=I$

> **Note:** If $Q$ is square, $P=I$


The component of projection:
$x_j = q_j^T * b$



#### Gram-Schmidt
independent vectors a, b

1. orthogonal vectors A, B, C
	$A = a, \;B = b - \frac{AA^T}{A^TA}b, \;C = c - \frac{AA^T}{A^TA}c - \frac{BB^T}{B^TB}c$ 

2. orthonormal vectors $q_1, q_2, q_3$
	$q_1 = \frac{A}{\begin{Vmatrix} A \end{Vmatrix}} ,q_2 = \frac{B}{\begin{Vmatrix} B \end{Vmatrix}} ,q_3 = \frac{C}{\begin{Vmatrix} C \end{Vmatrix}} $


-----------------------
Lecture 18
---
$$\begin{vmatrix} a&b \\ c&d \end{vmatrix} = ad - bc$$

#### Determinants   det A
**Property 1:** det I = 1.
**Property 2:** Exchange rows reverse sign of determinant.
**Property 3:** **LENEAR EACH ROW**
$$\begin{vmatrix} ta&tb \\ c&d\end{vmatrix} = t\begin{vmatrix} a&b \\ c&d \end{vmatrix}$$

$$\begin{vmatrix} a+a'&b+b' \\ c&d \end{vmatrix}=\begin{vmatrix} a&b \\ c&d \end{vmatrix}+\begin{vmatrix} a'&b' \\ c&d \end{vmatrix}$$

> **Note:** $det(A+B) \neq det(A) + det(B)$

**Property 4:** two equal rows -> det = 0
**Property 5:** Subtract l $\times$ row i from row k, **DETERMINANT DOESN'T CHANGE**.
**Property 6:** Row of zeros -> det A = 0
**Property 7:** Matrix U is upper triangular, then $det(U) = d_1*d_2*...d_n$, product of pivots(diagonal elements).
**Property 8:** $det(A) = 0$ when A is singular(noninvertible), $det(A) \neq 0$ when A is invertible.
**Property 9:** $det(AB) = det(A)det(B)$

- $det(A^{-1})={1\over det(A)}$
- $det(A^2) = (det(A))^2 $
- $det(2A) = 2^m det(A)$

**Property 10:** $det(A^T)=det(A)$

- Exchange columns reverse sign
- Column of zeros -> det A = 0

proof:
$\begin{vmatrix}A^T \end{vmatrix} = \begin{vmatrix}A \end{vmatrix}$
$\Rightarrow \begin{vmatrix}U^TL^T \end{vmatrix} = \begin{vmatrix}LU \end{vmatrix}$
$\Rightarrow \begin{vmatrix}U^T \end{vmatrix}\begin{vmatrix}L^T \end{vmatrix}=\begin{vmatrix}L \end{vmatrix}\begin{vmatrix}U \end{vmatrix}$


  [1]:https://raw.githubusercontent.com/JefferyFan/notebook/master/Linear_Algebra/assets/least_square.jpg