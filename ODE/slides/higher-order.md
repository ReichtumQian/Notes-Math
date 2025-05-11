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

## Table of Contents

---

# Solution Structure


---

# Reduction of Order

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

