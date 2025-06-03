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


---

## Quick Review of Measurable Function

---

## Quick Review of Lebesgue Integral

- **Property**: $f$ is L-integrable, then $f$ is finite a.e. (not versa vice: e.g., $\frac{1}{x}$ on $(0,1)$.)
- **Counterexample**: $f_n = \frac{1}{x}\chi_{[\frac{1}{n}, 1]} \xrightarrow{a.e.} f = \frac{1}{x}$, $f$ not integrable on $[0,1]$.
- $f_n$ are non-negative and measurable, $f_n \xrightarrow{m} f$, then ${\displaystyle \int_E f \mathrm{d} x\leq \liminf_{n \rightarrow \infty} \int_E f_n \mathrm{d} x}$.
- $f_k, g_k$ are measurable, $|f_k| \leq g_k$, $f_k \rightarrow f$ a.e., $g_k \rightarrow g$ a.e., ${\displaystyle \int_E g_k \mathrm{d} x \rightarrow \int_E g \mathrm{d} x}$, then
$$ \int_E f_k \mathrm{d} x \rightarrow \int_E f \mathrm{d} x. $$
- $f \in L(E)$, prove that ${\displaystyle \lim \limits _{k \rightarrow \infty} k \cdot m(\{|f| > k\}) = 0}$.
- Calculate: $\displaystyle \lim \limits _{n \rightarrow \infty} \int_0^1 \frac{nx^n}{1 + x^n}\mathrm{d} x$

---

## Quick Review of Leibniz Formula

- **Basic Concepts**: Monotonic, BV, AC.
- **Monotonic Function**: $f^\prime$ exists a.e., and it is L-integrable.
- **BV Function**: BV can be expressed as sum of monotonic functions. (so $f^{\prime}$ exists a.e., integrable)
- **AC Function**: AC is BV. (so $f^{\prime}$ exists a.e., integrable)
- **Newton-Leibniz**: If $F$ is AC, then ${\displaystyle F(x) = F(a) + \int_a^x F^{\prime}(t)\mathrm{d} t}$.




