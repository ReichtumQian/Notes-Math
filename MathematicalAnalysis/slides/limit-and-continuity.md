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

# Limits and Continuity

Speaker: Yixiao Qian

---

## Table of Contents

---

# Sequence Limit


---

# Function Limit

---

## Key Points of Function Limit

- **Definition of Function Limit**
- **Uniqueness of Function Limit**
- **Closure under Arithmetic Operations**: 
- **Heine-Cantor Theorem**

---

## Calculation of Function Limit

<div class=trick>

Commonly used Taylor expansions: When $x \rightarrow 0$

$$
\begin{array}{ll}
e^x = \sum\limits_{n = 0 }^{\infty}\frac{x^n}{n!}& \ln(1 + x) = \sum\limits_{n = 1}^{\infty}(-1)^{n-1}\frac{x^n}{n} \\
\sin x = \sum\limits_{n = 0}^{\infty}(-1)^n \frac{x^{2n+1}}{(2n+1)!}& \cos x = \sum\limits_{n = 0}^{\infty}(-1)^n \frac{x^{2n}}{(2n)!} \\
\frac{1}{1+x} = \sum\limits_{n = 0}^{\infty}(-1)^n x^n&\frac{1}{1 - x} = \sum\limits_{n = 0}^{\infty}x^n \\
(1+x)^{\alpha} = 1 + \alpha x + \frac{\alpha(\alpha - 1)}{2}x^2 + o(x^2)&(1 + x)^{\alpha} = \sum\limits_{n = 0}^{\infty}{\alpha \choose n} x^n
\end{array}
$$

Note when $x \rightarrow \infty$: $\frac{1}{1+x} = \frac{1}{x} \cdot \frac{1}{1+1/x} = \sum\limits_{n = 1}^{\infty} (-1)^{n-1} \frac{1}{x^n}$.
</div>


---

# Continuous Function


---

# Uniform Continuity


