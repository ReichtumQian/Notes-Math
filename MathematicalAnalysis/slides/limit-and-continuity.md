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

# Limits and Continuity

Speaker: Yixiao Qian

---

# Sequence Limit

---

## Concept and Properties of Sequence Limit

- **Definition of Sequence Limit**
- **Arithmetic Operations of Limit**
- **Cauchy's Criterion**
- **Basic Limits**: $\log n < n^a < b^n < n! < n^n$.
- **Number $e$**: $\lim \limits _{n \rightarrow \infty} (1 + \frac{1}{n})^n = e - \frac{e}{2n} + o(\frac{1}{n})$.
- **Stirling's Formula**: $n! \approx \sqrt{2\pi n} \left( \frac{n}{e} \right)^n$ and $\sqrt[n]{n!} \approx \frac{n}{e}$.
- **Euler's Constant**: $\sum_{k=1}^n \frac{1}{k} = \ln n + \gamma$.

<div class=note>

(1) Consider $a_n = \sum_{k=1}^n \frac{1}{k} - \ln n$. Then $a_n - a_{n-1} = \frac{1}{n} + \ln (1 - \frac{1}{n}) < 0$ is decreasing.
(2) $\ln n = \ln \frac{n}{n-1} + \ln \frac{n-1}{n-2} + \cdots + \ln \frac{2}{1}$, where $\ln \frac{n}{n-1} = \ln(1 + \frac{1}{n-1}) < \frac{1}{n-1}$. Then $a_n > 0$.

</div>

---

## Limits of Mean Values

- **Radical Mean Value of Finite Sequences**: $\lim \limits _{n \rightarrow \infty} \sqrt[n]{a_1^n + \cdots + a_m^n} = \max \{a_1,\cdots,a_m\}$.

<div class=note>

Denote $A = \max\{a_1,\cdots,a_m\}$, then $\sqrt[n]{A^n} \leq \sqrt[n]{a_1^n + \cdots + a_m^n} \leq \sqrt[n]{mA^n}$.

</div>

- **Limits of Mean Value**: If $\lim \limits _{n \rightarrow \infty} a_n = a$, $a_i > 0$, then
$$ \lim \limits _{n \rightarrow \infty} \frac{a_1 + \cdots + a_n}{n} = a, \quad \lim \limits _{n \rightarrow \infty} \sqrt[n]{a_1 \cdots a_n} = a. $$

<div class=note>

(1) $\forall \epsilon > 0$, $\exists N > 0$, $\forall n > N$, $|a_n - a| < \epsilon$.
(2) $\left| \frac{a_1+\cdots + a_n}{n} - a \right| \leq \frac{|a_1-a| + \cdots + |a_N - a|}{n} + \frac{|a_{N+1} - a| + \cdots + |a_n - a|}{n} \leq 2\epsilon$.
(3) For $\sqrt[n]{a_1 \cdots a_n}$, take logarithm.

</div>


---

## Limits of Roots and Division

- **Division**: $\lim \limits _{n \rightarrow \infty} a_n - a_{n-1} = a$, then $\lim \limits _{n \rightarrow \infty} \frac{a_n}{n} = a$.

<div class=note>

$$ \lim \limits _{n \rightarrow \infty} \frac{a_n}{n} = \lim \limits _{n \rightarrow \infty} \frac{a_1 + (a_2 - a_1) + \cdots + (a_n - a_{n-1})}{n}. $$

</div>

- **Roots**: $\lim \limits _{n \rightarrow \infty} \frac{a_n}{a_{n-1}} = b$, then $\lim \limits _{n \rightarrow \infty} \sqrt[n]{a_n} = b$.

<div class=note>

$$ \lim \limits _{n \rightarrow \infty} \sqrt[n]{a_n} = \lim \limits _{n \rightarrow \infty} \sqrt[n]{a_1 \cdot \frac{a_2}{a_1} \cdots \frac{a_n}{a_{n-1}}}. $$

</div>

- Find the limits: (1) $\lim \limits _{n \rightarrow \infty} \sqrt[n]{n!}$, (2) $\lim \limits _{n \rightarrow \infty} \frac{\sqrt[n]{n(n+1)\cdots (2n-1)}}{n}$.

<div class=note>

