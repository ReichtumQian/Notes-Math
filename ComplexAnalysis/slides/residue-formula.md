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

- Laurent Expansion
- Concept of Residue
- Residue Formula and Its Applications
- Argument Principle and Applications

---

# Laurent Expansion

---

## Laurent Expansion, Singularities and Zeros

- **Laurent Expansion**: $f$ is holomorphic, then it can be uniquely represented as
$$ f(z) = \sum_{n=-\infty}^{+\infty} a_n(z-z_n)^n $$

<div class=note>

$$ \sum_{n=0}^{\infty} a_n(z-z_0)^n \text{ is analytic part} \quad
\sum_{n=-\infty}^{-1}a_n(z-z_0)^n \text{ is principal part}.$$

</div>

- **Removable Singularity**: $f(z) = \sum_{n=0}^{+\infty} a_n(z-z_0)^n$.
- **Pole Singularity of Order $m$**: $f(z) = \sum_{n=-m}^{+\infty} a_n(z-z_0)^n$.
- **Essential Singularity**: $f(z) = \sum_{n=-\infty}^{+\infty}a_n(z-z_0)^n$.
- **Zeros of Order $m$**: $f(z) = \sum_{n=m}^{+\infty} a_n(z-z_0)^n$.

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

---

# Argument Principle and Applications

---

## Argument Principle and Its Generalizations

- **Meromorphic**: $f$ is holomorphic except poles at $\{z_0,z_1,\cdots\}$, these poles have no limit points.
- **Argument Principle**: $f$ meromorphic, $C$ closed contour. $f$ has no poles and never vanishes on $C$. $N_z$ the number of zeros of $f$ inside $C$, $N_p$ the poles (counted with multiplicities).
$$ \frac{1}{2\pi i} \int_C \frac{f^{\prime}(z)}{f(z)}\mathrm{d} z = N_z - N_p $$
- **Rouche's Theorem**: $f, g$ holomorphic, $C$ closed contour, $|f| > |g|$ for all $z \in C$. Then $N_z(f) = N_z(f+g)$ inside $C$.
- **Open Mapping Theorem**: $f$ holomorphic and non-constant, then $f$ is open.

---

## Applications of Argument Principle

---

## Applications of Rouche's Theorem

- Apply Rouche's theorem to prove fundamental theorem for algebra.

<div class=note>

Consider $f(z) = z^n$ and $g(z) = a_{n-1}z^{n-1} + \cdots + a_0$, $P(z) = f(z) + g(z)$. Take sufficiently large $R$ such that on $|z| = R$
$$ |f(z)| = R^n > (|a_{n-1}| + \cdots + |a_0|)R^{n-1} \geq |g(z)|.$$
Then $N_z(P) = N_z(f)$, and $z^n = 0$ has $n$ roots in $C$ ($z=0$ of multiplicity $n$), $P$ has $n$ roots.

</div>



