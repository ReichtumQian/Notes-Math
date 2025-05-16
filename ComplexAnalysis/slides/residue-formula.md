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

# Residue Formula

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Taylor Expansion and Laurent Expansion
- Concept of Residue
- Residue Formula and Its Applications
- Argument Principle and Applications

---

# Taylor Expansion and Laurent Expansion

---

## Taylor Expansion

- **Taylor Expansion**: Given $z_0 \in \mathbb{C}$, $f$ is holomorphic in $|z-z_0| < R$ (include $z_0$), then
$$ f(z) = \sum\limits_{n = 0}^{\infty} a_n(z-z_0)^n, \quad |z - z_0| < R. $$
- **Maximum Radius**: Let $R_{z_0}$ be the convergence radius of series at $z_0$,
$$ R_{z_0} = \sup \{R: f \text{ is holomorphic in } |z - z_0| < R\}. $$
- **Global Convergence**: Taylor series of entire functions converge globally. E.g., $e^z, \sin z$.
- **Local Convergence**: $\frac{1}{z-1}$ is convergent in $|z| < 1$ since $z = 1$ is a pole.

---

## Expand Functions to Taylor Series

- Expand $f(z) = \frac{1}{z-2} + e^{-z}$ at the origin, and find the convergence radius.

<div class=note>

(1) $\frac{1}{z-2} = - \frac{1}{2} \cdot \frac{1}{1-\frac{z}{2}} = - \frac{1}{2} \sum\limits_{n = 0}^{\infty} \left( \frac{z}{2} \right)^n$. (2) $e^{-z} = \sum\limits_{n = 0}^{\infty} \frac{(-1)^nz^n}{n!}$ (3) Convergence radius is $2$.

</div>

---

## Laurent Expansion, Singularities and Zeros

- **Laurent Expansion**: $z_0 \in \mathbb{C}$ (it can be a singularity of $f$), $f$ is holomorphic in $r < |z-z_0| < R$, it is uniquely represented as $f(z) = \sum_{n=-\infty}^{+\infty} a_n(z-z_0)^n$.

<div class=note>

$$ \sum_{n=0}^{\infty} a_n(z-z_0)^n \text{ is analytic part} \quad
\sum_{n=-\infty}^{-1}a_n(z-z_0)^n \text{ is principal part}.$$

</div>

- **Removable Singularity**: $f(z) = \sum_{n=0}^{+\infty} a_n(z-z_0)^n$, then $f(z_0) = a_0$.
- **Pole Singularity Order $m$**: $f(z) = \sum_{n=-m}^{+\infty} a_n(z-z_0)^n$, $f(z_0) \rightarrow \infty$, $(z-z_0)^mf(z_0) = a_{-m}$.
- **Isolated Singularity**: $z_0$ is a pole, $f$ is holomorphic in a punctured neighborhood.
- **Essential Singularity**: $f(z) = \sum_{n=-\infty}^{+\infty}a_n(z-z_0)^n$, then $\forall m, (z - z_0)^mf(z_0) \rightarrow \infty$.
- **Zeros of Order $m$**: $f(z) = \sum_{n=m}^{+\infty} a_n(z-z_0)^n$.

---

## Expand Functions to Laurent Series

- Expand $f(z) = \frac{1}{(z-1)^2}$ in $1 < |z| < +\infty$.

<div class=note>

It is equivalent to expand $f(z) = \frac{1}{z^2(1-\frac{1}{z})^2}$ in $|\frac{1}{z}| < 1$. We know when $|x| < 1$,
$$ \frac{1}{(1+x)^2} = \sum\limits_{n = 0}^{\infty} (-1)^{n} (n+1) x^n. $$
Then $f(z) = \frac{1}{z^2} \cdot \sum\limits_{n=0}^{\infty}(n+1) \frac{1}{z^n} = \sum\limits_{n = 0}^{\infty} (n+1)\frac{1}{z^{n+2}}$.

</div>

---

## Practice on Zeros

- $D = \{|z| < 1\}$, $f(z)$ defined on $D$. If $f^2$ and $f^3$ are holomorphic in $D$. Prove that $f(z)$ is also holomorphic.

<div class=note>

(1) For $z_0 \in D$ that $f(z_0) \neq 0$: $f(z_0) = \frac{f^3}{f^2}$ is holomorphic.
(2) For $z_0 \in D$ that $f(z_0) = 0$: Suppose $z_0$ is an $m$-order zero, then
$$ f^2(z) = (z-z_0)^{2m}\varphi(z), \quad f^3(z) = (z-z_0)^{3m}\psi(z). $$
$f(z) = \frac{f^3}{f^2} = (z-z_0)^m \frac{\varphi(z)}{\psi(z)}$, where $\varphi(z)$ and $\psi(z)$ are holomorphic. Then so is $f(z)$.

