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

## Monotonic Function

- **Monotonic Function**: For any $x < y$, $f(x) \leq f(y)$ (or $f(x) \geq f(y)$).
- **Almost-Everywhere Differentiable**: If $f$ is monotonic, then $f$ is differentiable a.e.

---

## Function of Bounded Variation (BV)

- **Variation**: Let $X = \{x_k\}_{0\leq k\leq n}$ where $a = x_0 < x_1 < \cdots < x_n = b_n$ be a paritition of $[a, b]$. *Variation of $f$ with respect to partition $X$* is
$$ V(x) = \sum_{k=1}^n |f(x_k) - f(x_{k-1})|. $$
- **Total Variation**: $T_a^b(f) = \sup \{V(x): X \text{ is partition of } [a, b]\}$ is the *total variation of $f$*.
- **Function of Bounded Variation**: $f$ is a *function of bounded variation* if $T_a^b(f) < \infty$.
- **Decomposition**: Any BV function is the difference of two monotonic functions.
- **Almost-Everywhere Differentiable**: Any BV function is differentiable a.e.

---

## Absolutely Continuous Function (AC)

- **Absolutely Continuous Function**: $\forall \epsilon > 0$, $\exists \delta > 0$, $\forall (a_k, b_k)_{1\leq k\leq n}$ are pairwise disjoint, $\sum_{k=1}^n(b_k-a_k) < \delta$,
$$ \sum\limits_{k = 1}^n |f(b_k) - f(a_k)| < \epsilon.$$
- **Uniform Continuity and Continuity**: AC implies uniform continuity and continuity.
- **Relation with BV**: Any AC function is BC.

---

# Leibniz Formula for Lebesgue Integral

---

## Lebesgue Indefinite Integral



