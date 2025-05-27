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

# Solving Higher-Order ODEs

Speaker: Yixiao Qian

---

# Solve Constant-Coefficients Higher-Order Linear ODEs

---

## Method of Characteristic Equation


The solution of $x^{(n)}(t) + a_{n-1}x^{(n-1)}(t) + \cdots + a_n x(t) = 0$ is determined by the roots of
$$ \lambda^n + a_{n-1}\lambda^{n-1} + \cdots + a_1 \lambda + a_n = 0. $$
Specifically, the fundamental solution system is composed of
1. For each **distinct real root** $\lambda$, include $ce^{\lambda t}$
2. For each **repeated real root** $\lambda$ of multiplicity $k$, include $c_1e^{\lambda t}, c_2 t e^{\lambda t}, \cdots, c_k t^{k-1}e^{\lambda t}$.
3. For each pair of **complex conjugate roots** $\alpha \pm \beta i$, include $c_1e^{\alpha t}\cos(\beta t)$ and $c_2e^{\alpha t}\sin (\beta t)$.
4. For **repeated complex roots**, analogously multiply $t^m$ to the base term.

<div class=note>

Why multiply by $t$ for each multiplicity: Consider $D = \frac{\mathrm{d}}{\mathrm{d}t}$, then ODE is
$$ (D - \lambda_1)^{m_1} (D - \lambda_2)^{m_2} \cdots (D- \lambda_k)^{m_k}x(t) = 0. $$
For $l < m_i$, $(D - \lambda_i)^{m_i} t^l e^{\lambda_i t} = 0$ and $e^{\lambda_i t}, te^{\lambda_i t},\cdots, t^{m_i-1}e^{\lambda_i t}$ exactly form a base of the space.

</div>

---

## Practice on Method of Characteristic Equation

- Solve $y^{\prime\prime} + 4y = 0$.

<div class=note>

The characteristic equation is $\lambda^2 + 4 = 0$, the roots are $\pm 2i$, then the general solution is
$$ y = c_1 \cos(2x) + c_2 \sin(2x). $$

</div>

---

## Method of Undetermined Coefficients

<div class=trick>

1. Guess the form of particular solution for each term in right hand side.
2. If the form is included in the solution of homogenous one, multiply by extra $t$.

</div>

- Solve $y^{\prime\prime} + 4y = \cos x - \sin 2x$.

<div class=note>

The general solution of homogenous equation is $y = c_1 \cos 2x + c_2 \sin 2x$.

(1) Consider $\cos x$: Assume $y_1=A\cos x + B \sin x$, then $y_1 = \frac{1}{3} \cos x$.
(2) Consider $\sin 2x$: Assume $y_2 = x[A\cos 2x + B \sin 2x]$ (since without $x$, it is included in solution of homogenous equation), then $y_2 = \frac{x}{4} \cos 2x$.

</div>

- Solve $y^{(3)} + y^{\prime\prime} = 3e^t + 4t^2$.

---

# Euler-Cauchy Equation

---

## Euler-Cauchy Equation

- **Euler-Cauchy Equation**: $x^ny^{(n)} + a_{n-1}x^{n-1}y^{(n-1)} + \cdots + a_1xy^{\prime} + a_0y = 0$.

<div class=note>

Assume $y = x^r$, get $f(r) = 0$, find the roots $r_1, r_2, \cdots, r_n$.
- For real root $r$: include $Cx^r$;
- For multiple roots $r$: include $(C_1 + C_2 \ln x + C_3 (\ln x)^2 + \cdots)x^r$.
- For $r = \alpha \pm i \beta$: include $x^{\alpha}[C_1 \cos (\beta \ln x) + C_2 \sin (\beta \ln x)]$.


</div>

- **Non-Homogenous Case**: Apply method of undetermined coefficients.

---

## Examples of Euler-Cauchy Equation

- Solve $x^2y^{\prime\prime} + 4xy^{\prime} + 3y = x$.

