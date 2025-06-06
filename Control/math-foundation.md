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


# Mathematical Foundation of Control Theory

Speaker: Yixiao Qian

---

## Laplace Transormations

- **Laplace Transformation**: $\displaystyle \hat{u}(s) = \mathcal{L} \{u(t)\} = \int_0^{+\infty} e^{-st}u(t)\mathrm{d} t$.
- **Linearity**: $\mathcal{L}\{a u(t) + bv(t)\} = a \hat{u}(s) + b \hat{v}(s)$.
- **Differentiation in Time**: $\mathcal{L} \{u^{\prime}(t)\} = s\hat{u}(s) - u(0)$.
- **Integration in Time**: $\displaystyle \mathcal{L}\{\int_0^t f(\tau)\mathrm{d} \tau\} = \frac{\hat{u}(s)}{s}$.
- **Convolution Product**: $\displaystyle (u \ast v) (t) = \int_0^t u(t - \sigma) v(\sigma)\mathrm{d} \sigma$.
- **Convolution Theorem**: $\mathcal{L}\{u \ast v\} = \hat{u}(s)\hat{v}(s)$.

---

## Final Value Theorem

- **Final Value Theorem**: $\lim \limits _{t \rightarrow \infty}u(t) = \lim \limits _{s \rightarrow 0} s\hat{u}(s)$.

<div class=note>

(1) Since $\mathcal{L}u^{\prime}(t) = s\hat{u}(s) - u(0)$, take limit $s \rightarrow 0$ on both sides.
(2) LHS: $\displaystyle \lim \limits _{s \rightarrow 0} \int_0^{+\infty}e^{-st}u^{\prime}(t)\mathrm{d} t = \int_0^{+\infty}u^{\prime}(t)\mathrm{d} t = u(\infty) - u(0)$.
(3) RHS: $\lim \limits _{s \rightarrow 0}s\hat{u}(s) - u(0)$.
(4) Comparing LHS and RHS yields the conclusion.

</div>


