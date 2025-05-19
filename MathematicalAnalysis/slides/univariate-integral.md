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

# Indefinite Integrals

---

## Commonly Used Indefinite Integrals

$$
\begin{align}
    &\int \sec x \, \mathrm{d}x = \ln|\sec x + \tan x| + c 
    && \int \sec x \tan x \, \mathrm{d}x = \sec x + c \\
    &\int \sec^2 x \, \mathrm{d}x = \tan x + c 
    && \int \csc^2 x \, \mathrm{d}x = -\cot x + c \\
    &\int \frac{1}{x^2 + a^2} \, \mathrm{d}x = \frac{1}{a} \arctan \frac{x}{a} + c 
    && \int \frac{1}{x^2 - a^2} \, \mathrm{d}x = \frac{1}{2a} \ln \left| \frac{x-a}{x+a} \right| + c \\
    &\int \frac{1}{\sqrt{x^2 + a^2}} \, \mathrm{d}x = \ln \left| x + \sqrt{x^2 + a^2} \right| + c 
    && \int \frac{1}{\sqrt{x^2 - a^2}} \, \mathrm{d}x = \ln \left| x + \sqrt{x^2 - a^2} \right| + c \\
    &\int \frac{1}{\sqrt{a^2 - x^2}} \, \mathrm{d}x = \arcsin \frac{x}{a} + c 
    && \int \ln x \, \mathrm{d}x = x \ln x - x + c
\end{align}
$$

---

## Indefinite Integrals of Rational Functions

- Calculate ${\displaystyle \int \frac{x}{(x+1)(x^2 + 2)}\mathrm{d} x}$.

<div class=note>

Hint: Assume $\frac{x}{(x+1)(x^2+2)} = \frac{A}{x+1} + \frac{Bx + C}{x^2 + 2}$. Then $A = -\frac{1}{3}$, $B = \frac{1}{3}$, $C = \frac{2}{3}$.

</div>

- Calculate ${\displaystyle \int \frac{\mathrm{d} x}{ax^2 + b}}$. 
- Calculate ${\displaystyle \int \frac{\mathrm{d} x}{(ax^2 + b)^2}}$. (Hint: ${\displaystyle - \int \frac{1}{2ax} \mathrm{d} \frac{1}{ax^2 + b}}$ and integrate-by-part.)
- Calculate ${\displaystyle \int \frac{\mathrm{d} x}{ax^2 + bx + c}}$. (Hint: ${\displaystyle \frac{1}{a} \int \frac{\mathrm{d} x}{(x+\frac{b}{2a})^2 + \frac{c}{a} - \frac{b^2}{4a^2}}}$ and become ${\displaystyle \int \frac{\mathrm{d} x}{ax^2 + b}}$.)
- Calculate ${\displaystyle \int \frac{x}{ax^2 + bx + c}\mathrm{d} x}$. (Hint: ${\displaystyle \frac{1}{2a} \int \frac{2ax + b}{ax^2 + bx + c} - \frac{b}{ax^2 + bx + c}\mathrm{d} x}$)

---

## Indefinite Integrals of $\ln x$ and $e^x$

- Calculate ${\displaystyle \int \ln(1 + \sqrt{x}) \mathrm{d} x}$.

---

## Indefinite Integrals of Trigonometric Functions

- Calculate the following integrals

$$
(1) \int \tan x\mathrm{d} x, \quad
(2) \int \sec x \mathrm{d} x, \quad
(3) \int \sec^3 x \mathrm{d} x.
$$

<div class=note>

(1) ${\displaystyle \int \tan x \mathrm{d} x = - \int \frac{\mathrm{d} \cos x}{\cos x} = - \ln |\cos x| + C}$.
(2) ${\displaystyle \int \sec x \mathrm{d} x = \int \frac{\sec x (\sec x + \tan x)}{\sec x + \tan x}\mathrm{d} x = \int \frac{\mathrm{d} (\sec x + \tan x)}{\sec x + \tan x} = \ln |\sec x + \tan x| + C}$.
(3) ${\displaystyle \int \sec^3 x \mathrm{d} x = \int \sec x \mathrm{d} \tan x = \sec x \tan x - \int \tan^2 x \sec x \mathrm{d} x}$. Since $\tan^2 x = \sec^2 x - 1$,
$$ \int \sec^3 x \mathrm{d} x = \sec x \tan x - \int \sec^3 x \mathrm{d} x + \int \sec x \mathrm{d} x $$

</div>

---

## Indefinite Integrals of Squared Functions

---

# Definite Integrals

---

## Key Points of Definite Integrals

- **Condition for Integrability**
- **Closure under Arithmetic Operations**
- **Closure under Composition**
- **Newton-Leibniz Formula**

---

## Mean-Value Theorem for Integrals

- If $f$ is strictly increasing, prove ${\displaystyle \int_a^b xf(x)\mathrm{d} x > \frac{a+b}{2} \int_a^b f(x)\mathrm{d} x}$.

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

- If ${\displaystyle \int_a^{+\infty}f(x)\mathrm{d} x}$ exists and $\lim \limits _{x \rightarrow \infty}f(x) = A$. Then $A = 0$.



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