</div>

---

# Concept of Residue

---

## Definition and Representation of Residue

- **Definition**: Given $f(z) = \sum\limits_{n=-\infty}^{+\infty}a_n(z-z_0)^n$, $a_{-1}$ for $z_0 \neq \infty$, $-a_{-1}$ for $z_0 = \infty$.
- **Representation at $z_0 \neq \infty$**: If $z_0$ is $m$-order pole, define $\varphi(z) = (z-z_0)^mf(z)$, then
$$ \operatorname{res}_{z_0} f = \lim \limits _{z \rightarrow z_0} \frac{\varphi^{(m-1)}(z)}{(m-1)!}.$$
- **Representation at $z_0 = \infty$**: If $z_1,\cdots,z_n$ are finite singularities
$$ \operatorname{res}_{z_0} f = - \sum\limits_{k=1}^n \operatorname{res}_{z_k} f.$$

---

## Calculate the Residue

- $f(z) = \frac{e^z - 1}{z^5}$ at $z = 0$.

<div class=note>

</div>

- $f(z) = \frac{1}{\sin \frac{1}{z}}$ at its poles.

<div class=note>

</div>

- $f(z) = \frac{1}{e^{z-1}}$ at $z = 1$ and $z = \infty$.

<div class=note>

$z = 1$: $1$.
$z = \infty$: $-1$.
</div>

---

# The Residue Formula

---

## The Residue Formula

<br>

- **Residue Formula**: Only one pole, then
$$ \int_C f(z)\mathrm{d} z = 2 \pi i \operatorname{res}_{z_0} f$$
- **Cauchy Residue Formula**: Poles $z_1,\cdots,z_n$, then
$$ \int_C f(z) \mathrm{d} z = 2 \pi i \sum\limits_{k = 1}^n \operatorname{res}_{z_k} f.$$

---

## Calculate Integrals using Residue Formula

- ${\displaystyle \frac{1}{2\pi i}\int_C \frac{e^z}{z(1-z)^3}\mathrm{d} z}$ where $C$ is a closed contour does not pass through $z = 0$ and $z = 1$.
- ${\displaystyle \int_{|z| = 1} \frac{\tan \pi z}{z^3}\mathrm{d} z}$.
- ${\displaystyle \int_{|z| = \frac{5}{2}} \frac{1}{(z-3)(z^5 - 1)}\mathrm{d} z}$.

---

# Applications of the Residue Formula

---

## Integrating Trigonometric Rational Functions

<div class=trick>

$$ \int_0^{2\pi} R(\cos \theta, \sin \theta)\mathrm{d} \theta = \int_{|z| = 1} R \left( \frac{z + z^{-1}}{2}, \frac{z - z^{-1}}{2} \right) \cdot \frac{1}{iz}\mathrm{d} z. $$
</div>

- ${\displaystyle \int_0^{2\pi} \frac{1}{a + \cos \theta}\mathrm{d} \theta}$, where $a > 1$.

<div class=note>

</div>

- ${\displaystyle \int_0^{2\pi} \sin^{2n}x \mathrm{d} x}$ where $n \in \mathbb{N}$.

---

## Integrating Rational Functions

<div class=trick>

Let $f(z) = \frac{P(z)}{Q(z)}$, where $(P(z), Q(z)) = 1$, $\operatorname{deg}(Q) \geq \operatorname{deg}(P) + 2$, $Q$ has no roots on $\mathbb{R}$, then
$$ \int_{-\infty}^{+\infty} f(x)\mathrm{d} x = 2 \pi i \sum \operatorname{res}_{z=a_k} f(z), $$
where $a_k$ are residues of $f(z)$ satisfying $\operatorname{Im}(a_k) > 0$.
</div>

- ${\displaystyle \int_0^{+\infty} \frac{x^2}{(x^2 + 1)(x^2 + 4)}\mathrm{d}x}$

- ${\displaystyle \int_{-\infty}^{+\infty} \frac{x^2}{(x^2 + a^2)^2}\mathrm{d} x}$

---

# Argument Principle and Applications

---

## Winding Number

- **Winding Number**: Given $\gamma: [a, b] \rightarrow \mathbb{C}$, and $c \in \mathbb{C}$ not on $\gamma$. Define $\theta(t) = \operatorname{arg}(\gamma(t) - c)$ and $\Delta (\gamma, c) = \theta(b) - \theta(a)$. The *winding number* is $w(\gamma, c) = \frac{\Delta(\gamma, c)}{2 \pi} \in \mathbb{Z}$.

<div class=note>

If $\gamma$ is closed, then the winding number is an integer.

</div>

