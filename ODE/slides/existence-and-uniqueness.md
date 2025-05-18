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
.question {
  background-color: #f5f5f5;
  padding: 10px;
  margin: 10px 0;
  text-align: left;
}
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

# Existence and Uniqueness of Solutions

Speaker: Yixiao Qian

---

## Table of Contents

---

# Euler's Polygonal Method

---

## Geometric Meaning of ODE

- **Geometric Meaning**: $y^{\prime} = f(x,y)$, then the tangent direction at $(x, y)$ is $f(x,y)$.
- Draw the direction/slope field of $y^{\prime} = x^2 + y^2$.

![center](assets/image.png)

---

## Euler's Polygonal Method

Here we consider the IVP
$$ y^{\prime} = f(x,y), \quad y(x_0) = y_0. $$

- **Euler's Forward Method**: $x_k = x_{k-1} + h$, and $y_{k+1} = y_k + f(x_k, y_k)h$.
- **Equicontinuous**: $\forall \epsilon > 0$, $\exists \delta > 0$, $\forall x_1, x_2$, $|x_1 - x_2| < \delta$, $|f_n(x_1) - f_n(x_2)| < \epsilon$ for all $n > 0$.
- **Uniform Boundedness**: $\exists M > 0$, $\forall x \in I$, $|f_n(x)| \leq M$ for all $n > 0$.
- **Ascoli-Arzela Theorem**: $\{f_n\}$ are equicontinuous and uniformly bounded, then there exist $f_{n_j} \rightrightarrows f$, $f$ is continuous.

<div class=note>

Since $f_{n_j}$ converges rather than $f_n$, then the Euler sequence may have multiple limits.

</div>

---

## Peano's Existence Theorem

- **Peano Existence Theorem**: $f$ is continous in $R: \{(x,y): |x-x_0| < a, |y-y_0| < b\}$. Then IVP has solution when $|x-x_0| \leq \alpha$, where $\alpha = \min \{a, \frac{b}{M}\}$, $M = \max_R |f|$.

<div class=note>

Why $\frac{b}{M}$? Assume $y^{\prime} \equiv M$, then the solution reaches the upper bound of $R$ when $\alpha = \frac{b}{M}$.

</div>


---


# Picard Existence and Uniqueness Theorem

---

## Picard Sequences

- **Integral Equation**: $y(x)$ follows $\displaystyle \frac{\mathrm{d} y}{\mathrm{d} x} = f(x,y)$ with $y(x_0) = y_0$ iff
$$ y(x) = y_0 + \int_{x_0}^x f(t,y(t))\mathrm{d} t $$
- **Picard Sequence**: $\varphi_0(x) = y_0$ and $\displaystyle \varphi_n(x) = y_0 + \int_{x_0}^x f(t, \varphi_{n-1}(t))\mathrm{d} t$ for $n \geq 1$.
- **Lipschitz Continuous**: $f(x,y)$ is *Lipschitz continuous with respect to $y$* if
$$ |f(x,y_1) - f(x,y_2)| \leq L |y_1 - y_2|, \quad \forall (x,y_1),(x,y_2) \in R.$$

---

## Properties of Picard Sequences

---

## Existence and Uniqueness Theorem

<div class=trick>

If $f(x,y)$ is Lipschitz continuous with respect to $y$ in $R = [x_0-a,x_0+a] \times [y_0-b,y_0+b]$. Then there exists a unique solution $y = \varphi(x)$ such that

$$ \frac{\mathrm{d} y}{\mathrm{d} x} = f(x,y), \quad x \in (x_0-h, x_0+h), \quad \varphi(x_0) = y_0, $$

where $h = \min \left( a, \frac{b}{M} \right)$, $M = \max_{(x,y) \in R} |f(x,y)|$.

</div>

---

## Practice on Existence and Uniqueness Theorem

<div class=question>

Assume $\frac{\mathrm{d} y}{\mathrm{d} x} = 2x + \sqrt{\max(0, y)}$ with $y(x_0) = y_0$.
(1) Write the corresponding integration equation;
(2) Write the Picard sequence;
(3) Determine if the solution exists and is unique.

</div>

<div class=note>

(1) The integration equation is ${\displaystyle y(x) = y_0 + \int_{x_0}^x \left[2t + \sqrt{\max(0, y(t))} \right]\mathrm{d} t}$.
(2) The Picard sequence is $y_0(x) = y_0$, $\displaystyle y_{n+1}(x) = y_0 + \int_{x_0}^x \left( 2t + \sqrt{\max (0, y_n(t))} \right)\mathrm{d} t$
(3) $F(x,y) = 2x + \sqrt{\max(0, y)}$. When $y > 0$, $F = 2x + \sqrt{y}$, when $y \leq 0$, $F = 2x$. Consider $y > 0$, $F^{\prime}_y = \frac{1}{2\sqrt{y}}$, when $y \rightarrow 0$, $F^{\prime}_y \rightarrow \infty$, then it does not satisfy Lipschitz condition.

</div>
