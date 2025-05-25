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

# Lebesgue Outer Measure

---

## Concept and Properties of Lebesgue Outer Measure

- **Definition**: $m^{\ast}(E) = \inf_{\{I_n\}} \left\{ \sum \ell(I_n) \right\}$ where $E \subset \cup_n I_n$.
- **Countable Sub-Additivity**: $m^{\ast}(\cup E_n) \leq \sum m^{\ast}(E_n)$.

<div class=note>

Why? Because the open intervals covering $\cup E_n$ maybe more compact than seperately.

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

- If $\{E_n\}$ is monotonically increasing, then $m^{\ast}(\lim \limits _{n \rightarrow \infty} E_n) = \lim \limits _{n \rightarrow \infty} m^{\ast}(E_n)$.

<div class=note>

(1) If $\lim \limits _{n \rightarrow \infty} m^{\ast}(E_n) = \infty$, then conclusion holds. So we only consider $m^{\ast}(E_n) \not \rightarrow \infty$.
(2) Take open set $G_n \supset E_n$, $m(G_n) < m^{\ast}(E_n) + \epsilon$. But $\lim \limits _{n \rightarrow \infty} G_n$ may not exist, so take $P_n = \cap_{k=n}^{\infty}G_k$, $P_n \nearrow$ and $E_n \subset P_n \subset G_n$. Then
$$ m^{\ast}(\cup_{n=1}^{\infty}E_n) \leq m(\cup_{n=1}^{\infty}P_n) = \lim \limits _{n \rightarrow \infty} m(P_n) \leq \lim \limits _{n \rightarrow \infty} m^{\ast}(E_n) + \epsilon. $$
(3) $\lim \limits _{n \rightarrow \infty} E_n = \cup_{n=1}^{\infty}E_n$, $m^{\ast}(\cup_{n=1}^{\infty}E_n) \geq m^{\ast}(E_n)$, so $m^{\ast}(\lim \limits _{n \rightarrow \infty} E_n) \geq \lim \limits _{n \rightarrow \infty} m^{\ast}(E_n)$.

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

- $E_n \nearrow$ (or $m(E_n) < \infty$ and $E_n \searrow$), then $m(\lim \limits _{n \rightarrow \infty} E_n) = \lim \limits _{n \rightarrow \infty} m(E_n)$

<div class=note>

Let $D_1 = E_1$, $D_n = E_n - E_{n-1}$ for $n \geq 2$. So $m(\lim E_n) = m(\cup D_n) = \sum m(D_n) = \lim m(E_n)$.

</div>

- $E_n$ are measurable, $m(\liminf\limits_{n \rightarrow \infty} E_n) \leq \liminf\limits_{n \rightarrow \infty} m(E_n)$.

<div class=note>

$m(\liminf\limits_{n\rightarrow \infty} E_n) = m(\cup_{n=1}^{\infty}\cap_{k=n}^{\infty}E_k) = \lim\limits_{n \rightarrow \infty} m(\cap_{k=n}^{\infty}E_k)$, and $m(\cap_{k=n}^{\infty} E_k) \leq m(E_n)$.

</div>

- $E_n$ are measurable, $m(\cup_{k=k_0}^{\infty}E_k) < \infty$ for some $k_0$, then $m(\limsup\limits_{n \rightarrow \infty}E_n) \geq \limsup\limits_{n \rightarrow \infty} m(E_n)$.

<div class=note>

$m(\cap_{n=1}^{\infty}\cup_{k=n}^{\infty}E_k)=\lim \limits _{n \rightarrow \infty} m(\cup_{k=n}^{\infty}E_k)$ and $m(\cup_{k=n}^{\infty}E_k) \geq m(E_n)$.
</div>

- **Conclusion**: If $m(\cup_{k=1}^{\infty}E_k) < \infty$ and $\lim \limits _{n \rightarrow \infty} E_n$ exists, then $m(\lim \limits _{n \rightarrow \infty} E_n) = \lim \limits _{n \rightarrow \infty} m(E_n)$.

---

## Operations on Measurable Sets

- If $E_1, E_2$ are measurable, prove that $m(E_1) + m(E_2) = m(E_1 \cup E_2) + m(E_1 \cap E_2)$.

<div class=note>

(1) $E_2$ is measurable, $m(E_1) = m(E_1 \cap E_2^c) + m(E_1 \cap E_2) = m(E_1 - E_2) + m(E_1 \cap E_2)$.
(2) $E_1$ is measurable, $m(E_2) = m(E_2 - E_1) + m(E_1 \cap E_2)$.
(3) Similarly, $m(E_1 \cup E_2) = m(E_1-E_2) + m(E_2-E_1) + m(E_1 \cap E_2)$.

</div>

- If $\{E_k\}_{1\leq k \leq n}$ ($E_k \subset [0,1]$) are measurable , $\sum_{k=1}^n m(E_k) > n-1$. Prove $m(\cap_{k=1}^n E_k) > 0$.

<div class=note>

(1) $I = [0, 1]$, then $m(I - \cap_{k=1}^n E_k) = m(\cup_{k=1}^n (I - E_k)) \leq \sum\limits_{k = 1}^n m(I-E_k) = n - \sum\limits_{k = 1}^n m(E_k)$
(2) Since $m(I - \cap_{k=1}^n E_k) = 1 - m(\cap_{k=1}^n E_k)$. Then $m(\cap_{k=1}^nE_k) > 1 - n + (n-1) = 0$.

</div>

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

(1) Assume for all open intervals $I$, $m(I \cap E) \leq \alpha \cdot m(I)$.
(2) There exists $G = \cup_n I_n$ such that $E \subset G$ and $m(G - E) < \epsilon$. Then $m(G) < m(E) + \epsilon$.
(3) Then $m(E) = m(E \cap G) = m(E \cap (\cup_n I_n)) = \sum_n m(E \cap I_n) \leq \alpha m(G) < \alpha m(E) + \alpha \epsilon$.

</div>

- $E$ measurable, $\exists \alpha \in (\frac{1}{2}, 1)$, for all $I \subset \mathbb{R}$ $m(E \cap I) \leq \alpha m(I)$. Prove $m(E) = 0$.

<div class=note>

Almost the same as the previous one.

</div>


