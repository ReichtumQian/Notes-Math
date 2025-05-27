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

# Bilinear Function and Quadratic Form

Speaker: Yixiao Qian

---

# Concept and Canonical Form of Quadratic Forms

---

## Concept of Quadratic Form

- **Quadratic Form**: $f(x_1,x_2,\cdots,x_n) = \sum_{i=1}^n a_{ii}x_i^2 + \sum_{1 \leq i < j \leq n}2a_{ij}x_ix_j$.
- **Matrix Form**: $A = (a_{ij})$, $f = x^TAx$.
- **Canonical Form**: $P^TAP = D$ where $D$ is diagonal, $x^TDx$ is called canonical form of $f$.
- **Completing-the-Square Method**: (1) If $x_1^2$ exists, group all terms containing $x_1$ togather; (2) If $x_1^2$ does not exist, but $x_1x_2$ exists, then let $x_1=y_1+y_2$, $x_2 = y_1-y_2$.
- **Elementary Transformation Method**: Perform row and corresponding column transformation on
$$
\begin{pmatrix}
  A \\ I
\end{pmatrix} \rightarrow
\begin{pmatrix}
  P^TAP \\ P
\end{pmatrix}
$$
- **Orthogonal Transformation Method**: (1) Find $\lambda_1,\cdots,\lambda_n$ (2) Find eigenvectors, for eigenvectors corresponding to the same $\lambda_i$, orthogonalization is needed.

---

## Application of Elementary Transformation Method

- Find the canonical form of $2x_1x_2 + 2x_1x_3 - 6x_2x_3$.

<div class=note>

$$
P =
\begin{bmatrix}
  1 & - \frac{1}{2} & 3\\
  1 & \frac{1}{2} & -1\\
  0 & 0 & 1
\end{bmatrix}, \quad
P^TAP = 
\begin{bmatrix}
  2 & & \\
    & - \frac{1}{2} & \\
   & & 6
\end{bmatrix}
$$

</div>

---

## Application of Orthogonal Transformation Method

- $f = 5x_1^2 + 5x_2^2 + 3x_3^2 - 2x_1x_2 + 6x_1x_3 - 6x_2x_3$. Find an orthogonal transformation $x = Ty$ and corresponding canonical form.

<div class=note>

(1) Eigenvalues: $\lambda_1 = 0$, $\lambda_2 = 4$, $\lambda_3 = 9$.
(2) Eigenvectors: $v_1 = (-1, 1, 2)^T$, $v_2 = (1,1,0)^T$, $v_3 = (1,-1,1)^T$
(3) Normalized Eigenvectors: $v_1 = \frac{1}{\sqrt{6}}(-1,1,2)^T$, $v_2 = \frac{1}{\sqrt{2}}(1,1,0)^T$, $v_3 = \frac{1}{\sqrt{3}}(1,-1,1)$.

</div>

- If $\lambda_1 \geq \lambda_2 \geq \cdots \geq \lambda_n$, then $\max_{x \in \mathbb{R}^n} \frac{x^TAx}{x^Tx} = \lambda_1, \quad \min_{x \in \mathbb{R}^n} \frac{x^TAx}{x^Tx} = \lambda_n$.

<div class=note>

(1) $\lambda_1 I - A$ is positive semi-definite, $x^T(\lambda_1 I - A)x \geq 0$, so $\lambda_1 \geq \frac{x^TAx}{x^Tx}$.
(2) There exists an unit vector $x_0 \in \mathbb{R}^n$ such that $Ax_0 = \lambda_1 x_0$, so $x_0^TAx_0 = \lambda_1 x_0^Tx_0 = \lambda_1$.

</div>

- Corollary: If $\lambda(A) > a$, $\lambda(B) > b$, then $\lambda(A+B) > a+b$.

---

# Positive Definite Quadratic Forms

---

## Key Points of Positive Definite Quadratic Forms

- **Positive Definite Quadratic Form**: For any non-zero $x_1,\cdots,x_n$, $f(x_1,\cdots,x_n) > 0$.
- **Minor Perspective**: Iff all leading principal minors (or all principal minors) greater than $0$
- **Congruent Perspective**: Iff congruent to the identity matrix (decomposed as $A = P^TP$).
- **Eigenvalue Perspective**: Iff all eigenvalues are positive.
- **Closure under Operations**: $A^{-1}$, $A^k$, $A+B$, $A^{\ast}$ are all positive definite.

