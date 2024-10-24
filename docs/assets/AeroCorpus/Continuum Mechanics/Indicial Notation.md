---
layout: default
title: Notes
permalink: /indicialNotation
---

# Indicial Notation
There is a summation convention introduced by Albert Einstein which uses Dummy Indices. 

$$
s = a_1 x_1 + a_2 x_2 + \ldots + a_n x_n = \sum_{i=1}^n a_i x_i
$$

can be reformulated as 

$$
s = a_i x_i
$$

where i is a dummy index, *which appears exactly twice* in a product. Since we are working in physical space, it is implicit that $n=3$. In some cases, $n=2$ for 2-D space. A dummy index can be replaced by any letter i.e. $s = a_j x_j = a_k x_k$ where $j$ and $k$ are dummy indices.

Though $s=\sum_{i=1}^n a_i x_i y_i$ is acceptable, it cannot be reformulated as $s=a_i x_i y_i$ in indicial notation since it appears more than twice. We can use dummy indices for double (or triple) summations as well: 

$$
s = \sum_{i=1}^n \sum_{j=1}^n a_{ij} x_i y_j = a_{ij} x_i y_j.
$$

The Cartesian coordinate system is useful for indicial notation. However, indicial notation falls short in non-orthonormal (where there are orthogonal unit basis vectors) coordinate systems which are used in curvilinear space.

### Free Indices
Given 

$$
\begin{align} 
x_1' &= a_{11} x_1 + a_{12} x_2 + a_{13} x_3 = a_{1j}x_j,\\
x_2' &= a_{21} x_1 + a_{22} x_2 + a_{23} x_3 = a_{2j}x_j,\\
x_3' &= a_{31} x_1 + a_{32} x_2 + a_{33} x_3 = a_{3j}x_j
\end{align}
$$

we can represent the vector $x'$ as 

$$
x_i'=a_{ij} x_j.
$$

The free indices are thus the subscripts $i$ since it appears exactly once in every term of an equation. We can use free indices with vector notation as well. An overbar represents a vector. Given some Cartesian basis $\bar{e}$, we know that 

$$
||\bar{e_i}|| = 1 = |\bar{e_i}|.
$$

We also know the dot product of the basis vectors 

$$
\bar{e}_1 \cdot \bar{e}_2 = 0.
$$

An example of using dummy and free indices in a vector equation is 

$$
\bar{e}_i = Q_{ij} e_j.
$$

Here, the dummy index is $j$ and the free index is $i$. There can also be more than one free index appearing in an equation i.e. 

$$
T_{ij} = A_{ij} B_{mj}
$$

where $i$ and $j$ are free indices and $m$ is the dummy index. Note that $T_{ij} = A_{im} B_{mn}$ is meaningless.

### Kronecker Delta
Denoted by $\delta_{ij}$ and defined by 

$$
\delta_{ij} = \begin{cases} 1 & i=j, \\ 0 & i \ne j \end{cases}.
$$

In Matrix form: 

$$
[S_{ij}] = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} = \begin{bmatrix} \delta_{11} & \delta_{12} & \delta_{13} \\ \delta_{21} & \delta_{22} & \delta_{23} \\ \delta_{31} & \delta_{32} & \delta_{33} \end{bmatrix}
$$

The properties of the Kronecker delta are that
1. $\delta_{ii} = \delta_{11} + \delta_{22} + \delta_{33} = 3$
2. $\delta_{im} a_m = \delta_{11} a_1 + \delta_{12} a_2 + \delta_{13} a_3 = a_1 \rightarrow \delta_{im} a_m = a_i$ where $i$ is the free index and $m$ is the dummy index.
3. $\delta_{1m} T_{mj} = \delta_{11} T_{ij} + \delta_{12} T_{2j} + \delta_{13} T_{3j} = T_{1j} \rightarrow \delta_{im} T_{mj} = T_{ij}$
4. If $$\{\bar{e}_1, \bar{e}_2, \bar{e}_3\}$$ is orthonormal, then $$\bar{e}_i \cdot \bar{e}_j = \delta_{ij}$$

Any vector $\bar{a}$ may be written in terms of its Cartesian components as 

$$
\bar{a} = a_1 e_1 + a_2 e_2 + a_3 e_3 = a_i e_i = a_j e_j
$$

### Permutation (Levi-Civita) Symbol
It is denoted by $\epsilon_{ijk}$ and defined by 

$$
\epsilon_{ijk} = \begin{cases}+1 & \text{ when } i,j,k \text{ form an even permutation}, \\ -1 & \text{ when } i,j,k \text{ form an odd permutation}, \\ 0 & \text{ otherwise} \end{cases}
$$

or more directly 

$$
\begin{align} 
\epsilon_{123} = \epsilon_{231} = \epsilon_{312} = & +1 \\ 
\epsilon_{321} = \epsilon_{132} = \epsilon_{213} = & -1
\end{align}
$$

and wherever the index is repeated, it is equal to zero. If $$\{\bar{e}_1, \bar{e}_2, \bar{e}_3\}$$ is an orthonormal basis, then 

$$
\bar{e}_i \times \bar{e}_j = \epsilon_{ijk} \bar{e}_k.
$$

Example: $$\bar{e}_1 \times \bar{e}_2 = \epsilon_{211} \bar{e}_1 + \epsilon_{112} \bar{e}_2 + \epsilon_{113} \bar{e}_3 = -\bar{e}_3$$. We can rewrite the cross product as 

$$
\bar{a} \times \bar{b} = \epsilon_{ijk} a_i b_j
$$

where $k$ is the index of the product. We can also express the product of two Levi-Civita symbol by write through the Kronecker Delta 

$$
\epsilon_{ijm}\epsilon_{klm} = \delta_{ik} \delta_{jl} - \delta_{il} \delta_{jk}.
$$

### Manipulations with Indicial Notation
1. Substitutions: If $a_i = V_{im} b_m, b_i = V_{im} C_m$. Let $b_m = V_{mn} C_n \rightarrow$ substitute into the first equation. Finally 

$$
a_i = V_{im} V_{mn} C_n
$$

2. Multiplication: $p = a_m b_m, q=c_m d_m$, evaluate $pq = a_m b_m c_n d_n$.
3. Dot product: $$\bar{a} = \bar{a}_i \bar{e}_i, \bar{b} = b_i \bar{e}_j$$, evaluate $$\bar{a} \cdot \bar{b} = a_i \bar{e}_i \cdot b_j \bar{e}_j$$. $$\bar{a} \cdot \bar{b} = a_i b_j \bar{e}_i \cdot \bar{e}_j = a_i b_i$$
4. Factoring: Given $T_{ij} n_j - n_i = 0$ where $n_i = \delta_{ij} n_j$. 

$$
T_{ij} n_j - \delta_{ij} n_j = (T_{ij} - \delta_{ij}) n_j = 0
$$

5. Contraction: $T_{ii} = T_{11} + T_{22} + T_{33}$ is the contraction of $T_{ij}$. $T_{ijk} = T_{i11} + T_{i22} + T_{i33}$ is one contraction of $T_{ijk}$.