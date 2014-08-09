

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



--------------------
Lecture 4
---

#### Transpose


-------
Lecture 5
---

#### Vector Space
Requirements
:   $V+W$ and $cV$ are in the space
:   all combinations $cV+dW$ are in the space


#### Subspace
That's a space: some vectors inside the given vector space, but still make up a **vector space** of their own.

The union of two subspace P and L is not a subspace. (不一定)
The Intersection of two subspace P and L is a subspace.

----------------

Lecture 6
----

$$Ax=\begin{bmatrix}1&1&2 \\ 2&1&3 \\ 3&1&4 \\ 4&1&5 \end{bmatrix}\begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = b$$



#### column space $C(A)$
Definition
:   all linear combinations of the columns. --- subspace of $R^m$

> In the exmaple, the column space is subspace of $R^4$

Which b's allow this system $Ax=b$ to be solved?
:   Can solve $Ax=b$ exactly when b is $C(A)$

Pivot Column
:   the columns that are linear independent.

>In the example, pivot columns are column 1 and 2. Or column 2 and 3. 
Because $Column 3 = Column 1 + Column2$

Dimension
:   


#### Nullspace $N(A)$
Definition
:   all solutions $x$ that $Ax=0$ --- subspace of $R^n$

> **Example: ** N(A) is $c\begin{bmatrix}1 \\ 1 \\ -1 \end{bmatrix}$

<br/>
> **Note:** must contains **ZERO vector**


#### row space


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

  [1]: http://v.163.com/special/opencourse/daishu.html
