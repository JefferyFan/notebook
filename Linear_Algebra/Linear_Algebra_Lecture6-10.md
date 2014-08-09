Linear Algebra
===
  [Lecture Vedio][1]


--------
Lecture 6
----

$$Ax=\begin{bmatrix}1&1&2 \\ 2&1&3 \\ 3&1&4 \\ 4&1&5 \end{bmatrix}\begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = b$$

#### column space $C(A)$
Definition
:   all linear combinations of the columns. --- subspace of $R^m$

> **Note:** In the exmaple, the column space is subspace of $R^4$

Which b's allow this system $Ax=b$ to be solved?
:   Can solve $Ax=b$ exactly when b is $C(A)$

Pivot Column
:   the columns that are linear independent.

>**Note:** In the example, pivot columns are column 1 and 2. Or column 2 and 3. 
Because $Column 3 = Column 1 + Column2$

Dimension
:	equals to the number of pivot columns.


#### Nullspace $N(A)$
Definition
:   all solutions $x$ that $Ax=0$ --- subspace of $R^n$

> **Note:**
>
> - N(A) is $c\begin{bmatrix}1 \\ 1 \\ -1 \end{bmatrix}$
> - Nullspace must contains **ZERO vector**


#### Row space
Definition
:	all linear combinations of the rows. --- subspace of $R^n$

--------------------
Lecture 7
---
#### sovle $Ax=0$, Nullspace
- First step: **Elimination**
$$
A = \begin{bmatrix}1&2&2&2 \\ 2&4&6&8 \\ 3&6&8&10 \end{bmatrix} 
  = \begin{bmatrix}1&2&2&2 \\ 0&0&2&4 \\ 0&0&0&0 \end{bmatrix} = U
$$

    >**Note:**
    >
    > - U is called **Echelon Form**
    > - Column 1 and 3 are **pivot columns**, Column 2 and 4 are free columns.
    > - $x_1$and$x_3$are pivot variables, $x_2$and$x_3$are free variables.
    > - **Rank**: The number of pivots

- Second step: **Solve $Ux=0$**
分别令free variable为0，求得Nullspace的base
令$x_2 = 1, x_4=0$，得$\begin{bmatrix}-2\\1\\0\\0\end{bmatrix}$
令$x_2 = 0, x_4=1$，得$\begin{bmatrix}2\\0\\-1\\1\end{bmatrix}$

    所以x解为：
$$x=c\begin{bmatrix}-2\\1\\0\\0\end{bmatrix}+d\begin{bmatrix}2\\0\\-1\\1\end{bmatrix}$$
也即是A的Nullspace $N(A)$

    > **Note:**

    >  - Reduced row echelon form: zeros above and below pivots and pivots equal 1.
    > $$R=\begin{bmatrix}1&2&0&-2 \\ 0&0&1&2 \\ 0&0&0&0 \end{bmatrix}$$
    >  - $Rank(A)=Rank(A^T)$


----------------
Lecture 8
---
#### sovle $Ax=b$
$A = \begin{bmatrix}1&2&2&2 \\ 2&4&6&8 \\ 3&6&8&10 \end{bmatrix} $

argmented matrix:  $\begin{bmatrix}A & b\end{bmatrix}$

$
\begin{bmatrix}1&2&2&2&b_1 \\ 2&4&6&8&b_2 \\ 3&6&8&10&b_3 \end{bmatrix} \Rightarrow
\begin{bmatrix}1&2&2&2&b_1 \\ 0&0&2&4&b_2-2b_1 \\ 0&0&0&0&b_3-b_2-b_1 \end{bmatrix} 
$


Solvability Condition on b
:	$Ax=b$ solvable if when b is in $C(A)$
:	if a combination of rows of A gives zero row, the same of combination of the enties of b must give 0.

#### To find complete solutions to $Ax=b$

1. $x_{particular}$
	- set all free variables($x_2$ and $x_4$) to zero
	- solve $Ax=b$ for pivot variables. (we get $x_1=-2$ and $x_3={3 \over 2}$)
	- $x_p=\begin{bmatrix}-2 \\ 0 \\ {3\over2} \\ 0 \end{bmatrix}$
2. $x_{nullspace}$
3. $x_{complete}=x_p + x_n$ , $x_n$ is any verctor in nullspace.

prove:
$Ax_p=b$ and $Ax_b=0 $, so $A(x_p+x_n)=b$



#### m by n matrix of rank r ($r \le m, r \le n$)
Full column rank means $r=n$

- No free variable
- $N(A)=\overrightarrow 0$
- solutions to $Ax=b$,$x=x_p$, unique solution if it exists. That is, 0 or 1 solution.

Full row rank means $r=m$

- can solve $Ax=b$ for every b
- left with $n-m$ free variables
- $Ax=b$ has 1 or infinite solutions


Full row rank and column rank $r=m=n$

- invertible 
- the reduced echelon form is identity matrix
- the nullspace is zero vector only
- $Ax=b$ has 1 solution

Rank $r<n, r<m$
- $Ax=b$ has 0 or infinite solutions



------------------

Lecture 9
---
Suppose A is m by n with m < n. Then there are nonzero solutions to $Ax=0$. (more unknowns than equations)
Reason: There will be free variables.


#### Linear independence
Definition
:	Vectors $x_1$, $x_2$, ... , $x_n$ are independent if no combination gives zero vector (except the zero combination).

> **Note:** 
>
> - Independent vecotors must not contain zero vector.
> 

When $v_1$, ... $v_n$ are columns of A, 

 - they are independent if nullspace of A is only the zero vector. **rank=n**
 - they are dependent if $Ac=0$ for some nonzero $c$. **rank < n**


#### Spaning a space

Definition
:	Vectors $v_1$, ... , $v_l$ spans a space means: the space consists of all combinations of those vectors.

> **Note:** The column vectors span the column space.



#### Basis
Definition
:	Basis for a space is a sequence of vectors $v_1$, ... , $v_d$ with two properties
		1. They are independent
		2. They span the space

In $R^n$， n vectors give basis if n*n matrix with those columns is invertible.

**Given a space, every basis for the space has the same number of vectors. --- DIMENSION**

> **Note:** 
>
> - Rank(A) = number of pivot columns = dimension of C(A)
> - dimesion N(A) = number of free variables = n - r

standard basis: the column of indentity.


-----------------

Lecture 10
---
$A$ is m by n.

#### Four fundamental subspace
1. Column space $C(A)$ in $R^m$
	dim $C(A)$ = rank
2. Nullspace $N(A)$ in $R^n$
3. Row space
all combinations of rows = all combinations of column of $A^T$ = $C(A^T)$ in $R^n$
4. Nullspace of $A^T$ = $N(A^T)$ --- left nullspace of $A$ in $R^m$


|   ---      | $C(A)$        | raw space | $N(A)$            | $N(A^T)$ |
| : --- :    | :---:         | :---:     | :---:             | :---:    |
| basis      | pivot columns | the first r row of $R$  | special solutions |  basis is in $E$, $EA=R$     |
| dimensions | r             | r         | n-r               | m-r      |  


> **Note:** $C(A) \neq C(R)$, $R$ is the echelon form of $A$



-------------------

  [1]: http://v.163.com/special/opencourse/daishu.html