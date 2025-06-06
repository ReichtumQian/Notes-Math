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

# Final Review: Real Analysis
Speaker: Yixiao Qian

---

## Quick Review of Lebesgue Measure

- **Disjoint Open Sets**: $E_n$ from disjoint open sets $S_n$, then $m^{\ast}(\cup E_n) = \sum m^{\ast}(E_n)$.
- If $\{E_n\}$ is monotonically increasing, then $m^{\ast}(\lim \limits _{n \rightarrow \infty} E_n) = \lim \limits _{n \rightarrow \infty} m^{\ast}(E_n)$.
- $E_n \nearrow$ (or $m(E_n) < \infty$ and $E_n \searrow$), then $m(\lim \limits _{n \rightarrow \infty} E_n) = \lim \limits _{n \rightarrow \infty} m(E_n)$
- $E_n$ are measurable, $m(\liminf\limits_{n \rightarrow \infty} E_n) \leq \liminf\limits_{n \rightarrow \infty} m(E_n)$.
- $E_n$ are measurable, $m(\cup_{k=k_0}^{\infty}E_k) < \infty$ for some $k_0$, then $m(\limsup\limits_{n \rightarrow \infty}E_n) \geq \limsup\limits_{n \rightarrow \infty} m(E_n)$.
- If $\{E_k\}_{1\leq k \leq n}$ ($E_k \subset [0,1]$) are measurable , $\sum_{k=1}^n m(E_k) > n-1$. Prove $m(\cap_{k=1}^n E_k) > 0$.
- If for any $\epsilon > 0$, there exists open set $G \supset E$ such that $m^{\ast}(G - E) < \epsilon$. Prove that $E$ is measurable.
- $E \subset \mathbb{R}$, $m(E) > 0$, $0 < \alpha < 1$. Prove there exists an open interval $I$, $m(I \cap E) > \alpha \cdot m(I)$.


---

## Quick Review of Measurable Function

- **Closure under Composition**: $f$ is continuous, $g$ is finite measurable, $f(g)$ is measurable.
- If $f_n \xrightarrow{a.e.} f$, $f_n$ are measurable. Prove that $f$ is measurable.
- **Convergent Set of Measurable Functions**: $f_n(x)$ are measurable on measurable set $D$, prove that the set that $f_n(x)$ is point-wise convergent is measurable.
- **By Continuous Function Sequences**: $f$ finite a.e. and measurable on $[a, b]$. Then there exists $g_n \in C([a,b])$, $g_n \xrightarrow{a.e.} f$.
- **Uniform to Pointwise**: $f_n$ measurable, $m(D)$ is arbitrary. Then $f_n \xrightarrow{a.u.} f$ implies $f_n \xrightarrow{a.e.} f$.
- **Uniform to Measure**: If $f_n \xrightarrow{a.u.} f$, then $f_n \xrightarrow{m} f$.
- **Generalized Riesz**: $f_n, f$ measurable and finite a.e. $m(D) < \infty$. Then $f_n \xrightarrow{m} f$ iff $\forall \{f_{n_i}\} \subset \{f_n\}$, there exists $\{f_{n_{ij}}\} \subset \{f_{n_i}\}$, $f_{n_{ij}} \xrightarrow{a.e.} f$.
- **Multiplication**: $f_n \xrightarrow{m} f$ and $g_k \xrightarrow{m} g$, $m(D) < \infty$ then $f_n g_n \xrightarrow{m} fg$.

---

## Quick Review of Lebesgue Integral

- **Property**: $f$ is L-integrable, then $f$ is finite a.e. (not versa vice: e.g., $\frac{1}{x}$ on $(0,1)$.)
- **Counterexample**: $f_n = \frac{1}{x}\chi_{[\frac{1}{n}, 1]} \xrightarrow{a.e.} f = \frac{1}{x}$, $f$ not integrable on $[0,1]$.
- $f_n$ are non-negative and measurable, $f_n \xrightarrow{m} f$, then ${\displaystyle \int_E f \mathrm{d} x\leq \liminf_{n \rightarrow \infty} \int_E f_n \mathrm{d} x}$.
- $f_k, g_k$ are measurable, $|f_k| \leq g_k$, $f_k \rightarrow f$ a.e., $g_k \rightarrow g$ a.e., ${\displaystyle \int_E g_k \mathrm{d} x \rightarrow \int_E g \mathrm{d} x}$, then
$$ \int_E f_k \mathrm{d} x \rightarrow \int_E f \mathrm{d} x. $$
- $f \in L(E)$, prove that ${\displaystyle \lim \limits _{k \rightarrow \infty} k \cdot m(\{|f| > k\}) = 0}$.
- Calculate: $\displaystyle \lim \limits _{n \rightarrow \infty} \int_0^1 \frac{nx^n}{1 + x^n}\mathrm{d} x$
- Suppose $E \subset \mathbb{R}^n$ is measurable, $f:E \rightarrow \mathbb{R}$ is non-negative and measurable, prove that
$$ \int_E f \mathrm{d} x = \int_0^{\infty} m(\{x \in E: f(x) > t\}) \mathrm{d} t. $$

---

## Quick Review of Leibniz Formula

- **Basic Concepts**: Monotonic, BV, AC.
- **Monotonic Function**: $f^\prime$ exists a.e., and it is L-integrable.
- **BV Function**: BV can be expressed as sum of monotonic functions. (so $f^{\prime}$ exists a.e., integrable)
- **AC Function**: AC is BV. (so $f^{\prime}$ exists a.e., integrable)
- **Newton-Leibniz**: If $F$ is AC, then ${\displaystyle F(x) = F(a) + \int_a^x F^{\prime}(t)\mathrm{d} t}$.




