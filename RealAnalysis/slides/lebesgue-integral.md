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

# Lebesgue Integrals

Speaker: Yixiao Qian

---

# Table of Contents

<br>

- Concept of Lebesgue Integral
- Properties of Lebesgue Integral
- Riemann Integral and Lebesgue Integral
- Multiple Integrals and Iterated Integrals

---

# Concept of Lebesgue Integral

---

## Definition of Lebesgue Integral

- **Characteristic Function**: $\chi_E(x) = 1$ for $x \in E$ and $\chi_E(x) = 0$ for $x \not \in E$.
- **Integral of Non-Negative Simple Function**: $\displaystyle \int_D f \mathrm{d} x = \sum\limits_{i = 1}^s a_i m(E_i)$.
- **Integral of Non-Negative Measurable Function**: $\displaystyle \int_D f \mathrm{d} x = \lim \limits _{n \rightarrow \infty} \int_D f_n\mathrm{d}x$.
- **Integral of Measurable Function**: ${\displaystyle \int_D f \mathrm{d} x = \int_D f_+ \mathrm{d} x - \int_D f_- \mathrm{d} x}$, where
$$ f_+ := \max\{0, f(x)\}, \quad f_-(x) := \max\{0, -f(x)\}. $$
- **Integrability**: $f$ is integrable (written $f \in L(E)$) if ${\displaystyle \int_E f \mathrm{d} x < \infty}$.

---

## Properties of Lebesgue Integrable Functions

- **Closure under Operations**: $\lambda f$, $f \pm g$, $fg$.
- **Almost-Everywhere Finite**: $f \in L(E)$ then $f$ is finite a.e.
- **Condition for Integrability**: Almost-everywhere bounded on finite-measure $E$. Note that finite a.e. is not enough.

<div class=note>

Example: $f = 1$ is not integrable on $(0, +\infty)$. $f = \frac{1}{x}$ is not integrable on $(0, 1)$.

</div>


---

## Approximation with respect to Integral

Let $f \in L([a, b])$, for any $\epsilon > 0$, there exists $g(x)$ such that

$$ \int_a^b |f(x) - g(x)| \mathrm{d} x < \epsilon. $$

- **Measurable and Bounded**

$$ g(x) =
\begin{cases}
  f(x) & |f(x)| \leq M;\\
  M \cdot \operatorname{sgn}(f(x)) & |f(x)| > M.
\end{cases}$$

$$ \int_a^b |f - g|\mathrm{d} x \leq \int_{\{|f| > M\}} (|f| + M) \mathrm{d} x < \epsilon. $$

---

## Approximation with respect to Integral

- **Continuous**: Since $g$ is bounded, by Lusin theorem, there exists $h(x) \in C(a, b)$ such that $m(g \neq h) < \epsilon$. 

$$ \int_a^b |f-h|\mathrm{d} x \leq \int_a^b|f-g|\mathrm{d} x+\int_a^b|g-h|\mathrm{d}x \leq 2\epsilon.$$

- **Polynomial**: There exists $P_n(x) \rightrightarrows h(x)$, then $\displaystyle \int_a^b P_n(x)\mathrm{d} x \rightarrow \int_a^b h(x)\mathrm{d} x$. There exists $N > 0$, such that $n > N$,

$$ \int_a^b |f - P_n| \mathrm{d} x \leq \int_a^b |f-h|\mathrm{d} x + \int_a^b |h-P_n|\mathrm{d} x \leq 3 \epsilon.$$

- **Step Function**: $P_n(x) \in R([a, b])$, then for any $\epsilon > 0$, there exists partition $T$ such that ${\displaystyle \left| \int_a^b P_n(x) - \varphi(x)\mathrm{d} x \right| < \epsilon}$, where $\varphi(x)$ takes $\sup P_n(x)$ in each sub-interval.

---

## What Happens When the Integral is Zero

<div class=trick>

For any $\sigma \in \mathbb{R}$, we have $\displaystyle \int_E f \mathrm{d} x \geq \int_{\{f \geq \sigma\}}f\mathrm{d} x \geq \sigma m(\{f \geq \sigma\})$.
</div>

