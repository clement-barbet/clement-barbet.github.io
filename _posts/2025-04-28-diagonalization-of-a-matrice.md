---
layout: post
title: Diagonalization of a matrice
date: 2025-04-28 22:25 +0200
math: true
---

## Lesson

Diagonolazing a matrix 

$$
A = 
PDP^{-1}
$$

### Prerequesites
Find $$\chi_A(\lambda)$$ and factor it
Count distinct roots. If there's $$n$$ . $$A$$ is diagonalizable.

If not, for each repeated root $$\lambda$$ :
- Solve $$(A - \lambda I)\vec{v} = 0$$ and compute $$dim(ker(A - \lambda i))$$
- Check if it equals the root multiplicity in $$\chi_A$$


## Example

Diagonalize A


$$
A = 
\begin{bmatrix}
4 & 2 \\
1 & 3
\end{bmatrix}
$$

$$
\chi_A(\lambda) =
\begin{vmatrix}
4 - \lambda & 2 \\
1 & 3 - \lambda
\end{vmatrix}
$$

$$
= (4 - \lambda)(3 - \lambda) - 2 = 0
$$

$$
= 12 - 4 \lambda - 3 \lambda + {\lambda}^2 - 2 = 0
$$

$$
= {\lambda}^2 - 7 \lambda + 10 = 0
$$

$$
= (\lambda - 5)(\lambda - 2) = 0
$$

$$
= \lambda = 2, 5
$$

We've n roots. So the matrice is diagonilizable.

### Calculate $$D$$
$$
D = 
\begin{bmatrix}
2 & 0 \\
0 & 5
\end{bmatrix}
$$

### Calculate $$P$$

$$
(A - 2 \lambda) =
\begin{bmatrix}
4 - 2 & 2 \\
1 & 3 - 2 
\end{bmatrix}
=
\begin{bmatrix}
 2 & 2 \\
1 & 1
\end{bmatrix}
$$

$$
ker(A - 2I) =
\begin{bmatrix}
-1 \\
1
\end{bmatrix}
$$

$$
ker(A - 5I) = 
\begin{bmatrix}
2 \\
1
\end{bmatrix}
$$

$$
P =
\begin{bmatrix}
-1 & 2 \\
1 & 1
\end{bmatrix}
$$

### Calculate $$P^{-1}$$
$$
P^{-1} =
\begin{bmatrix}
\frac{-1}{3} & \frac{2}{3} \\
\frac{1}{3} & \frac{1}{3}
\end{bmatrix}
$$



## Exercises