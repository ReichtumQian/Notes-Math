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

# Lebesgue Integrals

Speaker: Yixiao Qian

---

# Table of Contents

<br>

- Concept of Lebesgue Integral
- Properties of Lebesgue Integral

---

# Concept of Lebesgue Integral

---

## Definition of Lebesgue Integral

<br>

- **Characteristic Function**: $\chi_E(x) = 1$ for $x \in E$ and $\chi_E(x) = 0$ for $x \not \in E$.
- **Integral of Non-Negative Simple Function**: $\displaystyle \int_D f \mathrm{d} x = \sum\limits_{i = 1}^s a_i m(E_i)$.
- **Integral of Non-Negative Measurable Function**: $\displaystyle \int_D f \mathrm{d} x = \lim \limits _{n \rightarrow \infty} \int_D f_n\mathrm{d}x$.
- **Integral of Measurable Function**: ${\displaystyle \int_D f \mathrm{d} x = \int_D f_+ \mathrm{d} x - \int_D f_- \mathrm{d} x}$.
- **Almost-Everywhere Finite**: $f \in L(E)$ then $f$ is finite a.e.

---

## What Happens When the Integral is Zero

<div class=trick>

For any $\sigma \in \mathbb{R}$, we have $\displaystyle \int_E f \mathrm{d} x \geq \int_{\{f \geq \sigma\}}f\mathrm{d} x \geq \sigma m(\{f \geq \sigma\})$.
</div>

- $f$ is non-negative, ${\displaystyle \int_E f \mathrm{d} x = 0}$, then $f = 0$ a.e.

<div class=note>

Let $E_n = \{f \geq \frac{1}{n}\}$, and $\displaystyle \int_E f \mathrm{d} x \geq \int_{E_n} f \mathrm{d} x \geq \frac{1}{n}m(E_n)$. Then $m(\{f \neq 0\}) \leq \sum m(E_n) = 0$.
</div>

- $f_n$ are non-negative, ${\displaystyle \lim \limits _{n \rightarrow \infty} \int_E f_n \mathrm{d} x = 0}$, then $f_n \xrightarrow{m} 0$.

<div class=note>

Fix $n$, let $E_{\sigma} = \{f_n \geq \sigma\}$, ${\displaystyle \int_E f_n\mathrm{d} x \geq \int_{E_{\sigma}} f_n\mathrm{d} x \geq \sigma m(E_{\sigma})}$. Then $m(E_{\sigma}) \rightarrow 0$ when $n \rightarrow \infty$.
</div>

---

## What Happens When the Integral is Zero

<br>

- $f \in L(E)$, for any measurable $\varphi(x)$, ${\displaystyle \int_E f(x)\varphi(x) \mathrm{d} x = 0}$, then $f(x) = 0$ a.e.

<div class=note>

Let $E_n = \{f \geq \frac{1}{n}\}$ and $\varphi(x) = \chi_{E_n}(x)$. Then $\displaystyle \int_E f(x)\varphi(x)\mathrm{d} x = \int_{E_n}f \mathrm{d} x \geq \frac{1}{n}m(E_n)$.

</div>

- $f \in L([a,b])$, for any $k \in \mathbb{Z}^+$, ${\displaystyle \int_a^b x^k f(x) \mathrm{d} x = 0}$, then $f(x) = 0$ a.e.

---

## Approximation with respect to Integral

Let $f \in L([a, b])$, for any $\epsilon > 0$, there exists $g(x)$ such that

$$ \int_a^b |f(x) - g(x)| \mathrm{d} x < \epsilon. $$

- **Measurable and Bounded**

$$ g(x) =
\begin{cases}
  f(x) & |f(x)| \leq M;\\
  M \cdot \operatorname{sgn}(f(x)) & |f(x)| > M.
\end{cases}$$

$$ \int_a^b |f - g|\mathrm{d} x \leq \int_{\{|f| > M\}} (|f| + M) \mathrm{d} x < \epsilon. $$

---

## Approximation with respect to Integral

- **Continuous**: Since $g$ is bounded, by Lusin theorem, there exists $h(x) \in C(a, b)$ such that $m(g \neq h) < \epsilon$. 

$$ \int_a^b |f-h|\mathrm{d} x \leq \int_a^b|f-g|\mathrm{d} x+\int_a^b|g-h|\mathrm{d}x \leq 2\epsilon.$$

- **Polynomial**: There exists $P_n(x) \rightrightarrows h(x)$, then $\displaystyle \int_a^b P_n(x)\mathrm{d} x \rightarrow \int_a^b h(x)\mathrm{d} x$. There exists $N > 0$, such that $n > N$,

$$ \int_a^b |f - P_n| \mathrm{d} x \leq \int_a^b |f-h|\mathrm{d} x + \int_a^b |h-P_n|\mathrm{d} x \leq 3 \epsilon.$$

- **Step Function**: $P_n(x) \in R([a, b])$, then for any $\epsilon > 0$, there exists partition $T$ such that ${\displaystyle \left| \int_a^b P_n(x) - \varphi(x)\mathrm{d} x \right| < \epsilon}$, where $\varphi(x)$ takes $\sup P_n(x)$ in each sub-interval.

---

# Properties of Lebesgue Integral

---

## Key Properties of Lebesgue Integral

<br>

- **Absolute Continuity**
- **Levi's Monotone Convergence Theorem**
- **Fatou's Theorem**
- **LDCT**