(1) Denote $a_n = n!$, then $\frac{a_n}{a_{n-1}} = n \rightarrow \infty$, so the limit does not exist.
(2) Denote $a_n = \frac{n(n+1)\cdots (2n-1)}{n^n}$, then $\frac{a_n}{a_{n-1}} = \frac{2(2n-1)(n-1)^{n-1}}{n^n} = (4 - \frac{2}{n}) \cdot (1-\frac{1}{n})^{n \cdot \frac{n-1}{n}} \rightarrow \frac{4}{e}$.

</div>

---

## Use Definition of Definite Integral

- Calculate ${\displaystyle I = \lim \limits _{n \rightarrow \infty}  \left( \frac{1}{\sqrt{n^2 + 1^2}} + \frac{1}{\sqrt{n^2 + 2^2}} + \cdots + \frac{1}{\sqrt{n^2 + n^2}} \right)}$

<div class=note>

${\displaystyle I = \sum_{k=1}^n \frac{1}{n} \cdot \frac{1}{\sqrt{1 + (\frac{k}{n})^2}} = \int_0^1 \frac{1}{\sqrt{1 + x^2}}\mathrm{d} x = \ln(x + \sqrt{x^2 + 1}) \bigg|^1_0 = \ln(1 + \sqrt{2})}$.

</div>

- Calculate ${\displaystyle I = \lim \limits _{n \rightarrow \infty} \left( \frac{\sin \frac{\pi}{n}}{n + \frac{1}{n}} + \frac{\sin \frac{2}{n}\pi}{n + \frac{2}{n}} + \cdots + \frac{\sin \pi}{n + 1} \right)}$

<div class=note>

(1) $\frac{\sin \frac{i}{n}\pi}{n+1} \leq \frac{\sin \frac{i}{n}\pi}{n + \frac{i}{n}} \leq \frac{\sin \frac{i}{n}\pi}{n}$. (2) rhs is $\displaystyle \int_0^1 \sin \pi x \mathrm{d} x = \frac{2}{\pi}$ (3) lhs $\sum \frac{\sin \frac{i}{n}\pi}{n} = \frac{n}{n+1} \cdot \frac{1}{n} \sum \sin \frac{i}{n}\pi$.

</div>

- Calculate ${\displaystyle \lim \limits _{n \rightarrow \infty} \left( \frac{1}{n^2 + n + 1} + \frac{2}{n^2 + n + 2} + \cdots + \frac{n}{n^2 + n + n}\right)}$.

<div class=note>

(1) $\frac{k}{n^2 + 2n} \leq \frac{k}{n^2 + n + k} \leq \frac{k}{n^2 + n}$. (2) $\sum \frac{k}{n^2 + 2n} = \frac{n}{n+2} \cdot \frac{1}{n}\sum \frac{k}{n} \rightarrow \frac{1}{2}$. (3) rhs is similar.

</div>

---

## Applications of Monotone Convergence Theorem

- $a_1 = \sqrt{c}$, $a_{n+1} = \sqrt{a_n + c}$. Prove $a_n$ converges and find $\lim \limits _{n \rightarrow \infty} a_n$.

<div class=note>

$a_2 = \sqrt{c + \sqrt{c}} > a_1$. If $a_n > a_{n-1}$, then $a_{n+1} = \sqrt{a_n + c} > \sqrt{a_{n-1}+c} = a_n$.

</div>

- $a_1 = 1$, $a_{n+1} = \sqrt{2a_n}$. Prove $a_n$ converges and find $\lim \limits _{n \rightarrow \infty} a_n$.

<div class=note>

(1) $a_n < 2$, then $a_{n+1} = \sqrt{2a_n} < 2$. (2) $\frac{a_{n+1}}{a_n} = \sqrt{\frac{2}{a_n}} < 1$.

</div>


---

# Function Limit

---

## Concept and Properties of Function Limit

- **Definition of Function Limit**
- **Uniqueness of Function Limit**
- **Closure under Arithmetic Operations**: 
- **Heine-Cantor Theorem**
- Prove $\lim \limits _{x \rightarrow 0} \sin \frac{1}{x}$ does not exist.

<div class=note>

