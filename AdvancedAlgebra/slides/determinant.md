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

# Determinant

Speaker: Yixiao Qian

---

## Key Points of Determinant

- **Definition**: $|A| := \sum\limits_{\sigma \in S_n} \mathrm{sgn}(\sigma) \prod\limits_{i=1}^n a_{i,\sigma(i)}$, where $S_n$ is the set of permutations. The sign of $\sigma$ is $+1$ if it is even, $-1$ if odd.
- Calculate $|A|$ where $A$ is the matrix with anti-diagonal entries $a_1,a_2,\cdots,a_n$.

<div class=note>

$\operatorname{inv}(\sigma) = (n-1)+(n-2)+\cdots + 1 = \frac{n(n-1)}{2}$. Therefore, $|A| = (-1)^{\frac{n(n-1)}{2}}a_1a_2\cdots a_n$.

</div>

- **Elementary Transformation**: Interchange (change sign), Multiplication, Addition.
- **Minor**: $M_{ij}$ is determinant obtained by deleting $i$-th row and $j$-th column.
- **Cofactor**: $A_{ij} := (-1)^{i+j}M_{ij}$.
- **Expansion**: (1) $|A| = \sum_{i=1}^n a_{ij}A_{ij}$; (2) $0 = \sum_{k=1}^n a_{ik}A_{jk}$ for $i \neq j$.

<div class=note>

Why $\sum_{k=1}^n a_{ik}A_{jk} = 0$: Define a new matrix $B$ by replacing the $j$-th row of $A$ with $i$-th row.

</div>


