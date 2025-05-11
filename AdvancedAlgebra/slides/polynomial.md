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

# Polynomial

Speaker: Yixiao Qian

---

## Table of Contents

---

# Irreducible Polynomials and Remainder Theorem

---

## Irreducible Polynomials

---

## Remainder Theorem and Its Applications

- **Remainder Thoerem**: $f(x) \in \mathbb{P}[x]$, then $f(x) = (x-\alpha) q(x) + f(\alpha)$.

<div class=note>

Proof: By division, $f(x) = (x-\alpha)q(x) + c$. Take $x = \alpha$ we get $c = f(\alpha)$.

</div>

- If the remainders of $f$ divided by $(x-1), (x-2), (x-3)$ are $4, 8, 16$ respectively. Find the remainder of $f$ divided by $(x-1)(x-2)(x-3)$.

<div class=note>

Suppose $f(x) = g(x)(x-1)(x-2)(x-3) + h(x)$, then $\operatorname{deg}(h) = 2$ and $h(1) = 4$, $h(2)=8$, $h(3)=16$. Then we get
$$ h(x) = 2x^2 -2 x + 4. $$

</div>

---

