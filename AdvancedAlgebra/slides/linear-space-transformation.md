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

---

## Dimension Theorem

- **Dimension Theorem**: $V_1$, $V_2$ are subspaces of $V$ ($\operatorname{dim}V < \infty$), then
$$ \operatorname{dim}V_1 + \operatorname{dim}V_2 = \operatorname{dim}(V_1 + V_2) + \operatorname{dim}(V_1 \cap V_2). $$

---

## Direct Sum

---

# Minimal Polynomial

---

## Key Points

- **Hamilton-Cayley Theorem**: $f(\lambda) = |\lambda I - A|$ is an annihilating polynomial of $A$.


---

## Applications of Hamilton-Cayley Theorem

- Prove that $A^{-1}$ and $A^{\ast}$ can be represented as polynomials of $A$.




