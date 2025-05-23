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

- Residue Formula and Its Applications
- Argument Principle and Applications

---

# Residue Formula and Its Applications

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

$z = 0$ is a $4$-order pole. $\varphi(z) = z^4 f(z) = \frac{e^z - 1}{z} = \sum\limits_{n=1}^{\infty} \frac{z^{n-1}}{n!}$. So $\varphi^{(3)}(0) = \frac{1}{4}$, then $\operatorname{res}_{z=0}f = \frac{1}{24}$.

</div>

- $f(z) = \frac{1}{\sin \frac{1}{z}}$ at its poles.

<div class=note>

(1) Poles: $\sin \frac{1}{z} = 0$, i.e., $z = \frac{1}{k\pi}$. Since $\sin z \sim z$, so they are $1$-order poles.
(2) $\varphi(z) = \frac{z - \frac{1}{k\pi}}{\sin \frac{1}{z}}$, and apply L'Hospital, $\operatorname{res}_{z = 1/k\pi} f = \lim \limits _{z \rightarrow 1/k\pi} \varphi(z) = \frac{z^2}{-\cos \frac{1}{z}} = \frac{(-1)^{k+1}}{k^2\pi^2}$.

</div>

- $f(z) = \frac{1}{e^{z} - 1}$ at $z = 0$ and $z = \infty$.

<div class=note>

(1) $z = 0$ is a $1$-order pole, $\operatorname{res}_{z = 0}f = 1$. (2) $z = \infty$ is an essential singularity, $\operatorname{res}_{z=\infty} f = -1$.
</div>

---

## The Residue Formula

<br>

- **Residue Formula**: Only one pole, then
$$ \int_C f(z)\mathrm{d} z = 2 \pi i \operatorname{res}_{z_0} f$$
- **Cauchy Residue Formula**: Isolated poles $z_1,\cdots,z_n$, then
$$ \int_C f(z) \mathrm{d} z = 2 \pi i \sum\limits_{k = 1}^n \operatorname{res}_{z_k} f.$$

---

## Calculate Integrals using Residue Formula

- ${\displaystyle \int_{|z| = 2} \frac{e^z}{z(1-z)^3}\mathrm{d} z}$.

<div class=note>

$\operatorname{res}_{z=0}f = 1$, $\operatorname{res}_{z=1} f = - \frac{e}{2}$. Then $I = 2\pi i(1 - \frac{e}{2})$.

</div>

- ${\displaystyle \int_{|z| = 1} \frac{\tan \pi z}{z^3}\mathrm{d} z}$.

<div class=note>

(1) $f(z) = \frac{\sin \pi z}{z^3 \cos \pi z}$, poles are $z = 0$ (order $2$), $z = \pm \frac{1}{2}$ (order $1$).
(2) When $z = 0$, $f(z) = \frac{\sin \pi z}{z^3} = \sum_{n=0}^{\infty} (-1)^n \frac{z^{2n-2}}{(2n+1)!}$, so $\operatorname{res}_{z = 0} f = 0$.
(3) $z = \pm \frac{1}{2}$, $f(z) = \frac{\pm 1}{z^3 \cos \pi z}$, $\varphi(z) = \frac{\pm (z \mp \frac{1}{2})}{z^3\cos \pi z}$. Apply L'Hospital $\operatorname{res}_{z=\frac{1}{2}} f = - \frac{8}{\pi}$, $\operatorname{res}_{z=-\frac{1}{2}}f = \frac{8}{\pi}$.

</div>

---

## Integrating Trigonometric Rational Functions

<div class=trick>

$$ \int_0^{2\pi} R(\cos \theta, \sin \theta)\mathrm{d} \theta = \int_{|z| = 1} R \left( \frac{z + z^{-1}}{2}, \frac{z - z^{-1}}{2} \right) \cdot \frac{1}{iz}\mathrm{d} z. $$
</div>

- ${\displaystyle \int_0^{2\pi} \frac{1}{a + \cos \theta}\mathrm{d} \theta}$, where $a > 1$.