- **Integration Representation**: $\gamma: [a, b] \rightarrow \mathbb{C}$ closed, $c \not \in \gamma$, then
$$ w(\gamma, c) = \frac{1}{2\pi i} \int_{\gamma} \frac{\mathrm{d} \zeta}{\zeta - c}. $$

---

## Argument Principle and Its Generalizations

- **Meromorphic**: $f$ is holomorphic except poles at $\{z_0,z_1,\cdots\}$, which have no limit points.
- **Argument Principle**: $f$ meromorphic, $C$ closed contour. $f$ has no poles and never vanishes on $C$. $N_z$ the number of zeros of $f$ inside $C$, $N_p$ the poles (counted with multiplicities).
$$ \frac{1}{2\pi i} \int_C \frac{f^{\prime}(z)}{f(z)}\mathrm{d} z = N_z - N_p $$
- **Rouche's Theorem**: $f, g$ holomorphic, $C$ closed contour, $|f| > |g|$ for all $z \in C$. Then $N_z(f) = N_z(f+g)$ inside $C$.
- **Open Mapping Theorem**: $f$ holomorphic and non-constant, then $f$ is open.

---

## Proof of Fundamental Theorem for Algebra

- Apply argument principle to prove fundamental theorem for algebra.

<div class=note>

(1) Take sufficiently large $R$ such that all the roots of $P(z)$ lie in $|z| < R$. Then
$$ N = \frac{1}{2 \pi i} \oint_C \frac{P^{\prime}(z)}{P(z)}\mathrm{d} z = \frac{1}{2\pi i}\oint _C \frac{n}{z}\mathrm{d} z + \frac{1}{2\pi i} \oint_C \frac{Q^{\prime}(z)}{1 + Q(z)} \mathrm{d} z := I_1 + I_2. $$
(2) Here $Q(z) = \frac{a_{n-1}}{z} + \frac{a_{n-2}}{z^2} + \cdots + \frac{a_0}{z^n}$, $|Q(z)| < 1$ (When $R$ is sufficiently large)
(3) Calculate the integrals, $I_1 = n$ and $Q^{\prime}(z) \sim R^{-2}$ when $R \rightarrow \infty$
$$ \left| \oint_C \frac{Q^{\prime}(z)}{1 + Q(z)}\mathrm{d} z \right| \leq 2 \pi R \cdot \max \left| \frac{Q^{\prime}(z)}{1 + Q(z)} \right| \rightarrow 0 $$
(4) When $R$ is sufficiently large, the number of roots is $n$.

</div>

---

## Proof of Fundamental Theorem for Algebra

- Apply Rouche's theorem to prove fundamental theorem for algebra.

<div class=note>

Consider $f(z) = z^n$ and $g(z) = a_{n-1}z^{n-1} + \cdots + a_0$, $P(z) = f(z) + g(z)$. Take sufficiently large $R$ such that on $|z| = R$
$$ |f(z)| = R^n > (|a_{n-1}| + \cdots + |a_0|)R^{n-1} \geq |g(z)|.$$
Then $N_z(P) = N_z(f)$, and $z^n = 0$ has $n$ roots in $C$ ($z=0$ of multiplicity $n$), $P$ has $n$ roots.

</div>


---

## Apply Rouche's Theorem to Find Number of Roots

- Find the number of roots of $z^5 - 5z^3 - z + 3 = 0$ in unit disk.

<div class=note>

(1) $f = -5z^3+3$ and $g = z^5 - z$. On $|z| = 1$, $|f| \geq |5|-|3| = 2$, $|g| \leq 2$. Then $|f| \geq |g|$.
(2) Note when $|g(z_0)| = 2$, $z_0^4 = 1$, $z_0^3 \neq -1$, so $|f(z_0)| > 2 = |g(z_0)|$. Thus $|f| > |g|$.
(3) By Rouche's theorem, the number of roots of $f+g$ is equal to that of $f$, i.e., $3$.

</div>

- Find the number of roots of $z^8 + e^z + 6z + 1 = 0$ in $1 < |z| < 2$.

<div class=note>

Consider $f_1 = 6z$, $g_1 = z^8+e^z+1$; $f_2 = z^8$, $g_2 = e^z + 6z + 1$. $F = f_1 + g_1 = f_2 + g_2$.

(1) $|z| = 1$: $|f_1| = 6$, $|g_1| \leq 2+e$, then $|f_1| > |g_1|$. By Rouche, $F$ has $1$ roots inside $|z| = 1$
(2) $|z| = 2$: $|f_2| = 256$, $|g_2| \leq e^2+13$, then $|f_2| > |g_2|$. By Rouche, $F$ has $8$ roots inside $|z| = 2$
In conclusion, $F$ has $8 - 1 = 7$ roots in $1 < |z| < 2$.

</div>

---

