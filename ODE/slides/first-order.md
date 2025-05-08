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

# Solving First-Order ODEs

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Separable Equations and Generalizations
- Exact Equations
- First-Order Linear ODEs

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

- **Homogeneous Equation**: $y^{\prime} = g(\frac{y}{x})$, let $y = ux$, get $u + xu^{\prime} = g(u)$ and $u^{\prime} = \frac{g(u) - u}{x}$.

- Solve $xy^{\prime} + y(\ln x - \ln y) = 0$, with $y(1) = e^3$.

<div class=note>

Let $y = ux$, then $\frac{\mathrm{d} u}{u(\ln u - 1)} = \frac{\mathrm{d} x}{x}$. Then $u = e^{1\pm 2x}$ and $y = x e^{1 \pm 2x}$.
</div>

- Solve $x y^{\prime} + y = 2 \sqrt{xy}$.

<div class=trick>

Note: $\frac{\mathrm{d} u}{2 \sqrt{u} - 2u} = \frac{1}{x}\mathrm{d} x$, the left hand is quite hard to integrate. So we should not simply consider it as homogeneous equation.
</div>

<div class=note>

Consider $(xy)^{\prime} = 2 \sqrt{xy}$ and $u(x) = x \cdot y(x)$. Then $u = (x+c)^2$ or $0$, and $y=\frac{(x+c)^2}{x}$ or $0$.
</div>

---

# Exact Equations

---

## Exact Equations

- **Exact Equation**: $M(x,y)\mathrm{d} x + N(x,y)\mathrm{d} y = 0$ where $M_y = N_x$.
- **How to Solve**: $\displaystyle F(x,y) = \int M(x,y)\mathrm{d} x + h(y)$, where $h(y)$ follows $F_y^{\prime}(x,y) = N(x,y)$.
- **General Solution**: $F(x, y) = 0$.
- Solve $y^{\prime} = \frac{y}{2y \ln y + y - x}$.

<div class=note>

$(2y \ln y + y - x)\mathrm{d} y - y\mathrm{d} x = 0$. Then $\displaystyle F(x,y) = \int -y \mathrm{d} x + h(y) = -xy + h(y)$. Then
$$ F_y^{\prime}(x,y) = -x + h^{\prime}(y) = 2y \ln y + y - x. $$
$$ h(y) = \int 2y \ln y + y \mathrm{d} y = y^2 \ln y. $$
General solutions follow $-xy + y^2\ln y = C$.
</div>

---

# First-Order Linear ODEs

---

## First-Order Linear ODEs

<br>

- $y^{\prime} = P(x)y$: $y = C e^{\int P(x) \mathrm{d} x}$.
- $y^{\prime} = P(x) y + Q(x)$: $y = C(x)e^{\int P(x) \mathrm{d} x}$.
- Solve $y^{\prime} = \frac{y}{x + y^3}$.

<div class=note>

Take reciprocal $x^{\prime} = y^2 + \frac{1}{y} x$. Consider $x^{\prime}=\frac{1}{y}x$, solution is $x=cy$. Then consider $x=c(y)y$.
$$ c(y) = \frac{1}{3}y^3 + C \quad \Rightarrow \quad x = \frac{1}{3}y^4 + cy. $$
</div>




