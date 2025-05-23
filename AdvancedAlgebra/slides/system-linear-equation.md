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

# Systems of Linear Equations

Speaker: Yixiao Qian

---

# Least-Square Problems

---

## Concept and Solution of Least-Squared Problems

- **Least-Squared Problem**
- **Normal Equation**: $A^TAx = A^Tb$ where $A \in \mathbb{R}^{n\times m}$.
- **Rank of $A^TA$**: $r(A) = r(A^TA)$.

<div class=note>

If $Ax = 0$ then $A^TAx = 0$; If $A^TAx = 0$, then $x^TA^TAx = 0$ and $Ax = 0$. So $r(A) = r(A^TA)$.

</div>

- **Existence of Solution of Normal Equation**: The solution of $A^TAx = A^Tb$ exists.

<div class=note>

(1) $r(A^TA|A^Tb) = r(A^T[A|b]) \leq r(A^T) = r(A^TA)$. (2) $r(A^TA|A^Tb) \geq r(A^TA)$.

</div>












