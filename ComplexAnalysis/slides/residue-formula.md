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

# Residue Formula

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Concept of Residue
- Residue Formula
- Applications of Residue Formula

---

# Concept of Residue

---

## Definition and Representation of Residue

- **Definition**: Given $f(z) = \sum\limits_{n=-\infty}^{+\infty}a_n(z-z_0)^n$, $a_{-1}$ for $z_0 \neq \infty$, $-a_{-1}$ for $z_0 = \infty$.
- **Representation at $z_0 \neq \infty$**: If $z_0$ is $m$-order pole, define $\varphi(z) = (z-z_0)^mf(z)$, then
$$ \operatorname{res}_{z_0} f = \lim \limits _{z \rightarrow z_0} \frac{\varphi^{(m-1)}(z)}{(m-1)!}.$$
- **Representation at $z_0 = \infty$**: If $z_1,\cdots,z_n$ are finite singularities
$$ \operatorname{res}_{z_0} f = - \sum\limits_{k=1}^n \operatorname{res}_{z_k} f.$$

---

## Calculate the Residue

- $f(z) = \frac{e^z - 1}{z^5}$ at $z = 0$.

<div class=note>

</div>

- $f(z) = \frac{1}{\sin \frac{1}{z}}$ at its poles.

<div class=note>

</div>

- $f(z) = \frac{1}{e^{z-1}}$ at $z = 1$ and $z = \infty$.

<div class=note>

$z = 1$: $1$.
$z = \infty$: $-1$.
</div>

---

# The Residue Formula

---

## The Residue Formula

<br>

- **Residue Formula**: Only one pole, then
$$ \int_C f(z)\mathrm{d} z = 2 \pi i \operatorname{res}_{z_0} f$$
- **Cauchy Residue Formula**: Poles $z_1,\cdots,z_n$, then
$$ \int_C f(z) \mathrm{d} z = 2 \pi i \sum\limits_{k = 1}^n \operatorname{res}_{z_k} f.$$

---

## Calculate Integrals using Residue Formula

- ${\displaystyle \frac{1}{2\pi i}\int_C \frac{e^z}{z(1-z)^3}\mathrm{d} z}$ where $C$ is a closed contour does not pass through $z = 0$ and $z = 1$.
- ${\displaystyle \int_{|z| = 1} \frac{\tan \pi z}{z^3}\mathrm{d} z}$.
- ${\displaystyle \int_{|z| = \frac{5}{2}} \frac{1}{(z-3)(z^5 - 1)}\mathrm{d} z}$.

---

# Applications of the Residue Formula

---

## Integrating Trigonometric Rational Functions

<div class=trick>

$$ \int_0^{2\pi} R(\cos \theta, \sin \theta)\mathrm{d} \theta = \int_{|z| = 1} R \left( \frac{z + z^{-1}}{2}, \frac{z - z^{-1}}{2} \right) \cdot \frac{1}{iz}\mathrm{d} z. $$
</div>

- ${\displaystyle \int_0^{2\pi} \frac{1}{a + \cos \theta}\mathrm{d} \theta}$, where $a > 1$.

<div class=note>

</div>

- ${\displaystyle \int_0^{2\pi} \sin^{2n}x \mathrm{d} x}$ where $n \in \mathbb{N}$.

---

## Integrating Rational Functions

<div class=trick>

Let $f(z) = \frac{P(z)}{Q(z)}$, where $(P(z), Q(z)) = 1$, $\operatorname{deg}(Q) \geq \operatorname{deg}(P) + 2$, $Q$ has no roots on $\mathbb{R}$, then
$$ \int_{-\infty}^{+\infty} f(x)\mathrm{d} x = 2 \pi i \sum \operatorname{res}_{z=a_k} f(z), $$
where $a_k$ are residues of $f(z)$ satisfying $\operatorname{Im}(a_k) > 0$.
</div>

- ${\displaystyle \int_0^{+\infty} \frac{x^2}{(x^2 + 1)(x^2 + 4)}\mathrm{d}x}$

- ${\displaystyle \int_{-\infty}^{+\infty} \frac{x^2}{(x^2 + a^2)^2}\mathrm{d} x}$



