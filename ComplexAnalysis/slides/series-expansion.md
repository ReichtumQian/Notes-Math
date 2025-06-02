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

# Complex Series Expansions

Speaker: Yixiao Qian

---

# Taylor Expansion and Zeros

---

## Taylor Expansion

- **Taylor Expansion**: Given $z_0 \in \mathbb{C}$, $f$ is holomorphic in $|z-z_0| < R$ (include $z_0$), then
$$ f(z) = \sum\limits_{n = 0}^{\infty} a_n(z-z_0)^n, \quad |z - z_0| < R. $$
- **Maximum Radius**: Let $R_{z_0}$ be the convergence radius of series at $z_0$,
$$ R_{z_0} = \sup \{R: f \text{ is holomorphic in } |z - z_0| < R\}. $$
- **Global Convergence**: Taylor series of entire functions converge globally. E.g., $e^z, \sin z$.
- **Local Convergence**: $\frac{1}{z-1}$ is convergent in $|z| < 1$ since $z = 1$ is a pole.

---

## Zeros and Uniqueness Theorem

<br>

- **Zeros of Order $m$**: $f(z) = \sum_{n=m}^{+\infty} a_n(z-z_0)^n$.
- **Uniqueness Theorem**: $f$ holomorphic, has zeros $z_1,z_2,\cdots$, if $\lim \limits _{n \rightarrow \infty}z_n = w \in \mathbb{C}$, then $f \equiv 0$.

<div class=note>

The uniqueness theorem indicates that $f \not\equiv 0$ iff all the zeros of $f$ are isolated.

(1) $f(w) = f(\lim \limits _{n \rightarrow \infty} z_n) = \lim \limits _{n \rightarrow \infty} f(z_n) = 0$. And $f(z) = \sum_{n=0}^{\infty} \frac{f^{(n)}(w)}{n!}(z-w)^n$.
(2) Since $\lim \limits _{n \rightarrow \infty}z_n = w$, we know $\forall r > 0$, $\exists N > 0$, $\forall n > N$, $|z_n - w| < r$.
(3) If $f^{(m)}(w) \neq 0$, then $g(z) := \frac{f(z)}{(z-w)^m}$ satisfies $g(w) \neq 0$. There exists $r_0 > 0$ such that $g(z) \not\equiv 0$ in $D_{r_0}(w)$. But $f(z_n) = 0$ for $n > N$, which contradicts the condition.

</div>

- **Corollary**: $f, g$ are holomorphic, $f = g$ on $z_1,z_2,\cdots$, if $\lim \limits _{n \rightarrow \infty} z_n = w \in \mathbb{C}$, then $f \equiv g$.

---

## Expand Functions to Taylor Series

<br>

- Expand $f(z) = \frac{1}{z-2} + e^{-z}$ at the origin, and find the convergence radius.

<div class=note>

(1) $\frac{1}{z-2} = - \frac{1}{2} \cdot \frac{1}{1-\frac{z}{2}} = - \frac{1}{2} \sum\limits_{n = 0}^{\infty} \left( \frac{z}{2} \right)^n$. (2) $e^{-z} = \sum\limits_{n = 0}^{\infty} \frac{(-1)^nz^n}{n!}$ (3) Convergence radius is $2$.

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

# Laurent Expansion and Singularities

---

## Laurent Expansion and Singularities

- **Laurent Expansion**: $z_0 \in \mathbb{C}$ (maybe a singularity of $f$), $f$ holomorphic in $r < |z-z_0| < R$, it is uniquely represented as $f(z) = \sum_{n=-\infty}^{+\infty} a_n(z-z_0)^n$.
  - $\sum_{n=0}^{\infty} a_n(z-z_0)^n$ is analytic part, $\sum_{n=-\infty}^{-1}a_n(z-z_0)^n$ is principal part.
