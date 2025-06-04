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

- Here $d$ is noise, $r$ is reference, $y$ is output of the plant, $e$ is input of the controller.
- **Input and Output**: $x = [d, r]$, $y = [u,e]$. (The output can actually be any, you choose.)
![center w:700](assets/image.png)

- **Transfer Function**: $
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
 =
 \begin{bmatrix}
   (1+CP)^{-1} & C(1+PC)^{-1}\\
   -P(1+CP)^{-1} & (1+PC)^{-1}
 \end{bmatrix}
 \begin{bmatrix}
   \hat{d}\\ \hat{r}
 \end{bmatrix}
 $.

<div class=note>

Hereafter, we denote $S = (1+PC)^{-1}$ as the sensitivity and $PC$ the loop gain.

</div>

---

## Stability of Standard Feedback Connection

- **Stability Condition**: Iff (1) $S$ is stable; (2) No unstable pole-zero cancellation in $PC$.
- **Stable Pole-Zero Cancallation**: The pole/zero cancelled is in $\mathbb{C}_-$ (not include $\operatorname{Re}z = 0$)

<div class=note>

There is a pole-zero cancellation:
$$ P(s) = \frac{s}{(s+1)(s-2)}, \quad C(s) =   $$

</div>

---

## Example: Control of a First Order System

- **Proportional Control**: $C(s) = K$ (Constant Gain).

![center w:600](assets/image-3.png)






