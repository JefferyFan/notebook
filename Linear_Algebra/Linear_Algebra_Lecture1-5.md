Linear Algebra
===
Lecture 1-5

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



