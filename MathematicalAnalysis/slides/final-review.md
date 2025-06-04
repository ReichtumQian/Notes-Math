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

# Final Review: Mathematical Analysis

Speaker: Yixiao Qian

---

## Quick Review of Sequence Limit

Ignored.

---

## Quick Review of Function Limit

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

Note when $x \rightarrow \infty$: $\frac{1}{1+x} = \frac{1}{x} \cdot \frac{1}{1+1/x} = \sum\limits_{n = 1}^{\infty} (-1)^{n-1} \frac{1}{x^n}$. (From complex analysis we know the convergent radius is $1$)
</div>

---

## Quick Review of Continuity and Uniform Continuity

- $f: \mathbb{R} \rightarrow \mathbb{R}$. If (1) $\forall x, y \in \mathbb{R}$, $f(x+y) = f(x) + f(y)$. (2) $f$ is continuous at $x_0$. Prove there exists $a \in \mathbb{R}$ such that $f = ax$.
- $f$ is continuous at $x = 0$ and $x = 1$. $f(x^2) = f(x)$ for all $x$. Prove $f$ is constant.
- Prove followings are not uniformly continuous: (1)$x^2$ on $(0,+\infty)$; (2) $\frac{1}{x}$ on $(0, 1)$.
- Prove following are uniformly continuous: (1) $\cos \sqrt{x}$ on $[0, +\infty)$; (2) $\sqrt{x}$ on $[0, +\infty)$.

---

## Quick Review of Univariate Differential Calculus

- **Commonly Used Derivatives**: $\tan x$, $\sec x$, $\arcsin x$, $\arctan x$.
- $f^{\prime}$ exists, $f(a) < 0$, $f(b) < 0$, $\exists c \in (a,b)$, $f(c) > 0$. Prove $\exists \xi \in (a, b)$, $f(\xi) + f^{\prime}(\xi) = 0$.
- $f^{\prime\prime}$ exists, $f(a)=f(b)=0$. Prove $\exists \xi \in (a, b)$, $f^{\prime\prime}(\xi) = \frac{4}{(b-a)^2}f(\frac{a+b}{2})$.
- $f$ differenitable, $f(b) \neq f(a)$, if $f$ is non-linear, $\exists \xi, \eta \in (a, b)$, $f^{\prime}(\xi) < \frac{f(b) - f(a)}{b-a} < f^{\prime}(\eta)$.
- $\varphi(x)$ is convex on $[0, 1]$, prove ${\displaystyle \varphi(\frac{1}{2}) \leq \int_0^1 \varphi(x)\mathrm{d} x \leq \frac{\varphi(0) + \varphi(1)}{2}}$.

---

## Quick Review of Univariate Integral Calculus