- $f$ is non-negative, ${\displaystyle \int_E f \mathrm{d} x = 0}$, then $f = 0$ a.e.

<div class=note>

Let $E_n = \{f \geq \frac{1}{n}\}$, and $\displaystyle \int_E f \mathrm{d} x \geq \int_{E_n} f \mathrm{d} x \geq \frac{1}{n}m(E_n)$. Then $m(\{f \neq 0\}) \leq \sum m(E_n) = 0$.
</div>

- $f_n$ are non-negative, ${\displaystyle \lim \limits _{n \rightarrow \infty} \int_E f_n \mathrm{d} x = 0}$, then $f_n \xrightarrow{m} 0$.

<div class=note>

Fix $n$, let $E_{\sigma} = \{f_n \geq \sigma\}$, ${\displaystyle \int_E f_n\mathrm{d} x \geq \int_{E_{\sigma}} f_n\mathrm{d} x \geq \sigma m(E_{\sigma})}$. Then $m(E_{\sigma}) \rightarrow 0$ when $n \rightarrow \infty$.
</div>

---

## What Happens When the Integral is Zero

- $f \in L(\mathbb{R})$, for any open set $G \subset \mathbb{R}$, ${\displaystyle \int_G f\mathrm{d} x = 0}$, then $f(x) = 0$ a.e.

<div class=note>

Since $\displaystyle \frac{1}{h}\int_x^{x+h} f(t)\mathrm{d} t \rightarrow f(x)$ a.e. (Lebesgue differentiation theorem). Then $f = 0$ a.e.

</div>

- $f \in L(E)$, for any measurable $\varphi(x)$, ${\displaystyle \int_E f(x)\varphi(x) \mathrm{d} x = 0}$, then $f(x) = 0$ a.e.

<div class=note>

Let $E_n = \{f \geq \frac{1}{n}\}$ and $\varphi(x) = \chi_{E_n}(x)$. Then $\displaystyle \int_E f(x)\varphi(x)\mathrm{d} x = \int_{E_n}f \mathrm{d} x \geq \frac{1}{n}m(E_n)$.

</div>

- $f \in L([a,b])$, for any $k \in \mathbb{Z}^+$, ${\displaystyle \int_a^b x^k f(x) \mathrm{d} x = 0}$, then $f(x) = 0$ a.e.

---

## Closure under Operations

<br>

- $f \in L(\mathbb{R})$, $f(0) = 0$, $f^{\prime}(0)$ is finite, prove that $\displaystyle \frac{f(x)}{x} \in L(\mathbb{R})$.

<div class=note>

When $|x| < \delta$, ${\displaystyle \left| \frac{f(x)}{x} - A \right| < \epsilon}$. When $|x| > \delta$, both $f$ and $\frac{1}{x}$ are integrable.
</div>

---

# Key Results of Lebesgue Integral

---

## Key Results of Lebesgue Integral

- **Absolute Continuity**: $\forall \epsilon > 0$, $\exists \delta > 0$, $\exists A$, $m(A) < \delta$, ${\displaystyle \left| \int_A f \mathrm{d} x \right| < \epsilon}$.
- **Levi's Monotone Convergence Theorem** (MCT): $f, f_n$ are non-negative measurable, $f_n(x) \xrightarrow{a.e.} f(x)$ non-decreasingly for any $x \in D$, then ${\displaystyle \int_D f(x)\mathrm{d} x = \lim \limits _{n \rightarrow \infty} \int_D f_n\mathrm{d} x}$.
- **Fatou's Theorem**: $f_n$ are non-negative measurable, then ${\displaystyle \int_D \liminf_{n \rightarrow \infty} f_n\mathrm{d} x \leq \liminf_{n \rightarrow \infty} \int_D f_n\mathrm{d} x}$
- **LDCT**: $f$ and $f_n$ are measurable, $f_n \xrightarrow{a.e.} f$, $\exists g \in L(D)$, $|f_n| \leq g$ a.e., then $f,f_n \in L(D)$ and
$$ \lim \limits _{n \rightarrow \infty} \int_D f_n\mathrm{d} x = \int_D f \mathrm{d} x. $$
- **Counterexample**: $f_n = \frac{1}{x}\chi_{[\frac{1}{n}, 1]}$, $f_n \xrightarrow{a.e.} f = \frac{1}{x}$. Then $f_n \in L([0, 1])$ but $f \not \in L([0,1])$.

