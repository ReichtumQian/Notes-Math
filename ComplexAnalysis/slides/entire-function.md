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

# Entire Function

Speaker: Yixiao Qian

---

## Table of Contents

---

# Liouville's Theorem and Its Applications

---

## Liouville's Theorem

- **Liouville's Theorem**: If $f$ is entire and bounded, then it is constant.

<div class=note>

Cauchy's inequality implies $|f^{\prime}(z_0)| \leq \frac{B}{R}$ for any $z_0$ and $R$, where $B$ is a bound. Let $R \rightarrow \infty$ gives the result.

</div>

- **Fundamental Theorem for Algebra**: $P(z) = a_nz^n + \cdots + a_0$ ($n \geq 1$) has $n$ roots in $\mathbb{C}$, and
$$ P(z) = a_n(z-z_1)(z-z_2)\cdots (z-z_n). $$

<div class=note>

(1) If $P(z)$ has no roots, then $\frac{1}{P(z)}$ is entire and bounded. By Liouville's theorem, $P(z)$ is constant, which contradicts the condition.
(2) Then $P(z)$ must have a root $z_1$, and $P(z) = (z-z_1)Q(z)$. By induction, we can get the conclusion.
</div>

---

## Generalization of Liouville's Theorem

- **Bijective Entire Functions**: If $f$ is entire and bijective, then $f(z) = az + b$ ($a \neq 0$).

<div class=note>

(1) If $f = a_nz^n + a_{n-1}z^{n-1} + \cdots + a_0$, then $f^{\prime}(z)$ is an $n-1$-order polynomial. It has at least one zero $z_0$ in $\mathbb{C}$. $f^{\prime}(z_0) = 0$ contradicts the injectivity (see univalent function).
(2) If $f$ is not a polynomial, 

</div>

---

## Generalization of Liouville's Theorem

- **Holomorphic at $z=\infty$**: Let $w = \frac{1}{z}$, $f(\frac{1}{w})$ is holomorphic at $w = 0$.
- **Generalized Liouville's Theorem**: If $f$ is holomorphic on $\mathbb{C}_{\infty} := \mathbb{C} \cup \{\infty\}$, then $f(z)$ is constant.

<div class=note>

Since $f(\frac{1}{w})$ is holomorphic at $w = 0$, then $f(\frac{1}{w}) = a_0 + a_1w + a_2w^2 + \cdots$, substitue $w = \frac{1}{z}$
$$ f(z) = a_0 + \frac{a_1}{z} + \frac{a_2}{z} + \cdots \Rightarrow \lim \limits _{z \rightarrow \infty}f(z) = a_0. $$
When $|z| < R$, $f$ is bounded, and when $|z| \geq R$, $f \rightarrow a_0$ is also bounded. So $f$ is globally bounded, then Liouville's theorem gives the desired result.

</div>

---

## Applications of Liouville's Theorem

- If $f(z)$ has a unique pole at $z=1$ on $\mathbb{C}_{\infty}$, with principal part $\frac{1}{(z-1)^2}$, $f(0) = 1$. Find the expression of $f(z)$.

<div class=note>

$f(z) = \frac{1}{(z-1)^2} + g(z)$, where $g(z)$ has no pole on $\mathbb{C}_{\infty}$ ($z = \infty$ is not a pole). By generalized Liouville's theorem, $g(z)$ is constant. Then $f(z) = \frac{1}{(z-1)^2} + C$ satisfies $f(0) = 1$. So $C = 0$.

</div>