<div class=note>

(1) $\cos \theta = (z + z^{-1})/2$, so $\displaystyle I = \frac{1}{i} \int_{|z| = 1} \frac{2}{z^2 + 2az + 1}\mathrm{d} z$. Poles are $\alpha = - a + \sqrt{a^2 - 1}$, $\beta = -a - \sqrt{a^2 - 1}$. But $\beta$ lies outside $|z| = 1$, so we only consider $\alpha$.
(2) $\varphi(z) = \frac{2}{z - \beta}$, so $\operatorname{res}_{z = \alpha} f = \frac{2}{\alpha - \beta}$, then $I = \frac{2\pi}{\sqrt{a^2 - 1}}$.

</div>

- ${\displaystyle \int_0^{2\pi} \sin^{2n}x \mathrm{d} x}$ where $n \in \mathbb{N}$.

<div class=note>

$\displaystyle I = \frac{1}{4^n i} \int_{|z| = 1} \frac{(z^2 - 1)^{2n}}{z^{2n+1}}\mathrm{d} z$, where ${\displaystyle (z^2 - 1)^{2n} = \binom{2n}{k}(-1)^{2n-k}z^{2k}}$, $\displaystyle \operatorname{res}_{z=0}f = \binom{2n}{n} (-1)^n$.

</div>

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

- **Winding Number**: Given closed $\gamma: [a, b] \rightarrow \mathbb{C}$, and $c \in \mathbb{C}$ not on $\gamma$. $\theta(t) := \operatorname{arg}(\gamma(t) - c)$ and $\Delta (\gamma, c) := \theta(b) - \theta(a)$. The *winding number* is $w(\gamma, c) = \frac{\Delta(\gamma, c)}{2 \pi} \in \mathbb{Z}$

<div class=note>

Note that $\gamma$ is closed, and the winding number is an integer.

</div>

- **Integration Representation**: $\gamma: [a, b] \rightarrow \mathbb{C}$ closed, $c \not \in \gamma$, then
$$ w(\gamma, c) = \frac{1}{2\pi i} \int_{\gamma} \frac{\mathrm{d} \zeta}{\zeta - c}. $$

<div class=note>

(1) The curve $\gamma(t) = c + \rho(t) e^{i \theta(t)}$ where $t \in [a, b]$.
(2) Then $\displaystyle \int_{\gamma} \frac{\mathrm{d} \zeta}{\zeta - c} = \int_a^b \frac{\mathrm{d} (\rho(t) e^{i \theta(t)})}{\rho(t) e^{i \theta(t)}} = \int_a^b \left( \frac{\rho^{\prime}(t)}{\rho(t)} + i\theta^{\prime}(t) \right)\mathrm{d}t = \ln \frac{\rho(b)}{\rho(a)} + i(\theta(b) - \theta(a))$.
(3) When $\gamma$ is closed, $\rho(a) = \rho(b)$, so $\displaystyle \int_{\gamma} \frac{\mathrm{d} \zeta}{\zeta - c} = 2\pi i w(\gamma, c)$.

</div>

---

## Argument Principle and Its Generalizations

- **Argument Principle**: $f$ meromorphic, $C$ closed contour. $f$ has no poles and never vanishes on $C$. $N_z$ the number of zeros of $f$ inside $C$, $N_p$ the poles (counted with multiplicities).
$$ w(f(C(t)), 0) = \frac{1}{2\pi i} \int_C \frac{f^{\prime}(z)}{f(z)}\mathrm{d} z = N_z - N_p $$

<div class=note>

Here $C(t)$ ($t \in [a, b]$) is closed, $f(C(t))$ is also closed. And 
$$ w(f(C), 0) = \frac{1}{2\pi i} \int_{f(C)} \frac{\mathrm{d} \zeta}{\zeta} = \frac{1}{2\pi i} \int_C \frac{f^{\prime}(z)}{f(z)}\mathrm{d} z. $$

</div>

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


