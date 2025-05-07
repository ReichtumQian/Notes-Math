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
- Integrating Trigonometric Rational Functions
- Integrating Rational Functions

---

# Concept of Residue

---

## Definition and Representation of Residue

<br>

- **Definition**: $f(z) = \sum\limits_{n=-\infty}^{+\infty}a_n(z-z_0)^n$, $a_{-1}$ for $z_0 \neq \infty$, $-a_{-1}$ for $z_0 = \infty$.
- **Representation at $z_0 \neq \infty$**: If $z_0$ is $m$-order pole, define $\varphi(z) = (z-z_0)^mf(z)$, then
$$ \operatorname{res}_{z_0} f = \lim \limits _{z \rightarrow z_0} \frac{\varphi^{(m-1)}(z)}{(m-1)!}.$$
- **Representation at $z_0 = \infty$**: If $z_1,\cdots,z_n$ are finite singularities
$$ \operatorname{res}_{z_0} f = - \sum\limits_{k=1}^n \operatorname{res}_{z_k} f.$$


---

# The Residue Formula

---

## The Residue Formulas

<br>

- **Residue Formula**: Only one pole, then ${\displaystyle \int_C f(z)\mathrm{d} z = 2 \pi i \operatorname{res}_{z_0} f}$.
- **Cauchy Residue Formula**: Poles $z_1,\cdots,z_n$, then ${\displaystyle \int_C f(z) \mathrm{d} z} = 2 \pi i \sum\limits_{k = 1}^n \operatorname{res}_{z_k} f$.

---


