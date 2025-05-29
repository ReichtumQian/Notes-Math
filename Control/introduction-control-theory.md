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
  - **Proper**: $G(\infty) = D$ is finite. If $G(\infty) = 0$ then it is strictly proper.
  - **Rational**: Each entry in $G$ is ratio of two polynomials.

<div class=note>

Apply Laplace transformation to $\dot{x} = Ax + Bu$, then
$$ s \hat{x}(s) - x(0) = A\hat{x}(s) + B\hat{u}(s). $$
Then $\hat{x}(s) = (s I - A)^{-1}x(0) + (sI - A)^{-1}B\hat{u}(s)$. Substituting it into $\hat{y}(s) = C\hat{x}(s) + D\hat{u}(s)$ and take $x(0) = 0$, we get $\hat{y}(s) = [C(sI - A)^{-1}B + D]\hat{u}(s)$.

</div>

- **Conclusion**

$$
\begin{cases}
  \hat{y}(s) = G(s) \hat{u}(s) & \text{if } x(0) = 0;\\
  \hat{y}(s) = G(s)\hat{u}(s) + C(sI - A)^{-1}x(0) & \text{Otherwise}
\end{cases}
$$

---

## Structure of Transfer Function

- $(sI - A)^{-1} = \frac{1}{|sI - A|}(s I - A)^\ast$, where $|sI - A|$ is the characteristic polynomial of $A$, each entry of $(sI - A)^\ast$ is of the order either $n - 1$ (on the diagonal) or $n - 2$ (not on the diagonal).
- The transfer polynomial is strictly proper.
- $\lim \limits _{s \rightarrow \infty} G(s) = D$.
- Poles of $G$ are subset of $\sigma(A)$ (eigenvalues of $A$).
- **Minimal System**: No systems of lower order has the same transfer function.
- Example: $A =
\begin{bmatrix}
  3 & 0\\
  2 & -5
\end{bmatrix}
$, $B =
\begin{bmatrix}
  0 \\ 2
\end{bmatrix}
$, $C =
\begin{bmatrix}
  7 & 0
\end{bmatrix}
$, $D = 0$.

<div class=note>

Only take the first dimension keeps the transfer function.

</div>

- The probability of minimal system is $1$.

---

## Famous Transfer Function

- **LPF**: $G(s) = \frac{1}{1 + \tau s}$ for $\tau > 0$.
- **HPF**: $G(s) = \frac{\tau s}{1 + \tau s}$.
- **Example**: Spring. $mq_{tt} = k(-q) + d(-q_t)+u$, where $q$ is the position.

<div class=note>

Apply the Laplace transformation to solve it.
$$ ms^2 \hat{q}(s) - m sq(0) - m\dot{q}(0) + ds\hat{q}(s) - dq(0) + k\hat{q}(s) = \hat{u}(s). $$
The transfer function is
$$ G(s) = \frac{1}{ms^2 + ds + k}. $$

</div>

