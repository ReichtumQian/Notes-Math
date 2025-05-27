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

# Linear Space and Linear Transformations

Speaker: Yixiao Qian

---

# Concept of Linear Space

---

## Concept of Linear Space

- **Definition of Linear Space**: $8$ axioms.
- **Linear Dependence and Independence**: $k_1\alpha_1 + \cdots + k_n\alpha_n = 0$.
- **Finding Maximal Linearly Independent Subsets**: Form a matrix + Row operations.
- **Bases**: $\epsilon_1,\cdots,\epsilon_n$ can linearly represent all vectors in $V$.
- **Coordinate**: $\alpha = (\epsilon_1,\cdots,\epsilon_n)X$.
- **Transition Matrix**: $(\epsilon_1,\cdots,\epsilon_n) = (\eta_1,\cdots,\eta_n)T$.
- **Coordinate Transformation**: $\alpha = (\epsilon_1,\cdots,\epsilon_n)X = (\eta_1,\cdots,\eta_n)TX$, $Y = TX$.

---

# Operations on Linear Spaces

---

## Sum and Intersection of Linear Spaces

- **Subspace**: Subsets which are closed under addition and scalar multiplication.
- **Sum of Subspaces**: $V_1 + V_2 = \{\alpha = \alpha_1 + \alpha_2: \alpha_1 \in V_1, \alpha_2 \in V_2\}$.

<div class=note>

If $V_1 = \operatorname{span}(\alpha_1,\cdots,\alpha_n)$, $V_2 = \operatorname{span}(\beta_1,\cdots,\beta_m)$, then $V_1 + V_2 = \operatorname{span}(\alpha_1,\cdots,\alpha_n, \beta_1,\cdots,\beta_m)$

</div>

- **Intersection of Subspaces**: $V_1 \cap V_2 = \{\alpha: \alpha \in V_1, \alpha \in V_2\}$.

<div class=note>

$\alpha = x_1\alpha_1 + \cdots + x_n\alpha_n = y_1\beta_1 + \cdots + y_m\beta_m$. The coordinates follow linear equations
$$ [\alpha_1, \cdots, \alpha_n, \beta_1,\cdots, \beta_m]
\begin{bmatrix}
  X\\
  Y
\end{bmatrix} = 0.
$$

</div>

- **Sum and Intersection are Linear Spaces**: If $V_1, V_2$ are linear spaces, then so is their sum and intersection.

---

## Practice on Sum and Intersection

- If $V_1 = \operatorname{span}(\alpha_1, \alpha_2, \alpha_3)$, and $V_2 = \operatorname{span}(\beta_1, \beta_2)$. Find $V_1 + V_2$ and $V_1 \cap V_2$:
$$
\alpha_1=\begin{pmatrix}1\\2\\1\\0\end{pmatrix},\alpha_2=\begin{pmatrix}-1\\1\\1\\1\end{pmatrix},\alpha_3=\begin{pmatrix}0\\3\\2\\1\end{pmatrix},\beta_1=\begin{pmatrix}2\\-1\\0\\1\end{pmatrix},\beta_2=\begin{pmatrix}1\\-1\\3\\7\end{pmatrix}.
$$

<div class=note>

(1) $V_1 \cup V_2 = \operatorname{span}(\alpha_1,\alpha_2,\alpha_3,\beta_1,\beta_2)$.
(2) $\gamma \in V_1 \cap V_2$ satisfies $\gamma = k_1\alpha_1 + k_2\alpha_2 + k_3\alpha_3 = t_1\beta_1 + t_2\beta_2$. The coefficients follow the system of linear equations
$$ k_1\alpha_1 + k_2\alpha_2 + k_3\alpha_3 - t_1\beta_1 - t_2\beta_2 = \mathbf{0}. $$

</div>

---

## Difference between Sum and Union

- $V_1$ and $V_2$ are non-trivial subspaces of $V$, prove $\exists \alpha \in V$ such that $\alpha \not\in V_1$ and $\alpha \not\in V_2$.

