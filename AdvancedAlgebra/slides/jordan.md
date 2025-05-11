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

# Jordan Canonical Forms

Speaker: Yixiao Qian

---

## Table of Contents

<br>

- Existence of Jordan Canonical Form
- Properties of Jordan Canonical Form
- $\lambda$ Matrices

---

# Existence of Jordan Canonical Form

---

## Kernel Space Decomposition

- **Kernel Space Decomposition**: Let $f(x) = f_1(x)f_2(x)$ where $(f_1(x), f_2(x)) = 1$, then
$$ \operatorname{Ker}(f(\mathcal{A})) = \operatorname{Ker}(f_1(\mathcal{A})) \oplus \operatorname{Ker}(f_2(\mathcal{A})). $$

<div class=note>

We have ${\displaystyle \mathcal{I} = u(\mathcal{A})f_1(\mathcal{A}) + v(\mathcal{A})f_2(\mathcal{A})}$. Take $\alpha \in \operatorname{Ker}(f(\mathcal{A}))$, then
$$ \alpha = u(\mathcal{A})f_1(\mathcal{A})\alpha + v(\mathcal{A})f_2(\mathcal{A})\alpha := \alpha_1 + \alpha_2. $$
Since $f_2(\mathcal{A})\alpha_1 = u(\mathcal{A})f(\mathcal{A})\alpha = 0$, then $\alpha_1 \in \operatorname{Ker}(f_2(\mathcal{A}))$. Similarly $\alpha_2 \in \operatorname{Ker}(f_1(\mathcal{A}))$. For any $\alpha \in \operatorname{Ker}(f_1(\mathcal{A}))\cap \operatorname{Ker}(f_2(\mathcal{A}))$,
$$ \alpha = u(\mathcal{A})f_1(\mathcal{A})\alpha + v(\mathcal{A})f_2(\mathcal{A})\alpha = 0, $$
then it is direct sum.
</div>

- **Kernel of Zero Transformation**: $\operatorname{Ker}(\mathcal{O}) = V$.


---

## Generalized Eigenspaces Decomposition

- **Generalized Eigenspace Decomposition**: Let $m(\lambda) = (\lambda-\lambda_1)^{\ell_1} \cdots (\lambda - \lambda_s)^{\ell_s}$ be the minimial polynomial of $\mathcal{A}$, $G_{\lambda_i} := \operatorname{Ker}(\mathcal{A} - \lambda_i \mathcal{I})^{\ell_i}$, then
$$ V = G_{\lambda_1} \oplus G_{\lambda_2} \oplus \cdots \oplus G_{\lambda_s}. $$
- **Jordan Matrix for $\lambda$**: $J(\lambda) = \operatorname{diag}(J_1(\lambda), \cdots, J_m(\lambda))$, where $m$ is the geometric multiplicity of $\lambda$, $J_i$ is a $n_i \times n_i$ matrix.

<div class=note>

1. The degree of the term $(\lambda-\lambda_i)^{\ell_i}$ in $m(\lambda)$ satisfies $\ell_i = \max_i \{n_i\}$.
2. The algebraic multiplicity of $\lambda_i$ is $\sum_i n_i$.
3. $r(J_i) = n_i - 1$, $r(J(\lambda)) = \sum_i n_i - m$. And we can see $m$ is the geometric multiplicity.
</div>


---

## Cyclic Invariant Subspaces Decomposition

<br>

- **Cyclic Invariant Property**: $\mathcal{A}_i:=(\mathcal{A} - \lambda_i \mathcal{I})|_{G_{\lambda_i}}$ is nilpotent, with $\mathcal{A}_i^{\ell_i} = \mathcal{O}$.
- **Cyclic Invariant Space Decomposition**: There exists $v_1,\cdots,v_m \in G_{\lambda_i}$ such that
$$ G_{\lambda_i} = \operatorname{span}(v_1, \mathcal{A}_i v_1, \cdots, \mathcal{A}_i^{n_1-1}v_1) \oplus \cdots \oplus \operatorname{span}(v_m, \mathcal{A}_iv_m, \cdots, \mathcal{A}^{n_m - 1}_i v_m). $$
- **Jordan Blocks/Chains**:


---

# Properties of Jordan Canonical Form

---

## Powers of Jordan Canonical Form

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

Consider $J(\lambda) = \lambda I + N$, then $J(\lambda)^n = (\lambda I + N)^n = \sum_{i=0}^n \binom{n}{i} \lambda^{n-i}N^i$. Here, $N^i$ is a matrix with $1$s on the $k$-th superdiagonal and $0$s elsewhere. Then $N^{k-1} \neq O$ and $N^k = O$, so
$$ J(\lambda)^n = \sum\limits_{i=0}^{\min(n, k)} \binom{n}{i} \lambda^{n-i} N^i. $$

</div>

