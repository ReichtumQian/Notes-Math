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

## Table of Contents

<br>

- Bilinear Functions
- Concept and Canonical Form of Quadratic Forms
- Positive Definite Quadratic Forms

---

# Concept and Canonical Form of Quadratic Forms

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


