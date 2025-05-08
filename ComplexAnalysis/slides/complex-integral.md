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

</div>

- Calculate $\displaystyle \int_0^{2\pi a}2z^2 + 8z + 1 \mathrm{d} z$, where $x = a(\theta - \sin \theta)$ and $y = a(1-\cos \theta)$.


<div class=note>

Apply Newton-Leibniz formula, the integral is unrelated to the curve.
</div>

---

## Inequalities in Complex Integrals

<div class=trick>

If $|f(z)| \leq R_1$ and $|\mathrm{d} z| \leq R_2$ on $C$ parameterized by $z(\theta): [a, b] \rightarrow \mathbb{C}$, then
$$ \left| \int_C f(z) \mathrm{d} z \right| \leq \int_a^b R_1 R_2 \mathrm{d}\theta = R_1R_2(b-a). $$

</div>

- ${\displaystyle \left| \int_{\Gamma}(x^2+iy^2)\mathrm{d} z \right| \leq 2}$, where $\Gamma: -i \rightarrow i$.
- ${\displaystyle \left| \int_C e^{iz}\mathrm{d} z \right| \leq \pi}$, where $C$ is the upper circle from $R$ to $-R$.

---

# Cauchy's Theorem and Its Generalizations

---

## Cauchy's Theorem and Its Generalizations

- **Cauchy's Theorem**: $f$ is holomorphic in simply connected region $D$, $\gamma$ is a closed curve.
$$ \int_{\gamma} f \mathrm{d} z = 0. $$
- **Cauchy's Integral Formula**: $f$ is holomorphic in simply connected region $D$, $C$ the boundary with positive orintation.
$$ f(z) = \frac{1}{2 \pi i} \int_C \frac{f(\zeta)}{\zeta - z}\mathrm{d} \zeta, \quad z \in D. $$
- **Cauchy's Derivative Formula**:
$$ f^{(n)}(z) = \frac{n!}{2 \pi i} \int_C \frac{f(\zeta)}{(\zeta - z)^{n+1}}\mathrm{d} \zeta, \quad z \in D. $$
- **Liouville's Theorem**: If $f$ is entire and bounded, then it is constant.





