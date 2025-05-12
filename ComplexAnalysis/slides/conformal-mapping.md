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

# Properties of Holomorphic Functions

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

- **Conformal Mapping at $z_0$**: $f$ is holomorphic and (1) ${\displaystyle \lim \limits _{z \rightarrow z_0} \frac{|f(z) - f(z_0)|}{|z-z_0|} = |f^{\prime}(z_0)|}$ (2) Preserve angles in magnitude and orientation.
- **Equivalent Definition**: $f$ is holomorphic at $z_0$ and $f^{\prime}(z_0) \neq 0$.
- **Global Conformal Mapping**: $f$ is univalent

