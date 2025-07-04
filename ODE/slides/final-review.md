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

- **Characteristic Equation**: Distinct/Repeated Real Roots; Complex Conjugate Roots.
- **Undetermined Coefficients**: (1) $y^{\prime\prime} + 4y = \cos x - \sin 2x$; (2) $y^{(3)} + y^{\prime\prime} = 3e^t + 4t^2$.
- **Euler Equation**: $x^2y^{\prime\prime} + 4xy^{\prime} + 3y = x$.

<div class=note>

</div>

---

## Quick Review of System of ODEs

- **Solution of $\mathbf{x}^{\prime}(t) = A\mathbf{x}(t)$**: For each eigenvalue $\lambda$ of $A$, the corresponding solutions:

$$
e^{\lambda t} \mathbf{v}_k, \quad
e^{\lambda t} \left( \mathbf{v}_{k-1} + t\mathbf{v}_k \right), \quad \cdots, \quad
e^{\lambda t} \left( \mathbf{v}_0 + t\mathbf{v}_1 + \cdots + \frac{t^k}{k!}\mathbf{v}_k \right),
$$

where $\mathbf{v}_k$ is the solution of $(A - \lambda I)\mathbf{v} = 0$, $\mathbf{v}_0,\cdots,\mathbf{v}_{k-1}$ are solutions of $(A - \lambda I)\mathbf{v}_j = \mathbf{v}_{j+1}$.

- Solve Imhomogeneous ODEs:
$$
\begin{cases}
  x^{\prime} = x + y\\
  y^{\prime} = -x + 3y + e^{2t}
\end{cases}, \quad x(0) = 1, y(0) = -1.
$$

<div class=note>

Transform into higher-order ODE.

</div>

---

## Quick Review of Existence and Uniqueness