---

## Applications of Absolute Continuity

- Let $E$ be a measurable set, $f \in L(E)$, $e_n := \{|f| \geq n\}$. Prove that $\lim \limits _{n \rightarrow \infty} n \cdot m(e_n) = 0$.

<div class=note>

(1) $f$ is finite a.e., then $m(e_n) \rightarrow 0$. That is, $\forall \epsilon > 0$, $\exists N > 0$, $\forall n > N$, $m(e_n) < \delta$.
(2) By absolute continuity, for $\forall \epsilon > 0$, $\exists \delta > 0$, if $m(e_n) < \delta$, ${\displaystyle \int_{e_n} f \mathrm{d} x} < \epsilon$. Then
$$\epsilon > \int_{e_n} f \mathrm{d} x \geq n \cdot m(e_n). $$

</div>

---

## Generalizations of Levi's MCT

- $f, f_n$ are non-nagative measurable, $f_n \xrightarrow{m} f$ non-decreasingly for any $x \in D$. Prove that
$$ \int_D f \mathrm{d} x = \lim \limits _{n \rightarrow \infty} \int_D f_n \mathrm{d} x. $$

<div class=note>

(1) Since $f_n$ is non-decreasing, it converges to a function $g$ (maybe infinity). By MCT,
$$ \int_D g \mathrm{d} x = \lim \limits _{n \rightarrow \infty} \int_D f_n \mathrm{d} x. $$
(2) By Riesz, there exists $f_{n_k} \xrightarrow{a.e.} f$. Since $f_{n_k} \rightarrow g$, then $f = g$ a.e. This means
$$ \int_D f \mathrm{d} x = \int_D g \mathrm{d} x. $$

</div>

---

## Generalizations of Fatou's Theorem

- $f_n$ are non-negative and measurable, $f_n \xrightarrow{m} f$, then ${\displaystyle \int_E f \mathrm{d} x\leq \liminf_{n \rightarrow \infty} \int_E f_n \mathrm{d} x}$.

<div class=note>

By Riesz, $f_{n_k} \xrightarrow{a.e.} f$. Then ${\displaystyle \int_E f \mathrm{d} x \leq \liminf \int_E f_{n_k} \mathrm{d} x \leq \liminf \int_E f_n \mathrm{d} x}$.
</div>

- $f_n$ are measurable, $f$ is non-negative and measurable, $|f_n| \leq f$ a.e., then
$$\int_E \liminf_{n \rightarrow \infty} f_n \mathrm{d} x \leq \liminf_{n \rightarrow \infty} \int_E f_n \mathrm{d} x.$$

<div class=note>

$g_n = f + f_n$ is non-negative and measurable. Applying Fatou to $g_n$ yields the conclusion.
</div>

---

## Generalizations of Fatou's Theorem

- $f_k, g_k$ are measurable, $|f_k| \leq g_k$, $f_k \rightarrow f$ a.e., $g_k \rightarrow g$ a.e., ${\displaystyle \int_E g_k \mathrm{d} x \rightarrow \int_E g \mathrm{d} x}$, then
$$ \int_E f_k \mathrm{d} x \rightarrow \int_E f \mathrm{d} x. $$

<div class=note>

(1) $g_k \pm f_k$ are non-negative, $g_k \pm f_k \rightarrow g \pm f$ a.e.
(2) By Fatou, ${\displaystyle \liminf \int_E (g_k \pm f_k)\mathrm{d} x \geq \int_E (g \pm f) \mathrm{d} x}$, i.e.,
$$ \liminf \int_E g_k \mathrm{d} x + \liminf \int_E f_k \mathrm{d} x \geq \int_E (g+f)\mathrm{d} x $$
$$ \liminf \int_E g_k \mathrm{d} x - \limsup \int_E f_k \mathrm{d} x \geq \int_E (g-f)\mathrm{d} x $$
(3) ${\displaystyle \int_E f \mathrm{d} x \leq \liminf \int_E f_k \mathrm{d} x \leq \limsup \int_E f_k \mathrm{d} x \leq \int_E f \mathrm{d} x}$.
</div>

