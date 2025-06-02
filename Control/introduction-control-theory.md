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

# Introduction to Control Theory

Speaker: Yixiao Qian

---

# Concept of Linear System

---

## Linear Time-Invariant System

- **Linear Time-Invariant System (LTI)**: State $x(t) \in \mathbb{C}^n$, Input $u(t) \in \mathbb{C}^m$, Output $y(t) \in \mathbb{C}^p$.
$$
\Sigma: \quad \dot{x}(t) = A x(t) + Bu(t), \quad y(t) = Cx(t) + Du(t).
$$
- **Linear**: $(u_1(t), x_1(0)) \rightarrow (x_1(t), y_1(t))$, $(u_2(t), x_2(0)) \rightarrow (x_2(t), y_2(t))$
$$ (u_1(t) + u_2(t), x_1(0) + x_2(0)) \rightarrow (x_1(t)+x_2(t), y_1(t)+y_2(t)). $$
- **Time-Invariant**: The output of $(u(t), x(0))$ is same as that of $(u(t + \tau), x(\tau))$ after $t = \tau$.
- **Single-Input Single-Output (SISO)**: $m = p = 1$.
- **Multiple-Input Single-Output (MISO)**: $m > 1$, $p = 1$.
- **Order of $\Sigma$**: $n$ is order of $\Sigma$, which can be infinity.

---

## Laplace Transormations

- **Laplace Transformation**: $\displaystyle \hat{u}(s) = \mathcal{L} \{u(t)\} = \int_0^{+\infty} e^{-st}u(t)\mathrm{d} t$.
- **Linearity**: $\mathcal{L}\{a u(t) + bv(t)\} = a \hat{u}(s) + b \hat{v}(s)$.
- **Differentiation in Time**: $\mathcal{L} \{u^{\prime}(t)\} = s\hat{u}(s) - u(0)$.
- **Integration in Time**: $\displaystyle \mathcal{L}\{\int_0^t f(\tau)\mathrm{d} \tau\} = \frac{\hat{u}(s)}{s}$.
- **Convolution Product**: $\displaystyle (u \ast v) (t) = \int_0^t u(t - \sigma) v(\sigma)\mathrm{d} \sigma$.
- **Convolution Theorem**: $\mathcal{L}\{u \ast v\} = \hat{u}(s)\hat{v}(s)$.

---

## Transfer Function and Its Applications

- **Transfer Function**: $G(s) = C(sI - A)^{-1} B + D$, which is a proper rational function.

<div class=note>

Apply Laplace transformation to $\dot{x} = Ax + Bu$, then
$$ s \hat{x}(s) - x(0) = A\hat{x}(s) + B\hat{u}(s). $$
Then $\hat{x}(s) = (s I - A)^{-1}x(0) + (sI - A)^{-1}B\hat{u}(s)$. Substituting it into $\hat{y}(s) = C\hat{x}(s) + D\hat{u}(s)$ and take $x(0) = 0$, we get $\hat{y}(s) = [C(sI - A)^{-1}B + D]\hat{u}(s)$.

</div>

- **Conclusion**: Transfer function maps $\hat{u}(s)$ to $\hat{y}(s)$.

$$
\begin{cases}
  \hat{y}(s) = G(s) \hat{u}(s) & \text{if } x(0) = 0;\\
  \hat{y}(s) = G(s)\hat{u}(s) + C(sI - A)^{-1}x(0) & \text{Otherwise}
\end{cases}
$$

---

## Properties of Transfer Function

<div class=trick>

The formula of transfer function is
$$G(s) = C(sI - A)^{-1}B + D$$

</div>

- **Rational**: Each entry in $G$ is of the form $\frac{p(x)}{g(x)}$, $\operatorname{deg}(p) = n-1$ and $\operatorname{deg}(g) = n$.

<div class=note>

(1) $(sI - A)^{-1} = \frac{1}{|sI - A|}(s I - A)^\ast$, $|sI - A|$ is the characteristic polynomial, its degree is $n$.
(2) Entries of $(sI - A)^\ast$ are either $n - 1$-order (diagonal) or $n - 2$-order (not diagonal).

</div>