<div class=note>

We first solve $x^2y^{\prime\prime} + 4xy^{\prime} + 3y = 0$.

(1) Suppose $y = x^r$, then $r(r-1)x^r + 4rx^r + 3x^r = 0$, meaning $r(r-1) + 4r + 3 = 0$.
(2) We get $r = -\frac{3}{2} \pm \frac{\sqrt{3}}{2}i$, then $y = x^{- \frac{3}{2} \pm \frac{\sqrt{3}}{2}i} = x^{-\frac{3}{2}} e^{\pm \frac{\sqrt{3}}{2}i \ln x}$. The general solution is
$$ y = x^{- \frac{3}{2}} \left[ c_1 \cos \left( \frac{\sqrt{3}}{2} \ln x \right) + c_2 \sin \left( \frac{\sqrt{3}}{2} \ln x \right) \right]. $$

We look for particular solutions of $x^2y^{\prime\prime} + 4xy^{\prime} + 3y = x$. Assume $y_p = Ax + B$, then $y_p = \frac{x}{7}$.

</div>

- Solve $x^2 y^{\prime\prime} - 2x y^{\prime} + 2y = x^3$.

<div class=note>

$y = C_1 x + C_2 x^2 + \frac{1}{2}x^3$.

</div>

---

# Reduction of Order

---

## No Explicit $y$ Case

- **No Explicit $y$**: $y^{\prime\prime} = f(x,y^{\prime})$, consider $p = y^{\prime}$, then $p^{\prime} = f(x,p)$.

<div class=note>

Consider $p = p(y)$, then $y^{\prime\prime} = p^{\prime}_x(y) = y^{\prime}p^{\prime} = pp_y$.

</div

- Solve $y^{\prime 2} - y y^{\prime\prime} = 0$.

<div class=note>

(1) $p = y^{\prime}$, then $p^2 - ypp_y = 0$, $p(p-yp_y) = 0$. Then $p = 0$ or $p - y p_y = 0$.
(2) When $p = 0$, then $y \equiv 0$.
(3) When $p = yp_y$, then $p = C_1y$ and $y = C_2 e^{C_1x}$.

</div>

---

## No Explicit $x$ Case

- **No Explicit $x$**: $F(y,y^{\prime},\cdots,y^{(n)}) = 0$, consider $p = y^{\prime}$ as unknown function, $y$ as variable.

$$ p(y) := y^{\prime}(x) \Rightarrow y^{\prime\prime}(x) = \frac{\mathrm{d} p(y)}{\mathrm{d}x} = p^{\prime}(y) y^{\prime}(x) = p(y) p^{\prime}(y). $$

- Solve $yy^{\prime\prime} - 2(y^{\prime})^2 + y(y^{\prime})^3 = 0$ with $y(0) = 1$, and $y^{\prime}(0) = 3$.

<div class=note>

(1) Let $p(y) = y^{\prime}$, then $y^{\prime\prime}(x) = p(y) p^{\prime}(y)$. ODE is $ypp^{\prime} - 2p^2 + yp^3 = 0$, $p^{\prime} = 2 \frac{p}{y} - p^2$, which is Bernoulli's equation.
(2) Multiply both sides by $p^{-2}$, then $p^{-2}p^{\prime} = \frac{2}{y}p^{-1} - 1$. Take $z = p^{-1}$, then
$$ z^{\prime} = - \frac{2}{y}z + 1 \Rightarrow (y^2z)^{\prime} = y^2 \Rightarrow z = \frac{1}{3}y + \frac{c}{y^2}. $$
(3) Consider the initial conditions $p(1) = 3$, $z(1) = \frac{1}{3}$, we get $c = 0$. Thus $p = \frac{3}{y}$.
(4) Solve $y^{\prime} = \frac{3}{y}$, $y^2 = 6x + 1$ so $y = \sqrt{6x + 1}$.

</div>



