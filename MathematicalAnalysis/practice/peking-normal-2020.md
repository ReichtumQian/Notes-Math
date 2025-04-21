
# Peking Normal Univerisity 2020 Mathematical Analysis

## Problem 1

Find the limit

$$ \lim_{x \to \infty} x^{3} \left( \sqrt[3]{\frac{x^{3} + x}{x^{6} + x^{5} + 1}} - \sin \frac{1}{x}  \right). $$

**Solution**.

## Problem 2

If $a_n$ is a monotonically decreasing sequence. Prove that $\sum a_n$ and $\sum 2^{n-1}a_{2^n}$ have the same convergence behavior.

## Problem 3

Prove that $f(x) = \sqrt{x} \ln x$ is uniformly continuous in $(0, +\infty)$.

**Proof**. Note that $\lim \limits _{x \rightarrow 0}f(x) = 0$, then we can extend $f(x)$ to be defined at $x = 0$ with the value $f(0) = 0$. Then by Cantor theorem, we know it is uniformly continuous in $(0, 1)$. Now consider $[1, +\infty)$, take the derivative of $f(x)$:
$$
f^{\prime}(x) = \frac{\ln x + 2}{2 \sqrt{x}}, \quad
f^{\prime\prime}(x) = - \frac{x^{-\frac{1}{2}} \ln x}{4x},
$$ 
then we know the maximum value of $f^{\prime}(x)$ is at $x = 1$, being $f^{\prime}(1) = 1$. So $f(x)$ is Lipschitz continuous in $(1, +\infty)$, then it is uniformly continuous.

## Problem 4

## Problem 5

Calculate the triple integral

$$ \iiint_\Omega |x^2 + y^2 - 1| \mathrm{d}x \mathrm{d}y \mathrm{d}z, $$

where $\Omega$ is the region bounded by $x^2 + y^2 = 2z$ and $z = 2$.

**Solution**. 

