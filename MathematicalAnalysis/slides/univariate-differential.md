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

# Univariate Differential Calculus

Speaker: Yixiao Qian

---

# Derivatives and Differentials

---

## Key Points of Derivatives and Differentials

- **Differentiability and Derivative**: 
- **Derivative of Implicit Functions**: Differentiate both sides of an equation.
- **Derivative of Inverse Functions**: $\frac{\mathrm{d} y}{\mathrm{d} x} = \left( \frac{\mathrm{d} x}{\mathrm{d} y} \right)^{-1}$.
- **Derivative of Power-Exponential Functions**: $y(x) = u(x)^{v(x)}$, $\ln y(x) = v(x) \ln u(x)$.
- **Higher-Order Derivatives**: $[f(x)g(x)]^{(n)} = \sum_{k=0}^n \binom{n}{k} f^{(n-k)}(x)g^{(k)}(x)$.

---

## Commonly Used Derivatives

<br>

<div class=trick>

Commonly Used Trigonometric and Inverse Trigonometric Derivatives:

$$
\begin{array}{ll}
(\tan x)^{\prime} = \sec^2 x & (\cot x)^{\prime} = - \csc^2 x\\
(\sec x)^{\prime} = \sec x \tan x&  (\csc x)^{\prime} = - \csc x \cot x\\
(\sin x)^{(n)} = \sin \left( x + \frac{n\pi}{2} \right)&(\cos x)^{(n)} = \cos \left( x + \frac{n\pi}{2}\right)\\
(\arcsin x)^{\prime} = \frac{1}{\sqrt{1 - x^2}} & (\arccos x)^{\prime} = - \frac{1}{\sqrt{1 - x^2}} \\
(\arctan x)^{\prime} = \frac{1}{1 + x^2} & (\operatorname{arccot} x)^{\prime} = - \frac{1}{1 + x^2}
\end{array}
$$
</div>

---

## Practice on Derivatives

- If $y = \sin t$ and $x = \ln(\tan \frac{t}{2}) + \cos t$. Find the expression of $y^{\prime\prime}(x)$.

<div class=note>

(1) $\frac{\mathrm{d} y}{\mathrm{d} t} = \cos t$, $\frac{\mathrm{d} x}{\mathrm{d} t} = \frac{1}{2} \cdot \frac{\sec^2 \frac{t}{2}}{\tan \frac{t}{2}} - \sin t = \frac{1}{\sin t} - \sin t = \frac{\cos^2 t}{\sin t}$. Then $\frac{\mathrm{d} y}{\mathrm{d} x} = \tan t$.
(2) $\frac{\mathrm{d} y^{\prime}(t)}{\mathrm{d} t} = \sec^2 t$. Then
$$ \frac{\mathrm{d}^2 y}{\mathrm{d} x^2} = \frac{\mathrm{d} y^{\prime}}{\mathrm{d} t} / \frac{\mathrm{d} x}{\mathrm{d} t} = \sin t \cdot \sec^4 t. $$

</div>


---

# Differential Mean-Value Theorem

---

## Key Points of Mean-Value Theorems

- **Fermat's Theorem**: $x_0$ is extreme, then $f^{\prime}(x_0) = 0$.
- **Rolle**: $f(a) = f(b)$, then $\exists \xi \in (a, b)$ such that $f^{\prime}(\xi) = 0$.
- **Generalized Rolle**: If $\lim \limits _{x \rightarrow \infty} f(x) = f(0)$, $\exists \xi \in (0, +\infty)$, $f^{\prime}(\xi) = 0$.

<div class=note>

(1) $F(x) := f(x) - f(0)$, $\lim \limits _{x \rightarrow \infty}F(x) = 0$, $\forall \epsilon > 0$, $\exists X > 0$, $\forall x > X$, $|F(x)| < \epsilon$.
(2) $M:=\sup F$, $m := \inf F$, if $M = m$, $f$ is constant, $f^{\prime} \equiv 0$.
(3) If $M \neq m$, assume $M > 0$, take $\epsilon < M$, then $\exists x_0 \in [0, X]$, $f(x_0) = M$, then $f^{\prime}(x_0) = 0$.

</div>

- **Lagrange**: $\exists \xi \in (a, b)$ such that $\displaystyle f^{\prime}(\xi) = \frac{f(b)-f(a)}{b-a}$.
- **Cauchy**: $g(a) \neq g(b)$, $\exists \xi \in (a, b)$ such that $\displaystyle \frac{f^{\prime}(\xi)}{g^{\prime}(\xi)} = \frac{f(b)-f(a)}{g(b)-g(a)}$.
- **Auxiliary Function**: $\left( f e^{\int g \mathrm{d} x} \right)^{\prime} = [f^{\prime} + fg]e^{\int g \mathrm{d} x}$ for $f^{\prime}(\xi) + f(\xi)g(\xi)$.

---

## Applications of Rolle's Mean-Value Theorem

- If $0 \leq f(x) \leq xe^{-x}$, then $\exists \xi \in (0, +\infty)$, $f^{\prime}(\xi) = e^{-\xi}(1- \xi)$.

<div class=note>

$F(x) := f(x) - xe^{-x}$, $F(0) = 0$, $\lim \limits _{x \rightarrow +\infty}F(x) = 0$. The result follows generalized Rolle.

</div>

- $f$ is differenitable, $f(a) < 0$, $f(b) < 0$, $\exists c \in (a,b)$, $f(c) > 0$. Prove $\exists \xi \in (a, b)$, $f(\xi) + f^{\prime}(\xi) = 0$.

