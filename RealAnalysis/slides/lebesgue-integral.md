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
  text-align: center;
}
.warning {
  background-color: #fee;
  padding: 10px;
  margin: 10px 0;
  text-align: center;
}
</style>

# Lebesgue Integrals

Speaker: Yixiao Qian

---

# Table of Contents

<br>

- Concept of Lebesgue Integral

---

# Concept of Lebesgue Integral

---

## Definition of Lebesgue Integral

<br>

- **Characteristic Function**: $\chi_E(x) = 1$ for $x \in E$ and $\chi_E(x) = 0$ for $x \not \in E$.
- **Integral of Non-Negative Simple Function**: $\displaystyle \int_D f \mathrm{d} x = \sum\limits_{i = 1}^s a_i m(E_i)$.
- **Integral of Non-Negative Measurable Function**: $\displaystyle \int_D f \mathrm{d} x = \lim \limits _{n \rightarrow \infty} \int_D f_n\mathrm{d}x$.
- **Integral of Measurable Function**: ${\displaystyle \int_D f \mathrm{d} x = \int_D f_+ \mathrm{d} x - \int_D f_- \mathrm{d} x}$.


