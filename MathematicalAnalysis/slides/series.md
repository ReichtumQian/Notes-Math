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

# Series

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Numerical Series
- Function Sequences and Series
- Power Series

---

# Numerical Series

---

## Concept of Numerical Series

<br>

- **Convergence**: $S_n = \sum_{k=1}^n u_k$ is parital-sum, $S_n$ converges.
- **Necessary Condition**: $\lim \limits _{n \rightarrow \infty} u_n = 0$. (Since $\lim \limits _{n \rightarrow \infty} u_n = \lim \limits _{n \rightarrow \infty} S_n - \lim \limits _{n \rightarrow \infty} S_{n-1} = 0$)
- **Cauchy Criterion**: $\forall \epsilon > 0, \exists N > 0, N < m < m+p$, $|u_{m+1} + \cdots + u_{m+p}| < \epsilon$.

---

## Positive-Term Series

- **Integral Test**: $f$ non-negative and decreasing, then $\displaystyle \sum_{n=1}^{\infty} f(n) \sim \int_1^{+\infty}f(x) \mathrm{d} x$.

<div class=note>

$\sum_{n=1}^{\infty} \frac{1}{n^p}$ converges when $p > 1$, diverges when $p \leq 1$.

</div>

- **Comparison Test**: If $u_n \sim v_n$ when $n \rightarrow \infty$, then $\sum_{n=1}^{\infty} u_n \sim \sum_{n=1}^{\infty}v_n$.
- **Ratio Test**: $\lim \limits _{n \rightarrow \infty} \frac{u_{n+1}}{u_n} = q$. $q<1$ then $\sum u_n$ converges, $q > 1$ then diverges.
- **Root Test**: $\lim \limits _{n \rightarrow \infty} \sqrt[n]{u_n} = q$. $q <１$ then $\sum u_n$ converges, $q > 1$ then diverges.

---

## Arbitrary-Term Series

---

# Function Sequences and Series

---

## Uniform Convergence of Function Sequence

- **Uniform Convergence**: 


---

# Power Series

---



