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

# Measurable Functions

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Concept of Measurable Function
- Approximation by Simple and Continuous Functions
- Convergence Results in Measure Theory

---

# Concept of Measurable Function

---

## Definition of Measurable Function

- **Measurable Function**: $\{f > a\}$, $\{f \geq a\}$, $\{f = a\}$ etc. are measurable.
- **Equivalent Definition**: For any $r \in \mathbb{Q}$, $\{f > r\}$ is measurable.

<div class=note>

For any $a \in \mathbb{R}$, $\lim \limits _{n \rightarrow \infty} r_n = a$, then $\{f > a\} = \cap_{n=1}^{\infty} \{f > r_n\}$.
</div>

- **Limit form**: If $\{f > a + \frac{1}{n}\}$ is measurable ($n \neq 0$), then $\{f > a\}$, $\{f \geq a\}$ are measurable.

<div class=note>

$$\{f > a\} = \cup _{n=1}^{\infty} \{f > a + \frac{1}{n}\}, \quad
\{f \geq a\} = \cap _{n=1}^{\infty} \{f > a - \frac{1}{n}\}.
$$

</div>

- **Right Continuity of $m(\{f > a\})$)**: $\lim \limits _{n \rightarrow \infty} m(\{f > a + \frac{1}{n}\}) = m(\{f > a\})$.

<div class=note>

Note: if $\lim \limits _{n \rightarrow \infty} E_n$ exists and finite-measure, then $\lim \limits _{n \rightarrow \infty} m(E_n) = m(\lim \limits _{n \rightarrow \infty} E_n)$. (See Chapter2)
</div>

---

## Properties of Measurable Functions


- **Boundedness**: $f$ is basically bounded; $\{f_n\}$ are basically uniformly bounded.
- **Preimage of Measurable Functions**: For any open set $G$ or closed set $F$, $f^{-1}(G)$ and $f^{-1}(F)$ are measurable.

<div class=note>

$G = \cup_{k=1}^{\infty}(a_k, b_k)$, $f^{-1}(G) = \cup_{k=1}^{\infty}\{x: a_k < f(x) < b_k\}$ is measurable. $F = (F^c)^c$.

</div>

- **Closure under Operations**: $\pm$, $\times$, $/$, $\sup$, $\inf$, $\limsup$, $\liminf$.
- **Closure under Composition**: $f$ is continuous, $g$ is finite measurable, $f(g)$ is measurable.

<div class=note>

Since continuity, $G := f^{-1}(a, +\infty)$ is an open set in $\mathbb{R}$. $G = \cup_{k=1}^{\infty}(a_k,b_k)$, $g^{-1}(a_k,b_k)$ is measurable, then $g^{-1}(G)$ is measurable, and
$$ \{f(g(x)) > a\} = \{g(x) \in G\} = g^{-1}(G) \cap E \quad \text{is measurable.} $$
</div>

---

## Sequence of Measurable Functions

- **Convergent Set of Measurable Functions**: $f_n(x)$ are measurable on measurable set $D$, prove that the set that $f_n(x)$ is point-wise convergent is measurable.

<div class=note>

Fix $x$, Cauchy's convergence criterion says
$$ \forall k \in \mathbb{Z}^+, \exists N \in \mathbb{Z}^+, \forall m, n > N, \quad |f_n(x) - f_m(x)| < \frac{1}{k}. $$
Then the convergent point set is
$$ \cap_{k\geq 1} \cup_{N\geq 1} \cap_{m,n \geq N} \{|f_n - f_m| < \frac{1}{k}\}. $$
Since $f_n, f_m$ are measurable, then $\{|f_n - f_m| < \frac{1}{k}\}$ is measurable.
</div>


---

# Approximation by Simple and Continuous Functions

---

## Approximation by Simple Functions

- **By Simple Functions**: $\lim \limits _{n \rightarrow \infty} f_n(x) = f(x)$, $x \in E$. (1) Monotonically if $f \geq 0$; (2) Uniformly if $f$ is bounded.

<div class=note>

$$
f_n(x) =
\begin{cases}
  n & \text{if } f(x) \geq n;\\
  \frac{k-1}{2^n} & \text{if } \frac{k-1}{2^n} \leq f(x) < \frac{k}{2^n},\\
                    &k = -n2^n+1, \cdots, n2^n\\
  -n &  \text{if } f(x) < -n.
\end{cases}
$$

</div>

---

## Approximation by Continuous Functions

- **By Continuous Functions (Lusin)**: $f$ finite a.e. and measurable. Then it is basically continuous on finite measure set.

$$ \forall \epsilon > 0, \exists f^{\ast} \in C(D), \quad m(\{f \neq f^{\ast}\}) < \epsilon. $$

- **By Continuous Function Sequences**: $f$ finite a.e. and measurable on $[a, b]$. Then there exists $g_n \in C([a,b])$, $g_n \xrightarrow{a.e.} f$.

<div class=note>

By Lusin, there exists $f_n$ such that $m(\{f \neq f_n\}) < \frac{1}{n}$, then $f_n \xrightarrow{m} f$. Riesz implies $f_{n_k} \xrightarrow{a.e.} f$.

</div>