<div class=note>

(1) Take $\alpha \not \in V_1$, if $\alpha \not \in V_2$, then conclusion holds.
(2) Otherwise take $\beta \not \in V_2$, if $\beta \not \in V_1$, then conclusion holds.
(3) Otherwise, $\alpha \not \in V_1$, $\alpha \in V_2$, $\beta \in V_1$, $\beta \not \in V_2$, so $\gamma = \alpha + \beta$ not in either $V_1$ or $V_2$.

</div>

- $V_1$ and $V_2$ are two subspaces of $V$, prove that $V_1+V_2 = V_1 \cup V_2$ iff $V_1 \subseteq V_2$ or $V_2 \subseteq V_1$.

<div class=note>

(1) For any $\alpha \in V_1 + V_2$, $\alpha = \alpha_1 + \alpha_2$ where $\alpha_1 \in V_1$ and $\alpha_2 \in V_2$.
(2) $\alpha \in V_1 \cup V_2$, so $\alpha \in V_1$ or $\alpha \in V_2$. That is $\alpha_2 = \alpha - \alpha_1 \in V_1$ or $\alpha_1 = \alpha - \alpha_2 \in V_2$.

</div>

---

## Dimension Theorem

- **Dimension Theorem**: $V_1$, $V_2$ are subspaces of $V$ ($\operatorname{dim}V < \infty$), then
$$ \operatorname{dim}V_1 + \operatorname{dim}V_2 = \operatorname{dim}(V_1 + V_2) + \operatorname{dim}(V_1 \cap V_2). $$

<div class=note>

</div>

---

## Direct Sum

- **Direct Sum**: If $V_1 \cap V_2 = \emptyset$, then $V_1 + V_2 = V_1 \oplus V_2$.
- **Essential Equivalent Condition**: $V_1 + V_2 = V_1 \oplus V_2$ iff $\epsilon_1,\cdots,\epsilon_s, \eta_1,\cdots,\eta_r$ are linearly independent.

<div class=note>

Take $\alpha \in V_1 \cap V_2$, $\alpha = k_1\epsilon_1 + \cdots + k_s\epsilon_2 = l_1\eta_1 + \cdots + l_r\eta_r$. $\alpha = 0$ iff $k_i=0,l_i=0$ for all $i$.

</div>

- **Other Equivalent Condition**: (1) $\alpha = \alpha_1 + \alpha_2$ is unique; (2) $\operatorname{dim} V = \operatorname{dim}V_1 + \operatorname{dim} V_2$.

---

# Linear Mapping and Linear Transformation

---

## Concept of Linear Mapping

<br>

- **Linear Mapping**: $\varphi(\alpha + \beta) = \varphi(\alpha) + \varphi(\beta)$, $\varphi(c \alpha) = c \varphi(\alpha)$.
- **Matrix of Linear Mapping**: $(\mathcal{A}(\epsilon_1), \cdots, \mathcal{A}(\epsilon_n)) = (\epsilon_1,\cdots,\epsilon_n)A$.
- **Coordinate After Transformation**: $\alpha = (\epsilon_1,\cdots,\epsilon_n)x$, then $\mathcal{A}\alpha = (\epsilon_1,\cdots,\epsilon_n)Ax$.
- **Kernel and Image**: $\operatorname{Ker}(\varphi) = \{\alpha: \varphi(\alpha) = 0\}$, $\operatorname{Im}(\varphi) = \{\varphi(\alpha)\}$.
- **Representation of Kernel and Image**: $\operatorname{Ker}(\mathcal{A})$ is the solution space of $Ax = 0$. $\operatorname{Im}(\mathcal{A})$ is the column space of $A$.

---

## Dimension Theorem for Kernel and Image

- $\varphi: U \rightarrow V$, then $\operatorname{dim} \operatorname{Ker}(\varphi) + \operatorname{dim} \operatorname{Im}(\varphi) = \operatorname{dim} U$.

<div class=note>

