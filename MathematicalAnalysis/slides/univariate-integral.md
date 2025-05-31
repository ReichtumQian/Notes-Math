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

# Univariate Integrals

Speaker: Yixiao Qian

---

# Indefinite Integrals

---

## Commonly Used Indefinite Integrals

$$
\begin{align}
    &\int \sec x \, \mathrm{d}x = \ln|\sec x + \tan x| + c 
    && \int \sec x \tan x \, \mathrm{d}x = \sec x + c \\
    &\int \sec^2 x \, \mathrm{d}x = \tan x + c 
    && \int \csc^2 x \, \mathrm{d}x = -\cot x + c \\
    &\int \frac{1}{x^2 + a^2} \, \mathrm{d}x = \frac{1}{a} \arctan \frac{x}{a} + c 
    && \int \frac{1}{x^2 - a^2} \, \mathrm{d}x = \frac{1}{2a} \ln \left| \frac{x-a}{x+a} \right| + c \\
    &\int \frac{1}{\sqrt{x^2 + a^2}} \, \mathrm{d}x = \ln \left| x + \sqrt{x^2 + a^2} \right| + c 
    && \int \frac{1}{\sqrt{x^2 - a^2}} \, \mathrm{d}x = \ln \left| x + \sqrt{x^2 - a^2} \right| + c \\
    &\int \frac{1}{\sqrt{a^2 - x^2}} \, \mathrm{d}x = \arcsin \frac{x}{a} + c 
    && \int \ln x \, \mathrm{d}x = x \ln x - x + c
\end{align}
$$

---

## Indefinite Integrals of Rational Functions

- Calculate ${\displaystyle \int \frac{x}{(x+1)(x^2 + 2)}\mathrm{d} x}$.

<div class=note>

Hint: Assume $\frac{x}{(x+1)(x^2+2)} = \frac{A}{x+1} + \frac{Bx + C}{x^2 + 2}$. Then $A = -\frac{1}{3}$, $B = \frac{1}{3}$, $C = \frac{2}{3}$.

</div>

- Calculate ${\displaystyle \int \frac{\mathrm{d} x}{ax^2 + b}}$. 
- Calculate ${\displaystyle \int \frac{\mathrm{d} x}{(ax^2 + b)^2}}$. (Hint: ${\displaystyle - \int \frac{1}{2ax} \mathrm{d} \frac{1}{ax^2 + b}}$ and integrate-by-part.)
- Calculate ${\displaystyle \int \frac{\mathrm{d} x}{ax^2 + bx + c}}$. (Hint: ${\displaystyle \frac{1}{a} \int \frac{\mathrm{d} x}{(x+\frac{b}{2a})^2 + \frac{c}{a} - \frac{b^2}{4a^2}}}$ and become ${\displaystyle \int \frac{\mathrm{d} x}{ax^2 + b}}$.)
- Calculate ${\displaystyle \int \frac{x}{ax^2 + bx + c}\mathrm{d} x}$. (Hint: ${\displaystyle \frac{1}{2a} \int \frac{2ax + b}{ax^2 + bx + c} - \frac{b}{ax^2 + bx + c}\mathrm{d} x}$)

---

## Indefinite Integrals of Trigonometric Functions

- Calculate the following integrals

$$
(1) \int \tan x\mathrm{d} x, \quad
(2) \int \sec x \mathrm{d} x, \quad
(3) \int \sec^3 x \mathrm{d} x.
$$

<div class=note>

(1) ${\displaystyle \int \tan x \mathrm{d} x = - \int \frac{\mathrm{d} \cos x}{\cos x} = - \ln |\cos x| + C}$.
(2) ${\displaystyle \int \sec x \mathrm{d} x = \int \frac{\sec x (\sec x + \tan x)}{\sec x + \tan x}\mathrm{d} x = \int \frac{\mathrm{d} (\sec x + \tan x)}{\sec x + \tan x} = \ln |\sec x + \tan x| + C}$.
(3) ${\displaystyle \int \sec^3 x \mathrm{d} x = \int \sec x \mathrm{d} \tan x = \sec x \tan x - \int \tan^2 x \sec x \mathrm{d} x}$. Since $\tan^2 x = \sec^2 x - 1$,
$$ \int \sec^3 x \mathrm{d} x = \sec x \tan x - \int \sec^3 x \mathrm{d} x + \int \sec x \mathrm{d} x $$

</div>

---

## Applications of Integrals of Trigonometric Functions

$$
(1) \int \frac{1}{x^2 + a^2}\mathrm{d} x,
(2) \int \frac{1}{x^2 - a^2}\mathrm{d} x,
(3) \int \frac{1}{\sqrt{x^2 + a^2}}\mathrm{d} x,
(4) \int \frac{1}{\sqrt{x^2 - a^2}}\mathrm{d} x, 
(5) \int \frac{1}{\sqrt{a^2 - x^2}}\mathrm{d} x.
$$

<div class=note>

