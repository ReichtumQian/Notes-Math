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
- Solve $y^{\prime} = \cos^2 (x - y - 2023)$.

<div class=note>

(1) Take $u = x - y - 2023$, then $y^{\prime} = 1 - u^{\prime}$. ODE is $u^{\prime} = \sin^2 u$, solution $x = - \cot(u) + c$.
(2) Take back, we get $x = - \cot(x - y - 2023) + c$.

</div>

- Solve $(xy + \sqrt{1-x^2y^2})\mathrm{d} x + x^2 \mathrm{d} y = 0$.

<div class=note>

(1) Take $u(y) = x(y)y$, differentiating $y$, $\frac{\mathrm{d} u}{\mathrm{d} y} = \frac{\mathrm{d} x}{\mathrm{d}y}y + x$. Then $\mathrm{d} y = \frac{\mathrm{d} u - y\mathrm{d} x}{x}$ and $y = \frac{u}{x}$.
(2) $(u + \sqrt{1-u^2})\mathrm{d} x + x\mathrm{d} u - u\mathrm{d} x = 0$ or $\frac{\mathrm{d} u}{\mathrm{d} x} = - \frac{\sqrt{1-u^2}}{x}$. Solution $\arcsin(u) = - \ln |x| + c$.
(3) The general solution is $\arcsin (xy) + \ln |x| = c$.

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

- **Homogeneous Case** $y^{\prime} = P(x)y$: The solution is $y = C e^{\int P(x) \mathrm{d} x}$.

<div class=note>

We can also consider the integrating factor $\mu(x) = e^{\int -P(x)\mathrm{d} x}$. Then

$$ y^{\prime}=P(x)y \Leftrightarrow \frac{\mathrm{d}}{\mathrm{d} x}(\mu(x)y) = 0. $$

</div>

- **Non-Homogeneous Case** $y^{\prime} = P(x) y + Q(x)$: The solution is $y = C(x)e^{\int P(x) \mathrm{d} x}$ (variation of parameters).

<div class=note>

We can also consider the integrating factor $\mu(x) = e^{\int -P(x)\mathrm{d} x}$. Then

$$ \frac{\mathrm{d}}{\mathrm{d} x} [\mu(x) y] = Q(x) \mu(x) \Rightarrow y = \frac{\int Q(x)\mu(x)\mathrm{d} x + c}{\mu(x)}. $$

</div>

---

## Solve First-Order Linear ODEs

- Solve $y^{\prime} = \frac{y}{x + y^3}$.

<div class=note>

Take reciprocal $x^{\prime} = y^2 + \frac{1}{y} x$. Consider $x^{\prime}=\frac{1}{y}x$, solution is $x=cy$. Then consider $x=c(y)y$.
$$ c(y) = \frac{1}{3}y^3 + C \quad \Rightarrow \quad x = \frac{1}{3}y^4 + cy. $$
</div>

- Solve $xy \mathrm{d} x + (2x^2 + 3y^2 - 20) \mathrm{d} y = 0$.

<div class=note>

(1) Look at $y^{\prime} = - \frac{xy}{2x^2 + 3y^2 - 20}$ and $x^{\prime} = - \frac{2x^2 + 3y^2 - 20}{xy}$. To get a linear ODE, we choose $x(y)$.
(2) We do not want $x$ in denominator, so consider $\frac{x\mathrm{d}x}{\mathrm{d} y} = - \frac{2x^2 + 3y^2 - 20}{y}$, take $z = x^2$.
(3) $\frac{\mathrm{d} z}{\mathrm{d} y} = - \frac{4}{y}z - 6y + \frac{40}{y}$ is a linear ODE. Then $\frac{\mathrm{d}}{\mathrm{d} x}(y^4z) = -6y^5 + 40 y^3$, $z = -y^2 + 10 + cy^{-4}$.
(4) The solution is $x^2 = -y^2 + 10 + cy^{-4}$.

</div>

---

## Bernoulli's Equation

- **Bernoulli's Equation** $y^{\prime} = P(x)y + Q(x)y^n$: Multiply both sides by $y^{-n}$, take $z = y^{1-n}$.

<div class=note>

$$ y^{-n} y^{\prime} = P(x)y^{1-n} + Q(x) \Rightarrow z^{\prime} = P(x)z + Q(x). $$

</div>

- Solve $y^{\prime} = \frac{2}{x} y - y^2$.

<div class=note>

Multiply both sides by $y^{-2}$, and take $z = y^{-1}$, then $z^{\prime} = - \frac{2}{x}z + 1$
$$ (x^2z)^{\prime} = x^2 \Rightarrow z = \frac{1}{3}x + \frac{c}{x^2}. $$

</div>