---

## Use LDCT to Calculate Integral Limits

- Calculate ${\displaystyle \lim \limits _{k \rightarrow \infty} \int_0^{+\infty} e^{-x^k}}\mathrm{d} x$.

<div class=note>

(1) First calculate the limit function, denote $f_k(x) = e^{-x^k}$, then
$$f_k(x) \rightarrow f(x) =
\begin{cases}
  1 & x \in [0,1),\\
  e^{-1} & x = 1,\\
  0 & x > 1.
\end{cases}
\Rightarrow
f_k(x) \xrightarrow{a.e.}
f(x) =
\begin{cases}
  1 & x \in [0, 1],\\
  0 & x > 1.
\end{cases}$$

(2) Find the control function. When $x \in [0, 1]$, $e^{-x^k} \leq 1$, when $x > 1$, $e^{-x^k} \leq e^{-x}$. Take
$$ g(x) =
\begin{cases}
  1 & x \in [0, 1],\\
  e^{-x} & x > 1.
\end{cases}$$

(3) Apply LDCT, ${\displaystyle \lim \limits _{k \rightarrow \infty} \int_0^{+\infty} e^{-x^k}\mathrm{d} x = \int_0^{+\infty} \lim \limits _{k \rightarrow \infty} e^{-x^k}\mathrm{d} x}$, then
$$ \int_0^{+\infty} f \mathrm{d} x = \int_0^1 1 \mathrm{d} x + \int_1^{+\infty} 0 \mathrm{d} x = 1. $$

</div>

---

## Use LDCT to Calculate Integral Limits

- Calculate ${\displaystyle \lim \limits _{n \rightarrow \infty} \int_0^{\infty} \frac{\sin(x/n)}{x(1+x)}\mathrm{d} x}$.

<div class=note>

(1) When $x \in [0, 1]$, $f_n(x) \leq \frac{x/n}{x(1+x)} = \frac{1}{1+x} := g(x)$. $g(x)$ is bounded so $g \in L([0, 1])$.
(2) When $x > 1$, $f_n(x) \leq \frac{1}{x(1+x)} := h(x)$. $h(x) \sim \frac{1}{x^2}$ when $x \rightarrow \infty$, so $h \in L([1, +\infty))$.
(3) $f_n \xrightarrow{a.e.} 0$. So by LDCT the limit is $0$.

</div>

- Calculate ${\displaystyle \lim \limits _{n \rightarrow \infty} \int_0^1 \frac{nx e^{-nx}}{1+n^2x^2}\mathrm{d} x}$.

<div class=note>

(1) $\displaystyle f_n = \frac{nx e^{-nx}}{1+n^2x^2} \leq \frac{nx e^{-nx}}{2nx} = \frac{e^{-nx}}{2} \leq \frac{1}{2}$.
(2) $f_n \xrightarrow{a.e.} 0$, so by LDCT the limit is $0$.

</div>

---

## Use LDCT to Calculate Integral Limits

- Calculate $\displaystyle \lim \limits _{n \rightarrow \infty} \int_0^1 \frac{nx^n}{1 + x^n}\mathrm{d} x$.

<div class=note>

(1) Let $y = x^n$, then $\displaystyle I = \lim \limits _{n \rightarrow \infty} \int_0^1 \frac{y^{1/n}}{1 + y}\mathrm{d} y$. Denote $\displaystyle f_n(y) = \frac{y^{1/n}}{1 + y}$, $\displaystyle f(y) = \frac{1}{1+y}$.
(2) $\displaystyle |f_n(y)| \leq \frac{1}{1+y}$, so $\displaystyle \lim \limits _{n \rightarrow \infty} \int_0^1 f_n(y) \mathrm{d} y = \int_0^1 f(y)\mathrm{d} y = \ln 2$.

</div>

---

## Applications of LDCT

- $f \in L(E)$, prove that ${\displaystyle \lim \limits _{k \rightarrow \infty} k \cdot m(\{|f| > k\}) = 0}$.

