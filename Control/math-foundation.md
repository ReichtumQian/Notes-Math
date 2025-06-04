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

