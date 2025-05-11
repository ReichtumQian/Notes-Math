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

# Univariate Integrals

Speaker: Yixiao Qian

---

## Table of Contents


---

# Improper Integrals

---

## Definition of Improper Integrals

- **Improper Integrals**: ${\displaystyle \int_a^{+\infty}f(x)\mathrm{d} x := \lim \limits _{b \rightarrow +\infty}\int_a^b f(x)\mathrm{d} x}$ and ${\displaystyle \int_a^b f(x) \mathrm{d} x := \lim \limits _{\epsilon \rightarrow 0} \int_{a+\epsilon}^b f(x)\mathrm{d} x}$.

<div class=note>

Consider $\displaystyle F(t) = \int_a^t f(x)\mathrm{d} x$ as a function, then we can apply theory of function limit to convergence and Cauchy's criterion of improper integrals.

</div>

- **Statement of Convergence**: The improper integral converges iff there exists $A$ 
$$ \forall \epsilon > 0, \exists M > 0, \forall b > M, \quad \left| A - \int_a^b f(x) \mathrm{d} x \right| = \left| \int_b^{+\infty}f(x)\mathrm{d}x \right| < \epsilon. $$
- **Cauchy's Criterion**: The improper integral converges iff
$$ \forall \epsilon > 0, \exists M > 0, \forall t_1, t_2 > M, \quad \left| \int_a^{t_1} f(x)\mathrm{d} x - \int_a^{t_2}f(x)\mathrm{d} x \right| = \left| \int_{t_1}^{t_2} f(x)\mathrm{d} x \right| < \epsilon. $$

---

## Definition of Improper Integrals

- **Leibniz Formula**: ${\displaystyle \int_a^{+\infty} f(x)\mathrm{d} x = F(+\infty) - F(a)}$ and ${\displaystyle \int_a^b f(x)\mathrm{d} x = F(b) - F(a+0)}$.
- **Absolute and Conditional Convergence**: If ${\displaystyle \int_a^b |f(x)| \mathrm{d} x}$ converges, then ${\displaystyle \int_a^b f\mathrm{d} x}$ is *absolutely convergent*, otherwise it is *conditionally convergent*.

<div class=note>

Absolute convergence implies convergence, since Cauchy's criterion.

$$ \left| \int_{t_1}^{t_2} f(x)\mathrm{d} x \right| \leq \int_{t_1}^{t_2} |f(x)|\mathrm{d} x < \epsilon $$

</div>

- **Behavior of $\displaystyle \int_1^{+\infty} \frac{\mathrm{d} x}{x^p}$**: Converges when $p > 1$, diverges when $p \leq 1$.
- **Behavior of ${\displaystyle \int_0^1 \frac{\mathrm{d} x}{x^p}}$**: Converges when $p < 1$, diverges when $p \geq 1$.


---

## Properties of Convergent Improper Integrals


---

## Tests for Convergence

- **Compare Test**:
- **Dirichlet Test**:
- **Abel Test**:

---

## Improper Integrals involving $e^x$ and $\ln x$

<div class=trick>

</div>

---

## Several Sepecial Improper Integrals