- **(Strictly) Proper**: $G(\infty) = D$ (finite). If $D = 0$, then $G(\infty) = 0$, and it is strictly proper.
- **Poles**: Poles of $G$ are subset of $\sigma(A)$ (eigenvalues of $A$).
- **Minimal System**: No systems of lower order has the same transfer function. A linear system is minimal iff its poles are exactly $\sigma(A)$. (The posibility of minimal system is $1$)

---

## Several Famous Transfer Function

- **LPF**: $G(s) = \frac{1}{1 + \tau s}$ for $\tau > 0$.
- **HPF**: $G(s) = \frac{\tau s}{1 + \tau s}$.
- **Example**: Spring. $mq_{tt} = k(-q) + d(-q_t)+u$, where $q$ is the position.

<div class=note>

Apply the Laplace transformation to solve it.
$$ ms^2 \hat{q}(s) - m sq(0) - m\dot{q}(0) + ds\hat{q}(s) - dq(0) + k\hat{q}(s) = \hat{u}(s). $$
The transfer function is
$$ G(s) = \frac{1}{ms^2 + ds + k}. $$

</div>

---

# Stability of Linear System

---

## Stability of Linear System

- **Stability**: The system is *stable* if $e^{At} \rightarrow 0$.

<div class=note>

${\displaystyle x(t) = e^{At}x(0) + \int_0^t e^{A(t - \sigma)}B u(\sigma)\mathrm{d} \sigma}$. It means if $u = 0$, no matter how $x(0)$ be, $x(t) \rightarrow 0$.

</div>

- **Condition**: $\operatorname{Re}(\lambda_k) < 0$, or $\sigma(A) \subset \mathbb{C}_-$.

<div class=note>

Consider $A = H^{-1}JH$, then $e^{At} = H^{-1}e^{Jt}H$. Expand $e^{Jt}$, and each entry is like $e^{\lambda_i t}$.

</div>

- **Marginally Stable**: $\operatorname{Re}(\lambda_k) \leq 0$.

---

## Routh Test

- **Idea**: Determine if the system is stable without computing the eigenvalues.
- **Polynomial Stability**: If roots are in $\mathbb{C}_-$. If its coefficients are real, then they are positive. (and versa vice if $n = 2$)
- **Routh Test**: The polynomial is stable iff all entries of the first column are positive.

$$
\begin{bmatrix}
  1 & a_{n-2} & a_{n-4} & a_{n-6} & \cdots \\
  a_{n-1} & a_{n-3} & a_{n-5} & a_{n-7} & \cdots
\end{bmatrix}
$$

- **Calculation of $b$**: If $a_n$ is over, then substitute it with $0$.
- Derive the formula for $p(s) = s^3 + a_2s^2 + a_1 s + a_0$.

<div class=note>

$b_1 = \frac{-1}{a_2}(a_0 - a_1a_2)$ and $c_1 = \frac{-1}{b_1}(-a_0b_1) = a_0$. So it is stable 

</div>

- If $A$ is unstable and all entries in first column are non-zero, then the number of unstable eigenvalues of $A$ is equal to the number of sign changes in the first column.

---

## Stable Transfer Function

- **Stable Transfer Function**: Analytic and bounded on $\mathbb{C}_+$.
- **Rational Function Case**: Iff it is proper and all poles are in $\mathbb{C}_-$.
- Determine if $\frac{(s^2 - 1)e^{-7s}}{(s^2 + 2s + 5)(-s-3)}$ is stable.

<div class=note>

Yes, because $e^{-7s}$ is stable, $\frac{s^2 - 1}{(s^2 + 2s + 5)(-s-3)}$ is also stable.

</div>

- **Relation with Stable System**: Stable system implies stable transfer function . (Versa vice when system is minimal)

<div class=note>

(1) $G(s)$ is proper; (2) Poles of $G(s)$ are eigenvalues of $A$, which are in $\mathbb{C}_-$.

</div>

- Example: $A =
\begin{bmatrix}
  -3 & 0 \\ 5 & 2
\end{bmatrix}
$, $B =
\begin{bmatrix}
  3 \\ 11
\end{bmatrix}
$, $C =
\begin{bmatrix}
  8 & 0
\end{bmatrix}
$, $D = 0$. Find minimal system and transfer function, and their stability.


---

## Energy of Linear Systems

- **Energy**: $\displaystyle \|u\|^2 = \int_0^{\infty} |u(t)|^2 \mathrm{d} t$.
- If the input $u$ has finite energy, $G$ is stable, then $y$ has finite energy.