- **Counterexample**: $f = \chi_{\mathbb{Q} \cap [0, 1]}$ is finite a.e. and measurable on $[0, 1]$. But $\nexists  g \in C([a, b])$ such that $f = g$ a.e.


---

# Convergence Results in Measure Theory

---

## Pointwise Convergence and Uniform Convergence

- **Pointwise to Uniform (Egoroff)**: $f, f_n$ finite a.e. and measurable, $m(D) < \infty$. Then $f_n \xrightarrow{a.e.} f$ implies $f_n \rightrightarrows f$ basically on a closed subset $F$.
$$ \forall \epsilon > 0, \exists F \subset D, m(D - F) < \epsilon, \quad f_n(x) \rightrightarrows f(x), x \in F. $$
- **Uniform to Pointwise**: $f_n$ measurable, $m(D)$ is arbitrary. Then $f_n$ basically uniformly converges to $f$ implies $f_n \xrightarrow{a.e.} f$.

<div class=note>

(1) $\forall \delta > 0$, $\exists E_{\delta} \subset E$, $m(E - E_{\delta}) < \delta$ where $f_n \rightrightarrows f$. (2) Define $E_0 = \{f_n \not \rightrightarrows f\}$, $E_0 \subset E - E_{\delta}$ for any $\delta > 0$. Then $m(E_0) \leq m(E - E_{\delta}) < \delta$, $m(E_0) = 0$ and $f_n \xrightarrow{a.e.} f$.

</div>

---

## Convergence in Measure

<br>

- **Convergence in Measure**: $f, f_n$ measurable and finite a.e.
$$ \forall \delta > 0, \lim \limits _{n \rightarrow \infty} m(\{|f_n - f| \geq \delta\}) = 0. $$
- **Measure to Pointwise (Riesz)**: $f, f_n$ measurable and finite a.e. Then
$$ f_n \xrightarrow{m} f \quad \Rightarrow \quad  \exists \{f_{n_k}\}, f_{n_k} \xrightarrow{a.e.} f. $$
- **Pointwise to Measure (Lebesgue)**: $f_n,f$ measurable and finite a.e. $m(D) < \infty$. Then
$$ f_n \xrightarrow{a.e.} f \quad \Rightarrow \quad f_n \xrightarrow{m} f. $$

---

## Generalized Riesz Theorem

- **Generalized Riesz**: $f_n, f$ measurable and finite a.e. $m(D) < \infty$. Then $f_n \xrightarrow{m} f$ iff $\forall \{f_{n_i}\} \subset \{f_n\}$, there exists $\{f_{n_{ij}}\} \subset \{f_{n_i}\}$, $f_{n_{ij}} \xrightarrow{a.e.} f$.

<div class=note>

(1) $\Rightarrow$: By Riesz theorem. (2) $\Leftarrow$: Assume $f_n \not \xrightarrow{m} f$, then
$$ \exists \epsilon > 0, \exists \delta > 0, \forall N > 0, \exists n > N, \quad m(\{|f_n - f| > \delta\}) > \epsilon. $$
There exists $\{f_{n_i}\}$ such that $m(\{|f_{n_i} - f| > \delta\}) > \epsilon$, which contradicts $f_{n_{ij}} \xrightarrow{a.e.} f$.
</div>

- **Counterexample**: Why inverse of Riesz theorem is wrong?

<div class=note>

Take $f_n(x) = \chi_{[a_n,b_n]}(x)$ where $b_n - a_n = \frac{1}{2}$ and slide over $[0, 1]$. Define $f \equiv 0$, then
- $f_n \not \xrightarrow{m} f$: $m(\{|f_n(x)| \geq \epsilon\}) = \frac{1}{2}$.
- $f_{n_k} \xrightarrow{a.e.} f$: Since the interval keep sliding, then we can find such a subsequence.

</div>


---

## Properties of Convergence in Measure

- **Addition and Substraction**: If $f_k \xrightarrow{m} f$ and $g_k \xrightarrow{m} g$, then $f_k \pm g_k \xrightarrow{m} f_k \pm g_k$.

<div class=note>

$\{|(f_k+g_k) - (f+g)| > \epsilon\} \subset \{|f_k-f| + |g_k-g| > \epsilon\} \subset \{|f_k - f| > \frac{\epsilon}{2}\} \cup \{|g_k - g| > \frac{\epsilon}{2}\}$.
Define $A = \{|f_k-f| > \frac{\epsilon}{2}\}$, $B = \{|g_k-g| > \frac{\epsilon}{2}\}$, then $m(A \cup B) \leq m(A) + m(B) \rightarrow 0$.

</div>

- **Absolute Value and Extreme**: (1) $|f_k| \xrightarrow{m} |f|$ (2) $\min\{f_k, g_k\} \xrightarrow{m} \min\{f, g\}$
- **Multiplication**: $f_k \xrightarrow{m} f$ and $g_k \xrightarrow{m} g$, $m(D) < \infty$ then $f_k g_k \xrightarrow{m} fg$.

<div class=note>

By generalized Riesz, 

</div>

- **Composition**: If $f_k \xrightarrow{m} f$ on $[a, b]$, $g$ is continuous, then $g \circ f_k \xrightarrow{m} g \circ f$.