<div class=note>

(1) $F(x) := e^x f(x)$, $F(a) < 0$, $F(b) < 0$, $F(c) > 0$. $\exists x_1, x_2$ that $F(x_1) = F(x_2) = 0$.
(2) By Rolle, $\exists \xi \in (x_1, x_2)$, $F^{\prime}(\xi) = e^{\xi}[f(\xi) + f^{\prime}(\xi)] = 0$.

</div>


---

## Applications of Lagrange's Mean-Value Theorem

- $f$ differenitable, prove $\exists \xi \in (a, b)$, $f(\xi) + \xi f^{\prime}(\xi) = \frac{bf(b) - af(a)}{b-a}$.

<div class=note>

Note this example is not $f^{\prime} + fg$. Consider $F(x) = xf(x)$.

</div>

- $f$ differenitable, $f(b) \neq f(a)$, if $f$ is non-linear, $\exists \xi, \eta \in (a, b)$, $f^{\prime}(\xi) < \frac{f(b) - f(a)}{b-a} < f^{\prime}(\eta)$.

<div class=note>

Only prove lhs, assume it does not hold, then $\forall x \in (a, b)$, $f^{\prime}(x) \geq \frac{f(b) - f(a)}{b-a}$. Then
$$ F(x) = f(x) - \frac{f(b) - f(a)}{b-a}x \Rightarrow F^{\prime}(x) \geq 0, F(a) = F(b) = 0, $$
which implies $F^{\prime}(x) \equiv 0$. This contradicts the condition.

</div>


---

## Applications of Cauchy's Mean-Value Theorem

If $a < b$, $ab > 0$, $f \in C[a, b]$, differenitable on $(a, b)$, prove that $\exists \xi \in (a, b)$ such that
$$ \frac{af(b) - bf(a)}{a-b} = f(\xi) - \xi f^{\prime}(\xi). $$

<div class=note>

It is equivalent to prove that ${\displaystyle \frac{f(b)/b - f(a)/a}{1/b - 1/a} = f(\xi) - \xi f^{\prime}(\xi)}$. Define $g(x) = \frac{f(x)}{x}$ and $h(x) = \frac{1}{x}$. Then

$$ \frac{g(b) - g(a)}{h(b) - h(a)} = \frac{g^{\prime}(\xi)}{h^{\prime}(\xi)} = f(\xi) - \xi f^{\prime}(\xi). $$

</div>

---

# Convex Function

---

## Concept of Convex Function

- **Ratio Dividing Point Formula**: $\forall x \in [x_1, x_2]$, ${\displaystyle x = \frac{x_2 - x}{x_2 - x_1} x_1 + \frac{x - x_1}{x_2 - x_1}x_2}$.
- **Convex Function**: $f(\lambda x_1 + (1-\lambda)x_2) \leq \lambda f(x_1) + (1 - \lambda) f(x_2)$.
- **First-Order Derivative Form**: $f(x) \geq f(x_0) + f^{\prime}(x_0)(x-x_0)$ or $f^{\prime}(x)$ is increasing.
- **Second-Order Derivative Form**: $f^{\prime\prime}(x) \geq 0$.
- $\forall x_0 \in (0, 1)$, $\exists m \in \mathbb{R}$, $f(x) \geq f(x_0) + m(x-x_0)$ for any $x \in (0, 1)$. Prove $f$ is convex.

<div class=note>

Take $x_1, x_2$ satisfying $x_0 = \lambda x_1 + (1-\lambda)x_2$, we have $f(x_1) \geq f(x_0) + m(x_1 - x_0)$ and $f(x_2) \geq f(x_0) + m(x_2 - x_0)$, then
$$ \lambda f(x_1) + (1-\lambda)f(x_2) \geq f(x_0) +  \lambda m (x_1 - x_0) + (1 - \lambda) m(x_2 - x_0). $$
where the sum of the second term and the third term is zero.

</div>

---

## Integrals of Convex Functions

- $\varphi(x)$ is convex on $[0, 1]$, prove ${\displaystyle \varphi(\frac{1}{2}) \leq \int_0^1 \varphi(x)\mathrm{d} x \leq \frac{\varphi(0) + \varphi(1)}{2}}$.

<div class=note>

(1) $x = x \cdot 1 + (1-x) \cdot 0$, then ${\displaystyle \int_0^1 \varphi(x)\mathrm{d} x \leq \int_0^1 (1-x)\varphi(0) + x \varphi(1)\mathrm{d} x = \frac{\varphi(0) + \varphi(1)}{2}}$.
(2) Let $x = 1-t$, then ${\displaystyle \int_0^1 \varphi(x)\mathrm{d} x = \int_0^1 \varphi(1-x)\mathrm{d} x}$ and
$$ \int_0^1 \varphi(x)\mathrm{d} x = \int_0^1 \frac{1}{2}\varphi(x) + \frac{1}{2}\varphi(1-x)\mathrm{d} x \geq \int_0^1 \varphi \left( \frac{x}{2} + \frac{1 - x}{2} \right)\mathrm{d} x = \varphi \left( \frac{1}{2} \right). $$

</div>

- $\varphi$ is convex on $[a, b]$, prove ${\displaystyle \varphi(\frac{a+b}{2}) \leq \frac{1}{b-a} \int_a^b \varphi(x)\mathrm{d} x \leq \frac{\varphi(a) + \varphi(b)}{2}}$.

<div class=note>

Change variable $x = \lambda a + (1 - \lambda)b$.

</div>

