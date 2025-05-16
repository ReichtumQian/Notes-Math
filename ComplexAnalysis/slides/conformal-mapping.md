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

# Local Conformal Mappings

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
- **Condition for Conformal Mapping**: $f$ is holomorphic, then $f$ is conformal at $z_0$ iff $f^{\prime}(z_0) = |J_f(z_0)| \neq 0$.

<div class=note>

The scale factor is $|f^{\prime}(z_0)| \neq 0$ (Same for each direction). Angle-preserving is a property of holomorphic function when $f^{\prime}(z_0) \neq 0$.

</div>

---

# Univalent Mappings (Global Conformal Mappings)

---

## Univalent Mapping (Global Conformal Mapping)

- **Univalent Mapping**: $f$ is holomorphic and injective ($z_1 \neq z_2$, $f(z_1) \neq f(z_2)$).
- **Univalent Mapping is Conformal**: If $f(z)$ is univalent in $D$, then $f^{\prime}(z) \neq 0$ in $D$.

<div class=note>

Assume $f^{\prime}(z_0) = 0$, then $z_0$ is a $n$-order zero for $g(z) = f(z) - f(z_0)$ where $n \geq 2$. Denote $C:|z-z_0| = \delta$, $m = \inf_C |f(z) - f(z_0)|$. By Rouche's theorem when $0 < |a| < m$, 
$$ h(z) = f(z) - f(z_0) - a $$
has $n$ zeros inside $C$. Take $\delta$ sufficiently small such that $f(z)$ has no zeros other than $z_0$, then there exists $z_1,z_2,\cdots,z_n$ such that $f(z_i)-f(z_0)-a = 0$ and $z_i \neq z_0$. Then
$$ f(z_i) = f(z_0) + a, \quad i = 1,2,\cdots,n. $$
This contradicts the injectivity.

</div>

---

## Applications of Univalent Mapping

- Prove that except linear functions, there does not exist any entire function $f$ such that the inverse $f^{-1}$ is also entire.

<div class=note>

(1) Since $f$ and $f^{-1}$ are entire, then $f$ is bijective (surjective since $f^{-1}$ defined on every points in $\mathbb{C}$, injective since the existence of $f^{-1}$).
(2) $f$ is univalent, then $f^{\prime}(z) \neq 0$ for any $z \in \mathbb{C}$.
(3) Assume $f^{\prime}(z)$ is not constant, then 

</div>


