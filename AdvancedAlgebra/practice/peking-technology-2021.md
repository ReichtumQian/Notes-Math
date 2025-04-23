
# Peking University Institution of Technology Advanced Algebra 2021

## Problem 1: True or False?

T, T, F, T, T, T, NG, T, T, T

## Problem 2

Let $A$ be a $m$-order matrix, and $B$ be a $n$-order matrix. Find the adjugate matrix of 
$$ C = \begin{bmatrix} A & O \\ O & B \end{bmatrix} $$

**Solution**. Since $C^\ast C = |C| I$, we get $C^\ast = |A| \cdot |B| C^{-1}$, then
$$ C^\ast = \begin{bmatrix}
    |B| A^\ast & O\\
    O & |A| B^\ast
\end{bmatrix} $$

## Problem 4

Let $f(x),g(x)$ be two relatively prime polynomials, $A$ is an $n$-order matrix over $\mathbb{F}$. Prove that $f(A)g(A) = O$ if and only if 
$$ r(f(A)) + r(g(A)) = n. $$

**Proof**. Since $f(x), g(x)$ are relatively prime, then there exists $u(x), v(x)$ such that $u(x)f(x) + v(x)g(x) = 1$. Consider

$$ 
  \begin{bmatrix}
  f(A) & O\\
  O & g(A)
  \end{bmatrix}
  \rightarrow
  \begin{bmatrix}
  f(A) & v(A)g(A)\\
  O & g(A)
  \end{bmatrix}
  \rightarrow
  \begin{bmatrix}
  f(A) & u(A)f(A) + v(A)g(A)\\
  O & g(A)
  \end{bmatrix}
$$
Which is equivalent to
$$
  \begin{bmatrix}
  f(A) & I\\
  O & g(A)
  \end{bmatrix}
  \rightarrow
  \begin{bmatrix}
  O & I\\
  -f(A)g(A) & g(A)
  \end{bmatrix}
  \rightarrow
  \begin{bmatrix}
  O & I\\
  -f(A)g(A) & O
  \end{bmatrix}.
$$
Then we can see that $r(f(A)) + r(g(A)) = n$ if and only if $f(A)g(A) = O$.

## Problem 5

Let $W$ be a finite-dimensional $\mathcal{A}$-invariant subspace of $V$, where $\mathcal{A}$ is invertible. Prove (1) $\mathcal{A}|_W$ is an invertible transformation on $W$; (2) $W$ is an invariant subspace of $\mathcal{A}^{-1}$, and $(\mathcal{A}|_W)^{-1} = \mathcal{A}^{-1}|_W$

**Proof**. (1) Let $\epsilon_1,\cdots,\epsilon_r$ be a basis of $W$, and $\epsilon_1,\cdots,\epsilon_n$ be a basis of $V$. Since $\mathcal{A}$ is an invertible transformation in $V$, then
$$ k_1 \mathcal{A} \epsilon_1 + \cdots + k_n \mathcal{A} \epsilon_n = 0 $$
if and only if $k_1 = k_2 = \cdots = k_n = 0$. Similarly, 
$$ t_1 \mathcal{A} \epsilon_1 + \cdots + t_r \mathcal{A}\epsilon_r = 0 $$
if and only if $t_1 = t_2 = \cdots = t_r = 0$. This means that $\mathcal{A}|_W$ is an invertible linear transformation on $W$.

(2) Since $\mathcal{A}$ is invertible and $W$ is $\mathcal{A}$-invariant. Then $\mathcal{A}\alpha \in W$ if and only if $\alpha \in W$. For any $\alpha = (\epsilon_1,\cdots,\epsilon_r)\mathbf{x}\in W$, 
$$ \mathcal{A}(\mathcal{A}^{-1}\alpha) = \alpha \in W, $$
so $\mathcal{A}^{-1}\alpha \in W$, which indicates that $W$ is $\mathcal{A}^{-1}$-invariant. And
$$ \mathcal{A}^{-1}|_W (\epsilon_1, \cdots, \epsilon_r) =  (\mathcal{A}^{-1}\epsilon_1,\cdots,\mathcal{A}^{-1}\epsilon_r) = (\mathcal{A}|_W)^{-1}(\epsilon_1,\cdots,\epsilon_r).$$
So $(\mathcal{A}|_W)^{-1} = \mathcal{A}^{-1}|_W$.

## Problem 6

Let $U$ be a finite-dimensional subspace of Euclidean space $V$. Prove that $V = U \oplus U^{\perp}$.

**Proof**. By the difinition of orthogonal complement, we know $V = U + U^{\perp}$. Now, we prove that it is direct sum. For any $\alpha \in U$ and $\beta \in U^{\perp}$, assume $k_1 \alpha + k_2 \beta = 0$, then
$$ k_1 \langle \alpha, \alpha \rangle + k_2 \langle \alpha, \beta \rangle = 0 \Rightarrow k_1 \langle \alpha, \alpha\rangle = 0 \Rightarrow k_1 = 0 \Rightarrow k_1 = k_2 = 0. $$
So elements in $U$ and $U^{\perp}$ are linearly independent. Take $\alpha \in U \cap U^{\perp}$, and assume $U = \operatorname{span}(\epsilon_1,\cdots,\epsilon_m)$, and $U^{\perp} = \operatorname{span}(\eta_1,\cdots,\eta_n)$, then
$$ \alpha = k_1 \epsilon_1 + \cdots + k_m \epsilon_m = t_1 \eta_1 + \cdots + t_n\eta_n. $$
Then $k_1 \epsilon_1 + \cdots + k_m\epsilon_m - t_1\eta_1 - \cdots - t_n\eta_n = 0$, by the linearly independent property, we know all the coefficients are zero. So $\alpha = 0$, which means $U + U^{\perp} = U \oplus U^{\perp}$.

## Problem 7

Let $A$ be an $n$-order complex matrix with $r(A) = 1$. Find the Jordan canonical form of $A - I$.