<div class=note>

(1) The eigenvalues of $A^{-1}$, $A^k$, $A^{\ast}$ are positive. (2) $x^T(A+B)x = x^TAx+x^TBx>0$.

</div>

- **Diagonal Entries**: (1) $a_{ii} > 0$; (2) $2|a_{ij}| < a_{ii} + a_{ij}$ ($i \neq j$); (3) $a_{ij}$ satisfies $|a_{ij}| = \max\limits _{k,l} |a_{kl}|$ must lie on diagonal, and is positive.

<div class=note>

(1) $e_i^TAe_i = a_{ii} > 0$; (2) $(e_i+e_j)^TA(e_i+e_j) = a_{ii}+a_{jj} + 2a_{ij} > 0$; (3) $|a_{ij}| < \max\{a_{ii},a_{ij}\}$.

</div>

---

## Determine if a Quadratic Form is Positive Definite

- Determine when $f = x_1^2 + x_2^2 + 5x_3^2 + 2tx_1x_2 - 2x_1x_3 + 4x_2x_3$ is positive definite.

<div class=note>

$t \in (- \frac{4}{5}, 0)$.

</div>

- Determine if $f = \sum\limits_{i = 1}^n x_i^2 + \sum\limits_{1 \leq i < j \leq n}x_ix_j$ is positive definite.

<div class=note>

(1) The matrix $A = \frac{1}{2}(J + I)$ where $J$ is the all-one matrix, $I$ is the identity matrix.
(2) Eigenvalues of $J$ are $\lambda_1=n$ with multiplicity $1$, $\lambda_2=0$ with multiplicity $n-1$. (By calculate the determinant $|J - \lambda I|$)
(3) Eigenvalues of $A$ is $\lambda_1 = \frac{1}{2}(n+1)$ with multiplicity $1$, $\lambda_2=\frac{1}{2}$ with multiplicity $n-1$.
(4) All eigenvalues are positive, then $A$ is positive definite.

</div>

---

## Matrix Decomposition of Positive Definite Matrices

- **Identity Decomposition**: $A$ positive definite, then $A = P^TP$. (Congruent to identity).
- **Squared Decompositition**: $A$ is positive definite, then $A = C^2$ where $C$ is symmetric.

<div class=note>

There exists an orthogonal matrix $P$ such that $A = P\Lambda P^T$. Take $C = P \sqrt{\Lambda} P^T$.

</div>

- **Lemma (QR)**: Any inversible matrix $A = QR$, $Q$ orthogonal $R$ upper-triangular.

<div class=note>

Appy Schmidt orthogonalization to find an standard orthogonal basis and form $Q$.

</div>

- **Upper-Triangular Decomposition**: $A$ positive definite, $A = R^TR$, $R$ is upper-triangular.

<div class=note>

$A = P^TP$ and $P = QR$. Then $A = R^TR$.

</div>

---

## Simultaneous Diagonalization

- **Both Positive Definite**: $A, B$ positive definite, $\exists P$, $P^TAP, P^TBP$ are diagonal.

<div class=note>

(1) $A+B$ positive definite, $Q^T(A+B)Q = I$. Then $Q^TAQ + Q^TBQ = I$.
(2) There exists an orthogonal matrix $R$ such that $R^TQ^TAQR = \Lambda$, where $\Lambda$ is diagonal.
(3) $R^TQ^TBQR = I - R^TQ^TAQR = I - \Lambda$ is diagonal. Take $P = QR$.

</div>

- **One Positive Definite**: $A$ positive definite, $B$ real symmetric, $P^TAP$, $P^TBP$ are diagonal.

<div class=note>

(1) Take $\lambda > \max\limits_i |\lambda_i(B)|$, $C = \lambda I + B$ is positive definite. ($Q^TBQ = \Lambda$, $Q^TCQ = \lambda I + \Lambda$)
(2) There exists $P$ such that $P^TAP$ and $P^TCP$ are diagonal, then $P^TBP$ is also diagonal.

</div>



