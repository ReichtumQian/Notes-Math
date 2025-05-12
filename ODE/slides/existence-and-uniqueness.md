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

# Existence and Uniqueness of Solutions

Speaker: Yixiao Qian

---

## Table of Contents

---

# Picard Existence and Uniqueness Theorem

---

## Picard Sequences

- **Integral Equation**: $y(x)$ follows $\displaystyle \frac{\mathrm{d} y}{\mathrm{d} x} = f(x,y)$ with $y(x_0) = y_0$ iff
$$ y(x) = y_0 + \int_{x_0}^x f(t,y(t))\mathrm{d} t $$
- **Picard Sequence**: $\varphi_0(x) = y_0$ and $\displaystyle \varphi_n(x) = y_0 + \int_{x_0}^x f(t, \varphi_{n-1}(t))\mathrm{d} t$ for $n \geq 1$.
- **Lipschitz Continuous**: $f(x,y)$ is *Lipschitz continuous with respect to $y$* if
$$ |f(x,y_1) - f(x,y_2)| \leq L |y_1 - y_2|, \quad \forall (x,y_1),(x,y_2) \in R.$$

---

## Properties of Picard Sequences

---

## Existence and Uniqueness Theorem

<div class=trick>

If $f(x,y)$ is Lipschitz continuous with respect to $y$ in $R = [x_0-a,x_0+a] \times [y_0-b,y_0+b]$. Then there exists a unique solution $y = \varphi(x)$ such that

$$ \frac{\mathrm{d} y}{\mathrm{d} x} = f(x,y), \quad x \in (x_0-h, x_0+h), \quad \varphi(x_0) = y_0, $$

where $h = \min \left( a, \frac{b}{M} \right)$, $M = \max_{(x,y) \in R} |f(x,y)|$.

</div>

---

## Practice on Existence and Uniqueness Theorem

- If $f$ is continuous in $\mathbb{R}$. Prove that $y^{\prime} = -f(y)$, $y(x_0) = y_0$ has unique solution at $x = x_0$.

<div class=note>


</div>

