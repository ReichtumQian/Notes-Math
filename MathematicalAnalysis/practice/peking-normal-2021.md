
# Peking Normal Univerisity 2021 Mathematical Analysis

## Problem 1

Given $\lim \limits _{n \rightarrow \infty} n^{2n \ln \frac{1}{n}}a_n = 1$, determine the convergence behavior of the sequence $\sum a_n$.

**Proof**. With the condition, we know
$$ \lim_{n \to \infty} a_{n} = \frac{1}{n^{2n \ln \frac{1}{n}}}. $$
We know $|\ln \frac{1}{n}| <  |n^{\epsilon}|, n \rightarrow \infty$, where $\epsilon$ is an arbitrary real number. By compare test, $\sum \frac{1}{n^{2n+\epsilon}}$ is convergent, then $\sum a_{n}$ is convergent.

## Problem 2

If $0 < a < b < +\infty$, prove that there exists $\theta \in (a, b)$ such that
$$ ae^{b} - be^{a} = (1-\theta)e^{\theta}(a-b). $$

**Proof**. It is equivalent to prove that
$$ \frac{ae^{b} - be^{a}}{a - b} = \frac{\frac{e^{b}}{b} - \frac{e^{a}}{a}}{\frac{1}{b} - \frac{1}{a}} = (1-\theta)e^{\theta}. $$
Applying Cauchy's mean-value theorem yields the conclusion.

## Problem 3

Let $f(x) = \arctan x$, and $A$ be a constant. Prove that if
$$ B = \lim_{n \to \infty} \left( \sum_{k=1}^{n} f (\frac{k}{n}) - An \right) $$
exists and is finite. Evaluate $A$ and $B$.

**Solution**. We know
$$ A = \lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} f(\frac{k}{n}) - \frac{B}{n} = \int_{0}^{1} \arctan x\mathrm{d}x. $$
Use the integration-by-part formula, we get 
$$ \int_{0}^{1} \arctan x \mathrm{d} x = x \arctan x \big|_{0}^{1} - \int_{0}^{1} \frac{x}{1+x^{2}}\mathrm{d}x = \frac{\pi}{4} - \frac{1}{2} \ln 2. $$
And it is not hard to see that $B = 0$.

## Problem 4

If $f \in C(a, b)$, where $(a, b)$ is a finite interval. Prove that $f$ is uniformly continuous on $(a, b)$ if and only if $f(a+0)$ and $f(b-0)$ exist.

**Proof**. Left-to-right: If $f$ is uniformly continuous on $(a, b)$, then
$$ \forall \epsilon > 0, \exists \delta > 0, \forall x_{1}, x_{2}, |x_{1} - x_{2}| < \delta, |f(x_{1}) - f(x_{2})| < \epsilon. $$
We choose $x_{1}, x_{2}$ from $(a, a+\delta)$, then by the Cauchy criterion for convergence, we know $f(a+0)$ exists. Similarly, $f(b-0)$ exists.

Right-to-left: If $f(a+0)$ and $f(b-0)$ exist, then we can extend $f(x)$ to the closed interval $[a, b]$. And by Cantor theorem, we know the extended function is uniformly continuous on $(a, b)$, so is $f(x)$.

## Problem 5

Find the convergence region of $S(x) = \sum \limits _{n = 1}^{+\infty} \frac{x^{2n}}{n(2n+1)}$, and evaluate $S = \sum \limits_{n = 1}^{+\infty} \frac{1}{n(2n+1)2^{n}}$.

**Solution**. Use the Cauchy-Hadamard test, we know the radius of convergence satisfies
$$ \frac{1}{R} = \lim_{n \to \infty} \sqrt[n]{\frac{1}{n(2n+1)}} = 1. $$
And it converges in both right and left endpoints, so the convergence region is $[-1, 1]$. Consider $f_{1}(x) = \sum _{n = 1}^{\infty} \frac{x^{2n}}{n(2n+1)}$, $f_{2}(x) = xf_{1}(x)$, then
$$ f_{2}(x) = \sum \limits_{n = 1}^{\infty}\frac{x^{2n+1}}{n(2n+1)} \Rightarrow f_{2}^{\prime}(x) = \sum \limits_{n = 1}^{\infty} \frac{x^{2n}}{n} \Rightarrow f^{\prime\prime}_{2}(x) = \sum \limits_{n = 1}^{\infty} 2x^{2n-1} = \frac{2x}{1-x^{2}}.$$
Then integrating on both sides yields 
$$ f_{2}^{\prime}(x) = - \ln (1-x^{2}), f_{2}(x) = -(x+\frac{1}{2})\ln(1-x^{2}), f_{1}(x) = - \frac{2x + 1}{2x} \ln(1-x^{2}) $$
And $S = f_{1}(\frac{1}{\sqrt{2}}) = (1 + \frac{\sqrt{2}}{2}) \ln 2$.

## Problem 6

## Problem 7

Calculate the line integral
$$ I = \oint_{C} \frac{x \mathrm{d} y - y\mathrm{d}x}{x^{2} + 8y^{2}}, $$
where $C$ is a circle centered at $(1, 0)$ with radius $R (R > 0, R \neq 1)$, oriented counter-clockwise.

**Solution**. Let $P = \frac{-y}{x^{2} + 8y^{2}}$ and $Q = \frac{x}{x^{2} + 8y^{2}}$, we know that
$$ P_{y} = \frac{-(x^{2} + 8y^{2}) + y \cdot 16 y}{(x^{2} + 8y^{2})^{2}} = \frac{8y^{2} - x^{2}}{(x^{2} + 8y^{2})^{2}}, Q_{x} = \frac{x^{2} + 8y^{2} - 2x^{2}}{(x^{2} + 8y^{2})^{2}} = \frac{8y^{2} - x^{2}}{(x^{2} + 8y^{2})^{2}}. $$
If $R < 1$, then the region bounded by $C$ does not contain the origin, and by Green's theorem we know
$$ I = \iint_{D} Q_{x} - P_{y} \mathrm{d} x \mathrm{d} y = 0. $$
If $R > 1$, then exclude a small region bounded by $L_{1}: x^{2} + 8y^{2} = r^{2}$ with counter-clockwise orientation. The Green's theorem yields
$$ I =  \int_{L_{1}} P\mathrm{d} x + Q\mathrm{d} y = \frac{1}{r^{2}} \int_{L_{1}} x\mathrm{d} y - y\mathrm{d}x,$$
Applying Green's theorem again yields
$$ I = \frac{1}{r^{2}} \iint_{D_{1}} 2 \mathrm{d} x \mathrm{d} y = \frac{\sqrt{2}}{2} \pi. $$

## Problem 8

Discuss the uniform convergence behavior of
$$ f(t) = \int_{0}^{1} \frac{1}{x^{t}} \sin \frac{1}{x} \mathrm{d} x, $$
on $(0, 2)$.

