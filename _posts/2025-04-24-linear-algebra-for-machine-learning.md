---
layout: post
title: Linear Algebra for Machine Learning
date: 2025-04-24 20:27 +0200
math: true
---

# Exercises


Exercices are from the book [Mathematics for Machine Learning](https://mml-book.github.io/book/mml-book.pdf)

2.1 Let
$$
S = \mathbb{R} \setminus \{-1\}, 
\qquad 
a \star b := ab + a + b ,
\qquad 
a,b \in S .
$$
Show that $$(S, \star)$$ is an **Abelian group**.

<details markdown="1">
<summary>Show solution</summary>

**1. Closure**

For $$a,b \in S$$,  
$$a \star b = ab + a + b \in \mathbb{R}$$ is obvious.  
We must also show $$a \star b \neq -1$$.

$$
\begin{aligned}
ab + a + b
&= ab + a + b + 1 - 1 \\
&= a(b+1) + 1(b+1) - 1 \\
&= (a+1)(b+1) - 1 .
\end{aligned}
$$

Because $$a,b \neq -1$$, the factors $$a+1$$ and $$b+1$$ are both nonzero,  
so the expression above is never $$-1$$.  
Hence $$a \star b \in S$$, i.e. $$S$$ is closed under $$\star$$.

**2. Associativity**

We need $$(a \star b) \star c = a \star (b \star c)$$ for all $$a,b,c \in S$$.

$$
\begin{aligned}
(a \star b) \star c
&= (ab + a + b) \star c \\
&= (ab + a + b)c + (ab + a + b) + c \\
&= abc + ac + bc + ab + a + b + c \\
&= a + b + c + ab + ac + bc + abc .
\end{aligned}
$$

Similarly,

$$
\begin{aligned}
a \star (b \star c)
&= a \star (bc + b + c) \\
&= a(bc + b + c) + a + bc + b + c \\
&= abc + ab + ac + a + bc + b + c \\
&= a + b + c + ab + ac + bc + abc .
\end{aligned}
$$

The two expressions match, so $\star$ is associative.

**3. Identity element**

Let $$e \in S$$ satisfy $$a \star e = a$$ for all $$a \in S$$:

$$
ae + a + e = a 
\quad \Rightarrow \quad
ae + e = 0 
\quad \Rightarrow \quad
e(a+1) = 0 .
$$

Since $$a \ne -1$$, we conclude $$e = 0$$.  
Indeed, $$0 \in S$$ and

$$
a \star 0 = a \cdot 0 + a + 0 = a, 
\qquad
0 \star a = 0 \cdot a + 0 + a = a .
$$

So $$e = 0$$ is the identity.

**4. Inverse element**

Given $$a \in S$$, find $$y \in S$$ with $$a \star y = 0$$:

$$
ay + a + y = 0 
\quad \Rightarrow \quad
y(a + 1) = -a 
\quad \Rightarrow \quad
y = \frac{-a}{a+1} .
$$

Since $$a \ne -1$$, the denominator is nonzero, so $$y \in S$$.  
Thus every element $$a$$ has an inverse:

$$
a^{-1} = \frac{-a}{a+1} .
$$

**5. Commutativity**

$$
a \star b = ab + a + b = ba + b + a = b \star a ,
$$

because multiplication and addition are commutative in $$\mathbb{R}$$.

**Conclusion**

All group axioms are satisfied and the operation $\star$ is commutative, so

$$
\left( \mathbb{R} \setminus \{-1\},\; \star \right)
$$

is an **Abelian group**.

</details>

2.2 Solve
$$ 3 \star x \star x = 15$$