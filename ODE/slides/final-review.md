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

# Final Review: ODE

Speaker: Yixiao Qian

---

# Solving First-Order ODE

---

## Quick Review of First-Order ODE

- **Separable Equation**: $(xy + \sqrt{1-x^2y^2})\mathrm{d} x + x^2 \mathrm{d} y = 0$
- **Homogeneous Equation**: $x y^{\prime} + y = 2 \sqrt{xy}$.
- **Exact Equation**: Ignored.
- **First-Order Linear Equation**: $xy \mathrm{d} x + (2x^2 + 3y^2 - 20) \mathrm{d} y = 0$.
- **Bernoulli's Equation**: $y^{\prime} = \frac{2}{x} y - y^2$.
- $y = f(x,y^{\prime})$:
- $x = f(y,y^{\prime})$:

---

## Quick Review of Higher-Order ODE

- **Method of Characteristic Equation**: Distinct/Repeated Real Roots; (Repeated) Complex Conjugate Roots.
- **Method of Undetermined Coefficients**: (1) $y^{\prime\prime} + 4y = \cos x - \sin 2x$; (2) $y^{(3)} + y^{\prime\prime} = 3e^t + 4t^2$.
- **Euler Equation**: $x^2y^{\prime\prime} + 4xy^{\prime} + 3y = x$.

---

## Quick Review of System of ODEs


---

## Quick Review of Existence and Uniqueness

