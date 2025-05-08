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
.warning {
  background-color: #fee;
  padding: 10px;
  margin: 10px 0;
  text-align: left;
}
</style>

# Solving First-Order ODEs

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Separable Equations and Generalizations
- First-Order Linear ODEs
- Exact Equations

---

# Separable Equations and Its Generalizations

---

## Separable Equations

- **Separable Equation**: $y^{\prime} = f(x)\varphi(y)$, then ${\displaystyle \int \frac{\mathrm{d} y}{\varphi(y)} = \int f(x) \mathrm{d} x + c}$.
- Solve $2yy^{\prime} - y^2 - 2 = 0$ with $y(0) = 1$.

<div class=note>

$\frac{2y}{y^2+2}\mathrm{d} y = \mathrm{d} x$, then $\ln(y^2 + 2) = x + c$, where $c = \ln 3$. So the final answer is $y = \sqrt{3e^x - 2}$.
</div>

---

## Homogeneous Equations

- **Homogeneous Equation**: $y^{\prime} = g(\frac{y}{x})$, let $y = ux$, get $u + xu^{\prime} = g(u)$.
- Solve $x y^{\prime} + y = 2 \sqrt{xy}$.

<div class=note>

</div>

- Solve $xy^{\prime} + y(\ln x - \ln y) = 0$, with $y(1) = e^3$.

<div class=note>

</div>

---

# First-Order Linear ODEs

---



---

# Exact Equations

---




