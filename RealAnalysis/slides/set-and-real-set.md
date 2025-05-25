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

# Sets and Topology on $\mathbb{R}^n$

Speaker: Yixiao Qian

---

# Set Operations

---

## Set Operations and Properties

- **Five Operations**: $A \cup B$, $A \cap B$, $A - B$, $A \Delta B$, $A^c$.
- **Distributive Law**: $(A \cup B) \cap C = (A \cap C) \cup (B \cap C)$, $(A \cap B) \cup C = (A \cup C) \cap (B \cup C)$.
- **De Morgan's Law**: $(\cup A_i)^c = \cap A_i^c$, $(\cap A_i)^c = \cup A_i^c$.
- **Difference between Unions**: $\cup_n G_n - \cup_n E_n \subset \cup_n (G_n - E_n)$.

<div class=note>

$x$ in lhs is in any $G_n$ and not in all $E_n$. $x$ in rhs is in any $G_n$ and not in corresponding $E_n$.
</div>

- **Union of Difference**: $\cup_{n=1}^{\infty}(A - A_n) = A - \cap_{n=1}^{\infty}A_n$.

<div class=note>

$\forall x \in \text{lhs}$, $\exists n_0$, $x \in A$, $x \not\in A_{n_0}$. Then $x \not \in \cap_{n=1}^{\infty}A_n$, and $x \in \text{rhs}$.
$\forall x \in \text{rhs}$, $x \in A$, $x \not\in \cap_{n=1}^{\infty}A_n$. Then $\exists n_0$ such that $x \not \in A_{n_0}$, which means $x \in \text{lhs}$.
</div>

---

## Set Statement of Inequalities

- $\{f > g\} = \cup_{n=1}^{\infty}\{f > g + \frac{1}{n}\}$

<div class=note>

$\Rightarrow$: $f> g$ indicates there exists $n > 0$, $f > g + \frac{1}{n}$.
$\Leftarrow$: $f > g + \frac{1}{n} > g$.

</div>

- $\{f \geq g\} = \cap_{n=1}^{\infty} \{f > g - \frac{1}{n}\}$

<div class=note>

$\Rightarrow$: $f \geq g > g - \frac{1}{n}$.
$\Leftarrow$: For all $n \geq 1$, $g < f + \frac{1}{n}$, take $n \rightarrow \infty$, then $g \leq f$.

Note that
(1) If $a_n > b_n$, $\lim \limits _{n \rightarrow \infty} a_n = a$, $\lim \limits _{n \rightarrow \infty} b_n = b$, then $a \geq b$.
(2) If $a_n < c$, $\lim \limits _{n \rightarrow \infty} a_n = a$, then $a \leq c$.

</div>

---

## Set Statement of Supremum and Infimum

<div class=trick>

$\eta = \sup S$: (1) $\forall x \in S$, $x \leq \eta$; (2) $\forall \epsilon > 0, \exists x \in S, x > \eta - \epsilon$.
$\eta = \inf S$: (1) $\forall x \in S$, $x \geq \eta$; (2) $\forall \epsilon > 0, \exists x \in S, x < \eta + \epsilon$.

</div>

- $\{x: \inf_n \{f_n(x)\} < c\} = \cup _{n = 1}^{\infty} \{x: f_n(x) < c\}$

<div class=note>

$\Rightarrow$: Let $A = \inf_n \{f_n(x)\}$, $\epsilon < c - A$. For $x$ in lhs, $\exists n_0$, $f_{n_0}(x) < A + \epsilon < c$. Then $x$ in rhs.
$\Leftarrow$: For $x$ in rhs, $\exists n_0$, $f_{n_0}(x) < c$. Then $\inf_n f_n \leq f_{n_0}(x) < c$, which means $x$ in lhs.
</div>

- $\{x: \inf_n \{f_n(x)\} \geq c\} = \cap _{n = 1}^{\infty} \{x: f_n(x) \geq c\}$

<div class=note>

$$
\forall n \in \mathbb{Z}^+, f_n(x) \geq c
\Leftrightarrow x \in \cap_{n = 1}^{\infty} \{x: f_n(x) \geq c\}.
$$

</div>

- $\{x: \sup_n \{f_n(x)\} \leq c\} = \cap _{n = 1}^{\infty} \{x: f_n(x) \leq c\}$
- $\{x: \sup_n \{f_n(x)\} > c\} = \cup _{n = 1}^{\infty} \{x: f_n(x) > c\}$

---

# Limit of Set Sequences

---

## Concept of Set Sequence Limits

- **Upper Limit**: $\limsup \limits_{n \rightarrow \infty} A_n := \cap _{n = 1}^{\infty} \cup _{k = n} ^{\infty} A_k$, which means $\forall n > 0, \exists k \geq n, x \in A_k$.
- **Lower Limit**: $\liminf \limits_{n \rightarrow \infty} A_n := \cup _{n = 1}^{\infty} \cap _{k = n}^{\infty}A_k$, which means $\exists n > 0, \forall k \geq n, x \in A_k$.

<div class=note>

Note the inner parts $B_n := \cup_{k=n}^{\infty} A_k$ is decreasing, $B_n := \cap_{k=n}^{\infty}A_k$ is increasing.

</div>

- **Limit**: If $\limsup A_n = \liminf A_n$, then $A_n$ have a limit.
- **Monotone Case**: Monotone set sequence has limit, 
$$
\lim \limits _{n \rightarrow \infty} A_n = \cup _{n = 1}^{\infty} A_n ~~  \text{if increasing},
\quad \quad
\lim \limits _{n \rightarrow \infty} A_n = \cap _{n = 1}^{\infty} A_n ~~  \text{if decreasing}.
$$

<div class=note>

Monotone is a sufficient condition to have a limit. For example,
$$ A_n = \left( -\frac{1}{n}, 1 + \frac{(-1)^n}{n} \right) \rightarrow (0, 1) $$
has a limit but is not monotone.
</div>

---

## Upper Limit and Lower Limit of Set Sequences

- Let $A_{2n-1} = (0, \frac{1}{n})$, $A_{2n} = (0, n)$. Find $\limsup A_n$ and $\liminf A_n$.

- Let $A_n = \{\frac{m}{n}: m \in \mathbb{Z}\}$. Prove that $\limsup A_n = \mathbb{Q}$ and $\liminf A_n = \mathbb{Z}$.


---

## Limit of Set of Function Limit

- $f_n(x) \leq f_{n+1}(x)$ for all $x \in E$. Prove that the limit of $A_n = \{x : f_n(x) > c\}$ exists and
$$ \lim \limits _{n \rightarrow \infty} A_n = \{x : \lim \limits _{n \rightarrow \infty} f_n(x) > c\}. $$

<div class=note>

$\Rightarrow$: $\lim \limits _{n \rightarrow \infty} A_n = \cup_{n=1}^{\infty}A_n$. For $x$ in lhs, $\exists n_0$, $f_{n_0}(x) > c$, thus $x$ in rhs.
$\Leftarrow$: There exists a sufficiently large $n_0$ such that $f_{n_0}(x) > c$, then $x$ is in lhs.
</div>

---

# Topology on $\mathbb{R}^n$

---

## Key Points on Topology on $\mathbb{R}^n$

- **Open Sets in $\mathbb{R}$**: Any open set in $\mathbb{R}$ is the union of at most countably many pairwise-disjoint open intervals.
- **Continuous Mapping**: $f$ is continuous, $f(X) = Y$. If $Y$ is an open set, then $X$ is an open set.
- **Open Mapping**: $f$ is *open mapping* if it maps any open set $X$ to an open set $Y$.

