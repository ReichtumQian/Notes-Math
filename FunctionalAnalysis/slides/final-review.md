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

# Final Review: Functional Analysis

Speaker: Yixiao Qian

---

## Quick Review of Metric Space

- **Metric Space** and **Complete Metric Space**
- Validate (1) $C[a,b]$, (2) $C^{\infty}[a,b]$ are complete metric spaces.

<div class=note>

(1) The cauchy sequence $x_n(t) \rightrightarrows x(t)$, so $x(t) \in C[a,b]$.
(2) $f(t) = \frac{t}{1+t}$ is increasing.

</div>

- Validate $C[0,1]$ with $L^1[0,1]$ norm is not complete.

<div class=note>

$$ f_n(x) =
\begin{cases}
  0 & x \in [0, \frac{1}{2} - \frac{1}{n}];\\
  n(x-\frac{1}{2}+\frac{1}{n}) & x \in (\frac{1}{2}-\frac{1}{n}, \frac{1}{2}+\frac{1}{n});\\
  1 & x \in [\frac{1}{2} + \frac{1}{n}, 1].
\end{cases}
\rightarrow
f(x) =
\begin{cases}
  0 & x \in [0, \frac{1}{2});\\
  1 & x \in (\frac{1}{2}, 1].
\end{cases} \not \in C[0,1].
$$

</div>

- **Compact**, **Bounded**, **Totally Bounded** and **Their Relationship**
- **Contraction Mapping Theorem**

---

## Quick Review of Banach Space

- **Normed Linear Space** and **Banach Space**
- $\mathcal{B} :=\{\{x_n\}: \lim \limits _{n \rightarrow \infty} x_n = 0\}$, $\|x\| := \sup_{n\geq 1}|x_n|$. Prove $\mathcal{B}$ is Banach space.

---

## Quick Review of Hilbert Space

- **Polarization Identity**: $\langle x, y\rangle = \frac{1}{4} (\|x+y\|^2 - \|x-y\|^2)$.
- **Parallelogram Law**: $\|x+y\|^2 + \|x-y\|^2 = 2\|x\|^2 + 2\|y\|^2$.
- Validate $C[a,b]$ is not an inner product space. (Take $x = 2t$, $y = -2t + 2$ in $C[0,1]$.)

---

## Quick Review of Bounded Linear Operators

- **Bounded Linear Operator**: $\|Tx\| \leq M \cdot \|x\|$, $\|T\| := \inf_x M$. And $\mathcal{B}(E,F):=\{T: E \rightarrow F\}$.
- **Continuity and Boundedness**: $T$ is continuous iff $T$ is bounded.
- **Completeness**: If $E_1$ is complete, then $\mathcal{B}(E, E_1)$ is complete.
- **Uniform Boundedness Theorem**: $E,E_1$ are Banach spaces, $T_{\alpha}: E \rightarrow E_1$ are bounded. If for any $x \in E$, $\sup_{\alpha \in \mathcal{A}}\{\|T_{\alpha}x\|\} < \infty$. Then $\{T_{\alpha}\}$ are uniformly bounded.
- **Dual Space**: $E$ is a normed linear space. Its *dual space* is $E^{\ast}:=\mathcal{B}(E,\mathbb{P})$.
- **Riesz Representation Theorem**: $\mathcal{H}$ is a Hilbert space, for any $f \in \mathcal{B}(\mathcal{H}, \mathbb{P})$, there exists $u \in \mathcal{H}$ such that $f(x) = \langle u, x\rangle$.

