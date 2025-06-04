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


---

## Quick Review of Jordan Form



---

## Quick Review of Quadratic Form

