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

## Table of Contents

- Concept of Linear Space
- Operations on Linear Spaces

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

## Linear Mapping and Linear Transformation

---

# Minimal Polynomial

---

## Key Points

- **Hamilton-Cayley Theorem**: $f(\lambda) = |\lambda I - A|$ is an annihilating polynomial of $A$.


---

## Applications of Hamilton-Cayley Theorem

- Prove that $A^{-1}$ and $A^{\ast}$ can be represented as polynomials of $A$.




