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

# Nonlinear ODEs

Speaker: Yixiao Qian

---

## Table of Contents

---

# Lyapunov Stability

---

## Concept of Lyapunov Stability

- **Lyapunov Stable**: Consider $\mathbf{x} = \mathbf{f}(\mathbf{x})$, $f(0) = 0$ where $f$ is locally Lipschitz. The solution $x = 0$ is *Lyapunov stable* if
$$ \forall \epsilon > 0, \exists \delta > 0, \|x(0)\|<\delta, \quad \|x(t)\| < \epsilon, \quad \forall t \geq 0. $$
- **Asymptotic Stability**: Add $\lim \limits _{t \rightarrow \infty}\|x(t)\| = 0$ when $\|x(0)\| < \delta$.


