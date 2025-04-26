
# Peking Jiaotong University Mathematical Analysis 2021

## Problem 1

Calculate the limit
$$ \lim \limits _{x \rightarrow 0} \frac{e - (1+x)^{\frac{1}{x}}}{x}. $$

**Proof**. $(1 + x)^{\frac{1}{x}} = e ^{\frac{1}{x} \ln (1 + x)}$, where $\ln (1 + x) = x - \frac{1}{2}x^2 + o(x^2)$, then
$$ (1 + x)^{\frac{1}{x}} = e^{1 - \frac{1}{2}x + o(x)} = e[e^{-\frac{1}{2}x + o(x)}] = e[1 - \frac{1}{2}x + o(x)] $$
so the numerator is $\frac{1}{2}ex + o(x)$, so the limit is $\frac{e}{2}$.

## Problem 2

If $x = \ln(t + \sqrt{1 + t^2})$, $y = \arctan t$, calculate $\frac{\mathrm{d}^2 y}{\mathrm{d} x^2}$.

**Solution**. $\frac{\mathrm{d} x}{\mathrm{d} t} = \frac{1}{\sqrt{1 + t^2}}$, $\frac{\mathrm{d} y}{\mathrm{d} t} = \frac{1}{1+t^2}$. Then
$$ \frac{\mathrm{d} y}{\mathrm{d} x} = \frac{1}{\sqrt{1 + t^2}}. $$
Next, 
$$ \frac{\mathrm{d}^2 y}{\mathrm{d} x^2} = \frac{\frac{\mathrm{d} y}{\mathrm{d} x}}{\mathrm{d} t} / \frac{\mathrm{d}x}{\mathrm{d}t} = - \frac{t}{1+t^2}. $$

## Problem 3

If $f(x)$ is continuous in $[a, b]$, differentiable in $(a, b)$, $f(a) = f(b) = 0$. Prove that there exists $\xi \in (a, b)$ such that $f^{\prime}(\xi) + 3\xi^2 f(\xi) = 0$.

**Solution**. Consider $F(x) = f(x)e^{x^3}$, then $F^{\prime}(x) = f^{\prime}(x)e^{x^3} + 3x^2f(x)e^{x^3}$. $F(a) = F(b) = 0$, so by Rolle's mean-value theorem, there exists $\xi \in (a, b)$ such that
$$ F^{\prime}(\xi) = 0 \Rightarrow f^{\prime}(\xi) + 3\xi^2 f(\xi) = 0. $$

## Problem 4

Determine if the improper integral $\int_1^{+\infty} \frac{1}{x^2 (\sqrt{1 + x^2})^3}\mathrm{d} x$ is convergent.

**Solution**. When $x$ approximates infinity, the integrand function
$$ \frac{1}{x^2 (\sqrt{1 + x^2})^3} \sim \frac{1}{x^5}, $$
by compare test of improper integral, the improper integral is convergent.

## Problem 6

Find the convergent radius and region of $\sum\limits_{n = 1}^{\infty} \frac{(-1)^{n-1}}{n(2n-1)}x^{2n}$, and find the sum function.

**Solution**. By Cauchy-Hadamard test, the radius of convergence satisfies
$$ \frac{1}{R} = \lim \limits _{n \rightarrow \infty} \sqrt[n]{\frac{1}{n(2n-1)}} = 1,$$
so the radius of convergence is $1$. When $x = \pm 1$, the numerical series is convergent using the Leibniz's test. So the convergent region is $[-1, 1]$. Denote $f(x) = \sum\limits_{n = 1}^{\infty} \frac{(-1)^{n-1}}{n(2n-1)}x^{2n}$, 
$$ f^{\prime}(x) = 2\sum\limits_{n = 1}^{\infty} \frac{(-1)^{n-1}}{2n-1}x^{2n-1}, \quad f^{\prime\prime}(x) = 2 \sum\limits_{n = 1}^{\infty} (-1)^{n-1}x^{2n-2} = 2\sum\limits_{n = 1}^{\infty} (-x^2)^{n-1} = \frac{2}{1+x^2}. $$
Thus, $f^{\prime}(x) = 2 \arctan x$ and $f(x) = 2x\arctan x - \ln(1+x^2)$.

## Problem 7

Prove that $\sum\limits_{n = 1}^{\infty} \frac{1}{n^3} \ln (1 + n^2 x^2)$ is uniformly convergent in $[0, 1]$, and the sum function has continuous derivative.

**Proof**. For $x \in $

