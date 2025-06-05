---
marp: true
---
<style>
  section {
    font-family: 'LXGW Bright';
  }

  h1, h2, h3 {
    font-family: 'LXGW Bright';
  }
</style>
<style>
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
</style>
<style>
.note {
  background-color: #eef;
  padding: 10px;
  margin: 10px 0;
  text-align: left;
}
.trick {
  background-color: #fee;
  padding: 10px;
  margin: 10px 0;
  text-align: left;
}
</style>

# Final Review: Advanced Algebra

Speaker: Yixiao Qian

---

## Quick Review of Polynomial

Ignored.

---

## Quick Review of Determinant

Ignored.

---

## Quick Review of Matrix

- **Diagonal Dominant**: If $|a_{ii}| > \sum_{j\neq i}|a_{ij}|$, then $|A| \neq 0$.
- **Corollary**: There exists $t \in \mathbb{R}$ such that $tI + A$ is invertible.
- **Real Symmetric Matrix**: (1) $\lambda_i \in \mathbb{R}$; (2) $\xi_i$ belonging to different $\lambda_i$ are orthogonal.
- **Orthogonal Similarity**: There exists an orthogonal matrix $P$ such that $P^TAP = \Lambda$.

---

## Quick Review of System of Linear Equations

- **Rank of $A^TA$**: $r(A) = r(A^TA)$.
- **Existence of Solution of Normal Equation**: The solution of $A^TAx = A^Tb$ exists.

---

## Quick Review of Linear Space and Transformation

- $V_1$ and $V_2$ are non-trivial subspaces of $V$, prove $\exists \alpha \in V$ such that $\alpha \not\in V_1$ and $\alpha \not\in V_2$.
- $V_1$ and $V_2$ are two subspaces of $V$, prove that $V_1+V_2 = V_1 \cup V_2$ iff $V_1 \subseteq V_2$ or $V_2 \subseteq V_1$.
- **Dimension Theorem**: $V_1$, $V_2$ are subspaces of $V$ ($\operatorname{dim}V < \infty$), then
$$ \operatorname{dim}V_1 + \operatorname{dim}V_2 = \operatorname{dim}(V_1 + V_2) + \operatorname{dim}(V_1 \cap V_2). $$
- $\varphi: U \rightarrow V$, then $\operatorname{dim} \operatorname{Ker}(\varphi) + \operatorname{dim} \operatorname{Im}(\varphi) = \operatorname{dim} U$.
- **Idempotent Space Decomposition**: $\mathcal{A}$ idempotent, then $V = \operatorname{Ker}(\mathcal{A}) \oplus \operatorname{Im}(\mathcal{A})$.
- $\mathcal{A},\mathcal{B}$ idempotent, $\operatorname{Im}(\mathcal{A}) = \operatorname{Im}(\mathcal{B})$ iff $\mathcal{A}\mathcal{B} = \mathcal{B}$ and $\mathcal{B}\mathcal{A} = \mathcal{A}$.
- $\mathcal{A}, \mathcal{B}$ idempotent, $\operatorname{Ker}(\mathcal{A}) = \operatorname{Ker}(\mathcal{B})$ iff $\mathcal{A}\mathcal{B} = \mathcal{A}$ and $\mathcal{B}\mathcal{A} = \mathcal{B}$.
- Prove that $A^{-1}$ and $A^{\ast}$ can be represented as polynomials of $A$.
- Find (1) eigenvalues; (2) eigenvectors; (3) if $A$ is diagonalizable. $
A = \begin{bmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
0 & 0 & 3
\end{bmatrix}
$

---

## Quick Review of Jordan Form

- **Kernel Space Decomposition**: Let $f(x) = f_1(x)f_2(x)$ where $(f_1(x), f_2(x)) = 1$, then
$$ \operatorname{Ker}(f(\mathcal{A})) = \operatorname{Ker}(f_1(\mathcal{A})) \oplus \operatorname{Ker}(f_2(\mathcal{A})). $$
- **Jordan Matrix for $\lambda$**: $J(\lambda) = \operatorname{diag}(J_1(\lambda), \cdots, J_m(\lambda))$, where $m$ is the geometric multiplicity of $\lambda$, $J_i$ is a $n_i \times n_i$ matrix.
- Find the Smith normal form of $\lambda I - A$:
$$
A =
\begin{bmatrix}
-1 & 1 & 3\\
3 & 0 & -4\\
-2 & 1 & 4
\end{bmatrix}
$$
- Given $A$, find Jordan canonical form $J$, and transition matrix $P$ such that $P^{-1}AP = J$:

$$
A =
\begin{bmatrix}
  2 & 3 & 2\\
  1 & 8 & 2\\
  -2 & -14 & -3
\end{bmatrix}.
$$


---

## Quick Review of Quadratic Form

- **Existence of Canonical Form**
- **Elementary Transformation Method**: What if the diagonal elements are zero.
- Find the canonical form of $2x_1x_2 + 2x_1x_3 - 6x_2x_3$.
- $f = 5x_1^2 + 5x_2^2 + 3x_3^2 - 2x_1x_2 + 6x_1x_3 - 6x_2x_3$. Find an orthogonal transformation $x = Ty$ and corresponding canonical form.
- If $\lambda_1 \geq \lambda_2 \geq \cdots \geq \lambda_n$, then $\max_{x \in \mathbb{R}^n} \frac{x^TAx}{x^Tx} = \lambda_1, \quad \min_{x \in \mathbb{R}^n} \frac{x^TAx}{x^Tx} = \lambda_n$.
- Determine if $f = \sum\limits_{i = 1}^n x_i^2 + \sum\limits_{1 \leq i < j \leq n}x_ix_j$ is positive definite.
- **Both Positive Definite**: $A, B$ positive definite, $\exists P$, $P^TAP, P^TBP$ are diagonal.
- **One Positive Definite**: $A$ positive definite, $B$ real symmetric, $P^TAP$, $P^TBP$ are diagonal.


