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

# Series

Speaker: Yixiao Qian

---

# Numerical Series

---

## Concept of Numerical Series

<br>

- **Convergence**: $S_n = \sum_{k=1}^n u_k$ is partial-sum, $S_n$ converges.
- **Necessary Condition**: $\lim \limits _{n \rightarrow \infty} u_n = 0$. (Since $\lim \limits _{n \rightarrow \infty} u_n = \lim \limits _{n \rightarrow \infty} S_n - \lim \limits _{n \rightarrow \infty} S_{n-1} = 0$)
- **Cauchy Criterion**: $\forall \epsilon > 0, \exists N > 0, N < n < n+p$, $|u_{n+1} + \cdots + u_{n+p}| < \epsilon$.

---

## Positive-Term Series

- **Integral Test**: $f$ non-negative and decreasing, then $\displaystyle \sum_{n=1}^{\infty} f(n) \sim \int_1^{+\infty}f(x) \mathrm{d} x$.

<div class=note>

$\sum_{n=1}^{\infty} \frac{1}{n^p}$ converges when $p > 1$, diverges when $p \leq 1$.

</div>

- **Comparison Test**: If $u_n \sim v_n$ when $n \rightarrow \infty$, then $\sum_{n=1}^{\infty} u_n \sim \sum_{n=1}^{\infty}v_n$.
- **Ratio Test**: $\lim \limits _{n \rightarrow \infty} \frac{u_{n+1}}{u_n} = q$. $q<1$ then $\sum u_n$ converges, $q > 1$ then diverges.
- **Root Test**: $\lim \limits _{n \rightarrow \infty} \sqrt[n]{u_n} = q$. $q <１$ then $\sum u_n$ converges, $q > 1$ then diverges.

---

## Applications of Comparison Test

$$
(1) \sum\limits_{n=1}^{\infty} \frac{1}{\sqrt{n^2 + 1}}, \quad
(2) \sum\limits_{n = 1}^{\infty} 2^n \sin \frac{\pi}{3^n}, \quad
(3) \sum\limits_{n = 1}^{\infty} (\sqrt[n]{2} - 1)
$$

<div class=note>

(1) $\frac{1}{n}$ diverges; (2) $\frac{2^n}{3^n} \pi$ converges; (3) $2^{\frac{1}{n}} - 1 \sim \frac{1}{n} \ln 2$ diverges.

</div>

$$
(1) \sum\limits_{n = 1}^{\infty} \frac{1}{3^{\ln n}}, \quad
(2) \sum\limits_{n = 2}^{\infty} \frac{1}{(\ln n)^{\ln n}}, \quad
(3) \sum\limits_{n = 1}^{\infty} \frac{1}{n^{2n \sin \frac{1}{n}}}, \quad
(4) \sum\limits_{n = 1}^{\infty} \frac{\ln(n+1)}{e^n}.
$$

<div class=note>

(1) $\frac{1}{n^{\ln 3}}$ converges; (2) $\frac{1}{n^{\ln(\ln n)}} < \frac{1}{n^2}$ converges; (3) $2 n \sin \frac{1}{n} \sim 2$ converges;
(4) $\ln(n+1) < n^{\epsilon}$, $e^n > n^{\infty}$, converges. (More strictly, $n^2 \frac{\ln(n+1)}{e^n} \rightarrow 0$).

</div>

---

## Application of Inequalities

- $\sum a_n$ is positive-term, is convergent. Prove $\sum \frac{\sqrt{a_n}}{n}$ converges.

<div class=note>

Apply Cauchy-Schwarz inequality $\sum \frac{\sqrt{a_n}}{n} \leq \left( \sum a_n \right)^{1/2} \left( \sum \frac{1}{n^2} \right)^{1/2}$.

</div>


---

## Arbitrary-Term Series

<br>

- **Absolute\&Conditional Convergence**: $\sum\limits_{n = 1}^{\infty} |a_n|$ converges (absolute), else (conditional).
- **Leibniz Test**: $a_n$ decreases to $0$, then $\sum\limits_{n = 1}^{\infty} (-1)^{n-1}a_n$ converges.
- **Dirichlet Test**: (1) $\sum\limits_{k=1}^n a_k$ bounded; (2) $b_n$ decreases to $0$.
- **Abel Test**: (1) $\sum\limits_{n = 1}^{\infty}a_n$ converges; (2) $b_n$ monotone and bounded.

