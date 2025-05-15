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

## Table of Contents

---

# Matrix Rank

---

## Concept and Properties of Matrix Rank

<br>

- **Definition**: (1) Rank of row-vector group; (2) Order of largest non-zero minor.
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

- **Product**: $r(AB) \leq \min\{r(A), r(B)\}$.
- **Summation**: $r(A + B) \leq r(A) + r(B)$.
- **Sylvester's Inequality**: $A, B$ are $n$-order, then $r(A) + r(B) \leq r(AB) + n$.
- **Polynomial Matrix**: $f(x)=f_1(x)f_2(x)$, $(f_1,f_2) = 1$, then $f(A) = O$ iff
$$ r(f_1(A)) + r(f_2(A)) = n. $$






