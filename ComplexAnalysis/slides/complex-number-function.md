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

- **Complex-Valued Function**: $f(z) = u(z) + v(z) i$.
- **Holomorphic Function**: $f^{\prime}(z_0) := \lim \limits _{h \rightarrow 0} \frac{f(z_0+h) - f(z_0)}{h}$ ($h \in \mathbb{C}$) exists.
- **Entire**: $f$ is holomorphic in $\mathbb{C}$.
- **Representation**: $f^{\prime}(z_0) = u_x(z_0) + v_x(z_0)i = v_y(z_0) - iu_y(z_0)$.

<div class=note>

Take $h \in \mathbb{R}$, $f^{\prime}(z_0) = u_x(z_0) + v_x(z_0)i$. Take $h = ik$, $f^{\prime}(z_0) = v_y(z_0) - iu_y(z_0)$.

</div>

- **Zero Derivative**: If $f(z)$ is holomorphic, $f^{\prime}(z) \equiv 0$, then $f(z)$ is constant.

<div class=note>

$f^{\prime}(z) \equiv 0$ implies $u_x \equiv u_y \equiv v_x \equiv v_y \equiv 0$. Then $f$ is constant.

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

- **Cauchy-Riemann Equation**: $f$ is holomorphic iff $u,v$ have continuous derivatives and
$$
\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y},
\frac{\partial u}{\partial y} = - \frac{\partial v}{\partial x}, \quad
\text{or} \quad
\frac{\partial f}{\partial \overline{z}} = 0$$

<div class=note>

Cauchy-Riemann equation implies that any function relies on $\overline{z}$ is not holomorphic.

</div>

---

## Example of Cauchy-Riemann Equation

Prove $f(z)$ satisifies Cauchy-Riemann equation, but is not differentiable at the origin.

$$ f(z) =
\begin{cases}
  \frac{x^3 - y^3 + i(x^3 + y^3)}{x^2 + y^2} & \text{if } z \neq 0;\\
  0 & \text{if } z = 0.
\end{cases}
$$

<div class=note>

Write $f(x,y) = u(x,y) + iv(x,y)$, then $u_x(0,0) = 1$, $u_y(0,0)=-1$, $v_x(0,0)=1$, $v_y(0,0) = 1$.
Choose $y = kx$, then
$$ \lim \limits _{(x,y) \rightarrow (0,0)} \frac{f(x,y) - f(0,0)}{x + iy}  $$
does not exist.

</div>

---

## Cases of Constant Function

- If $f(z)$ is holomorphic, $\overline{f(z)}$ is holomorphic, then $f(z)$ is constant.

<div class=note>

C-R equation on $f$ implies $u_x=v_y, u_y=-v_x$. C-R equation on $\overline{f}$ implies $u_x=-v_y, u_y = v_x$.

$$ u_x \equiv u_y \equiv v_x \equiv v_y \equiv 0. $$

</div>

- If $f(z)$ is holomorphic, $|f(z)|$ is constant, then $f(z)$ is constant.

<div class=note>

$\overline{f(z)} = \frac{|f(z)|^2}{f(z)}$, then $|f(z)|$ is constant implies $\overline{f(z)}$ is holomorphic.

</div>

- If $f(z)$ is holomorphic, $\operatorname{Re}(f(z)) \equiv 0$, then $f(z)$ is constant.

<div class=note>

$u(x,y) \equiv 0$ implies $u_x \equiv u_y \equiv 0$. Then C-R equation implies $v_x \equiv v_y \equiv 0$.

</div>




