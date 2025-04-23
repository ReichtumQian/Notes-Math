
# Peking Institution of Technology Mathematical Analysis 2021

## Problem 1

(1) Find $\lim \limits _{x \rightarrow 0} \frac{e^x \sin x - x (1+x)}{x^3}$.

**Solution**. Use the Taylor expansion, $e^x = 1 + x + \frac{x^2}{2} + o(x^2)$ and $\sin x = x - \frac{1}{6}x^3 + o(x^3)$. Then
$$ \lim \limits _{x \rightarrow 0} \frac{x + x^2 + \frac{1}{3} x^3 - x (1 + x) + o(x^3)}{x^3} = \frac{1}{3}. $$

(2) Find $\lim \limits _{n \rightarrow \infty} \left( \cos \frac{1}{n} \right)^{n^2}$.

**Solution**. Use the Taylor expansion, we know $\cos x = 1 - \frac{1}{2}x^2 + o(x^2)$, then
$$ \lim \limits _{n \rightarrow \infty} (\cos \frac{1}{n})^{n^2}
= \lim \limits _{n \rightarrow \infty} \left[ (1 - \frac{1}{2n^2})^{-2n^2} \right]^{-1/2} = e^{-\frac{1}{2}}.$$

(3) Let $y = f(x) = 2x - \frac{1}{2} \cos x$, find the derivative of $x = f^{-1}(y)$ at $y = - \frac{1}{2}$.

**Solution**. When $y_0 = -\frac{1}{2}$, $x_0 = 0$. Then
$$ x^{\prime}(y_0) = \frac{1}{y^{\prime}(x_0)} = \frac{1}{2}. $$

(4) Given $I(y) = \int_{y^2}^{y^3} e^{-x^2y} \mathrm{d} x$, find $I^{\prime}(y)$.

**Solution**. 

## Problem 2

(1) Prove that $\cos x < 1 - \frac{x^2}{2!} + \frac{x^4}{4!}$

**Proof**. $\cos x = \sum\limits_{n = 0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!}$, then not hard to see.

(2) Prove that $(b - a)^2 - \left( \int_a^b \cos x\mathrm{d} x \right)^2 - \left( \int_a^b \sin x \mathrm{d}x  \right)^2 < \frac{(b-a)^4}{12}.$

**Proof**. Use the result of (1).

## Problem 3

Find the radius of convergence, convergent region, sum function of $\sum\limits_{n = 0}^{\infty} \frac{x^n}{2^n(n+1)}$.

**Solution**. (1) Use the root test, $R = 2$. (2) When $x = 2$, the series is $\sum \frac{1}{n+1}$, which is divergent. When $x = -2$, the series is $\sum \frac{(-1)^n}{n+1}$, which is convergent using the Leibniz's test. Therefore, the convergent region is $[-2, 2)$. (3) Let $f(x) = \sum\limits_{n = 0}^{\infty} \frac{(x/2)^n}{n+1}$, $g(t) = \sum\limits_{n = 0}^{\infty} \frac{t^n}{n+1}$, let
$$h(t) = tg(t) = \sum\limits_{n = 0}^{\infty} \frac{t^{n+1}}{n+1} \Rightarrow h^{\prime}(t) = \sum\limits_{n = 0}^{\infty} t^n = \frac{1}{1-t}. $$
So $h(t) = - \ln(1-t)$, $g(t) = - \frac{\ln(1-t)}{t}$, $f(x) = - \frac{\ln(1-x/2)}{x/2}$.

## Problem 4

Suppose $f(x)$ is continuous at $x_0$, $|f(x)|$ is differentiable at $x_0$, prove that $f(x)$ is differentiable at $x_0$.

**Proof**. If $f(x_0) \neq 0$, without loss of generality, we assume that $f(x) > 0$. Since $f(x)$ is a continuous function, there exists $\delta > 0$ such that for all $x \in (x_0 - \delta, x_0 + \delta)$, $f(x) > 0$. In this case, according to definition of differentiability, $f(x)$ is differentiable at $x_0$ if and only if $|f(x)|$ is differentiable at $x_0$.

On the other hand, if $f(x_0) = 0$, then the differentiability of $|f(x)|$ yields the existence of
$$ \lim \limits _{h \rightarrow 0} \frac{|f(x_0+h)| - |f(x_0)|}{h} = \lim \limits _{h \rightarrow 0} \frac{|f(x_0+h)|}{h} $$
When $h$ approximates $0^-$, assume the limit is $A$. Then when $h$ approaximates $0^+$, the limit is $-A$. Since the existence of the limit, we know $A = -A$, i.e., $A = 0$. Then the limit
$$ \lim \limits _{h \rightarrow 0} \frac{f(x_0 + h) - f(x_0)}{h} = 0.$$

## Problem 5

Prove that the improper integral
$$ \int_0^{+\infty} \frac{e^{\sin x} \sin 2x}{x^{p}} \mathrm{d} x$$
is absolutely convergent when $1 < p < 2$, and conditionally convergent when $0 < p \leq 1$, and diverges otherwise.

**Proof**. Consider two regions, $(0, 1)$ and $(1, +\infty)$. Consider $(0, 1)$ first, when $x \rightarrow 0$, $\frac{e^{\sin x} \sin 2x}{x^p} \sim \frac{2}{x^{p-1}}$, so absolutely converges when $p-1 < 1$, i.e., $p < 2$, diverges when $p \geq 2$.

Next, we consider $(1, +\infty)$, take the absolute value, then
$$ \int_1^{+\infty} \left| \frac{e^{\sin x} \sin 2x}{x^p} \right| \mathrm{d} x \leq \int_1^{+\infty} \frac{e}{x^p}\mathrm{d} x,$$
so the improper integral is absolutely convergent if $p > 1$. When $1 \geq p > 0$, by Dirichlet test, $F(y) = \int_1^y e^{\sin x} \sin 2x\mathrm{d} x$ is bounded and $\frac{1}{x^p}$ monotonically decreases to zero, so it is conditionally convergent.