---

## Examples of Arbitrary-Term Series

$$
(1) \sum\limits_{n = 1}^{\infty} \frac{(-1)^n}{n^{p+\frac{1}{n}}}, \quad
(2) \sum\limits_{n = 1}^{\infty} \frac{(-1)^n}{n^p \ln^q n}, \quad
(3) \sum\limits_{n = 1}^{\infty} \sin(n \pi + \frac{1}{n^p}).
$$

<div class=note>

(1) $p > 1$ converges absolutely. $1 \geq p > 0$, $f(x):=x^{p+\frac{1}{x}}$, then $f^{\prime}(x) > 0$ when $x$ is sufficiently large, so converges conditionally. $p \leq 0$, $a_n \not \rightarrow 0$, diverges.
(2) 
(3) $\sin (n\pi + \frac{1}{n^p}) = (-1)^n \sin (\frac{1}{n^p})$. When $p > 1$, absolutely converges; When $1 \geq p > 0$, conditionaly converges; When $p \leq 0$, diverges.

</div>

$$
\sum\limits_{n = 1}^{\infty} \frac{\cos nx}{n^p}, \quad \sum\limits_{n = 1}^{\infty} \frac{\sin nx}{n^p}, \quad \text{where } x \neq k \pi.
$$

<div class=note>

$\sum_{k=1}^n \cos kx$ and $\sum_{k=1}^n \sin kx$ are bounded. $\frac{1}{n^p} \rightarrow 0$. By Dirichlet test, they are convergent.

</div>


---

# Function Sequences

---

## Uniform Convergence of Function Sequence

- **Uniform Convergence**: $\forall \epsilon > 0$, $\exists N > 0$, $\forall n > N$, $|f_n(x) - f(x)| < \epsilon$ holds for all $x \in D$.
- **Cauchy Criterion**: $\forall \epsilon > 0$, $\exists N > 0$, $\forall m,m+p > N$, $|f_{m+p}(x)-f_{m}(x)| < \epsilon$ holds for $x \in D$
- **Criterion for Non-Uniform Convergence**: $\exists \{x_n\}$, $f_n(x_n) - f(x_n) \not \rightarrow 0$.
- **Compact Convergence**: $f_n \rightrightarrows f$ on any closed/compact subset of $D$.

<div class=note>

Compact convergence implies all results (continuity, integrability, etc) on open set.

</div>

- **Weiestrass Test**: If $|f(x) - f_n(x)| \leq a_n$ for all $x$, $\lim \limits _{n \rightarrow \infty} a_n = 0$ is positive-term, then $f_n \rightrightarrows f$
- **Closure under Operations**: $kf_n$, $f_n+g_n$, $f_ng_n$ (if bounded), $1/f_n$ (if no roots).
- **Uniform Boundedness**: $\exists M > 0$, $\forall n > 0$, $|f_n(x)| \leq M$ for all $x$.
- **Boundedness of Limit Function**: If $f_n \rightarrow f$ pointwisely. Then $f_n \rightrightarrows f$, $f_n$ bounded > $f_n$ uniformly bounded > $f$ bounded.

---

## Determine if A Function Converges Uniformly

$$
(1) \sin \frac{x}{n}, \quad
(2) \frac{x}{1+n^2x^2}, \quad
(3) \frac{nx}{1+n^2x^2}.
$$

<div class=note>

(1) $f = 0$; Take $x_n = n$, $f_n(x_n) = \sin 1 \neq f(x_n)$, so not uniformly convergent; But it converges uniformly on any closed subset.
(2) $f = 0$; $|f_n - f| \leq \frac{1}{2n} \rightarrow 0$, then uniformly convergent.
(3) $f = 0$; Take $x = \frac{1}{n}$, $f_n(x_n) = \frac{1}{2} \neq f(x_n)$, not uniformly convergent.

</div>

- Determine if $f_n = x^n \ln x$ is uniformly convergent on $(0, 1]$.

