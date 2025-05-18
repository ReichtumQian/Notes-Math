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

# Multivariable Integrals

Speaker: Yixiao Qian

---

## Table of Contents

---

# Parametric Integrals

---

## Proper Parametric Integrals

- **Proper Parametric Integrals**: ${\displaystyle F(t) := \int_{\alpha(t)}^{\beta(t)} f(x, t)\mathrm{d} x}$, where $t \in [a, b]$.
- **Properties**: $f(x,t), f_t(x,t)$ continuous, $\alpha(t),\beta(t)$ differentiable, then

$$
\lim \limits _{t \rightarrow t_0} \int_{\alpha(t)}^{\beta(t)}f(x,t)\mathrm{d} x
= \int_{\alpha(t_0)}^{\beta(t_0)} f(x, t_0)\mathrm{d} x,
$$
$$
\frac{\mathrm{d}}{\mathrm{d}t} \int_{\alpha(t)}^{\beta(t)} f(x, t)\mathrm{d} x
= f(\beta(t), t)\beta^{\prime}(t) - f(\alpha(t), t) \alpha^{\prime}(t)
+ \int_{\alpha(t)}^{\beta(t)}f_t(x, t)\mathrm{d} x.
$$

- **Example**: Given $\displaystyle F(x) = \int_0^x (x^2 - t^2)f(t)\mathrm{d} t$, find $F^{\prime}(x)$.

<div class=note>

$$
F^{\prime}(x) = [(x^2 - x^2)f(x) \cdot 1] - [(x^2 - 0)f(0)\cdot 0] + \int_0^x 2xf(t)\mathrm{d} t
              = \int_0^x 2xf(t)\mathrm{d} t.
$$

</div>

---

## Practice on Proper Parametric Integrals

- $f$ has continuous derivatives, $f(0)=0$, $f^{\prime}(0) \neq 0$, $\displaystyle F(x) = \int_0^x (x^2 - t^2)f(t)\mathrm{d} t$. Find $k$ such that $F^{\prime}(x)$ and $x^k$ are infinitesimals of the same order when $x \rightarrow 0$.

<div class=note>

$\displaystyle F^{\prime}(x) = \int_0^x 2x f(t)\mathrm{d} t$ and $f(t) = f(0) + f^{\prime}(0)t + o(t^2)$, then

$$ F^{\prime}(x) = 2x \int_0^x f^{\prime}(0)t + o(t^2)\mathrm{d} t = f^{\prime}(0)x^3 \quad \Rightarrow \quad k = 3. $$

</div>

---

## Improper Parametric Integrals

- **Improper Parametric Integral**: $\displaystyle \Phi(t) = \int_c^{+\infty} f(x,t)\mathrm{d} x$.
- **Uniform Convergence**: $\forall \epsilon > 0$, $\exists M > 0$, $\forall A > M$,
$$\displaystyle \left| \int_c^{+\infty}f(x,t)\mathrm{d} x - \int_c^Af(x,t)\mathrm{d}x \right| = \left| \int_A^{+\infty} f(x,t)\mathrm{d} x \right| < \epsilon, \quad t \in I.$$
- **Cauchy Criterion**: $\forall \epsilon > 0$, $\exists M > 0$, $\forall A_1, A_2 > M$, $\displaystyle \left| \int_{A_1}^{A_2}f(x,t)\mathrm{d} x \right| < \epsilon$ for all $t \in I$.
- **M-Test**: $|f(x,t)| \leq g(x)$, $\displaystyle \int_c^{+\infty}g(x)\mathrm{d} x$ exists implies ${\displaystyle \int_c^{+\infty}f(x,t)\mathrm{d} x}$ uniformly converges.
- **Dirichlet Test**:
- **Abel Test**:

---

## Apply Definition to Prove Uniform Convergence

- Prove that ${\displaystyle \int_0^{+\infty} \frac{\sin xy}{y}\mathrm{d} y}$ uniformly converges on $[\delta, +\infty)$, but it does not uniformly converge on $(0, +\infty)$.

<div class=note>

</div>


---

# Multiple Integrals


---

# Line Integrals

---

## Key Points of Line Integrals

---

# Surface Integrals

---

## Surface Integral with Respect to Area

- **Surface Area Formula 1**: If $z = f(x,y)$, then $\displaystyle S = \iint_D \sqrt{1 + f_x^2 + f_y^2}\mathrm{d} x \mathrm{d} y$.
- **Surface Area Formula 2**: If $x=x(u,v)$, $y = y(u,v)$, $z = z(u, v)$, $\displaystyle S = \iint_D \sqrt{EG - F^2}\mathrm{d} u\mathrm{d} v$, where $E=x_u^2+y_u^2+z_u^2$, $F=x_ux_v+y_uy_v+z_uz_v$, $G = x_v^2+y_v^2+z_v^2$.
- **Surface Integral with Respect to Area Formulas**:
$$
\iint_S f(x,y,z)\mathrm{d}S = \iint_D f(x,y,z(x,y)) \sqrt{1 + z_x^2 + z_y^2}\mathrm{d} x \mathrm{d} y.
$$
$$
\iint_S f(x,y,z)\mathrm{d}S = \iint_D f(x(u,v),y(u,v),z(uv)) \sqrt{EG-F^2}\mathrm{d} u \mathrm{d} v.
$$

---

## Surface of a Vector Field

- **Surface of a Vector Field Formula**: Define $A = |\frac{\partial(y,z)}{\partial(u,v)}|$, $B = |\frac{\partial(z,x)}{\partial(u,v)}|$, $C = |\frac{\partial(x,y)}{\partial(u,v)}|$,
$$
\iint_S R(x,y,z)\mathrm{d}x\mathrm{d}y = \pm \iint_{D_{xy}} R(x,y,z(x,y))\mathrm{d}x\mathrm{d}y.
$$
$$
\iint_S P\mathrm{d}y\mathrm{d}z + Q\mathrm{d}z\mathrm{d}x + R\mathrm{d}x\mathrm{d}y
= \pm \iint_D (PA + QB + RC)\mathrm{d}u\mathrm{d}v,
$$
- **Gauss's Theorem**: $V \subset \mathbb{R}^3$ is closed, $S$ is boundary of $V$
$$
\iint  _{S_+}P\mathrm{d}y \mathrm{d}z + Q \mathrm{d}z \mathrm{d}x + R \mathrm{d}x \mathrm{d}y = \iiint_V (\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z})\mathrm{d}x \mathrm{d}y \mathrm{d}z
$$









