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

By Lusion, there exists $f_k$ such that $m(\{f \neq f_k\}) < \frac{1}{k}$.

</div>


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

## Convergence in Measure and Pointwise Convergence

- **Convergence in Measure**: $f, f_n$ measurable and finite a.e.
$$ \forall \delta > 0, \lim \limits _{n \rightarrow \infty} m(\{|f_n - f| \geq \delta\}) = 0. $$

- **Measure to Pointwise (Riesz)**: There exists a subsequence.
- **Pointwise to Measure (Lebesgue)**: On finite measure set.