(1) Assume $\operatorname{Ker}(\varphi) = \operatorname{span}(\alpha_1,\cdots,\alpha_r)$ and $U = \operatorname{span}(\alpha_1,\cdots,\alpha_n)$. Then
$$
\operatorname{Im}(\varphi) = \operatorname{span}(\varphi(\alpha_1),\cdots,\varphi(\alpha_n))
= \operatorname{span}(\varphi(\alpha_{r+1}),\cdots,\varphi(\alpha_n)).
$$
(2) If $k_{r+1}\varphi(\alpha_{r+1}) + \cdots + k_n \varphi(\alpha_n) = 0$, then $\varphi(k_{r+1}\alpha_{r+1} + \cdots + k_n\alpha_n) = 0$. Therefore
$$ k_{r+1}\alpha_{r+1} + \cdots + k_n \alpha_n \in \operatorname{Ker}(\varphi) \Rightarrow k_{r+1} = \cdots = k_n = 0. $$

</div>

- $\mathcal{A}: V \rightarrow V$, $W$ is a subspace of $V$, then $\operatorname{dim} \mathcal{A}W + \operatorname{dim} (\operatorname{Ker}\mathcal{A} \cap W) = \operatorname{dim}W$.

<div class=note>

$\operatorname{Ker} \mathcal{A} \cap W = \operatorname{span}(\alpha_1,\cdots,\alpha_r)$, $W = \operatorname{span}(\alpha_1,\cdots,\alpha_n)$. Prove $\mathcal{A}W = \operatorname{span}(\mathcal{A}\alpha_{r+1},\cdots,\mathcal{A}\alpha_n)$ has dimension $n-r$.

</div>

---

## Application of Dimension Theorem

- $\sigma: V \rightarrow V$, $V$ is a finite-dimension linear space. $\sigma$ is injective iff $\sigma$ is surjective.

<div class=note>

(1) $\sigma$ is injective iff $\operatorname{Ker}(\sigma) = \{0\}$ (Otherwise $\sigma(\alpha) = \sigma(\alpha + \beta)$ for $\beta \in \operatorname{Ker}(\sigma)$).
(2) By dimension theorem, $\operatorname{Ker}(\sigma) = \{0\}$ iff $\operatorname{Im}(\sigma) = \operatorname{dim}(V)$, which means $\sigma$ is surjective.

</div>

---

## Kernel and Image of Idempotent Linear Transformation

<br>

- **Image of Idempotent Transformation**: For $\alpha \in \operatorname{Im}(\mathcal{A})$, $\mathcal{A}\alpha = \alpha$.

<div class=note>

$\exists \beta \in V$, $\mathcal{A}\beta = \alpha$, then $\mathcal{A} \alpha = \mathcal{A}^2 \beta = \mathcal{A}\beta = \alpha$.

</div>

- **Idempotent Space Decomposition**: $\mathcal{A}$ idempotent, then $V = \operatorname{Ker}(\mathcal{A}) \oplus \operatorname{Im}(\mathcal{A})$.

<div class=note>

(1) $\alpha = \alpha - \mathcal{A}\alpha + \mathcal{A}\alpha$, where $\alpha - \mathcal{A}\alpha \in \operatorname{Ker}(\mathcal{A})$ and $\mathcal{A}\alpha \in \operatorname{Im}(\mathcal{A})$.
(2) For $\alpha \in \operatorname{Im}(\mathcal{A}) \cap \operatorname{Ker}(\mathcal{A})$, so $\alpha = \mathcal{A}\alpha = 0$.

</div>


---

## Practice on Kernel and Image of Idempotent Linear Transformation

- $\mathcal{A},\mathcal{B}$ idempotent, $\operatorname{Im}(\mathcal{A}) = \operatorname{Im}(\mathcal{B})$ iff $\mathcal{A}\mathcal{B} = \mathcal{B}$ and $\mathcal{B}\mathcal{A} = \mathcal{A}$.

<div class=note>