(1) Let $x = a \tan t$, then ${\displaystyle \int \frac{1}{x^2 + a^2}\mathrm{d}x = \int \frac{1}{a^2 \sec^2 t} \cdot a \sec^2 t \mathrm{d} t = \frac{t}{a}}$. So $I = \frac{1}{a} \arctan \frac{x}{a}$.

</div>


---

## Indefinite Integrals of Squared Functions

$$
(1) \int \sqrt{a^2 - x^2}\mathrm{d} x, \quad
(2) \int \sqrt{x^2 + a^2}\mathrm{d} x, \quad
(3) \int \sqrt{x^2 - a^2}\mathrm{d} x.
$$


---

# Definite Integrals

---

## Key Points of Definite Integrals

- **Condition for Integrability**: $\sum_i \omega_i \Delta x_i < \epsilon$.
- **Property**: If $f$ is integrable, then $f$ is bounded.
- **Closure under Arithmetic Operations**: $kf(x)$, $f(x) \pm g(x)$, $f(x)g(x)$.

<div class=note>

Assume $|f| \leq M$ and $|g| \leq N$, $\omega_i^{fg} \Delta x_i \leq M \omega_i^g \Delta x_i + N \omega_i^f \Delta x_i$.

</div>

- **Closure under Composition**: $f$ continuous, $\varphi$ integrable, then $f(\varphi(x))$ integrable.
- **Newton-Leibniz Formula**: ${\displaystyle \int_a^b f(x)\mathrm{d} x = F(b) - F(a)}$.
- **Mean-Value Theorem**: If $g(x)$ does not change sign, ${\displaystyle \int_a^b f(x)g(x)\mathrm{d} x = f(\xi) \int_a^b g(x)\mathrm{d} x}$.

---

## Applications of Mean-Value Theorem

- If $f$ is strictly increasing, prove ${\displaystyle \int_a^b xf(x)\mathrm{d} x > \frac{a+b}{2} \int_a^b f(x)\mathrm{d} x}$.

<div class=note>

(1) $\displaystyle \int_a^b (x - \frac{a+b}{2}) f(x)\mathrm{d} x = \int_a^{\frac{a+b}{2}}(x-\frac{a+b}{2})f(x)\mathrm{d}x + \int_{\frac{a+b}{2}}^b (x - \frac{a+b}{2})f(x)\mathrm{d} x$.
(2) In first term take $t = \frac{a+b}{2} - t$, and second term $t = x - \frac{a+b}{2}$. Then
$$ I = \int_0^{\frac{b-a}{2}} t \left[ f(\frac{a+b}{2} + t) - f(\frac{a+b}{2} - t) \right] \mathrm{d} t > 0 $$



</div>

---

## Wallis Formula

- **$[0, \frac{\pi}{2}]$**: $\displaystyle I(m,n) = \int_0^{\frac{\pi}{2}} \sin^m x \cos^n x\mathrm{d} x$, then
$$ I(m,n) =
\begin{cases}
  \frac{(m-1)!!(n-1)!!}{(m+n)!!} \frac{\pi}{2} & \text{if m,n are even;}\\
  \frac{(m-1)!!(n-1)!!}{(m+n)!!} & \text{otherwise.}
\end{cases}$$
- **$[0,\pi]$**: $\displaystyle J(m,n) = \int_0^{\pi} \sin^m x \cos^n x\mathrm{d} x$. If $n$ is even $J(m,n) = 2I(m,n)$, and $0$ otherwise.
- **$[0,2\pi]$**: $\displaystyle K(m,n) = \int_0^{2\pi} \sin^m x \cos^n x\mathrm{d} x$. If $n,m$ are even $K(m,n) = 4I(m,n)$, and $0$ else.



---

# Improper Integrals

---

## Definition of Improper Integrals

- **Improper Integrals**: ${\displaystyle \int_a^{+\infty}f(x)\mathrm{d} x := \lim \limits _{b \rightarrow +\infty}\int_a^b f(x)\mathrm{d} x}$ and ${\displaystyle \int_a^b f(x) \mathrm{d} x := \lim \limits _{\epsilon \rightarrow 0} \int_{a+\epsilon}^b f(x)\mathrm{d} x}$.

<div class=note>

Consider $\displaystyle F(t) = \int_a^t f(x)\mathrm{d} x$ as a function, then we can apply theory of function limit to convergence and Cauchy's criterion of improper integrals.

</div>

- **Statement of Convergence**: The improper integral converges iff there exists $A$ 
$$ \forall \epsilon > 0, \exists M > 0, \forall b > M, \quad \left| A - \int_a^b f(x) \mathrm{d} x \right| = \left| \int_b^{+\infty}f(x)\mathrm{d}x \right| < \epsilon. $$
- **Cauchy's Criterion**: The improper integral converges iff
$$ \forall \epsilon > 0, \exists M > 0, \forall t_1, t_2 > M, \quad \left| \int_a^{t_1} f(x)\mathrm{d} x - \int_a^{t_2}f(x)\mathrm{d} x \right| = \left| \int_{t_1}^{t_2} f(x)\mathrm{d} x \right| < \epsilon. $$

---

## Definition of Improper Integrals