<div class=note>

(1) Let $f_k := |f| \cdot \chi_{E_k}$, $|f_k| < |f|$ where $|f| \in L(E)$. (2) $|f|$ is finite a.e., then $f_k \rightarrow 0$ a.e.
$$ k \cdot m(\{|f| > k\}) \leq \int_{E_k} |f| \mathrm{d} x = \int_E f_k \mathrm{d} x \rightarrow 0.  $$
</div>

- $f$ is measurable, $\forall \epsilon > 0$, $\exists g_{\epsilon}, h_{\epsilon} \in L(E)$, $g_{\epsilon} \leq f \leq h_{\epsilon}$, ${\displaystyle \int_E [h_{\epsilon} - g_{\epsilon}]\mathrm{d} x < \epsilon}$. Prove that $f \in L(E)$.

<div class=note>

(1) $f-g_{\frac{1}{n}} \leq h_{\frac{1}{n}}-g_{\frac{1}{n}} \in L(E)$, (2) ${\displaystyle \int_E f - g_{\frac{1}{n}} \mathrm{d} x \leq \int_E h_{\frac{1}{n}} - g_{\frac{1}{n}} \mathrm{d} x < \frac{1}{n}}$, then $f - g_n \rightarrow 0$ a.e.
$$ f - g_n \in L(E) \Rightarrow f = (f-g_n)+g_n \in L(E). $$
</div>

---

# Multiple Integrals and Iterated Integrals

---

## Key Results of Multiple Integrals and Iterated Integrals

- **Tonelli Theorem**: $f(x,y) \geq 0$ is measurable on $\mathbb{R}^p \times \mathbb{R}^q$. $f(x,\cdot)$ and $f(\cdot,y)$ are measurable and integrable a.e., then
$$
\int_{\mathbb{R}^p \times \mathbb{R}^q} f(x,y)\,\mathrm{d}x\mathrm{d}y 
= \int_{\mathbb{R}^p} \left( \int_{\mathbb{R}^q} f(x,y)\,\mathrm{d}y \right)\mathrm{d}x
= \int_{\mathbb{R}^q} \left( \int_{\mathbb{R}^p} f(x,y)\,\mathrm{d}x \right)\mathrm{d}y.
$$
- **Interchange of Summation and Integration**: $\{f_n(x)\}$ are non-negative measurable on $\mathbb{R}^p$, then
$$
\int_{\mathbb{R}^p} \sum_{n=1}^\infty f_n(x) \,\mathrm{d}x 
= \sum_{n=1}^\infty \int_{\mathbb{R}^p} f_n(x) \,\mathrm{d}x.
$$
- **Fubini Theorem**: $f(x,y)$ is integrable over $\mathbb{R}^p \times \mathbb{R}^q$. $f(x,\cdot)$ and $f(\cdot, y)$ are integrable a.e., 
$$
\int_{\mathbb{R}^p \times \mathbb{R}^q} f(x,y)\mathrm{d} x\mathrm{d}y 
= \int_{\mathbb{R}^p} \left[ \int_{\mathbb{R}^q} f(x,y)\mathrm{d} y \right]\mathrm{d} x.
$$

---

## Applications of Tonelli and Fubini Theorems

- $E$ is measurable, $f:E \rightarrow \mathbb{R}$ is non-negative and measurable. $G(f)$ is defined as $\{(x,y) \in \mathbb{R}^2: x \in E, y = f(x)\}$. Prove that $G(f)$ is measurable and $m(G(f)) = 0$.

<div class=note>

(1) Define $F:\mathbb{R}^2 \rightarrow \mathbb{R}$ that $F(x,y) = y - f(x)$. It is measurable on $E \times \mathbb{R}$ and we have $G(f) = F^{-1}(0) \cap (E \times \mathbb{R})$, which means $G(f)$ is measurable.
(2) For any $x \in E$, $G_x := \{y: (x,y) \in G(f)\}$ is single-point set $\{f(x)\}$.
(3) By Tonelli theorem,
$$ m(G(f)) = \int_{E} m(G_x) \mathrm{d} x = \int_E 0 \mathrm{d} x = 0.$$

</div>






