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

# Leibniz Formula for Lebesgue Integrals

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Special Functions in Lebesgue Theory
- Leibniz Formula for Lebesgue Integral

---

# Special Functions in Lebesgue Theory

---

## Monotonic Functions

- **Monotonic Function**: For any $x < y$, $f(x) \leq f(y)$ (or $f(x) \geq f(y)$).
- **Almost-Everywhere Differentiable**: If $f$ is monotonic, then $f$ is differentiable a.e.

---

## Function of Bounded Variation (BV)

- **Variation**: Let $X = \{x_k\}_{0\leq k\leq n}$ where $a = x_0 < x_1 < \cdots < x_n = b_n$ be a paritition of $[a, b]$. *Variation of $f$ with respect to partition $X$* is
$$ V(x) = \sum_{k=1}^n |f(x_k) - f(x_{k-1})|. $$
- **Total Variation**: $\bigvee_a^b(f) = \sup \{V(x): X \text{ is partition of } [a, b]\}$ is the *total variation of $f$*.
- **Addition of Total Variation**: $\bigvee_a^b(f) = \bigvee_a^c (f) + \bigvee_c^b(f)$.
- **Function of Bounded Variation**: $f$ is a *function of bounded variation* if $\bigvee_a^b(f) < \infty$.
- **Boundedness**: Any BV function is bounded.

<div class=note>

For any $x \in [a, b]$, $|f(x) - f(a)| < \bigvee _a^b f(x) < \infty$.

</div>

- **Closure under Operations**: $f\pm g$, $fg$ are BV; if $|g(x)| \leq \epsilon > 0$ then $f/g$ is BV.

---

## Fundamental Property of BV Function

- **Decomposition**: $f$ is a BV function iff it is the difference of two monotonic functions.

<div class=note>

(1) $\Leftarrow$ is direct.
(2) $\Rightarrow$: For any $a \leq x_1 < x_2 \leq b$, $f(x_2)-f(x_1) \leq \bigvee_{x_1}^{x_2}(f) = \bigvee_a^{x_2}(f) - \bigvee_a^{x_1}(f)$. Then
$$ \bigvee_a^{x_1}(f) - f(x_1) \leq \bigvee_a^{x_2}(f) - f(x_2). $$
$F(x) = \bigvee_a^x(f) - f(x)$ is monotonically increasing, then $f(x) = \bigvee_a^x(f) - [\bigvee_a^x(f) - f]$ is the difference of two monotonic functions.

</div>

---

## Properties of BV Functions

- **Almost-Everywhere Differentiable**: Any BV function is differentiable a.e.
- **Continuous not Bounded-Variation**: $f = x \cos \frac{\pi}{2x}$ with $f(0) = 0$ is continuous on $[0, 1]$, but does not have bounded variation.

<div class=note>

Take $X_n = \left\{ 0, \frac{1}{2n}, \frac{1}{2n-1}, \cdots, \frac{1}{3}, \frac{1}{2}, 1 \right\}$, $|f(\frac{1}{k})| = \frac{1}{k}, 0$ when $k = 0,1 (\operatorname{mod} 2)$. Then
$$ V(X_n) =  2 \cdot \frac{1}{2n} + 2 \cdot \frac{1}{2n-2} + \cdots + 2 \cdot \frac{1}{2} = 1 + \frac{1}{2} + \cdots + \frac{1}{n} \rightarrow \infty $$

</div>

- **Bounded-Variation not Continuous**: $f(x) = 0$ for $x \in [0,1)$ with $f(1) = 1$ is bounded-variation but not continuous on $[0, 1]$.

---

## Absolutely Continuous Function (AC)

- **Absolutely Continuous Function**: $\forall \epsilon > 0$, $\exists \delta > 0$, $\forall (a_k, b_k)_{1\leq k\leq n}$ are pairwise disjoint, $\sum_{k=1}^n(b_k-a_k) < \delta$,
$$ \sum\limits_{k = 1}^n |f(b_k) - f(a_k)| < \epsilon.$$
- **Closure under Operations**: $f \pm g$, $fg$, and $f/g$ ($g \neq 0$) are AC.
- **Closure under composition**: $f,\varphi$ are AC, $\varphi$ is strictly increasing, then $f(\varphi)$ is AC.
- **Relation with BV**: Any AC function is BC.

