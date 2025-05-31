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
$$
\int_{t_1}^{t_2} \mathrm{d} t \int_{x_1(t)}^{x_2(t)} f(x,t)\mathrm{d} x = \int_{x_1}^{x_2} \mathrm{d} x \int_{t_1(x)}^{t_2(x)} f(x,t)\mathrm{d} t.
$$


---

## Practice on Properties of Proper Parametric Integrals

- Given $\displaystyle F(x) = \int_0^x (x^2 - t^2)f(t)\mathrm{d} t$, find $F^{\prime}(x)$.

<div class=note>

$$
F^{\prime}(x) = [(x^2 - x^2)f(x) \cdot 1] - [(x^2 - 0)f(0)\cdot 0] + \int_0^x 2xf(t)\mathrm{d} t
              = \int_0^x 2xf(t)\mathrm{d} t.
$$

</div>

- Calculate ${\displaystyle \int_0^1 \frac{x^b - x^a}{\ln x}\mathrm{d} x}$ where $0 < a < b$.

<div class=note>

(1) ${\displaystyle \int _a^b x^y \mathrm{d} y = \frac{x^y}{\ln x} \bigg|^b _a = \frac{x^b - x^a}{\ln x}}$.
(2) ${\displaystyle I = \int_0^1 \mathrm{d} x \int_a^b x^y \mathrm{d} y = \int_a^b \mathrm{d} y \int_0^1 x^y \mathrm{d} x = \ln \frac{1+b}{1+a}}$.

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
- **Uniform Convergence Statement**: $\forall \epsilon > 0$, $\exists M > 0$, $\forall A > M$,
$$\displaystyle \left| \int_c^{+\infty}f(x,t)\mathrm{d} x - \int_c^Af(x,t)\mathrm{d}x \right| = \left| \int_A^{+\infty} f(x,t)\mathrm{d} x \right| < \epsilon, \quad t \in I.$$
- **Cauchy Criterion**: $\forall \epsilon > 0$, $\exists M > 0$, $\forall A_1, A_2 > M$, $\displaystyle \left| \int_{A_1}^{A_2}f(x,t)\mathrm{d} x \right| < \epsilon$ for all $t \in I$.
- **M-Test**: $|f(x,t)| \leq g(x)$, $\displaystyle \int_c^{+\infty}g(x)\mathrm{d} x$ exists implies ${\displaystyle \int_c^{+\infty}f(x,t)\mathrm{d} x}$ uniformly converges.
- **Dirichlet Test**: (1) ${\displaystyle \int_c ^N f(x,t) \mathrm{d} x}$ uniformly bounded to $t$; (2) $g(x,t) \rightrightarrows 0$ decreasingly when $x \rightarrow \infty$ with respect to $t$.
- **Abel Test**: (1) ${\displaystyle \int_c^{+\infty} f(x,t)\mathrm{d} x}$ converges uniformly; (2) $g(x,t)$ uniformly bounded to $t$.

---

## Determine Uniform Convergence

- ${\displaystyle \int_0^{+\infty} \frac{\sin xy}{y}\mathrm{d} y}$ uniformly converges on $[\delta, +\infty)$, but not on $(0, +\infty)$.

<div class=note>

(1) ${\displaystyle \left| \int_{\delta}^A \sin (xy) \mathrm{d} y\right| = \left|\frac{\cos(ax) - \cos(Ax)}{x}\right| \leq \frac{2}{\delta}}$ is uniformly bounded. $\displaystyle \frac{1}{y} \rightrightarrows 0$. By Dirichlet.
(2) ${\displaystyle \sup_{x \in (0, +\infty)} \left| \int_A^{+\infty} \frac{\sin xy}{y}\mathrm{d} y \right| = \sup_{x \in (0, +\infty) }\left| \int_{Ax}^{+\infty} \frac{\sin u}{u}\mathrm{d} u \right| \geq \left| \int_0^{+\infty} \frac{\sin u}{u}\mathrm{d} u \right| = \frac{\pi}{2}}$.

</div>

- ${\displaystyle \int_1^{+\infty} \frac{\sin x}{1+xe^y}\mathrm{d} x}$ on $[0, +\infty)$.

<div class=note>

(1) $\displaystyle \left| \int_1^N \sin x \mathrm{d} x \right|$ is uniformly bounded. (2) $\displaystyle \frac{1}{1+xe^y} \leq \frac{1}{1+x} \rightarrow 0$. By Dirichlet test.

</div>

---

## Determine Uniform Convergence

- ${\displaystyle \int_0^{+\infty} e^{-xy} \frac{\sin x}{x}\mathrm{d} x}$ on $[0, +\infty)$.

<div class=note>

(1) ${\displaystyle \int_0^{+\infty} \frac{\sin x}{x} \mathrm{d} x}$ is uniformly convergent with respect to $y$.
(2) $e^{-xy}$ decreases with respect to $x$, and $0 < e^{-xy} < 1$ is uniformly bounded.

</div>

---

## Some Commonly Used Integrals

- If $p > 0$, then ${\displaystyle \int_0^{+\infty} e^{-px} \frac{\sin bx - \sin ax}{x} \mathrm{d} x = \arctan \frac{b}{p} - \arctan \frac{a}{p}}$.

- **Dirichlet Integral**: ${\displaystyle \int_0^{+\infty} \frac{\sin x}{x} \mathrm{d} x = \frac{\pi}{2}}$.

- **Normal Distribution Integral**: ${\displaystyle \int_0^{+\infty} e^{-x^2}\mathrm{d} x = \frac{\sqrt{\pi}}{2}}$.

<div class=note>

$\displaystyle I^2 = \iint_{[0, +\infty)^2} e^{-(x^2+y^2)}\mathrm{d} x \mathrm{d} y = \int_0^{\frac{\pi}{2}}\mathrm{d} \theta \int_0^{\infty} e^{-r^2}r \mathrm{d} r \mathrm{d} \theta = \frac{\pi}{4}$.

</div>


---

# Multiple Integrals

---

## Double Integral

- **Iterated Integral**
- **Change of Vairable**:
- **Polar Coordinate Transformation**

---

## Triple Integral

- **Projection Method**
- **Cross-Section Method**
- **Change of Variable**
- **Cylindrical Coordinate Transformation**
- **Spherical Coordinate Transformation**

---

# Line Integrals and Surface Integrals

---

## Line Integrals

- **With Respect to Arc Length**: ${\displaystyle \int_{\Gamma} f(x,y,z)\mathrm{d} s = \int_a^b f(x(t),y(t),z(t))\sqrt{x^{\prime 2} + y^{\prime 2} + z^{\prime 2}}\mathrm{d} t}$
- **Of a Vector Field**: $\displaystyle \int_{\Gamma} P \mathrm{d} x + Q\mathrm{d} y + R \mathrm{d} z = \int_a^b [Px^{\prime}(t) + Qy^{\prime}(t) + Rz^{\prime}(t)]\mathrm{d} t$.
- **Green's Theorem**: ${\displaystyle \oint_{\partial \Omega} P \mathrm{d} x + Q\mathrm{d} y = \iint_{\Omega} \left( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \right)\mathrm{d} x \mathrm{d} y}$.
- **Application of Green's Theorem**: Calculate ${\displaystyle \oint_L \frac{x\mathrm{d} y - y\mathrm{d} x}{ax^2 + by^2}}$ where $a, b > 0$, $L$ doesn't pass through the origin, but enclose it.


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

## Surface Integral of a Vector Field

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









