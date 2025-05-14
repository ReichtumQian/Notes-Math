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

## Table of Contents

---

# Derivatives and Differentials

---

## Key Points of Derivatives and Differentials

- **Differentiability and Derivative**: 
- **Derivative of Implicit Functions**: Differentiate both sides of an equation.
- **Derivative of Inverse Functions**: $\frac{\mathrm{d} y}{\mathrm{d} x} = \left( \frac{\mathrm{d} x}{\mathrm{d} y} \right)^{-1}$.
- **Derivative of Power-Exponential Functions**

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
- **Lagrange**: $\exists \xi \in (a, b)$ such that $\displaystyle f^{\prime}(\xi) = \frac{f(b)-f(a)}{b-a}$.
- **Cauchy**: $g(a) \neq g(b)$, $\exists \xi \in (a, b)$ such that $\displaystyle \frac{f^{\prime}(\xi)}{g^{\prime}(\xi)} = \frac{f(b)-f(a)}{g(b)-g(a)}$.

---

## Applications of Cauchy's Mean-Value Theorem

If $a < b$, $ab > 0$, $f \in C[a, b]$, differenitable on $(a, b)$, prove that $\exists \xi \in (a, b)$ such that
$$ \frac{af(b) - bf(a)}{a-b} = f(\xi) - \xi f^{\prime}(\xi). $$


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

