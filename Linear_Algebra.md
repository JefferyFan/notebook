

# Linear Agbebra

  [Lecture Vedio][1]

---------------

Lecture 2
---

$$ AB=R $$


- 单个元素计算
$$ R_{ij} = \sum_{k=1} ^n A_{ik} B_{kj} $$

- 列线性组合
结果矩阵的每一列都可以看成是矩阵A的列的线性组合。
$$ Column_{j} \; of  \; R = A * Column_j \; of \; B $$


- 行线性组合
结果矩阵的每一行都可以看成是矩阵B的行的线性组合。
$$ Row_j \; of \; R = Row_j \; of \; A * B $$

----------------
Lecture 3
---
#### 矩阵乘法$ AB=C $

1. columns of C are combinations of columns of A
2. rows of C are combinations of rows of B
3. $C_{ij}=\sum_{k=1}^n a_{ik}*b_{kj}$
4. $AB=\sum_{k=1}^n (column \; k \; of \; A) * (row \; k \; of \; B) $
5. Block multiply
$$\begin{bmatrix}A_1 & A_2 \\ A_3 & A_4\end{bmatrix}\begin{bmatrix}B_1 & B_2 \\ B_3 & B_4\end{bmatrix}=\begin{bmatrix}A_1B_1+A_2B_2 & \cdots \\ \cdots  & \cdots \end{bmatrix}$$
    

#### Inverse
If A is square and invertible, $A^{-1}A=I=AA^{-1}$

> **Note:** Invertible = nonsingular

存在$A\overrightarrow{x}=0(\overrightarrow{x} \neq 0)$，则$A$不可逆。

#### Find Inverse
$$A=\begin{bmatrix}a&c \\ b&d \end{bmatrix}, find A^{-1}$$

$$
\begin{bmatrix}a&c&1&0 \\ b&b&0&1 \end{bmatrix} \Rightarrow 
\begin{bmatrix}1&0&e&f \\ 0&1&g&h \end{bmatrix} \Rightarrow
A^{-1}=\begin{bmatrix}e&f \\ g&h \end{bmatrix}
$$

Prove:
suppose $EA=I$, $E$ is the emlination matrix.
so, we get $E=A^{-1}$
then, $E[A\;I]=[I\;E]=[I\;E^{-1}]$

> **Note:** The inverse of $AB$ is $B^{-1}A^{-1}$ since $ABB^{-1}A^{-1}=I$

--------------------
Lecture 4
---
#### Transpose
formula: $(A^T)_{ij}=A_{ji}$

formula: $AB=C \Rightarrow B^TA^T=C^T$

> **Note:** $(A^{-1})^T = (A^T)^{-1}$
> prove: $AA^{-1}=I \Rightarrow (A^{-1})A^T=I^T=I \Rightarrow (A^{-1})^T = (A^T)^{-1}$


#### Permutations
置换矩阵，用于行交换，通过交换Identity的行得到。

Example: 
$\begin{bmatrix}0&1&0 \\ 1&0&0 \\ 0&0&1 \end{bmatrix}A$交换了A的第一行和第二行。

对于某一维度的矩阵，所有的Permutation形成一个族群。在族群内，$P^{-1}=P^T$，$P^{-1}$和${P^T}$都在族群内。


#### Symmetric Matrix
formaul: $A^T = A$

> **Note:** $R^TR$ is always symetric.
> prove: $(R^TR)^T=R^T(R^T)^T=R^TR$


#### Product of elimination matrices $PA=LU$
$A=\begin{bmatrix}2&1 \\ 8&7 \end{bmatrix}$

Do elimination
$E_{21}A=\begin{bmatrix}1&0 \\ -4&1 \end{bmatrix}\begin{bmatrix}2&1 \\ 8&7 \end{bmatrix}=\begin{bmatrix}2&1 \\ 0&3 \end{bmatrix}=U$

Figure out L
$A=\begin{bmatrix}2&1 \\ 8&7 \end{bmatrix}=\begin{bmatrix}1&0 \\ 4&1 \end{bmatrix}\begin{bmatrix}2&1 \\ 0&3 \end{bmatrix}=LU$

> **Note:** $L=E^{-1}$

also
$A=\begin{bmatrix}2&1 \\ 8&7 \end{bmatrix}
=\begin{bmatrix}1&0 \\ 4&1 \end{bmatrix}\begin{bmatrix}2&1 \\ 0&3 \end{bmatrix}
=\begin{bmatrix}1&0 \\ 4&1 \end{bmatrix}\begin{bmatrix}2&0 \\ 0&3 \end{bmatrix}\begin{bmatrix}1 & 1 \over 2 \\ 0 & 1\end{bmatrix}
=LDU$

> **Note:** D is diagonal matrix，非对角线上的元素都为0

-------
Lecture 5
---

#### Vector Space
combinations still in space. --- ***CLOSE**

Requirements
:   $V+W$ and $cV$ are in the space
:   all combinations $cV+dW$ are in the space


#### Subspace
That's a space: some vectors inside the given vector space, but still make up a **vector space** of their own.

The **union** of two subspace P and L is **not a subspace**. (不一定)
The **intersection** of two subspace P and L is **a subspace**.

> **Note:** All subspace of $R^2$:
> 
>  - $R^2$
>  - any line through $\begin{bmatrix}0 \\0\end{bmatrix}$
>  - $\begin{bmatrix}0 \\0\end{bmatrix}$ alone

----------------

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

Lecture 11
---
#### New vector space M
suppose M: All 3 by 3 matrices.  dimension is 9

Subspace of M:

- upper triangulars: dimension is 6
- symmetric matrices: dimension is 6
- diagonal matrices: dimension is 3.

Basis for M = all 3 by 3's
$\begin{bmatrix}1&0&0 \\ 0&0&0 \\ 0&0&0 \end{bmatrix} ... \begin{bmatrix}0&0&0 \\ 0&0&0 \\ 0&0&1 \end{bmatrix}$

#### Rank one matrix
$A=\begin{bmatrix}1&4&5 \\ 2&8&10 \end{bmatrix}=\begin{bmatrix}1 \\ 2 \end{bmatrix} \begin{bmatrix}1&4&5\end{bmatrix}$

Rank One Matrix $A = uv^T$


In $R^4$, $v=\begin{bmatrix}v_1&v_2&v3&v_4\end{bmatrix}, v_1 + v_2+v_3+v_4=0$ is a subspace.


#### Graph
nodes, edges.

small world graph


--------------------

Lecture 12
---










  [1]: http://v.163.com/special/opencourse/daishu.html
