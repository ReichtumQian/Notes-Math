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

# Solution Structure of Systems of ODEs

---

## Linear Independence of Solutions

- **Linear Independence**: If $c_1\mathbf{x}_1(t) + \cdots + c_n\mathbf{x}_n(t) = 0$ for all $t$, then $c_1=c_2=\cdots=c_n=0$.
- **Wronsky Determinant**: $\mathbf{x}_1(t),\cdots,\mathbf{x}_n(t)$ are solutions of $\mathbf{x}^{\prime}(t) = A(t)\mathbf{x}(t)$, then they linearly independent iff
$$
W(t) =
\begin{vmatrix}
  x_{11}(t) & x_{12}(t) & \cdots & x_{1n}(t)\\
  x_{21}(t) & x_{22}(t) & \cdots & x_{2n}(t)\\
  \vdots & \vdots & \ddots & \vdots \\
  x_{n1}(t) & x_{n2}(t) & \cdots & x_{nn}(t)
\end{vmatrix} \neq 0 , \quad \forall t.
$$
- **Liouville Formula**: $W(t) = W(t_0) e^{\int_{t_0}^t \operatorname{tr} A(s) \mathrm{d} s}$. Then $W(t) \neq 0$ ($\forall t$) iff $W(t_0) \neq 0$.

<div class=note>

Note that $\mathbf{x}_1 = (1,0,0)^T$, $\mathbf{x}_2=(t,0,0)^T$, $\mathbf{x}_3=(t^2,0,0)^T$ are linearly independent, but $W(t) \equiv 0$. Because they are not solutions of $\mathbf{x}^{\prime}=A\mathbf{x}$.

</div>

---

## Solution Structure of $\mathbf{x}^{\prime}(t) = A(t)\mathbf{x}(t)$

<br>

- **Fundamental Solution System**: Arbitrary $n$ linear independent solutions $\mathbf{x}_1(t),\cdots,\mathbf{x}_n(t)$.
- **Fundamental Solution Matrix**: $\Phi(t) := [\mathbf{x}_1(t),\cdots,\mathbf{x}_n(t)]$.

<div class=note>

Note that fundamental solution matrix is not unique. Given two $\Phi(t)$ and $\Psi(t)$, then there exists an invertible matrix $C$ such that $\Phi = \Psi C$.

</div>

- **Linear Independence**: $\mathbf{x}_1(t),\cdots,\mathbf{x}_n(t)$ are linearly independent iff $|\Phi(t)| \neq 0$ for all $t$.
- **General Solution**: $\mathbf{x}(t) = \Phi(t)C = c_1\mathbf{x}_1(t) + \cdots + c_n\mathbf{x}_n(t)$.

---

## Solution Structure of $\mathbf{x}^{\prime}(t) = A(t)\mathbf{x}(t) + \mathbf{b}(t)$

- **Solution Structure**: $\mathbf{x}^{\ast} + c_1\mathbf{x}_1(t) + \cdots + c_n\mathbf{x}_n(t)$, where $\mathbf{x}^{\ast}$ is a particular solution, $\mathbf{x}_i(t)$ are fundamental solution system of $\mathbf{x}^{\prime}(t) = A(t)\mathbf{x}(t)$.
- **Variation of Parameters**: $\mathbf{x}(t) = \Phi(t)C(t)$, where $C(t)$ follows $C^{\prime}(t) = \Phi^{-1}(t)\mathbf{b}(t)$ and $C(t_0) = \Phi^{-1}(t_0)\mathbf{x}(t_0)$.
- Solve the following ODEs
$$
\mathbf{x}^{\prime} =
\begin{bmatrix}
  1 & 1\\
  0 & 1
\end{bmatrix}
\mathbf{x} +
\begin{bmatrix}
  e^{-t}\\
  0
\end{bmatrix}, \quad \mathbf{x}(t_0) =
\begin{bmatrix}
  -1\\1
\end{bmatrix}
$$


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

## Examples of Homogeneous Systems

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

---

## Examples of Inhomogeneous Systems

- Solve ODEs
$$
\begin{cases}
  x^{\prime} = x + y\\
  y^{\prime} = -x + 3y + e^{2t}
\end{cases}, \quad x(0) = 1, y(0) = -1.
$$

<div class=note>

</div>



