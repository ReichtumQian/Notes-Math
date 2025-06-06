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

# Introduction to Control System

Speaker: Yixiao Qian

---

# Standard Feedback Connection

---

## Standard Feedback Connection

- $d(t)$ is disturbance, $r(t)$ is reference, $y(t)$ is output of the plant, $e(t)$ is tracking error.
- **Input and Output**: $x = [d, r]$, $y = [u,e]$. (The output can actually be any, you choose.)

![center w:500](assets/image.png)

<div class=note>

$d(t),r(t),y(t),e(t)$ are time-signals. $P(s)$ and $C(s)$ are transfer functions of P and C. 

</div>

- **Transfer Func**: $
G(s) =
\begin{bmatrix}
  1 & -C\\
  P & 1
\end{bmatrix}^{-1}
 =
 \begin{bmatrix}
   (1+CP)^{-1} & C(1+PC)^{-1}\\
   -P(1+CP)^{-1} & (1+PC)^{-1}
 \end{bmatrix}$. $G(0)$ is *DC gain*.

<div class=note>

It is not hard to see that$\begin{bmatrix}
  \hat{d} \\ \hat{r}
\end{bmatrix} =
\begin{bmatrix}
  1 & -C\\
  P & 1
\end{bmatrix}
\begin{bmatrix}
  \hat{u}\\ \hat{e}
\end{bmatrix}$. Then $G(s) = \begin{bmatrix}
  1 & -C\\
  P & 1
\end{bmatrix}^{-1}$.

</div>


---

## Stability of Standard Feedback Connection

- **Loop Gain**: The relation between $e$ and $y$, that is $P(s)C(s)$.
- **Sensitivity**: $e=r-y$ and $y=PCe$, then $S := \frac{e}{r} = (1+PC)^{-1}$.
- **Stability Condition**: Iff (1) $S$ is stable; (2) No unstable pole-zero cancellation in $PC$.
- **Stable Pole-Zero Cancallation**: The pole/zero cancelled is in $\mathbb{C}_-$ (not include $\operatorname{Re}z = 0$)

<div class=note>

There is a stable pole-zero cancellation:
$$ P(s) = \frac{s}{(s+1)(s-2)}, \quad C(s) = \frac{5(s+1)}{s^2 + 1}.  $$

</div>

---

# Control of a First Order System

---

## Concept of a First Order System

- **Plant**: The transfer function is $\frac{k}{1+Ts}$, where $T$ is time constant, $k$ is gain.
- **Proportional Control**: The transfer function $C(s) = K$ (Constant Gain).

![center w:600](assets/image-3.png)

---

## First Order System without Controller

In this example, we ignore the controller and only consider the plant (a water heater).
- **Input**: Power $u$, which is a step function meaning ON ($u \equiv u_0$ after turning on).
- **Output**: Temperature $y$, which is step response.
- **What is $y$ when $t \rightarrow \infty$**: The limit $y \rightarrow P(0)u_0 = ku_0$ , where $P(0)$ is the *DC gain*.

<div class=note>

(1) $\hat{y}(s) = P(s) \hat{u}(s)$, where $\displaystyle \hat{u}(s) = \int_0^{+\infty} e^{-st} u_0\mathrm{d} t = \frac{u_0}{s}$.
(2) By final value theorem, $\lim \limits _{t \rightarrow \infty}y(t) = \lim \limits _{s \rightarrow 0}s \hat{y}(s) = P(0)u_0$.

</div>

![center w:300](assets/image-6.png)


---

## First Order System with Controller

- **Step Response**: $y_{\text{step}} = \frac{kK}{1+kK} (1 - e^{- \frac{t}{\tau}})$, $\tau = \frac{T}{1+kK}$. (What is $y$ if $r$ jumps from $0$ to $1$)

<div class=note>

(1) Sensitivity: $S(s) = (1 + \frac{kK}{1+Ts})^{-1} = \frac{1+Ts}{1 + kK + Ts}$.
(2) Transfer function from $r$ to $y$: $G(s) = 1 - S(s) = \frac{kK}{1+Ts+kK}$.
(3) The Laplace transformation of step jump is $\frac{1}{s}$. The output is $G(s)\frac{1}{s} = \frac{kK}{Ts^2 + as + kKs}$.
(4) Calculate the inverse Laplace: $y(t) = \frac{kK}{1+kK}$

</div>

- **Error**: $e_{\text{step}}(\infty) = \frac{1}{1+kK}$ (so $y$ constantly has this error compared to $r$).

![center w:500](assets/image-4.png)

---

# PI Controller

---

## Steady-State Error

- **Steady-State Error**: $e_{ss}$ means $e \rightarrow 0$ if $d$ and $r$ stays unchanged for an amount of time.
- $e_{ss} = S(0) r_{ss} - S(0)P(0)d_{ss}$, $S = \frac{1}{1+PC}$. To make $e_{ss} \rightarrow 0$, we should let $S(0) = 0$, $C(0) = \infty$. (This works only if $P(0) \neq 0$).

---

## PI Controller

- $C(s) = K_p + \frac{K_i}{s}$: Commonly used, and $K_p$ can $K_i$ can be adjusted.
- Water Heater Example: $S(s) = \frac{Ts^2 + s}{Ts^2 + s + kK_i}$, the numerator is stable, no pole-zero cancellation, so it is stable. $S(0) = 0$, so $e_{ss} \rightarrow 0$.
- Transfer Function: $G(s) = \frac{kK_i}{Ts^2 + s + kK_i}$, or wirtten
$$ G(s) = \frac{\omega_n^2}{s^2 + 2\zeta \omega_ns + \omega_n^2}, \quad \omega_n^2 = \frac{kK_i}{T}, \zeta = \frac{1}{2 \sqrt{kK_iT}}. $$

The poles are symmetric with respect to the real axis, satisfying $\omega_n = |p|$ and $\zeta = \cos \varphi$.


---

# PD Controller

---

## Concept of PD Controller

- $C(s) = K_p + K_ds$.
- Since it is not proper, we use approximations $C(s) = K_p + \frac{K_ds}{1 + Ts}$.
- $s = i\omega$, when $\omega < < \frac{1}{T}$, then $Ts \sim 0$.
- We can use PD controller to stablize the controller.

---

## System Approximation

- $P(s) = \frac{k}{s^2 + a_1s + a_0} + Q(s)$, where $Q(s)$ is usually very small in the frequency range.






