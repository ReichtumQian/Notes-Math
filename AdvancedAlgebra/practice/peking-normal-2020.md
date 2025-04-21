
# Peking Normal University 2020 Advanced Algebra

## Problem 1

Let $f(x)$ be a polynomial over $\mathbb{F}$, and $a$ be a non-zero constant. If for any $x$, $f(x) = f(x + a)$, prove that $f(x)$ is a constant polynomial.

**Proof**. Without loss of generality, assume $f(x)$ is an $n$-order polynomial. Then according to the condition, for any $x_0 \in \mathbb{F}$,

$$ f(x_0) = f(x_0 + a) = f(x_0 + 2a) = \cdots = f(x_0 + na). $$

This implies that $f(x) - f(x_0)$ has $n + 1$ roots. If $n \neq 0$, then it contradicts the fact that an $n$-order polynomial only has $n$ roots. Hence, $n = 0$ and $f(x)$ is a constant polynomial.

## Problem 2

Let $A$ be an $m \times n$ matrix, and $b$ be an $m$-dimensional vector. Prove that (1) $r(A^TA) = r(A)$; (2) The solution of the system of linear equations $A^TAx = A^Tb$ exists.

**Proof**. (1) Consider two systems of linear equations $A^TAx = 0$ and $Ax = 0$. Now we prove that the solution of them are the same. If $x_0$ is a solution of $Ax = 0$, then 
$$ A^TAx_0 = A^T(Ax_0) = 0,$$
so the left-to-right direction holds. Next, if $x_0$ is a solution of $A^TAx = 0$, then 
$$x_0^TA^TAx_0 = (Ax_0)^T(Ax_0) = 0, $$
since $(Ax_0)^T(Ax_0)$ is the sum of square terms, then each element of $Ax_0$ is zero. In conclusion, since the two systems of linear equations have the same solutions, $r(A^TA) = r(A)$.

(2) We consider the rank of the matrix $(A^TA | A^Tb)$, on the one hand
$$ r(A^TA|A^Tb) = r(A^T[A|b]) \leq r(A^T) = r(A^TA). $$
On the other hand, $r(A^TA|A^Tb) \geq r(A^TA)$, which implies $r(A^TA|A^Tb) = r(A^TA)$ and the existence of the solution.

## Problem 3

Let $A, B$ be two $n$-order matrices, prove that $(AB)^\ast = B^\ast A^\ast$.

## Problem 4

Let $A$ be a real symmetric matrix and $|A| < 0$, prove that there exists $x$ such that $x^TAx < 0$.

**Proof**. Since $A$ is a real symmetric matrix, all the eigenvalues of $A$ are real, and $A$ is similar to a diagonal matrix. Suppose $P$ is an orthogonal matrix such that
$$ P^TAP = \Lambda = \operatorname{diag}(\lambda_1, \cdots, \lambda_n), $$
Since $|A| < 0$, $A$ has negative eigenvalue. Without loss of generality, suppose $\lambda_k < 0$. Then choose $y = \mathbf{e}_k$, and we have
$$ y^T \Lambda y = \lambda_k < 0, $$
let $x = Py$, then $x^TAx = y^T \Lambda y < 0$.

## Problem 5

Suppose $\sigma$ is a linear transformation on a finite-dimensional vector space $V$. Prove that $\sigma$ is injective if and only if $\sigma$ is surjective.

**Proof**. Left-to-right: If $\sigma$ is injective, then $\operatorname{Ker}(\sigma) = \{0\}$. Because if $\sigma(u) = \sigma(v)$, then
$$
\sigma(u - v) = 0 \Rightarrow u - v \in \operatorname{Ker} \sigma,
$$
and the definition of injective mapping implies that $u = v$, i.e., $\operatorname{Ker}(\sigma) = \{0\}$. Then the dimension theorem deduces that $\operatorname{Im}(\sigma) = \operatorname{dim}(V)$, so $\sigma$ is surjective.

Right-to-left: Since $\sigma$ is surjective, then $\operatorname{Im}\sigma = V$, $\operatorname{dim}(\operatorname{Im} \sigma) = n$, then $\operatorname{dim}(\operatorname{Ker} \sigma) = 0$, which is equivalent to $\sigma$ is injective.




