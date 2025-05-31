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

# Analysis Foundation

Speaker: Yixiao Qian

---

# Trigonometric Functions

---

## Commonly Used Formulas

- **Sum-Difference Formulas**: $\sin (\alpha \pm \beta)$, $\cos(\alpha \pm \beta)$, $\tan (\alpha \pm \beta)$.
- Prove that $\arctan A - \arctan B = \frac{A - B}{1 + AB}$. (Hint: Consider $\tan (\arctan A - \arctan B)$.)
- **Universal Formulas**: $\sin \alpha$, $\cos \alpha$, $\tan \alpha$.
- **Double Angle Formulas**: $\sin 2\alpha$, $\cos 2\alpha$, $\tan 2\alpha$.
- **Half Angle Formulas**: $\sin \frac{\alpha}{2}$, $\cos \frac{\alpha}{2}$, $\tan \frac{\alpha}{2}$.
- **Product-to-Sum and Sum-to-Product**: Derived from Sum-Difference Formulas.
- **Inequalities**: $\frac{2x}{\pi} < \sin x < x < \tan x$ for $x \in (0, \frac{\pi}{2})$.
- **Alternating Properties**: $(-1)^n \sin nx = \sin (x+\pi)n$, $(-1)^n \cos nx = \cos (x + \pi)n$.
- Calculate $I_1 = \sum_{k=1}^n \sin kx$ and $I_2 = \sum_{k=1}^n \cos kx$.

<div class=note>

$\sin \frac{x}{2} I_1 = \sum \sin kx \cdot \sin \frac{x}{2} = - \frac{1}{2} \sum [\cos(k+\frac{1}{2})x - \cos(k-\frac{1}{2})x]= \frac{1}{2} \left[ \cos \frac{x}{2} - \cos(n+\frac{1}{2})x \right]$.

</div>

---

# Inequalities

---

## Commonly Used Inequalities

- **Logarithmic Inequality**: $\frac{x}{1+x} \leq \ln(1 + x) \leq x$.
- **Harmonic Series Inequality**: $\ln (n+1) < 1 + \frac{1}{2} + \cdots + \frac{1}{n} < 1 + \ln n$.

<div class=note>

(1) By $\frac{x}{1+x} \leq \ln(1+x) \leq x$, take $x = \frac{1}{n}$ we get $\frac{1}{n+1} \leq \ln \frac{n+1}{n} \leq \frac{1}{n}$.
(2) Summing all the terms up gives the desired result.

</div>

- **Jensen's Inequality**: $\sum_{i=1}^n t_i = 1$, $f$ is convex, then $\sum_{i=1}^n t_if(x_i) \geq f(\sum_{i=1}^n t_i x_i)$.
- Example: $\sum_{i=1}^n p_i = 1$, prove that $\sum_{i=1}^n p_i(x_i - \ln p_i) \leq \ln(\sum_{i=1}^n e^{x_i})$.

<div class=note>

(1) Since $x_i = \ln(e^{x_i})$, it is equivalent to prove $\sum p_i \ln \frac{e^{x_i}}{p_i} \leq \ln (\sum e^{x_i})$.
(2) Let $t_i = \frac{e^{x_i}}{p_i}$, and $\ln x$ is convex, then $\sum p_i \ln t_i \leq \ln (\sum t_ip_i)$.

</div>



