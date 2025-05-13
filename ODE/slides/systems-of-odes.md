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

# Systems of ODEs

Speaker: Yixiao Qian

---

## Table of Contents

---

---

# Solving Constant-Coefficients Systems of ODEs

---

## Matrix Exponential

- **Matrix Exponential**: $e^A := \sum_{n=0}^{\infty} \frac{A^n}{n!}$.
- **Properties**: $e^{A+B} = e^A e^B$.
- **Powers of a Jordan Block**: The $n$-order power of $J(\lambda)_{k \times k}$ is

$$
  J(\lambda)^n = 
  \begin{bmatrix}
  \lambda^n & \binom{n}{1}\lambda^{n - 1} & \binom{n}{2}\lambda^{n - 2} & \cdots & \binom{n}{k - 1}\lambda^{n - k + 1} \\
  0 & \lambda^n & \binom{n}{1}\lambda^{n - 1} & \cdots & \binom{n}{k - 2}\lambda^{n - k + 2} \\
  \vdots & \vdots & \ddots & \ddots & \vdots \\
  0 & 0 & \cdots & \lambda^n & \binom{n}{1}\lambda^{n - 1} \\
  0 & 0 & \cdots & 0 & \lambda^n
  \end{bmatrix}
$$

<div class=note>

Hint: Consider $J = \lambda I + N$, where $N$ is matrix with $1$s on superdiagonal.

</div>

---

## Solving Constant-Coefficients Systems of ODEs

Here we consider the system of ODEs

$$ \mathbf{x}^{\prime} = A\mathbf{x}(t). $$

- **Matrix-Form Solution**: $\mathbf{x}(t) = e^{At} c$.
- **Fundamental Solution System**: For each eigenvalue $\lambda$ of $A$, the corresponding solutions:

$$
e^{\lambda t} \mathbf{v}_0, \quad
e^{\lambda t} \left( \mathbf{v}_0 + t\mathbf{v}_1 \right), \quad \cdots, \quad
e^{\lambda t} \left( \mathbf{v}_0 + t\mathbf{v}_1 + \cdots + \frac{t^k}{k!}\mathbf{v}_k \right),
$$

where $\mathbf{v}_k$ is the solution of $(A - \lambda I)\mathbf{v} = 0$, $\mathbf{v}_0,\cdots,\mathbf{v}_{k-1}$ are solutions of $(A - \lambda I)\mathbf{v}_j = \mathbf{v}_{j+1}$.

---

## Examples

- Solve ODEs
$$
\begin{cases}
x'=-x + 3y-3z\\
y'=x + y-2z\\
z'=x - y
\end{cases}\quad x(0)=y(0)=z(0)=1
$$

<div class=note>

(1) $\lambda_1 = -1$ with multiplicity $2$, $\lambda_2 = 2$ with multiplicity $1$.
(2) For $\lambda_1 = -1$, $(\lambda_1 I - A)\mathbf{v}_1 = 0$, then $\mathbf{v}_1 = (0,1,1)^T$. $(\lambda_1 I - A)\mathbf{v}_2 = \mathbf{v}_1$, then $\mathbf{v}_1 = (1,0,0)^T$.
(3) For $\lambda_2 = 2$, $(\lambda_2 I - A)\mathbf{v} = 0$, then $\mathbf{v} = (1,1,0)$.
(4) The fundamental solution system is
$$ e^{-t}(0,1,1)^T, \quad e^{-t}t (1,0,0)^T, \quad e^{2t}(1,1,0)^T. $$
(5) $\mathbf{x} = (c_2 t e^{-t} + c_3 e^{2t}, c_1e^{-t} + c_2e^{2t}, c_1e^{-t})$. Then $c_1 = c_2 = 1$, $c_3 = 0$.

</div>



