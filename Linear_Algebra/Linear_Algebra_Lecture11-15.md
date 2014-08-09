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



  [1]: https://raw.githubusercontent.com/JefferyFan/notebook/master/Linear_Algebra/assets/simple_graph.jpg
  [2]: https://raw.githubusercontent.com/JefferyFan/notebook/master/Linear_Algebra/assets/current_flow.jpg