- **Removable Singularity**: $f(z) = \sum_{n=0}^{+\infty} a_n(z-z_0)^n$, then $f(z_0) = a_0$.
- **Pole Singularity Order $m$**: $f(z) = \sum_{n=-m}^{+\infty} a_n(z-z_0)^n$, $f(z_0) \rightarrow \infty$, $(z-z_0)^mf(z_0) = a_{-m}$.
- **Isolated Singularity**: $z_0$ is a pole, $f$ is holomorphic in a punctured neighborhood.
- **Essential Singularity**: $f(z) = \sum_{n=-\infty}^{+\infty}a_n(z-z_0)^n$, $\lim \limits _{z \rightarrow z_0}f(z)$ does not exist.

<div class=note>

Great Picard's Theorem: $f(z)$ takes on all possible complex values on any punctured neighborhood of the essential singularity $z_0$.

</div>

- **Meromorphic**: $f$ is holomorphic except poles at $\{z_0,z_1,\cdots\}$, which have no limit points.

---

## Expand Functions to Laurent Series

- Expand $f(z) = \frac{\sin z}{z - \pi}$ on (1) $0 < |z-\pi| < \infty$; (2) $0 < |z| < \pi$.

<div class=note>

(1) $f(z) = -\frac{\sin(z - \pi)}{z-\pi} = \sum_{n=0}^{\infty} (-1)^{n+1}\frac{(z-\pi)^{2n}}{(2n+1)!}$. (Laurent Expansion Centered at Singularity)
(2) $f(z) = \frac{1}{z-\pi} \cdot \sin z = -\frac{1}{\pi} \cdot \frac{1}{1 - \frac{z}{\pi}} \cdot \sin z = \frac{1}{\pi} \cdot (\sum_{n=0}^{\infty} \frac{z^n}{\pi^n})(\sum_{n=0}^{\infty} (-1)^n \frac{z^{2n+1}}{(2n+1)!})$. (Taylor)

</div>

- Expand $f(z) = \frac{1}{(z-1)^2}$ in $1 < |z| < +\infty$.

<div class=note>

It is equivalent to expand $f(z) = \frac{1}{z^2(1-\frac{1}{z})^2}$ in $|\frac{1}{z}| < 1$. We know when $|x| < 1$,
$$ \frac{1}{(1+x)^2} = \sum\limits_{n = 0}^{\infty} (-1)^{n} (n+1) x^n. $$
Then $f(z) = \frac{1}{z^2} \cdot \sum\limits_{n=0}^{\infty}(n+1) \frac{1}{z^n} = \sum\limits_{n = 0}^{\infty} (n+1)\frac{1}{z^{n+2}}$. (Laurent not Centered at Singularity)

</div>

---

# Laurent Expansion and Singularities at $z = \infty$

---

## Singularities and Laurent Expansion at $z = \infty$

- **Pole at $\infty$**: $f(z) = \infty$ when $z \rightarrow \infty$.
- **Laurent Expansion at $\infty$**: If $f$ is holomorphic when $|z| > R$, then $f = \sum\limits_{n=-\infty}^{+\infty}a_nz^n$.
- **Pole of Order $m$**: $f(z) = \sum\limits_{n = -\infty}^m a_nz^n$ at $z = \infty$ (or $f(\frac{1}{z}) = \sum\limits_{n = -m}^{\infty} a_nz^n$ at $z = 0$).
- **Essential Singularity**: $f(z) = \sum\limits_{n = -\infty}^{+\infty}a_nz^n$ at $z = \infty$.
- Prove if $f$ is entire, has pole (not essential singularity) at $z = \infty$, then it is a polynomial.

<div class=note>

(1) $f$ is entire, then $z=0$ is not a pole, so $f = \sum\limits_{n=0}^{\infty}a_nz^n$ in $\mathbb{C}$.
(2) If $z = \infty$ is an $m$-order pole, $f(z) = \sum\limits_{n=-\infty}^m a_nz^n$ when $|z| > R$,  where $m \neq \infty$.
(3) When $|z| > R$, the two series are identical, so $f(z) = \sum\limits_{n = 0}^m a_nz^n$, which is a polynomial.

</div>




