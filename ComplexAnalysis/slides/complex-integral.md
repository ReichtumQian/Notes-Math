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

# Complex Integrals and Cauchy's Theorem

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Complex Integrals
- Cauchy's Theorem and Its Generalizations

---

# Complex Integrals

---

## Complex Integrals

- **Integral of Parametrized Curve**: $\gamma: [a, b] \rightarrow \mathbb{C}$, then ${\displaystyle \int_{\gamma} f(z)\mathrm{d} z = \int_a^b f(z(t))z^{\prime}(t)\mathrm{d} t}$.
- **Newton-Leibniz Formula**: ${\displaystyle \int_{\gamma}f(z)\mathrm{d}z = F(w_2) - F(w_1)}$, $F$ is primitive of $f$, $\gamma$ begins at $w_1$ and ends at $w_2$.
- Calculate ${\displaystyle \int_C |z| \mathrm{d} z}$ where $C: 0 \rightarrow 1 + i$.

<div class=note>

$C$ is $z = t + it$ where $t \in [0, 1]$, $\mathrm{d} z = (1+i)\mathrm{d}t$. ${\displaystyle \int_C |z| \mathrm{d} z = \int_0^1 \sqrt{2}t (1+i)\mathrm{d} t = \frac{\sqrt{2}}{2}(1 + i)}$.

</div>

- Calculate $\displaystyle \int_0^{2\pi a}2z^2 + 8z + 1 \mathrm{d} z$, where $x = a(\theta - \sin \theta)$ and $y = a(1-\cos \theta)$.


<div class=note>

$$ I = \frac{2}{3} z^3 + 4z^2 + z \bigg|^{2\pi a}_0 = \frac{16}{3} \pi^3 a^3 + 16 \pi^2 a^2 + 2 \pi a. $$
</div>

---

## Inequalities in Complex Integrals

<div class=trick>

If $|f(z)| \leq R_1$ and $|\mathrm{d} z| \leq R_2$ on $C$ parameterized by $z(\theta): [a, b] \rightarrow \mathbb{C}$, then
$$ \left| \int_C f(z) \mathrm{d} z \right| \leq \int_a^b R_1 R_2 \mathrm{d}\theta = R_1R_2(b-a). $$

</div>

- ${\displaystyle \left| \int_{\Gamma}(x^2+iy^2)\mathrm{d} z \right| \leq 2}$, where $\Gamma: -i \rightarrow i$.

<div class=note>

$\Gamma: z = 0 + it$ then $|x^2 + iy^2| = |it|^2 \leq 1$ and $|\mathrm{d}z| = |t| \leq 1$. ${\displaystyle \left| \int_{\Gamma}(x^2+iy^2)\mathrm{d} z \right| \leq \int_0^2 1 \mathrm{d} t = 2}$.

</div>

- ${\displaystyle \left| \int_C e^{iz}\mathrm{d} z \right| \leq \pi}$, where $C$ is the upper circle from $R$ to $-R$.

<div class=note>

$|e^{iz}| = |e^{- iR \cos \theta - R \sin \theta}| = e^{-R \sin \theta}$, $|\mathrm{d}z| = |Rie^{i\theta}\mathrm{d}\theta| = R\mathrm{d}\theta$. Then ${\displaystyle \left| \int_C e^{iz}\mathrm{d}z \right| \leq \int_0^{2\pi} e^{-R\sin\theta} R \mathrm{d}\theta}$

</div>

---

# Cauchy's Theorem and Its Generalizations

---

## Cauchy's Theorem and Its Generalizations

- **Cauchy's Theorem**: $f$ holomorphic in simply connected $D$, $\gamma$ closed curve. $\displaystyle \int_{\gamma} f \mathrm{d} z = 0$
- **Cauchy's Integral Formula**: $\displaystyle f(z) = \frac{1}{2 \pi i} \int_C \frac{f(\zeta)}{\zeta - z}\mathrm{d} \zeta$ for $z \in D$, $C$ is positive boundary.
- **Cauchy's Derivative Formula**: ${\displaystyle f^{(n)}(z) = \frac{n!}{2 \pi i} \int_C \frac{f(\zeta)}{(\zeta - z)^{n+1}}\mathrm{d} \zeta}$ for $z \in D$.

<div class=trick>

Residue formula is generalized Cauchy's (integral) theorem, so we ignore their applications.

</div>

- **Cauchy's Inequality**: Denote $\|f\|_C := \sup_{z \in C}|f(z)|$ as the supremum of $|f|$ on boundary $C$
$$ |f^{(n)}(z_0)| \leq \frac{n! \|f\|_C}{R^n}.$$

<div class=note>

$$ \left| \int_C \frac{f(\zeta)}{(\zeta - z)^{n+1}}\mathrm{d} \zeta \right| \leq 2 \pi R \cdot \frac{\|f\|_C}{R^{n+1}} = \frac{2 \pi \|f\|_C}{R^n}.$$

</div>

---