Take $a_n = \frac{1}{2n\pi}$ and $b_n = \frac{1}{2n\pi + \frac{\pi}{2}}$. $\lim \limits _{n \rightarrow \infty} (a_n - b_n) = 0$ but $f(a_n) - f(b_n) \not \rightarrow 0$.

</div>

---

## Calculation of Function Limit

<div class=trick>

Commonly used Taylor expansions: When $x \rightarrow 0$

$$
\begin{array}{ll}
e^x = \sum\limits_{n = 0 }^{\infty}\frac{x^n}{n!}& \ln(1 + x) = \sum\limits_{n = 1}^{\infty}(-1)^{n-1}\frac{x^n}{n} \\
\sin x = \sum\limits_{n = 0}^{\infty}(-1)^n \frac{x^{2n+1}}{(2n+1)!}& \cos x = \sum\limits_{n = 0}^{\infty}(-1)^n \frac{x^{2n}}{(2n)!} \\
\frac{1}{1+x} = \sum\limits_{n = 0}^{\infty}(-1)^n x^n&\frac{1}{1 - x} = \sum\limits_{n = 0}^{\infty}x^n \\
(1+x)^{\alpha} = 1 + \alpha x + \frac{\alpha(\alpha - 1)}{2}x^2 + o(x^2)&(1 + x)^{\alpha} = \sum\limits_{n = 0}^{\infty}{\alpha \choose n} x^n
\end{array}
$$

Note when $x \rightarrow \infty$: $\frac{1}{1+x} = \frac{1}{x} \cdot \frac{1}{1+1/x} = \sum\limits_{n = 1}^{\infty} (-1)^{n-1} \frac{1}{x^n}$. (From complex analysis we know the convergent radius is $1$)
</div>


---

# Continuous Function

---

## Concept and Applications of Continuity

- **Continuity**: $\lim \limits _{x \rightarrow x_0}f(x) = f(x_0)$.
- **Intermediate-Value Theorem**: $f \in C[a, b]$, $a \leq x_1 < x_2 \leq b$, $f$ takes any value between $f(x_1)$ and $f(x_2)$.
- $f, g \in C[0, 1]$, $\max f = \max g$, prove $f(\xi) = g(\xi)$.

<div class=note>

Assume $f(x_1) = \max f$, $g(x_2) = \max g$. $F(x) := f(x) - g(x)$, $F(x_1) \geq 0$ and $F(x_2) \leq 0$.

</div>

- $f \in C[0, 2a]$, $f(0) = f(2a)$, prove $\exists \xi \in [0, a]$, $f(\xi) = f(\xi + a)$.

<div class=note>

$F(x) := f(x) - f(x+a)$. $F(0) = f(0) - f(a)$, $F(a) = f(a) - f(0)$, meaning $F(0) = - F(a)$.

</div>

- $f \in C[0,1]$, $f(0) = f(1) = 0$, prove $\exists \xi \in [0, 1]$, $f(\xi + \frac{1}{n}) = f(\xi)$.

<div class=note>

$F(x) := f(x + \frac{1}{n}) - f(x)$. $F(0) + F(\frac{1}{n}) + \cdots + F(\frac{n-1}{n}) = f(1) - f(0) = 0$. All zero or have $\pm$.

</div>

---

## Practice on Continuous Function

- $f: \mathbb{R} \rightarrow \mathbb{R}$. If (1) $\forall x, y \in \mathbb{R}$, $f(x+y) = f(x) + f(y)$. (2) $f$ is continuous at $x_0$. Prove there exists $a \in \mathbb{R}$ such that $f = ax$.

<div class=note>

(1) $f(x+y) = f(x) + f(y)$: $f(0) = 0$, $-f(x) = f(-x)$, $f(nx) = nf(x)$, $f(\frac{m}{n}x) = \frac{m}{n}f(x)$.
(2) For $q \in \mathbb{Q}$, $f(q) = qf(1)$. So we take $a = f(1)$.
(3) $f$ continuous at $0$: Take $\{q_n\} \subset \mathbb{Q}$, $q_n \rightarrow 0$. Then $f(q_n) = f(x_0 + q_n) - f(x_0) \rightarrow 0 = f(0)$.
(4) $f \in C(\mathbb{R})$: For $q_n \rightarrow 0$, $f(x+q_n) = f(x) + f(q_n) \rightarrow f(x)$.
(5) For $q_n \rightarrow x$, $f(x) = \lim \limits _{n \rightarrow \infty} f(q_n) = \lim \limits _{n \rightarrow \infty} aq_n = ax$.

