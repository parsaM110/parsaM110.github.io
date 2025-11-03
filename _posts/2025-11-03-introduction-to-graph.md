---
title: Introduction to Graph Theory
date: 2025-05-04 11:02:00 +0800
categories: [Math]
tags: []
author: parsa
math: true
image:
  path: assets/headers/2025-05-04-event-triggered-control-and-stability.png
  alt: Math
---
# Graph Laplacian, Eigenvalues, and Eigenvectors

## Eigenvalue Equation
$$
A v = \lambda v
$$

---

## Laplacian Matrix \( L \)

Given an adjacency matrix \( A \) and degree matrix \( D \):
$$
L = D - A
$$

- Row sum of \( L \) is zero:  
  $$
  \sum_j L_{ij} = 0
  $$
- Therefore:
  $$ 
  L \cdot \mathbf{1} = 0 
  $$
  where:
  $$
  \mathbf{1} =
  \begin{bmatrix}
  1 \\
  1 \\
  \vdots \\
  1
  \end{bmatrix}
  $$

Thus, \( \lambda = 0 \) is an eigenvalue, and \( \mathbf{1} \) is an eigenvector.

---

## Normalized Form
$$
I - L = \frac{1}{m} \mathbf{1}\mathbf{1}^T, \quad \|v\| < 1
$$

---

## Graph Example

v1 ---- v2
| |
v4 ---- v3


### Adjacency Matrix \( A \)
$$
A =
\begin{bmatrix}
0 & 1 & 0 & 1 \\
1 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
1 & 0 & 1 & 0
\end{bmatrix}
$$

### Degree Matrix \( D \)
$$
D =
\begin{bmatrix}
2 & 0 & 0 & 0 \\
0 & 2 & 0 & 0 \\
0 & 0 & 2 & 0 \\
0 & 0 & 0 & 2
\end{bmatrix}
$$

### Laplacian Matrix \( L = D - A \)
$$
L =
\begin{bmatrix}
2 & -1 & 0 & -1 \\
-1 & 2 & -1 & 0 \\
0 & -1 & 2 & -1 \\
-1 & 0 & -1 & 2
\end{bmatrix}
$$

---

## Eigenvalue Properties

- \(0\) is an eigenvalue of \(L\)  
- Corresponding eigenvector:
  $$
  \mathbf{1} = 
  \begin{bmatrix}
  1 \\ 1 \\ 1 \\ 1
  \end{bmatrix}
  $$
- General eigenvalue equation:
  $$
  Lx = \lambda x
  $$

---

## Example Calculation

Let:
$$
x =
\begin{bmatrix}
3 \\ 4 \\ 5 \\ 6
\end{bmatrix}
$$

Then:
$$
Lx =
\begin{bmatrix}
2 & -1 & 0 & -1 \\
-1 & 2 & -1 & 0 \\
0 & -1 & 2 & -1 \\
-1 & 0 & -1 & 2
\end{bmatrix}
\begin{bmatrix}
3 \\ 4 \\ 5 \\ 6
\end{bmatrix}
=
\begin{bmatrix}
2(3) - 4 - 6 \\
-3 + 2(4) - 5 \\
-4 + 2(5) - 6 \\
-3 - 5 + 2(6)
\end{bmatrix}
=
\begin{bmatrix}
-4 \\ 0 \\ 0 \\ 4
\end{bmatrix}
$$

---

## Notes

- **Adjacency matrix (A):** Shows which nodes are connected.  
- **Degree matrix (D):** Diagonal with node degrees.  
- **Laplacian (L):** Symmetric, positive semi-definite.  
- **Eigenvalues:**  
  - Smallest eigenvalue = 0  
  - Number of zero eigenvalues = number of connected components  
- **Fiedler Vector:** Eigenvector of the 2nd smallest eigenvalue (used for clustering)

---

## Sources 
- https://csustan.csustan.edu/~tom/Clustering/GraphLaplacian-tutorial.pdf


<!-- End of document -->
