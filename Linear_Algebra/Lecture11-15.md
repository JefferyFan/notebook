Linear Algebra
===
Lecture 11-15

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
#### Graph and Network
Graph: Nodes, Edge

![Simple Graph][1]

#### Incidence Matrix
The columns represent nodes, the rows represent edges.
$A=\begin{bmatrix}-1&1&0&0 \\ 0&-1&1&0 \\ -1&0&1&0 \\ -1&0&0&1 \\ 0&0&-1&1\end{bmatrix}$

> **Note:** Edge 1,2,3 form subgraph or loop.
> $dim N(A)=1$

1. potentials at nodes: $x=x_1, x_2, x_3, x_4$
$Ax$: find potential difference on edges
2. currents $y_1, y_2, y_3, y_4, y_5$ one edges
3. $A^Ty=0$  --- Kirchaffs Current Law
$dimN(A^T)=2$

![Current Flow][2]

$\begin{bmatrix}-1&0&-1&-1&0 \\ 1&-1&0&0&0 \\ 0&1&1&0&-1 \\ 0&0&0&1&1 \end{bmatrix} \begin{bmatrix}y_1\\y_2\\y_3\\y_4\\y_5\end{bmatrix}=\begin{bmatrix}0\\0\\0\\0\end{bmatrix}$
即是:
$-y_1-y_4-y-4=0 \Rightarrow$   KCL，节点电流和为0
$\vdots$

> **Note:** Basis for $N(T)$ 可以根据graph中loop来找。
> $dim N(A^T)=m-r$

**Tree**: graph with no loop.

> **Note:** number of loops = number of edges - (number of nodes - 1)
> That is Euler's formula: **number of nodes - number of edges + number of loops = 1**



-----------------

Lecture 13
---
review

------------------

Lecture 14
---
#### Orthogonal Vectors 
$x \cdot y = x^Ty=0 \Rightarrow x \bot y \Rightarrow \begin{Vmatrix}x\end{Vmatrix}^2+\begin{Vmatrix}y\end{Vmatrix}^2=\begin{Vmatrix}x+y\end{Vmatrix}^2$

$\begin{Vmatrix}x\end{Vmatrix}^2=x^Tx$

> **Note:** 利用勾股定理可证明以上formula

**Zero vector is orthogonal to any vector.**


#### Orthogonal Subspaces 
Subspace S is orthogonal to subspace T 
means: every vector in S is orthogonal every vector in T.

若两个子空间互相垂直且相交，肯定不会相交于一个非零向量。

1. row space is orthogonal to nullspace
prove: 
for $x$ in nullspace, $Ax=0$
that is:
$$\begin{bmatrix}row_1 \\ row_2 \\ \cdots \\ row_m\end{bmatrix}x=0 \\ \Rightarrow row_1 \cdot x = 0,\cdots $$
Then the basis of row space is orghogonal to all x in nullspace, so row space is orghogonal to nullspace.

2. column space is orghogonal to nullspace of $A^T$


#### Complements
nullspace and row space are orthogonal complements in $R^n$
Nullspace contains **all** vectors $\bot$ row space.





-------------

Lecture 15
---
$N(A^TA) = N(A)$ and $rank\;of \;AA^T=rank \;of\; A$
$AA^T$ is invertible exactly if A has independent columns.

#### Two dimension projection
b projection on a:
![Projection][3]

$a^T(b-xa)=0 \Rightarrow xa^Ta=a^Tb \Rightarrow x=\frac {a^Tb} {a^Ta}$

Projection $p=a \frac {a^Tb} {a^Ta} $

Projection Matrix --- P: projection $p = Pb$
$Projectjon \; Matrix\;P= \frac {aa^T} {a^Ta}$

Property of Projection Matrix:

1. $C(P)$ is line through $a$
2. $rank(P)=1$
3. $P^T=P$
4. $p^2=P$


#### WHY project?
Because $Ax=b$ may have no solution. 
Solve $A\widehat x=p$ instead. $p$ is projection of b onto column space.

#### Three(or more) dimension projection.
$p=A\widehat x$ Find $\widehat x$
Key: $e=b-A\widehat x$ is perpendicular(垂直) to the plane.
$a_1,a_2$ are the basis of plane.

$\begin{bmatrix}a_1^T \\ a_2^T \end{bmatrix}(b-A\widehat x)=\begin{bmatrix}0\\0\end{bmatrix} \Rightarrow A^T(b-A\widehat x)=0$
$\Rightarrow $ $e$ in $N(A^T)$ $\Rightarrow e \bot C(A)$
$\Rightarrow A^TA \widehat x=A^Tb$
$\Rightarrow \widehat x=(A^TA)^{-1}A^Tb$
$\Rightarrow p=A\widehat x=A(A^TA)^{-1}A^Tb$
$\Rightarrow P=A(A^TA)^{-1}A^T$

Property of Projection Matrix P:

1. $P^T=P$
2. $P^2=P$


#### Least Squares --- Fitting by a line



------------------------





  [1]: https://raw.githubusercontent.com/JefferyFan/notebook/master/Linear_Algebra/assets/simple_graph.jpg
  [2]: https://raw.githubusercontent.com/JefferyFan/notebook/master/Linear_Algebra/assets/current_flow.jpg
  [3]: https://raw.githubusercontent.com/JefferyFan/notebook/master/Linear_Algebra/assets/projection.jpg