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

# Complex Numbers and Complex Functions

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Complex Numbers
- Holomorphic Functions

---

# Complex Numbers

---

## Algebra Form of Complex Numbers

- **Complex Number**: $z = x + iy$, $x = \operatorname{Re}z$, $y = \operatorname{Im}z$.
- **Complex Conjugate**: $\overline{z} = x - iy$.
- **Absolute Value**: $|z| = x^2 + y^2$.
- **Properties of Absolute Value**: (1) $|z|^2 = z \cdot \overline{z}$; (2) $|z| \leq |x| + |y|$; (3) $|z+w| \leq |z| + |w|$.

---

## Polar Form of Complex Numbers

- **Polar Form of Complex Number**: $z = r e^{i\theta}$, where $r = |z|$ and $e^{i\theta} = \cos \theta + i \sin \theta$.
- **Solution of $z^n = re^{i\theta}$**: $z_k = \sqrt[n]{r} e^{\frac{2k\pi + \theta}{n}i}$ for $k = 0,1,\cdots,n-1$.
- Find the roots of $(1 + z)^5 = (1 - z)^5$.

<div class=note>

$\left( \frac{1+z}{1-z} \right)^5 = 1$, then $\frac{1+z}{1-z} = e^{\frac{2k\pi}{5}i} := w_k$ for $k = 0,1,2,3,4$. Thus $z = \frac{w_k}{w_k + 1}$.
</div>


---

# Holomorphic Functions

---

## Key Points of Holomorphic Function

- **Holomorphic Function**: $f^{\prime}(z_0) := \lim \limits _{h \rightarrow 0} \frac{f(z_0+h) - f(z_0)}{h}$ ($h \in \mathbb{C}$) exists.
- **Entire**: $f$ is holomorphic in $\mathbb{C}$.
- **Representation**: $f^{\prime}(z_0) = u_x(z_0) + v_x(z_0)i = v_y(z_0) - iu_y(z_0)$.

<div class=note>

Take $h \in \mathbb{R}$, $f^{\prime}(z_0) = u_x(z_0) + v_x(z_0)i$. Take $h = ik$, $f^{\prime}(z_0) = v_y(z_0) - iu_y(z_0)$.

</div>

---

## Cauchy-Riemann Equation

- **Partial Derivatives**:
$$
\frac{\partial f}{\partial z} := \frac{1}{2} \left( \frac{\partial f}{\partial x} + \frac{1}{i} \frac{\partial f}{\partial y} \right), \quad
\frac{\partial f}{\partial \overline{z}} := \frac{1}{2} \left( \frac{\partial f}{\partial x} - \frac{1}{i} \frac{\partial f}{\partial y} \right).$$

<div class=note>

Why above derivatives: $f(x,y) = f(z, \overline{z})$, with $x(z, \overline{z}) = \frac{1}{2}(z + \overline{z})$ and $y(z, \overline{z}) = \frac{1}{2}(z - \overline{z})$,

$$
f_z = f_x x_z + f_y y_z = \frac{1}{2}(f_x + \frac{1}{i}f_y), \quad
f_{\overline{z}} = f_x x_{\overline{z}} + f_y y_{\overline{z}} = \frac{1}{2}(f_x - \frac{1}{i}f_y).
$$

</div>

- **Cauchy-Riemann Equation**: $f = u + iv$ is holomorphic iff $u,v$ have continuous derivatives and
$$
\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y},
\frac{\partial u}{\partial y} = - \frac{\partial v}{\partial x}, \quad
\text{or} \quad
\frac{\partial f}{\partial \overline{z}} = 0$$


