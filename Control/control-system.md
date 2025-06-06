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

## Concept of Control System

- **Components**: **Plant** (object to be controlled), **Controller**, **Reference/Demand**.
- **Signal**: **Physiccal Signal**, **Analog** (continuous-valued), **Digital** (discrete-valued).
- **Continuous/Discrete-Time**: Function defined on $[0, +\infty)$ or $\{0,1,2,\cdots\}$.

---

## Standard Feedback Connection

- $d(t)$ is noise, $r(t)$ is reference, $y(t)$ is output of the plant, $e(t)$ is input of the controller.
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
- **Loop Gain**: Remove $d$ and $r$, input $x$, output $P(s)C(s)x$
- **Sensitivity**: $e=r-y$ and $y=PCe$, then $S := \frac{e}{r} = (1+PC)^{-1}$.


---

## Stability of Standard Feedback Connection

- **Stability Condition**: Iff (1) $S$ is stable; (2) No unstable pole-zero cancellation in $PC$.
- **Stable Pole-Zero Cancallation**: The pole/zero cancelled is in $\mathbb{C}_-$ (not include $\operatorname{Re}z = 0$)

<div class=note>

There is a pole-zero cancellation:
$$ P(s) = \frac{s}{(s+1)(s-2)}, \quad C(s) =   $$

</div>

---

# Control of a First Order System

---

## Example: Control of a First Order System

- **Plant**: The transfer function is $\frac{k}{1+Ts}$, where $T$ is time constant, $k$ is gain.
- **Proportional Control**: The transfer function $C(s) = K$ (Constant Gain).

![center w:600](assets/image-3.png)

---

## Step Response of First Order System

- **Step Response**: $y_{\text{step}} = \frac{kK}{1+kK} (1 - e^{- \frac{t}{\tau}})$, $\tau = \frac{T}{1+kK}$. (What is $y$ if $r$ jumps from $0$ to $1$)
- **Error**: $e_{\text{step}}(\infty) = \frac{1}{1+kK}$ (so $y$ constantly has this error compared to $r$).

![center w:700](assets/image-4.png)



