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

## Convergence Behavior of Power Series

- **Abel's Theorem**: (1) $\sum a_nx_0^n$ converges, for $|x| < |x_0|$, $\sum a_nx^n$ converges absolutely. (2) $\sum a_nx_0^n$ diverges, for $|x| > |x_0|$, $\sum a_nx^n$ diverges.
- **Radius of Convergence**: $|x| < R$, $\sum a_nx^n$ converges absolutely; $|x| > R$, $\sum a_nx^n$ diverges.
- **Cauchy-Hadamard Test**: $\frac{1}{R} = \lim \limits _{n \rightarrow \infty} \sqrt[n]{|a_n|}$.
- **Ratio Test**: $\frac{1}{R} = \lim \limits _{n \rightarrow \infty} \frac{|a_{n+1}|}{|a_n|}$.
- Find the Convergence Region: (1) $\sin x$ and $\cos x$, (2) $e^x$, (3) $\ln (1+x)$, (4) $\frac{1}{1-x}$.

<div class=note>

(1) $\sin x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!}$, $\frac{1}{R} = \sqrt[n]{\frac{1}{(2n+1)!}} \rightarrow 0$, then $R = \infty$. So is $\cos x$.
(2) $e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}$, $\frac{1}{R} = \sqrt[n]{\frac{1}{n!}} \rightarrow 0$. Then $R = \infty$.
(3) $\ln x = \sum_{n=1}^{\infty} (-1)^{n-1} \frac{x^n}{n}$, $\frac{1}{R} = \sqrt[n]{\frac{1}{n}} \rightarrow 1$. Then $R = 1$. The convergence region is $(-1,1]$.
(4) $\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n$, $\frac{1}{R} = \sqrt[n]{1} = 1$. The convergence region is $(-1,1)$.

</div>

---

## Sum Function of Power Series




---

## Power Series Expansion

- **Expansion of Rational Functions**: $f(x) = \frac{x^2}{x^2 - 3x + 1}$

<div class=note>

(1) Decompose: $\frac{x^2}{x^2-3x+1} = 1 + \frac{4}{x-2} - \frac{1}{x-1}$ (Method of Undetermined Coefficients)
(2) $\frac{1}{x-2} = -\frac{1}{2} \cdot \frac{1}{1 - \frac{x}{2}} = - \frac{1}{2} \sum\limits_{n=0}^{\infty} \left( \frac{x}{2} \right)^n$ and $\frac{1}{x-1} = - \frac{1}{1-x} = - \sum\limits_{n = 0}^{\infty} x^n$.

</div>

- **Take Integration**: $f(x) = \frac{1}{(1+x)^2}$.

<div class=note>

Consider $\displaystyle F(x) = \int_0^x \frac{1}{(1+t)^2}\mathrm{d} t$. Then $F(x) = -\frac{1}{1+x} + 1 = 1 - \sum_{n=0}^{\infty} (-x)^n$. $f(x) = F^{\prime}(x)$.

</div>

- **Take Derivative**: (1) $f(x) = \arctan x$, (2) $f(x) = \arctan \frac{1-kx}{1+kx}$.

<div class=note>

(1) $f^{\prime}(x) = \frac{1}{1+x^2} = \sum_{n=0}^{\infty}(-1)^nx^{2n}$. Then $f = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1}$.

</div>



