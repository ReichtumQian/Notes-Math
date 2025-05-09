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

## Key Points of Measurable Function

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

## Properities of Measurable Functions


- **Boundedness**: $f$ is basically bounded; $\{f_n\}$ are basically uniformly bounded.

<div class=note>

</div>

- **Closure under Operations**: $\pm$, $\times$, $/$, $\sup$, $\inf$, $\limsup$, $\liminf$.
- **Closure under Composition**: $f$ is continuous, $g$ is finite and measurable, then $f(g)$ is measurable.

---

## Determine if a Funcion is Measurable

- If for any $[\alpha, \beta] \subset (a, b)$, $f$ is measurable on $[\alpha, \beta]$. Prove $f$ is measurable on $(a, b)$.

<div class=note>

$E_n = \{x \in [a + \frac{1}{n}, b - \frac{1}{n}], f > c\}$ is measurable. $E_n$ is increasing, $E = \cup_{n=1}^{\infty}E_n$ is also measurable. This means $f$ is measurable on $(a, b)$.
</div>



---

# Approximation by Simple and Continuous Functions

---

## Approximation by Simple and Continuous Functions

<br>

- **Approximation by Simple Functions**: $\lim \limits _{n \rightarrow \infty} f_n(x) = f(x)$, $x \in E$.
- **Approximation by Continuous Functions (Lusin)**: Basically continuous on finite measure set.

---

# Convergence Results in Measure Theory

---

## Convergence Results in Measure Theory

<br>

- **Pointwise to Uniform (Egoroff)**: Basically on finite measure set.
- **Measure to Pointwise (Riesz)**: There exists a subsequence.
- **Pointwise to Measure (Lebesgue)**: On finite measure set.