<div class=note>

(1) Limit function is $f = 0$; Define $g_n(x) = |f_n| = - x^n \ln x$.
(2) Find Extreme: $g_n^{\prime}(x) = x^{n-1}(-n\ln x - 1)$, $\max_{x \in (0, 1)} g_n(x) = g_n(e^{- \frac{1}{n}}) = \frac{1}{ne}$.
(3) Apply M-Test: $|f_n(x)| \leq \frac{1}{ne} \rightarrow 0$, so $f_n \rightrightarrows 0$.

</div>


---

## Uniform Convergence of Picard Sequence

- If $f \in C[a, b]$, $f_0(x) = f(x)$, $\displaystyle f_{n+1}(x) = \int_a^x f_n(t)\mathrm{d} t$, prove $f_n(x)$ is uniformly convergent.

<div class=note>

(1) $|f(x)| \leq M$, so $\displaystyle |f_1(x)| \leq \int_a^x |f_0(t)|\mathrm{d} t \leq M(x-a)$;
(2) $\displaystyle |f_2(x)| \leq \int_a^x |f_1(t)|\mathrm{d} t = M [\frac{1}{2}x^2 - ax + \frac{1}{2}a^2] = \frac{(x-a)^2}{2}M$.
(3) Similarly, $\displaystyle |f_n(x)| \leq \int_a^x |f_{n-1}(t)|\mathrm{d} t \leq \frac{(x-a)^n}{n!}M \leq \frac{(b - a)^n}{n!}M \rightarrow 0$.

</div>


---

## Uniform Convergence of Derivative

- $f^{\prime}$ is continuous, $a_n \nearrow +\infty$ is positive. Prove $f_n = a_n \left[ f(x + \frac{1}{a_n}) - f(x) \right] \rightrightarrows f^{\prime}(x)$ on $[a, b]$

<div class=note>

(1) By Lagrange mean-value theorem, $\exists \xi_n < \frac{1}{a_n}$ such that $f_n(x) = f^{\prime}(x + \xi_n)$.
(2) $f^{\prime} \in C[a, b]$ and uniformly continous. $\forall \epsilon > 0$, $\exists \delta > 0$, $|x_1 - x_2| < \delta$, $|f^{\prime}(x_1) - f^{\prime}(x_2)| < \epsilon$.
(3) Since $a_n \nearrow \infty$, $\exists N > 0$, $\forall n > N$, $\xi_n < \frac{1}{a_n} < \delta$, then
$$|f_n(x) - f^{\prime}(x)| = |f^{\prime}(x + \xi_n) - f^{\prime}(x)| < \epsilon.$$

</div>

- **Common Example**: $n \left[ f(x+\frac{1}{n}) - f(x) \right] \rightrightarrows f^{\prime}(x)$.

<div class=note>

This formula indicates that ${\displaystyle \lim \limits _{n \rightarrow \infty} \frac{f(x + \frac{1}{n}) - f(x)}{1/n} = f^{\prime}(x)}$ is uniform.

</div>

---

## Uniform Convergence of Integral

- $f$ is continuous, $f_n(x) = \frac{1}{n} \sum\limits_{k = 1}^n f \left( x + \frac{k}{n} \right)$, $\displaystyle F(x) = \int_0^1 f(x+t)\mathrm{d} t$. Prove that $f_n \rightrightarrows F$ on any closed interval $[a, b]$.

<div class=note>

(1) Write $\displaystyle F(x) = \sum_{k=1}^n \int_{\frac{k-1}{n}}^{\frac{k}{n}} f(x+t)\mathrm{d} t$, then
$$|f_n(x) - F(x)| \leq \sum_{k=1}^n \int_{\frac{k-1}{n}}^{\frac{k}{n}} \left| f(x + \frac{k}{n}) - f(x+t) \right|\mathrm{d} t.$$
(2) $f$ is uniformly continuous on $[a, b]$. $\forall \epsilon > 0$, $\exists \delta > 0$, $|x_1 - x_2| < \delta$, $|f(x_1) - f(x_2)| < \epsilon$.
(3) Take $\frac{1}{n} < \delta$, then $|f(x+\frac{k}{n}) - f(x+t)| < \epsilon$ for $t \in (\frac{k-1}{n}, \frac{k}{n})$, and $|f_n(x) - F(x)| < \epsilon$.

