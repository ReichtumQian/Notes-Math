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

# Conformal Mapping

Speaker: Yixiao Qian

---

## Table of Contents

---

# Geometric Interpretation of the Complex Derivative

---

## Angle-Preserving Property of Complex Mappings

- **Angle between two Curves**: Given $C_1:z=z_1(t)$ and $C_2:z=z_2(t)$, the *angle between them at $z_0=z(t_0)$* is $\theta = \operatorname{arg}[z^{\prime}_1(t_0)] - \operatorname{arg} [z^{\prime}_2(t_0)]$.

<div class=note>

Note that $z^{\prime}(t)$ is the complex tangent vector to $z(t)$ at the corresponding point.

</div>

- **Behavior of Complex Mapping**: If $f$ maps $C:z=z(t)$ to $C^{\prime}:z=w(t)$, and $f^{\prime}(z_0) \neq 0$,
$$ \operatorname{arg}[w^{\prime}(t_0)] = \operatorname{arg}[f^{\prime}(z_0)] + \operatorname{arg}[z^{\prime}(t_0)]. $$

<div class=note>

$w(t) = f(z(t))$, by chain rule, $w^{\prime}(t_0) = f^{\prime}(z_0) \cdot z^{\prime}(t_0)$. Given $z = z_1z_2$, then
$$\operatorname{arg}(z) = \operatorname{arg}(z_1) + \operatorname{arg}(z_2).$$

</div>

- **Angle Preservation**: If $f$ is differentiable at $z_0$, then it is angle-preserving at $z_0$, i.e.,

$$ \operatorname{arg}[w^{\prime}_1(t_0)] - \operatorname{arg}[w^{\prime}_2(t_0)] = \operatorname{arg}[z^{\prime}_1(t_0)] - \operatorname{arg}[z^{\prime}_2(t_0)] $$

---

## Scaling Property and Conformal Mapping

- **Local Scale Factor**: If $f$ is differentiable at $z_0$, then the *scale factor at $z_0$* is
$$ \lim \limits _{z \rightarrow z_0} \frac{|f(z) - f(z_0)|}{|z - z_0|} = |f^{\prime}(z_0)|. $$
- **Conformal Mapping**: If $f$ is angle-preserving and has unchanged scale factor (for each direction) at $z_0$, then it is *conformal at $z_0$*
- **Condition for Conformal Mapping**: If $f$ is holomorphic, then $f$ is conformal at $z_0$ iff $f^{\prime}(z_0) \neq 0$.

<div class=note>

The scale factor is $|f^{\prime}(z_0)| \neq 0$ (Same for each direction). Angle-preserving is a property of holomorphic function when $f^{\prime}(z_0) \neq 0$.

</div>

---

---

## Open Mapping Theorem

- **Open Mapping Theorem**: If $f$ is holomorphic in a domain $D$, then $f(D)$ is also a domain (open and connected set).

<div class=note>

Does continuous functions preserve domain? No, like $f(z) = |z|$ maps any domain to $x$ axis.

</div>

---

## Univalent Mapping

- **Univalent Mapping**: $f$ is holomorphic and injective ($z_1 \neq z_2$, $f(z_1) \neq f(z_2)$).
- **Properties of Univalent Mapping**: If $f(z)$ is univalent in $D$, then $f^{\prime}(z) \neq 0$ in $D$.

<div class=note>

Assume $f^{\prime}(z_0) = 0$, then $f(z) = f(z_0) + a_k(z-z_0)^k + o[(z-z_0)^k]$ where $k \geq 2$. Then by local mapping theorem

</div>

---


## Conformal Mapping

- **Equivalent Definition**: $f$ is holomorphic at $z_0$ and $f^{\prime}(z_0) \neq 0$.
- **Global Conformal Mapping**: $f$ is univalent