---

## Analysis Properties of AC Functions

- **Uniform Continuity and Continuity**: AC implies uniform continuity and continuity.
- **Differentiability**: Any AC function is differentiable a.e. and its derivative is integrable.
- **Leibniz Formula**: If $f$ is AC, then $\displaystyle f(x) = f(a) + \int_a^x f^{\prime}(t)\mathrm{d} t$.

---

## Applications of AC Functions

- If $f$ is AC on $[0, 1]$, $f(0) = 0$, prove that ${\displaystyle \int_0^1 |f(x)f^{\prime}(x)|\mathrm{d} x \leq \int_0^1 |f^{\prime}(x)|^2 \mathrm{d} x}$.

<div class=note>

(1) $f$ is AC and $f(0) = 0$, then ${\displaystyle f(x) = \int_0^x f^{\prime}(t) \mathrm{d} t}$, it is equivalent to prove
$$ \int_0^1 \left( \int_0^x |f^{\prime}(t)|\mathrm{d}t \right) |f^{\prime}(x)|\mathrm{d}x \leq \int_0^1 |f^{\prime}(x)|^2 \mathrm{d} x. $$
(2) By Tonelli theorem, the left-hand side equals to ${\displaystyle \int_0^1 \int_t^1 |f^{\prime}(t)| \cdot |f^{\prime}(x)|\mathrm{d} x \mathrm{d} t}$
(3) Since symmetry, ${\displaystyle \int_0^1 \int_t^1 |f^{\prime}(t)| \cdot |f^{\prime}(x)|\mathrm{d} x \mathrm{d} t \leq \left( \int_0^1 |f^{\prime}(x)| \mathrm{d} x \right)^2}$.
(4) By Cauchy-Schwarz inequility
$$ \left( \int_0^1 |f^{\prime}(x)|\mathrm{d}x \right)^2 \leq \int_0^1 1^2 \mathrm{d} x \cdot \int_0^1 |f^{\prime}(x)|^2 \mathrm{d} x = \int_0^1 |f^{\prime}(x)|^2\mathrm{d} x. $$

</div>


---

# Leibniz Formula for Lebesgue Integral

---

## Lebesgue Indefinite Integral

- **Lebesgue Indefinite Integral**: ${\displaystyle F(x) = \int_a^x f(t)\mathrm{d} t}$ for $x \in [a, b]$.
- **Fundamental Theorem**: $F^{\prime}(x) = f(x)$ a.e.
- **Indefinite Integral is BV**: $F(x)$ is BV on $[a, b]$, and
$$ \bigvee_a^b(F) = \int_a^b |F^{\prime}(t)| \mathrm{d} t = \int_a^b |f(t)|\mathrm{d}t. $$
- **Indefinite Integral is AC**: $F(x)$ is AC on $[a, b]$

---

## Apply Indefinite Integral to Calculate Total Variation

- If $f$ has continuous derivative, $x_1<x_2<\cdots<x_n$ are roots of $f^{\prime}(x)$, what is $\bigvee_a^b (f)$?

<div class=note>

$$ \bigvee_a^b(f) = \int_a^{x_1}|f^{\prime}(t)|\mathrm{d} t + \int_{x_1}^{x_2}|f^{\prime}(t)| \mathrm{d}t + \cdots + \int_{x_n}^b |f^{\prime}(t)|\mathrm{d}t. $$

</div>

- Calculate $\bigvee_0^{4\pi} (\cos x)$.

<div class=note>

$f^{\prime}(x) = -\sin x$, then roots of $f^{\prime}(x) = 0$ are $0, \pi, 2\pi, 3\pi, 4\pi$.
$$ \bigvee_0^{4\pi}(\cos x) = 4 \int_0^{\pi} |\sin x|\mathrm{d}x = 8. $$

</div>






