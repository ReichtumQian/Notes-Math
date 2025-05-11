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