</div>


---

# Uniform Continuity

---

## Concept and Properties of Uniform Continuity

<br>

- **Uniform Continuity**: $\forall \epsilon > 0$, $\exists \delta > 0$, $\forall x_1, x_2$, $|x_1 - x_2| < \delta$, $|f(x_1) - f(x_2)| < \epsilon$.
- **Sequence Perspective**: $f$ is uniformly continuous iff for any $x_n, y_n$, $\lim \limits _{n \rightarrow \infty} (x_n - y_n) = 0$, $\lim \limits _{n \rightarrow \infty} [f(x_n) - f(y_n)] = 0$.
- Prove followings are not uniformly continuous: (1)$x^2$ on $(0,+\infty)$; (2) $\frac{1}{x}$ on $(0, 1)$.

<div class=note>

(1) Take $x_n = \sqrt{n}$, $y_n = \sqrt{n+1}$; (2) Take $x_n = \frac{1}{n}$, $y_n = \frac{1}{n+1}$.

</div>


---

## Cantor Theorem and Its Generalizations

- **Cantor Theorem**: If $f \in C[a, b]$, then it is uniformly continous on $[a, b]$.
- **On Open Intervals**: $f \in C(a,b)$, $f$ is uniformly continuous iff $\lim \limits _{x \rightarrow a^+}f$ and $\lim \limits _{x \rightarrow b^-}f$ exists.

<div class=note>

$\Leftarrow$ by adding two endpoints. $\Rightarrow$ when $x_1,x_2 \in (a, a+\delta)$, we have $|f(x_1) - f(x_2)| < \epsilon$.

</div>

- **On Infinite Intervals**: $f \in C[a, +\infty)$, $\lim \limits _{x \rightarrow +\infty}f(x) = A$, then it is uniformly continous.

<div class=note>

(1) By Cauchy's criterion, $\forall x_1, x_2 > M$, $|f(x_1) - f(x_2)| < \epsilon$.
(2) By Cantor, $\forall x_1, x_2 \in [a, M+\delta]$, $|f(x_1) - f(x_2)| < \epsilon$.


</div>

- Determine uniform continuity: (1) $\frac{1}{x}$ on $(0, 1)$; (2) $\sqrt{x}$ on $(0, 1)$; (3) $\frac{1}{x}$ on $[1, +\infty)$.

<div class=note>

(1) No, because $\frac{1}{x} \rightarrow \infty$ when $x \rightarrow 0$. (2) Yes, because limits exist. (3) Yes, $\lim \limits _{x \rightarrow \infty}\frac{1}{x} = 0$.

</div>

---

## Lipschitz Continuity

- **Lipschitz Continuity**:
- **Implies Uniform Continuity**: If $f$ is Lip continuous, then $f$ is uniformly continuous.
- **Bounded Derivative**: $f^{\prime}$ is bounded, then $f$ is Lip continuous.

<div class=note>

Unbounded derivative does not mean $f$ is not uniformly continuous. E.g., $f = \sqrt{x}$ on $(0,1)$. $f^{\prime} = \frac{1}{2 \sqrt{x}} \rightarrow \infty$ when $x \rightarrow 0^+$.

</div>

- Prove following are uniformly continuous: (1) $\cos \sqrt{x}$ on $[0, +\infty)$; (2) $\sqrt{x}$ on $[0, +\infty)$.

<div class=note>

(1) $f^{\prime} = - \frac{\sin \sqrt{x}}{2 \sqrt{x}}$. $f \in C[0, 1]$, so $f$ is uniformly continuous on $[0, 1]$. When $x > 1$, $|f^{\prime}| \leq \frac{1}{2}$, so $f$ is Lip continuous, which implies uniform continuity.
(2) $f^{\prime} = \frac{1}{2 \sqrt{x}}$. $f \in C[0, 1]$, so $f$ is uniformly continuous on $[0, 1]$. When $x > 1$, $|f^{\prime}| \leq \frac{1}{2}$, so $f$ is Lip continuous, which implies uniform continuity.

</div>