</div>

---

## Properties of Limit Function: Continuity

- **Local Continuity**: $f_n \rightrightarrows f$ on $(a, b)$, $\lim \limits _{x \rightarrow x_0}f_n(x) = a_n$, then $\lim \limits _{x \rightarrow x_0}f(x) = \lim \limits _{n \rightarrow \infty} a_n$. 

<div class=note>

Note: The result can also be written as $\lim \limits _{n \rightarrow \infty} \lim \limits _{x \rightarrow x_0} f_n(x) = \lim \limits _{x \rightarrow x_0} \lim \limits _{n \rightarrow \infty} f_n(x)$.
(1) Existence of $\lim \limits _{n \rightarrow \infty} a_n$: By $f_n \rightrightarrows f$, then $\forall \epsilon > 0$, $\exists N > 0$, $\forall m,n > N$, $|f_n(x) - f_m(x)| < \epsilon$. Take $x \rightarrow x_0$, then $|a_n - a_m| < \epsilon$, which means $A = \lim \limits _{n \rightarrow \infty} a_n$ exists (Cauchy's criterion).
(2) $\lim \limits _{x \rightarrow x_0}f(x) = A$: $|f(x) - A| \leq |f(x) - f_n(x)| + |f_n(x) - a_n| + |a_n - A| < 3\epsilon$.

</div>

- **Global Continuity**: $f_n \rightrightarrows f$ on any closed subset, $f_n$ continuous, then $f$ is continuous. ($f_n \rightrightarrows f$ on the entire $(a, b)$ is stronger)

</div>

- **Uniform Continuity**: $f_n$ uniformly continuous, $f_n \rightrightarrows f$, then $f$ is uniformly continuous.

<div class=note>

Consider $|f(x_1) - f(x_2)| \leq |f(x_1) - f_n(x_1)| + |f_n(x_1) - f_n(x_2)| + |f_n(x_2) - f(x_2)| < 3 \epsilon$.

</div>

---

## Properties of Limit Function: Integrability

- **Term-by-Term Integration**: $f_n \rightrightarrows f$ on $[a, b]$, $f_n$ integrable on $[a, b]$. Then $f(x)$ integrable
$$ \int_a^b f(x)\mathrm{d} x = \lim \limits _{n \rightarrow \infty} \int_a^b f_n(x)\mathrm{d} x. $$

<div class=note>

(1) Integrability: $\forall \epsilon >0$, $\exists N > 0$, $\forall n > N$, $|f(x) - f_n(x)| < \epsilon$. Then
$$
\begin{align}
  |f(x_1) - f(x_2)| &\leq |f(x_1) - f_n(x_1)| + |f_n(x_1) - f_n(x_2)| + |f_n(x_2) - f(x_2)|\\
                    &\leq \epsilon + \omega_i^{f_n} + \epsilon = \epsilon^{\prime}.
\end{align}
$$
(2) Value of Integral: $\displaystyle \left| \int_a^b f_n(x)\mathrm{d} x - \int_a^b f(x)\mathrm{d} x \right| \leq \int_a^b |f_n(x) - f(x)|\mathrm{d} x < \epsilon$.

</div>

- **Corollary**: If $f_n(x) \rightrightarrows f$, $f_n$ are integrable, then $f$ is integrable and for any integrable $g(x)$
$$ \int_{x_0}^x f_n(t)g(t)\mathrm{d} t \rightrightarrows \int_{x_0}^x f(t)g(t)\mathrm{d} t. $$

---

## Properties of Limit Function: Differentiability

- **Term-by-Term Differentiation**: $f_n^{\prime}$ are continuous, $f_n^{\prime} \rightrightarrows g$, there exists $x_0$ that $f_n(x_0)$ converges. Then $f_n(x) \rightrightarrows f$, and
$$ f^{\prime}(x) = \lim \limits _{n \rightarrow \infty} f_n^{\prime}(x). $$

<div class=note>

We know $\displaystyle f_n(x) = f_n(x_0) + \int_{x_0}^x f_n^{\prime}(t)\mathrm{d} t$ and $\displaystyle \int_{x_0}^x f_n^{\prime}(t)\mathrm{d} t \rightrightarrows \int_{x_0}^x g(t)\mathrm{d} t$. Then
$$ f(x) = \lim \limits _{n \rightarrow \infty} f_n(x_0) + \int_{x_0}^x g(t)\mathrm{d} t \Rightarrow f^{\prime}(x) = g(x). $$

</div>

---

# Function Series

---

## Uniform Convergence of Function Series

- **Uniform Convergence**: $\sum_{n=1}^{\infty}u_n(x) \rightrightarrows S(x)$ iff $S_n(x) = \sum\limits_{k=1}^n u_n \rightrightarrows S(x)$.
- **Definition**: $\forall \epsilon > 0$, $\exists N > 0$, $\forall n > N$, $|S(x) - \sum\limits_{k=1}^n u_k(x)| = |\sum\limits_{k=n+1}^{\infty}u_k(x)| < \epsilon$ for all $x \in D$.
- **Cauchy's Criterion**: $\forall \epsilon > 0$, $\exists N > 0$, $\forall n > m > N$, $|\sum\limits_{k=m+1}^n u_k(x)| < \epsilon$ for all $x \in D$.
- **Uniform Convergence of Each Term**: If $\sum\limits_{n=1}^{\infty}u_n(x)$ converges uniformly, then $u_n \rightrightarrows 0$.
- **M-Test**: If $\sum\limits_{n=1}^{\infty}M_n$ converges, $|u_n(x)| \leq M_n$ for all $x$. Then $\sum\limits_{n=1}^{\infty}u_n(x)$ converges uniformly.
- **Dirichlet Test**: If $\sum_{k=1}^nu_k(x)$ is uniformly bounded; $v_k(x) \rightrightarrows 0$, is monotone with respect to $n$ when fixing $x$.
- **Abel Test**: If $\sum_{n=0}^{\infty}u_n(x)$ converges uniformly; $v_n(x)$ is uniformly bounded and monotone with respect to $n$ when fixing $x$.

---

## Properties of Limit Function

- **Continuity**: $\sum u_n(x) \rightrightarrows S(x)$ on $[a, b]$, $u_n$ continuous, then $S(x)$ continuous on $[a,b]$
$$ \sum (\lim \limits _{x \rightarrow x_0} u_n(x)) = \lim \limits _{x \rightarrow x_0}(\sum u_n(x)). $$
- **Integrability**: $\sum u_n(x) \rightrightarrows S(x)$ on $[a, b]$, $u_n(x)$ continuous, then
$$ \sum \int_a^b u_n(x)\mathrm{d} x = \int_a^b \sum u_n(x)\mathrm{d} x. $$
- **Differentiability**: $u^{\prime}_n$ continuous, $\sum u_n(x_0)$ converges, $u^{\prime}_n(x) \rightrightarrows g(x)$. Then
$$ \sum u^{\prime}_n(x) = (\sum u_n(x))^{\prime}. $$

---

# Power Series

---

## Radius of Convergence

- **Radius of Convergence**: $|x| < R$, $\sum a_nx^n$ converges absolutely; $|x| > R$, $\sum a_nx^n$ diverges.
- **Cauchy-Hadamard Test and Ratio Test**: $\frac{1}{R} = \lim \limits _{n \rightarrow \infty} \sqrt[n]{|a_n|}$, $\frac{1}{R} = \lim \limits _{n \rightarrow \infty} \frac{|a_{n+1}|}{|a_n|}$.
- Find the Convergence Region: (1) $\sin x$ and $\cos x$, (2) $e^x$, (3) $\ln (1+x)$, (4) $\frac{1}{1-x}$.

<div class=note>

(1) $\sin x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!}$, $\frac{1}{R} = \sqrt[n]{\frac{1}{(2n+1)!}} \rightarrow 0$, then $R = \infty$. So is $\cos x$.
(2) $e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}$, $\frac{1}{R} = \sqrt[n]{\frac{1}{n!}} \rightarrow 0$. Then $R = \infty$.
(3) $\ln x = \sum_{n=1}^{\infty} (-1)^{n-1} \frac{x^n}{n}$, $\frac{1}{R} = \sqrt[n]{\frac{1}{n}} \rightarrow 1$. Then $R = 1$. The convergence region is $(-1,1]$.
(4) $\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n$, $\frac{1}{R} = \sqrt[n]{1} = 1$. The convergence region is $(-1,1)$.

