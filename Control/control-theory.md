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

- **Plant**: The object to be controlled.


---

## Classification of Signals

- **Physics**:
- **Analog**: Values are continuous
- **Digital**: Finite number of possible values (due to noise or uncertainty)
- **Continuous/Discrete-Time**: Function defined on $[0, +\infty)$ or $\{0,1,2,\cdots\}$.
- **Sampling**: Generate discrete-time signal from continuous-time signal.

---

## Standard Feedback Connection

- **Input and Output**: $x = [d, r]$, $y = [u,e]$. (The output can actually be any, you choose.)
- **Aim**: (1) Stable System; (2) Small Tracking Error.
- **Transfer Function**: We know $
\begin{bmatrix}
  \hat{u}\\ \hat{e}
\end{bmatrix} =
\begin{bmatrix}
  1 & -C\\
  P & 1
\end{bmatrix}^{-1}
\begin{bmatrix}
  \hat{d} \\ \hat{r}
\end{bmatrix}
 =$,
- **Transfer Function along the Circuit**: $d$ to $u$ is $S$; $d$ to $y$ is $SP$; $r$ to $y$.
- **Condition**: The feedback connection is stable iff (1) The sensitivity $S = (1+PC)^{-1}$ is stable; (2) There is no unstable pole-zero cancellation in $PC$ (loop gain).
- **Stable Pole-Zero Cancallation**: The pole/zero cancelled is in $\mathbb{C}_-$ (not include $\operatorname{Re}z = 0$)

<div class=note>

There is a pole-zero cancellation:
$$ P(s) = \frac{s}{(s+1)(s-2)}, \quad C(s) =   $$

</div>

---

## Example: Control of a First Order System