- **Leibniz Formula**: ${\displaystyle \int_a^{+\infty} f(x)\mathrm{d} x = F(+\infty) - F(a)}$ and ${\displaystyle \int_a^b f(x)\mathrm{d} x = F(b) - F(a+0)}$.
- **Absolute and Conditional Convergence**: If ${\displaystyle \int_a^b |f(x)| \mathrm{d} x}$ converges, then ${\displaystyle \int_a^b f\mathrm{d} x}$ is *absolutely convergent*, otherwise it is *conditionally convergent*.

<div class=note>

Absolute convergence implies convergence, since Cauchy's criterion.

$$ \left| \int_{t_1}^{t_2} f(x)\mathrm{d} x \right| \leq \int_{t_1}^{t_2} |f(x)|\mathrm{d} x < \epsilon $$

</div>

- **Behavior of $\displaystyle \int_1^{+\infty} \frac{\mathrm{d} x}{x^p}$**: Converges when $p > 1$, diverges when $p \leq 1$.
- **Behavior of ${\displaystyle \int_0^1 \frac{\mathrm{d} x}{x^p}}$**: Converges when $p < 1$ (includes $p < 0$), diverges when $p \geq 1$.


---

## Properties of Convergent Improper Integrals

- If ${\displaystyle \int_a^{+\infty}f(x)\mathrm{d} x}$ exists and $\lim \limits _{x \rightarrow \infty}f(x) = A$. Then $A = 0$.

<div class=note>

If $A > 0$, $\exists X > 0$, $\forall x > X$, $f(x) > \frac{A}{2}$. Then $\displaystyle \int_X^{+\infty} f(x)\mathrm{d} x > \int_X^{+\infty}\frac{A}{2} \mathrm{d}x \neq 0$.

</div>

- If $f \in C[a, +\infty)$, ${\displaystyle \int_a^{+\infty} f(x)\mathrm{d} x}$ exists. $\lim \limits _{x \rightarrow +\infty}f(x)$ may not exist. (Example: ${\displaystyle \int_1^{+\infty} \sin x^2 \mathrm{d}x}$.)
- If $f$ is uniformly continuous on $[a, +\infty)$, ${\displaystyle \int_a^{+\infty}f(x)\mathrm{d} x}$ exists, prove that $\lim \limits _{x \rightarrow +\infty} f(x) = 0$.

<div class=note>

(1) Assume $\lim \limits _{x \rightarrow +\infty}f(x) \neq 0$, then $\exists \epsilon >0$, $\forall X > 0$, $\exists x_0 > X$, $|f(x_0)| > \epsilon$.
(2) By uniform continuity, $\exists \delta > 0$, $\forall x \in [x_0, x_0+\delta]$, $|f(x) - f(x_0)| < \frac{\epsilon}{2}$. Then $|f(x)| \geq \frac{\epsilon}{2}$.
(3) $\displaystyle |\int_{x_0}^{x_0+\delta} f(x)\mathrm{d} x| = \int_{x_0}^{x_0+\delta}|f(x)|\mathrm{d} x \geq \frac{\epsilon\delta}{2}$, this contradicts Cauchy's criterion.

</div>


---

## Tests for Convergence

- **Compare Test**: (1) ${\displaystyle \int_0^{+\infty} \frac{x}{1-e^x}\mathrm{d} x}$; (2) ${\displaystyle \int_0^{+\infty} \frac{\ln x}{e^x}}$; (3) ${\displaystyle \int_3^{+\infty} \frac{\mathrm{d} x}{x^p (\ln x)^q (\ln \ln x)^r}}$.

<div class=note>

(1) When $x = 0$ the limit is $1$; When $x \rightarrow \infty$, $f(x) \sim \frac{x}{x^{+\infty}}$, so it converges.
(2) When $x = 0$, $|\frac{\ln x}{e^x}| \leq |x^{-\epsilon}|$, so converges. When $x \rightarrow \infty$, $e^x \sim x^{+\infty}$, so converges.

</div>

- **Dirichlet Test**: (1) ${\displaystyle \int_a^x f(t)\mathrm{d} t}$ is bounded; (2) $g(x)$ decreases to $0$.
- **Abel Test**: (1) ${\displaystyle \int_a^{+\infty}f(t)\mathrm{d} t}$ converges; (2) $g(x)$ monotone and bounded.
- Discuss convergence behavior: (1) ${\displaystyle \int_0^{+\infty} \frac{\sin x}{x^p}}$; (2) ${\displaystyle \int_0^{+\infty} \sin x^2 \mathrm{d} x}$.

<div class=note>

(1) $x = 0$: $\frac{\sin x}{x^p} \sim \frac{1}{x^{p-1}}$, so $p < 2$. $x \rightarrow \infty$: $\int_1^x \sin t\mathrm{d} t$ bounded, $\frac{1}{x^p} \rightarrow 0$ for $p > 0$.
(2) Take $x = \sqrt{t}$, then $I = \int_0^{+\infty} \frac{\sin t}{2 \sqrt{t}}\mathrm{d} t$. Then $f \sim t^{\frac{1}{2}}$ when $x = 0$, by Dirichlet when $x \rightarrow \infty$.

</div>









