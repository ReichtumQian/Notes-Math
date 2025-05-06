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
.warning {
  background-color: #fee;
  padding: 10px;
  margin: 10px 0;
  text-align: left;
}
</style>

# Lebesgue Measure

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Lebesgue Outer Measure
- Lebesgue Measure
- A Non-Mesurable Set Example
- Approximation by Open and Closed Sets

---

# Lebesgue Outer Measure

---

## Key Points of Lebesgue Outer Measure

<br>

- **Definition**: $m^{\ast}(E) = \inf_{\{I_n\}} \left\{ \sum \ell(I_n) \right\}$.
- **Countable Sub-Additivity**: $m^{\ast}(\cup E_n) \leq \sum m^{\ast}(E_n)$.

<div class=note>

$$m^*\left(\bigcup_n E_n\right) \leq \sum_n \sum_k \ell(I_k^{(n)}) < \sum_n \left[m^*(E_n) + \frac{\epsilon}{2^n}\right] = \sum_n m^*(E_n) + \epsilon.$$
</div>

- **Additivity**: $E_n$ from disjoint measurable sets $S_n$, then $m^{\ast}(\cup E_n) = \sum m^{\ast}(E_n)$.
- **Continuity**: $f(x) = m^{\ast}([a, x] \cap E)$ is continuous.

---

# Lebesgue Measure

---

## Key Points of Lebesgue Measure

<br>

- **Measurable Set**: For any $A \subset \mathbb{R}$, $m^{\ast}(A) \geq m^{\ast}(A \cap E) + m^{\ast}(A \cap E^c)$.
- **Closure under Operations**: $A^c$, $\cup$, $\cap$, $\limsup$, $\liminf$.
- **Countable Sub-Additivity**: $A_n$ are arbitrary, then $m(\cup_n A_n) \leq \sum_n m(A_n)$.
- **Countable Additivity**: $A_n$ are pairwise-disjoint, then $m(\cup_n A_n) = \sum_n m(A_n)$.

---

# A Non-Measurable Set Example

---

# Approximation by Open and Closed Sets

---


