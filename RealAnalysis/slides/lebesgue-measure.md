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

- **Definition**: $m^{\ast}(E) = \inf_{\{I_n\}} \left\{ \sum \ell(I_n) \right\}$.
- **Countable Sub-Additivity**: $m^{\ast}(\cup E_n) \leq \sum m^{\ast}(E_n)$.

<div class=note>

$$m^*\left(\bigcup_n E_n\right) \leq \sum_n \sum_k \ell(I_k^{(n)}) < \sum_n \left[m^*(E_n) + \frac{\epsilon}{2^n}\right] = \sum_n m^*(E_n) + \epsilon.$$
</div>

- **Corollary of Sub-Additivity**: $m^{\ast}(E) - m^{\ast}(F) \leq m^{\ast}(E - F)$, including the case $F \subset E$.

- **Continuity**: $f(x) = m^{\ast}([a, x] \cap E)$ is continuous.

<div class=note>

Prove that $f(x_2) - f(x_1) \leq |x_2 - x_1|$.

</div>

---

## Additivity of Lebesgue Outer Measure

- **Disjoint Open Sets**: $E_n$ from disjoint open sets $S_n$, then $m^{\ast}(\cup E_n) = \sum m^{\ast}(E_n)$.

<div class=note>

Take open set $U \supset \cup E_n$, $m^{\ast}(\cup E_n) > m(U) - \epsilon$. Define $U_n := U \cap S_n$,
$$ m^{\ast}(\cup E_n) > m(U) - \epsilon = \sum m(U_n) -\epsilon \geq \sum m^{\ast}(E_n) -\epsilon. $$
</div>

- **Non-Zero Distance**: If $d(E_1, E_2) = \inf\{d(x_1,x_2):x_1 \in E_1, x_2 \in E_2\} > 0$, then $m^{\ast}(E_1 \cup E_2) = m^{\ast}(E_1) + m^{\ast}(E_2)$.

<div class=note>

Since distance is non-zero, then we can find disjoint open sets $S_1, S_2$ such that $E_1 \subset S_1$, $E_2 \subset S_2$.

</div>

---

## Limit of Lebesgue Outer Measure


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

## Definition of Lebesgue Measure

---

# A Non-Measurable Set Example

---

# Approximation by Open and Closed Sets

---

## Approximation Results for Measurable Sets

<br>

- **Open Sets**: There exists an open set $G \supset E$ such that $m^{\ast}(G - E) < \epsilon$.
- **Closed Sets**: There exists a closed set $F \subset E$ such that $m^{\ast}(E - F) < \epsilon$.
- **Squeeze Theorem**: If there exists measurable sets $A_n$ and $B_n$ such that $A_n \subset E \subset B_n$ and $\lim \limits _{n \rightarrow \infty} m(B_n - A_n) = 0$, then $E$ is measurable




