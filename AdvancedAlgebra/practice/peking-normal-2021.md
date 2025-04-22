
# Peking Normal University 2020 Advanced Algebra

## Problem 1

Let $A = \operatorname{diag}\{a_{1}, a_{2}, \cdots, a_{n}\}$, where $a_{i} \neq a_{j}$ when $i \neq j$. Denote $W = \{X \in M_{n}(\mathbb{R}): XA = AX\}$. Prove (1) $W$ is a linear space on $\mathbb{R}$; (2) $W$ is the set composed of all the $n$-order diagonal matrices; (3) $I, A, \cdots, A^{n-1}$ is a basis of $W$.

**Proof**. (1) Omitted. (2) First it is not hard to see that all the diagonal metrices satisfy $XA = AX$. Assume there exists $x_{ij} \neq 0, i \neq j$, then $(XA)_{ij} = a_{j}x_{ij}$ while $(AX)_{ij} = a_{i}x_{ij}$, then $XA \neq AX$. (3) Let $k_{1}I + \cdots + k_{n}A^{n-1} = O$ yields all the coefficients are $0$, then the dimension of $I, A, \cdots, A^{n-1}$ is $n$. This means that $W$ can be linearly represented by this vector set.

## Problem 2

Determine if the polynomial $f(x) = x^{5} - 3x^{2} + 5$ over $\mathbb{C}$ has multiple factors.

**Solution**. Consider $f^{\prime}(x) = 5x^{4} - 6x = 5x(x^{3} - \frac{6}{5})$. Since $f(0) \neq 0$, then $x$ is not a factor of $f(x)$. Assume $(x^{3} - \frac{6}{5}) = (x-x_{1})(x-x_{2})(x - x_{3})$, if any of $x_{1}, x_{2}, x_{3}$ is root of $f(x)$, then
$$ 0 = \frac{6}{5}x^{2} - 3x^{2} + 5 = 5 - \frac{9}{5}x^{2} \Rightarrow x^{2} = \frac{25}{9} \Rightarrow x = \pm \frac{5}{3}, $$
which do not satify $x^{3} = \frac{6}{5}$, thus $f(x)$ does not have any multiple factor/root on $\mathbb{C}$.

## Problem 3

If the quadratic form $f$ is positive definte, find the range of $a$:
$$ f(x_{1}, x_{2}, x_{3}) = ax_{1}^{2} + ax_{2}^{2} + ax_{3}^{2} + 2x_{1}x_{2} - 2x_{1}x_{3} - 2x_{2}x_{3}. $$

**Solution**. The matrix of the quadratic form is
$$ A = \begin{bmatrix} 
a & 1 & -1\\
1 & a & -1\\
-1 & -1 & a
\end{bmatrix}.  $$
$f$ is positive definite if and only if all the principal minors of $A$ are positive. Then $a > 0$, $a^{2} - 1 > 0$, and $a^{3} - 3a + 2 > 0$. Therefore when $a > 1$, $f$ is positive definite.

## Problem 4

Let $\mathcal{A}$ be a linear transformation on $V$, satisfying $\mathcal{A}^{3} = \mathcal{A}$. Prove that
$$ V = \operatorname{Ker}(\mathcal{A}^{2}) \oplus \operatorname{Im}(\mathcal{A}^{2}). $$

**Proof**. Since $\mathcal{A}^{3} = \mathcal{A}$, applying $\mathcal{A}$ again on both sides yields
$$ \mathcal{A}^{4} = \mathcal{A}^{2}, $$
which implies that $\mathcal{A}^{2}$ is an idempotent transformation. Now we prove that for any idempotent transformation $\mathcal{B}$, we have $V = \operatorname{Ker}(\mathcal{B}) \oplus \operatorname{Im}(\mathcal{B})$. For any $\alpha \in V$,
$$ \alpha = (\alpha - \mathcal{B}\alpha) + \mathcal{B}\alpha, $$
where $\alpha - \mathcal{B} \alpha \in \operatorname{Ker}(\mathcal{B})$ and $\mathcal{B}\alpha \in \operatorname{Im}(\mathcal{B})$, so $V = \operatorname{Ker}(\mathcal{B}) + \operatorname{Im}(\mathcal{B})$. Next, we prove it is direct sum. For any $\beta \in \operatorname{Ker}(\mathcal{B}) \cap \operatorname{Im}(\mathcal{B})$, there exists $\gamma \in V$ such that $\mathcal{B}\gamma = \beta$, then
$$ \mathcal{B} \gamma = \mathcal{B}^{2} \gamma = \mathcal{B}\beta = 0, $$
which implies that $\beta = 0$, and the intersection of the kernel and image of $\mathcal{B}$ only contains zero vector. So the sum is a direct sum.

## Problem 5

Let $A$ be an $n$-order complex matrix. Prove that there exists a positive integer $N$ such that $A^{N} = I$ if and only if $A$ is diagonalizable and all the eigenvalues are roots of unity.

**Proof**. Left-to-right: Since $A$ is a complex matrix, there exists an invertible matrix $P$ such that $P^{-1}AP = J$, where $J$ is the Jordan canonical form of $A$. Then $I = P^{-1}A^{N}P = J^{N}$, it is direct to see that if $J$ is not a diagonal matrix, then $I = J$ never holds. Since the diagonal entries of $J$ are eigenvalues of $A$, then $\lambda_{i}^{N} = 1$, which implies that all the eigenvalues of $A$ are roots of unity.

Right-to-left: Since $A$ is diagonalizable, then there exists an invertible matrix $P$ such that $P^{-1}AP = \Lambda$, where $\Lambda$ is a diagonal matrix with its diagonal entries being the eigenvalues of $A$. Sicne $\lambda_{i}^{N_{i}} = 1$, then choose $N = \max_{i}(N_{i})$, then 
$$ P^{-1}A^{N}P = \Lambda^{N} = I \Rightarrow A^{N} = I. $$
