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

# Inner Product Spaces

Speaker: Yixiao Qian

---

## Concept of Euclidean Space

- **Definition**: Linearity, Symmetry, Positive-Definiteness.
- **Matric Matrix**: $G_{ij} = \langle \epsilon_i, \epsilon_j \rangle$.
- **Representation of Inner Product**: $\langle \alpha, \beta \rangle = X^T G Y$.
- **Orthogonal**: $\langle \alpha, \beta \rangle = 0$.
- **Orthogonal Implies Linear Independence**: If $\alpha_1,\cdots,\alpha_n$ are orthogonal, then they are linearly independent.
- **Standard Orthogonal Basis**: Pairwise-orthogonal and unit basis.
- **Schmidt Orthogonalization**: $\epsilon_1 = \alpha_1$, $\epsilon_s = \alpha_s - \sum_{i=1}^{s-1} \frac{\langle \alpha_s, \epsilon_i\rangle}{\langle \epsilon_i, \epsilon_i \rangle} \epsilon_i$.
- **QR Decomposition**: $Q = [\epsilon_1,\cdots,\epsilon_n]$, then $A = QR$.








