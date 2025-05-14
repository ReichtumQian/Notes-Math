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

<br>

- If $\{E_n\}$ is monotonically increasing, then $m^{\ast}(\lim \limits _{n \rightarrow \infty} E_n) = \lim \limits _{n \rightarrow \infty} m^{\ast}(E_n)$.

<div class=note>

If $\lim \limits _{n \rightarrow \infty} m^{\ast}(E_n) = \infty$, then conclusion holds. Take open set $G_n \supset E_n$, $m(G_n) < m^{\ast}(E_n) + \epsilon$.
$$ E_n \subset \cap_{s=n}^{\infty} G_s := P_n \Rightarrow m(P_n) < m^{\ast}(E_n) + \epsilon. $$
$P_n$ is also monotonically increasing, then
$$ m^{\ast}(\lim \limits _{n \rightarrow \infty} E_n) = m^{\ast}(\cup_{n=1}^{\infty}E_n) \leq m(\cup_{n=1}^{\infty}P_n)= \lim \limits _{n \rightarrow \infty} m(P_n) \leq \lim \limits _{n \rightarrow \infty} m^{\ast}(E_n)+\epsilon. $$

</div>

---

# Lebesgue Measure

---

## Key Points of Lebesgue Measure

<br>

- **Measurable Set**: For any $A \subset \mathbb{R}$, $m^{\ast}(A) \geq m^{\ast}(A \cap E) + m^{\ast}(A \cap E^c)$.
- **Countable Sub-Additivity**: $A_n$ are arbitrary, then $m(\cup_n A_n) \leq \sum_n m(A_n)$.
- **Countable Additivity**: $A_n$ are pairwise-disjoint, then $m(\cup_n A_n) = \sum_n m(A_n)$.
- **Corollary**: If $E \subset F$, then $m(F - E) = m(F) - m(E)$.
- **Closure under Operations**: $A^c$, $\cup$, $\cap$, $\limsup$, $\liminf$.

---

## Prove Sets are Measurable

- If $E$ satisfies $m^{\ast}(E) = 0$, then $E$ is measurable, $m(E) = 0$.

<div class=note>

For any $A$, $0 \leq m^{\ast}(A \cap E) \leq m^{\ast}(E) = 0$. Then $m^{\ast}(A) \geq m^{\ast}(A \cap E^c)$ holds.

</div>

- If $A$ is measurable, $A \Delta B$ is measurable, then $B$ is measurable.

<div class=note>

$A \cap B = A - [(A \Delta B) \cap A]$ is measurable, $B = [(A \Delta B) - A] \cup (A \cap B)$ is measurable.

</div>

- $A \subset \mathbb{R}$, if $m^{\ast}(A) = 0$ and $A$ is an open set, then $A = \emptyset$.

<div class=note>

Suppose $A \neq \emptyset$, then there exists $x \in A$ such that $(x-\epsilon, x+\epsilon) \subset A$. Then
$$ m^{\ast}(A) \geq m^{\ast}(x - \epsilon, x + \epsilon) = 2\epsilon > 0. $$

</div>


---

## Limit of Lebesgue Measure

- $E_n$ are measurable, $m(\liminf\limits_{n \rightarrow \infty} E_n) \leq \liminf\limits_{n \rightarrow \infty} m(E_n)$.

<div class=note>

$m(\liminf\limits_{n\rightarrow \infty} E_n) = m(\cup_{n=1}^{\infty}\cap_{k=n}^{\infty}E_k) = \lim\limits_{n \rightarrow \infty} m(\cap_{k=n}^{\infty}E_k)$, and $m(\cap_{k=n}^{\infty} E_k) \leq m(E_n)$.

</div>

- $E_n$ are measurable, $m(\cup_{k=k_0}^{\infty}E_k) < \infty$ for some $k_0$, then $m(\limsup\limits_{n \rightarrow \infty}E_n) \geq \limsup\limits_{n \rightarrow \infty} m(E_n)$.

<div class=note>

$m(\cap_{n=1}^{\infty}\cup_{k=n}^{\infty}E_k)=\lim \limits _{n \rightarrow \infty} m(\cup_{k=n}^{\infty}E_k)$ and $m(\cup_{k=n}^{\infty}E_k) \geq m(E_n)$.
</div>

- If $m(\cup_{k=1}^{\infty}E_k) < \infty$ and $\lim \limits _{n \rightarrow \infty} E_n$ exists, then $m(\lim \limits _{n \rightarrow \infty} E_n) = \lim \limits _{n \rightarrow \infty} m(E_n)$.

<div class=note>

By two previous statements.

</div>

---

# A Non-Measurable Set Example

---

# Approximation by Open and Closed Sets

---

## Approximation Results for Measurable Sets

- **Open Sets**: There exists an open set $G \supset E$ such that $m(G - E) < \epsilon$.

<div class=note>

$m(E) < \infty$: Take open intervals $I_n$, $E \subset \cup I_n$, $m(E) > \sum \ell(I_n) - \epsilon$. Take $G = \cup I_n$.
$m(E) = \infty$: Take $E_n = E \cap [n, n+1)$ where $n \in \mathbb{Z}$. For each $E_n$ take $G_n = \cup_k I_n^{(k)}$, where $E_n \subset \cup_k I_n^{(k)}$ and $m(G_n - E_n) < \frac{\epsilon}{2^n}$. Take $G = \cup_n G_n$.
</div>

- **Closed Sets**: There exists a closed set $F \subset E$ such that $m(E - F) < \epsilon$.
- **Squeeze Theorem**: If there exists measurable sets $A_n$ and $B_n$ such that $A_n \subset E \subset B_n$ and $\lim \limits _{n \rightarrow \infty} m(B_n - A_n) = 0$, then $E$ is measurable

---

## Applications of Approximation Results

- $E \subset \mathbb{R}$, $m(E) > 0$, $0 < \alpha < 1$. Prove there exists an open interval $I$, $m(I \cap E) > \alpha \cdot m(I)$.

<div class=note>

(1) There exists an open set $G$ such that $G \supset E$ and $m(G - E) < \frac{1 - \alpha}{\alpha} m(E)$. Then
$$ m(G) = m(G-E) + m(E) < \frac{1}{\alpha} m(E) \Rightarrow \alpha m(G) < m(E). $$
(2) Since $G \subset \mathbb{R}$, then $G = \cup_n (a_n, b_n)$ where $(a_i, b_i)$ are disjoint. Then
$$ m(E) = m(E \cap G) = m(\cup_n (E \cap (a_n, b_n))) = \sum_n m(E \cap (a_n, b_n)),  $$
Since $m(E) > \alpha m(G) = \alpha \sum_n m(a_n, b_n)$. This means there must there exists $i$ such that $m(E \cap (a_i, b_i)) > \alpha m(a_i, b_i)$.

</div>

