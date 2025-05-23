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

# Matrix

Speaker: Yixiao Qian

---

# Matrix Rank

---

## Concept and Properties of Matrix Rank

- **Definition**: (1) Rank of row-vector group; (2) Order of largest non-zero minor.
- **Product with Invertible Matrices**: If $P, Q$ invertible, then $r(A) = r(PAQ)$.
- **Matrix Decomposition**: $A = P
\begin{bmatrix}
  I_r & O\\
  O & O
\end{bmatrix} Q$
- **Column-Full-Rank and Row-Full-Rank**: $
A = P
\begin{bmatrix}
  I_r \\ O
\end{bmatrix}
\begin{bmatrix}
  I_r & O
\end{bmatrix} Q
$
- **Invertible and Idempotent**: $
A = PQQ^{-1}
\begin{bmatrix}
  I_r & O\\
  O & O
\end{bmatrix} Q
$

---

## Rank Inequalities

- **Block Matrices**: $r
\begin{pmatrix}
  A & O \\ O & B
\end{pmatrix}
 = r(A) + r(B)$, $r
 \begin{pmatrix}
   A & O \\ C & B
 \end{pmatrix} \geq r(A) + r(B)
 $.
- **Product**: $r(AB) \leq \min\{r(A), r(B)\}$. (Hint: From vector perspective).
- **Summation**: $r(A + B) \leq r(A) + r(B)$. (Hint: From vector perspective).
- **Sylvester's Inequality**: $r(A) + r(B) \leq r(AB) + n$, where $A,B$ are $n$-order.
- **Frobenius inequality**: $r(ABC) \geq r(AB)+r(BC) - r(B)$, where $A,B,C$ are $n$-order.

<div class=note>

$$
\begin{bmatrix}ABC&\\&B\end{bmatrix}\to\begin{bmatrix}ABC&O\\BC&B\end{bmatrix}\to\begin{bmatrix}O&-AB\\BC&B\end{bmatrix}.
$$

</div>

---

## Rank of Polynomial Matrices

- **Polynomial Matrices**: $f(x)=f_1(x)f_2(x)$, $(f_1(x),f_2(x)) = 1$, then $f(A) = O$ iff
$$ r(f_1(A)) + r(f_2(A)) = n. $$

<div class=note>

$$
\begin{align}
  \left[
    \begin{array}{cc}
      f_1(A)&\\
      &f_2(A)
    \end{array}
  \right] &\rightarrow \left[
    \begin{array}{cc}
      f_1(A)&f_1(A)u(A) + v(A)f_2(A)\\
      O&f_2(A)
    \end{array}
  \right] = \left[
    \begin{array}{cc}
      f_1(A)&I\\
      O&f_2(A)
    \end{array}
  \right]\\
  &\rightarrow \left[
    \begin{array}{cc}
      O&I\\
      -f_2(A)f_1(A)& f_2(A)
    \end{array}
  \right] \rightarrow \left[
    \begin{array}{cc}
      O&I\\
      -f(A)&O
    \end{array}
  \right].
\end{align}
$$


</div>

- Prove that $r(A-I) + r(A) = n$ iff $A$ is idempotent.
- Prove that $r(A-I) + r(A+I) = n$ iff $A^2 = I$.

---

# Inverse and Adjugate Matrices

---

# Several Special Matrices

---

## Real Symmetric Matrix

- **Definition**: $a_{ij} \in \mathbb{R}$ and $A^T = A$.
- **Eigenvalues and Eigenvectors**: (1) $\lambda_i \in \mathbb{R}$; (2) $\xi_i$ belonging to different $\lambda_i$ are orthogonal.
- **Orthogonal Similarity**: 

---

## Nilpotent Matrix


---

## Idempotent Matrix