</div>

---

## Uniform Convergence of Power Series

- **Closed Interval**: $\sum a_nx^n$ uniformly converges in any $[a, b] \subset (x_0-R, x_0+R)$

<div class=note>

(1) Define $c = \max \{|a|, |b|\}$, $c \in (-R, R)$. Then $\forall x \in [a, b]$, $|a_nx^n| \leq |a_nc^n|$.
(2) Since $\sum a_nc^n$ converges, then $\sum a_nx^n$ is uniformly convergent. (M-Test)

</div>

- **Generalized Abel Theorem**: If $\sum a_n c^n$ and $\sum a_nd^n$ converges, then $\sum a_nx^n$ uniformly converges in $[c, d]$.
- **Corollary**: If $\sum a_n R^n$ converges, then for any $a \in (-R, R)$, $\sum a_nx^n$ uniformly converges in $[a, R]$.

---

## Practice on Uniform Convergence of Power Series

- $f(x) = \sum_{n=1}^{\infty} \frac{x^n}{n^2 \ln(n+1)}$. Prove (1) $f \in C[0,1]$, $f^{\prime} \in C(-1,1)$; (2) $f^{\prime}_+(-1)$ exists; (3) $f^{\prime}_-(1)$ does not exist.

<div class=note>

(1) $f(1) = \sum \frac{1}{n^2 \ln (n+1)}$ converges, $\sum \frac{x^n}{n^2 \ln (n+1)}$ uniformly converges in $[0, 1]$. So $f \in C[0, 1]$.
(2) $f^{\prime}(x) = \sum \frac{x^{n-1}}{n \ln (n+1)}$, $\sum \frac{x^{n-1}}{n \ln (n+1)}$ uniformly converges in closed subset of $(0, 1)$, then $f^{\prime}(x) \in C(-1, 1)$.
(3) $\sum \frac{(-1)^{n-1}}{n \ln (n+1)}$ converges, then $f_+^{\prime}(-1)$ exists. $\sum \frac{1}{n \ln(n+1)}$ diverges, so $f_-^{\prime}(1)$ does not exist.

