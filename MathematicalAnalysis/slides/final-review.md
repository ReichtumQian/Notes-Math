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

- **Commonly Used Integrations**: ${\displaystyle \int \frac{1}{x^2 \pm a^2}\mathrm{d} x}$
- **Rational Function**: ${\displaystyle \int \frac{\mathrm{d} x}{(ax^2 + b)^2}}$
- If $f$ is strictly increasing, prove ${\displaystyle \int_a^b xf(x)\mathrm{d} x > \frac{a+b}{2} \int_a^b f(x)\mathrm{d} x}$.

---

## Quick Review of Series

- Determine if $f_n = x^n \ln x$ is uniformly convergent on $(0, 1]$.
- If $f \in C[a, b]$, $f_0(x) = f(x)$, $\displaystyle f_{n+1}(x) = \int_a^x f_n(t)\mathrm{d} t$, prove $f_n(x)$ is uniformly convergent.
- $f^{\prime}$ is continuous, $a_n \nearrow +\infty$ is positive. Prove $f_n = a_n \left[ f(x + \frac{1}{a_n}) - f(x) \right] \rightrightarrows f^{\prime}(x)$ on $[a, b]$
- **Local Continuity**: $f_n \rightrightarrows f$ on $(a, b)$, $\lim \limits _{x \rightarrow x_0}f_n(x) = a_n$, then $\lim \limits _{x \rightarrow x_0}f(x) = \lim \limits _{n \rightarrow \infty} a_n$. 
- **Uniform Continuity**: $f_n$ uniformly continuous, $f_n \rightrightarrows f$, then $f$ is uniformly continuous.
- **Term-by-Term Integration**: $f_n \rightrightarrows f$ on $[a, b]$, $f_n$ integrable on $[a, b]$. Then $f(x)$ integrable
$$ \int_a^b f(x)\mathrm{d} x = \lim \limits _{n \rightarrow \infty} \int_a^b f_n(x)\mathrm{d} x. $$
- **Expansion**: $f(x) = \arctan \frac{1-kx}{1+kx}$.

---

## Quick Review of Multivariable Integral

- Calculate ${\displaystyle \int_0^1 \frac{x^b - x^a}{\ln x}\mathrm{d} x}$ where $0 < a < b$.
- ${\displaystyle \int_0^{+\infty} \frac{\sin xy}{y}\mathrm{d} y}$ uniformly converges on $[\delta, +\infty)$, but not on $(0, +\infty)$.
- ${\displaystyle \int_1^{+\infty} \frac{\sin x}{1+xe^y}\mathrm{d} x}$ on $[0, +\infty)$, ${\displaystyle \int_0^{+\infty} e^{-xy} \frac{\sin x}{x}\mathrm{d} x}$ on $[0, +\infty)$.
- If $p > 0$, then ${\displaystyle \int_0^{+\infty} e^{-px} \frac{\sin bx - \sin ax}{x} \mathrm{d} x = \arctan \frac{b}{p} - \arctan \frac{a}{p}}$.
- **Normal Distribution Integral**: ${\displaystyle \int_0^{+\infty} e^{-x^2}\mathrm{d} x = \frac{\sqrt{\pi}}{2}}$.
- **Green's Theorem**: Calculate ${\displaystyle \oint_L \frac{x\mathrm{d} y - y\mathrm{d} x}{ax^2 + by^2}}$ where $a, b > 0$, $L$ doesn't pass through the origin, but enclose it.
- **Gauss's Theorem**: Calculate ${\displaystyle I = \iint_S \frac{x\mathrm{d}y\mathrm{d}z + y\mathrm{d}z\mathrm{d} x + z\mathrm{d}x \mathrm{d} y}{(ax^2+by^2+cz^2)^{\frac{3}{2}}}}$, where $S$ does not pass origin.