(1) $\forall \alpha \in V$, $\exists \beta \in V$, $\mathcal{B}\alpha = \mathcal{A}\beta$. Then $\mathcal{A}(\mathcal{B}\alpha) = \mathcal{A} (\mathcal{A}\beta) = \mathcal{A} \beta = \mathcal{B} \alpha \Rightarrow \mathcal{A} \mathcal{B} = \mathcal{B}$.
(2) $\forall \gamma \in \operatorname{Im}(\mathcal{A})$, $\mathcal{B} \mathcal{A} \gamma = \mathcal{A} \gamma = \gamma \Rightarrow \mathcal{B} \gamma = \gamma$.

</div>

- $\mathcal{A}, \mathcal{B}$ idempotent, $\operatorname{Ker}(\mathcal{A}) = \operatorname{Ker}(\mathcal{B})$ iff $\mathcal{A}\mathcal{B} = \mathcal{A}$ and $\mathcal{B}\mathcal{A} = \mathcal{B}$.

<div class=note>

(1) $V = \operatorname{Im}(\mathcal{A}) \oplus \operatorname{Ker}(\mathcal{A})$, then $\alpha = \alpha_1 + \alpha_2$.
(2) $\mathcal{B}\alpha = \mathcal{B}\alpha_1$, $\mathcal{B}\mathcal{A}\alpha = \mathcal{B}\alpha_1$.

</div>

---

## Similarity


---

# Eigenvalues and Eigenvectors

---

## Key Points of Eigenvalues and Eigenvectors

- **Definition**: $\mathcal{A}\xi = \lambda \xi$.
- **Eigenspace**: $V_{\lambda} := \{\xi: \mathcal{A}\xi = \lambda \xi\}$, $V_{\lambda}$ is a subspace of $V$.
- **Characteristic Polynomial**: $f(\lambda) = |\lambda I - A|$.
- **Linear Independence of Eigenvectors**: Eigenvectors belonging to different eigenvalues are linearly independent.

<div class=note>

Prove by induction, assume that $\xi_1, \cdots, \xi_{k-1}$ are linearly independent.
(1) Suppose $c_1\xi_1 + \cdots + c_k\xi_k = 0$, applying $\mathcal{A}$ yields $c_1\lambda_1\xi_1 + \cdots + c_k\lambda_k \xi_k = 0$.
(2) Multiplying by $\lambda_k$ yields $c_1\lambda_k \xi_1 + \cdots + c_{k-1}\lambda_k \xi_{k-1} = 0$.
(3) Substract two equations, $c_1(\lambda_1 - \lambda_k)\xi_1 + \cdots + c_{k-1}(\lambda_{k-1} - \lambda_k)\xi_{k-1} = 0$. So $c_i = 0$.

</div>


---

## Similarity Diagonalization


---

## Practice on Eigenvalues and Eigenvectors

- Find (1) eigenvalues; (2) eigenvectors; (3) if $A$ is diagonalizable.

$$
\begin{bmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
0 & 0 & 3
\end{bmatrix}
$$

<div class=note>

(1) $\lambda_1 = 1$, $\lambda_2 = \lambda_3 = 3$.
(2) $\mathbf{v} = k(1, 0, 0)^T$ for $\lambda = 1$; $\mathbf{v} = k(1, 1, 0)^T$ for $\lambda = 3$.
(3) No. Because algebraic multiplicity does not equal to geometric multiplicity.

</div>


---

# Minimal Polynomial

---

## Key Points

- **Hamilton-Cayley Theorem**: $f(\lambda) = |\lambda I - A|$ is an annihilating polynomial of $A$.
- **Minimal Polynomial**: $m(\lambda)$ and $f(\lambda)$ has same roots (except the multiplicity).
- **Diagonalization**: $A$ is diagonalizable iff $m_A(\lambda)$ splits into linear factors.


---

## Applications of Hamilton-Cayley Theorem

- Prove that $A^{-1}$ and $A^{\ast}$ can be represented as polynomials of $A$.