</div>




---

## Sum Function of Power Series




---

## Power Series Expansion

- **Expansion of Rational Functions**: $f(x) = \frac{x^2}{x^2 - 3x + 2}$

<div class=note>

(1) Decompose: $\frac{x^2}{x^2-3x+2} = 1 + \frac{4}{x-2} - \frac{1}{x-1}$ (Method of Undetermined Coefficients)
(2) $\frac{1}{x-2} = -\frac{1}{2} \cdot \frac{1}{1 - \frac{x}{2}} = - \frac{1}{2} \sum\limits_{n=0}^{\infty} \left( \frac{x}{2} \right)^n$ and $\frac{1}{x-1} = - \frac{1}{1-x} = - \sum\limits_{n = 0}^{\infty} x^n$.

</div>

- **Take Integration**: $f(x) = \frac{1}{(1+x)^2}$.

<div class=note>

Consider $\displaystyle F(x) = \int_0^x \frac{1}{(1+t)^2}\mathrm{d} t$. Then $F(x) = -\frac{1}{1+x} + 1 = 1 - \sum_{n=0}^{\infty} (-x)^n$. $f(x) = F^{\prime}(x)$.

</div>

- **Take Derivative**: (1) $f(x) = \arctan x$, (2) $f(x) = \arctan \frac{1-kx}{1+kx}$.

<div class=note>

(1) $f^{\prime}(x) = \frac{1}{1+x^2} = \sum_{n=0}^{\infty}(-1)^nx^{2n}$. Then $f = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1}$. (2) $f = \arctan 1 - \arctan kx$.

</div>



