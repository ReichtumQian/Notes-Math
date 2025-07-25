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

# Complex Integrals and Cauchy's Theorem

Speaker: Yixiao Qian

---

# Complex Integrals

---

## Complex Integrals

- **Integral of Parametrized Curve**: $\gamma: [a, b] \rightarrow \mathbb{C}$, then ${\displaystyle \int_{\gamma} f(z)\mathrm{d} z = \int_a^b f(z(t))z^{\prime}(t)\mathrm{d} t}$.
- **Newton-Leibniz Formula**: ${\displaystyle \int_{\gamma}f(z)\mathrm{d}z = F(w_2) - F(w_1)}$, $F$ is primitive of $f$, $\gamma$ begins at $w_1$ and ends at $w_2$.
- ${\displaystyle \int_{\partial \Omega} \frac{\overline{z}}{z^2 + 1}\mathrm{d}z}$, where $\partial \Omega$ consists of $L_1: -1 \rightarrow 1$ and $L_2$ upper semicircle $|z| = 1$.

<div class=note>

(1) $I_1$: $z = t$ for $t \in [-1,1]$. ${\displaystyle \int_{-1}^1 \frac{t}{t^2+1}\mathrm{d} t} = 0$ since it is an odd function.
(2) $I_2$: $z = e^{i\theta}$ for $\theta \in [0, \pi]$. Change $\mathrm{d}z = ie^{i\theta}\mathrm{d} \theta$, we get ${\displaystyle \int_{L_2} \frac{\overline{z}}{z^2+1}\mathrm{d} z = i\int_0^{\pi} \frac{1}{2}\mathrm{d} \theta = \frac{\pi}{2}i}$.

</div>

---

## Inequalities in Complex Integrals

<div class=trick>

If $|f(z)| \leq R_1$ and $|\mathrm{d} z| \leq R_2$ on $C$ parameterized by $z(\theta): [a, b] \rightarrow \mathbb{C}$, then
$$ \left| \int_C f(z) \mathrm{d} z \right| \leq \int_a^b R_1 R_2 \mathrm{d}\theta = R_1R_2(b-a). $$

</div>

- ${\displaystyle \left| \int_{\Gamma}(x^2+iy^2)\mathrm{d} z \right| \leq 2}$, where $\Gamma: -i \rightarrow i$.

<div class=note>

$\Gamma: z = 0 + it$ then $|x^2 + iy^2| = |it|^2 \leq 1$ and $|\mathrm{d}z| = |t| \leq 1$. ${\displaystyle \left| \int_{\Gamma}(x^2+iy^2)\mathrm{d} z \right| \leq \int_0^2 1 \mathrm{d} t = 2}$.

</div>

- ${\displaystyle \left| \int_C e^{iz}\mathrm{d} z \right| \leq \pi}$, where $C$ is the upper circle from $R$ to $-R$.

<div class=note>

$|e^{iz}| = |e^{- iR \cos \theta - R \sin \theta}| = e^{-R \sin \theta}$, $|\mathrm{d}z| = |Rie^{i\theta}\mathrm{d}\theta| = R\mathrm{d}\theta$. Then ${\displaystyle \left| \int_C e^{iz}\mathrm{d}z \right| \leq \int_0^{2\pi} e^{-R\sin\theta} R \mathrm{d}\theta}$

</div>

---

# Cauchy's Theorem and Its Generalizations

---

## Cauchy's Theorem and Its Generalizations

- **Cauchy's Theorem**: $f$ holomorphic in simply connected $D$, $\gamma$ closed curve. $\displaystyle \int_{\gamma} f \mathrm{d} z = 0$
- **Cauchy's Integral Formula**: $\displaystyle f(z) = \frac{1}{2 \pi i} \int_C \frac{f(\zeta)}{\zeta - z}\mathrm{d} \zeta$ for $z \in D$, $C$ is positive boundary.
- **Cauchy's Derivative Formula**: ${\displaystyle f^{(n)}(z) = \frac{n!}{2 \pi i} \int_C \frac{f(\zeta)}{(\zeta - z)^{n+1}}\mathrm{d} \zeta}$ for $z \in D$.

<div class=trick>

Residue formula is generalized Cauchy's (integral) theorem, so we ignore their applications.

</div>

- **Cauchy's Inequality**: Denote $\|f\|_C := \sup_{z \in C}|f(z)|$ as the supremum of $|f|$ on boundary $C$
$$ |f^{(n)}(z_0)| \leq \frac{n! \|f\|_C}{R^n}.$$

<div class=note>

$$ \left| \int_C \frac{f(\zeta)}{(\zeta - z)^{n+1}}\mathrm{d} \zeta \right| \leq 2 \pi R \cdot \frac{\|f\|_C}{R^{n+1}} = \frac{2 \pi \|f\|_C}{R^n}.$$

</div>

---

## Applications of Cauchy's Theorem

- $f$ holomorphic, $f^{(n)}(0) = n!$, what is ${\displaystyle \int_{|z| = 1} \frac{f(z)}{z^4}\mathrm{d} z}$.

<div class=note>

${\displaystyle \int_{|z| = 1} \frac{f(z)}{z^4} \mathrm{d} z = \frac{2\pi i}{6} \cdot f^{(3)}(0)} = 2 \pi i$.

</div>

---

# Liouville's Theorem and Its Applications

---

## Liouville's Theorem

- **Liouville's Theorem**: If $f$ is entire and bounded, then it is constant.

<div class=note>

Cauchy's inequality implies $|f^{\prime}(z_0)| \leq \frac{B}{R}$ for any $z_0$ and $R$, where $B$ is a bound. Let $R \rightarrow \infty$ gives the result.

</div>

- **Fundamental Theorem for Algebra**: $P(z) = a_nz^n + \cdots + a_0$ ($n \geq 1$) has $n$ roots in $\mathbb{C}$, and
$$ P(z) = a_n(z-z_1)(z-z_2)\cdots (z-z_n). $$

<div class=note>

(1) If $P(z)$ has no roots, then $\frac{1}{P(z)}$ is entire and bounded. By Liouville's theorem, $P(z)$ is constant, which contradicts the condition.
(2) Then $P(z)$ must have a root $z_1$, and $P(z) = (z-z_1)Q(z)$. By induction, we can get the conclusion.
</div>

---

## Applications of Liouville's Theorem

- If $f$ is entire, $\exists M > 0$, $|f(z)| \leq M \cdot |z|^{1/2}$ holds for all $z \in \mathbb{C}$. Prove that $f$ is constant.

<div class=note>

(1) Let $R = |z|$, then by Cauchy's inequality, $|f^{(n)}(0)| \leq \frac{n! M R^{1/2}}{R^n} \rightarrow 0$ for all $n \geq 1$.
(2) Since $f$ is entire, $f = \sum_{n=0}^{+\infty}a_nz^n$ converges in $\mathbb{C}$. Then $f(z) \equiv a_0$.

</div>

- If $f$ is entire, $\operatorname{Re}(f)$ has upper bound $M$ on $\mathbb{C}$. Prove $f$ is constant.

<div class=note>

(1) Define $g(z) = e^{f(z)}$, then $|g(z)| = e^{\operatorname{Re}(f(z))} \leq e^M$.
(2) By Liouville's theorem, $g(z) \equiv C$.
(3) Since $e^{f(z)} \equiv C$ and $f$ is entire. Taking derivative we know $f^{\prime}(z) e^{f(z)} \equiv 0$, so $f^{\prime}(z) \equiv 0$ since $e^{f(z)} \equiv C$.

</div>




