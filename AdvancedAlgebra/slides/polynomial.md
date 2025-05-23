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

# Theory of Divisibility

---

## Divisibility and GCD

- **Polynomial Division**: $f(x)=g(x)q(x)$, $g$ *divisor*, $q$ *quotient*, $f$ is *multiple* of $g$, $g$ *divide* $f$.
- **Division with Remainder**: $f(x) = g(x)q(x) + r(x)$, $r(x)$ is *remainder*.
- **Common Divisor**: If $d(x) | g(x)$ and $d(x)|f(x)$.
- **Greatest Common Divisor**: $d(x) = (f(x), g(x))$ is divisor with highest degree.
- **Euclidean Algorithm**: $d(x) = (f(x),g(x))$, then $d(x) = u(x)f(x) + v(x)g(x)$.

<div class=note>

(1) $u(x)$ and $v(x)$ may not unique.
(2) $d(x) = u(x)f(x) + v(x)g(x)$ doesn't necessarily mean $d(x) = (f(x),g(x))$.

</div>

- **Invariance of GCD**: $(f(x),g(x)) = (af(x) + bg(x), cf(x) + dg(x))$ if $ad - bc \neq 0$.

<div class=note>

(1) Denote lhs $l(x)$. Obviously $l(x) | af(x)+bg(x)$, $l(x) | cf(x)+dg(x)$.
(2) Denote rhs $(f_1(x),g_1(x))$. Then $f(x) = \frac{df_1(x) - bg_1(x)}{ad-bc}$, $g(x) = \frac{ag_1(x) - cf_1(x)}{ad - bc}$. Apply (1) again.

</div>


---

## Details in Euclidean Algorithm

- Find $u(x)$ and $v(x)$ such that $r_3(x) = u(x)f(x) + v(x)g(x)$ if
$$
f(x) = q_1(x)g(x) + r_1(x), \quad
g(x) = q_2(x)r_1(x) + r_2(x), \quad
r_1(x) = q_3(x)r_2(x) + r_3(x), \quad
r_2(x) = q_4(x)r_3(x).
$$

<div class=note>

(1) $r_1(x) = f(x) - q_1(x)g(x)$.
(2) $r_2(x) = -q_2(x)f(x) + [q_1(x)q_2(x) + 1]g(x)$.
(3) $r_3(x) = r_1(x) - q_3(x)r_2(x) = [1+q_2(x)q_3(x)]f(x) - [q_1(x) + q_3(x) + q_1(x)q_2(x)q_3(x)]g(x)$.

</div>

- Given $f(x) = x^4 + 3x^3 - x^2 - 4x - 3$, $g(x) = 3x^3 + 10x^2 + 2x - 3$. Find GCD, $u(x)$, $v(x)$.


---

## Relatively Prime Polynomials

<br>

- **Relatively Prime**: $(f(x),g(x)) = 1$.
- **Equivalent Condition**: $f$ and $g$ are relatively prime iff there exist $u(x), v(x)$ such that
$$ u(x)f(x) + v(x)g(x) = 1. $$
- **Application**: If $(f(x),g(x)) = d(x)$, then $(f(x^m), g(x^m)) = d(x^m)$.

<div class=note>

(1) Assume $f(x) = d(x)f_1(x)$ and $g(x) = d(x)g_1(x)$. $u(x)f_1(x)+v(x)g_1(x) = 1$.
(2) $u(x^m)f_1(x^m) + v(x^m)g_1(x^m) = 1$, then $(f(x^m), g(x^m)) = d(x^m)$.

</div>

---


# Irreducible Polynomials and Remainder Theorem

---

## Irreducible Polynomials and Remainder Theorem

- **Irreducible Polynomial**: $p(x)$ that cannot be expressed as product of any other two.
- **Irreducible Polynomial Factorization**: $f(x) = cp_1^{r_1}(x) \cdots p_s^{r_s}(x)$ uniquely.
- Prove that $(f(x)g(x), f(x)+g(x)) = 1$ if $(f(x), g(x)) = 1$.

<div class=note>

Write the factorization, it is not hard to see.

</div>

- **Remainder Thoerem**: $f(x) \in \mathbb{P}[x]$, then $f(x) = (x-\alpha) q(x) + f(\alpha)$.

<div class=note>

Proof: By division, $f(x) = (x-\alpha)q(x) + c$. Take $x = \alpha$ we get $c = f(\alpha)$.

</div>

- Prove that $x^d - 1 |x^n - 1$ iff $d|n$.

<div class=note>

Over $\mathbb{C}$, $x^d - 1 = (x - x_1)\cdots (x-x_d)$. Then $x_i^n = 0$ for all $i$ iff $n = kd$.

</div>

---

## Applications of Remainder Theorem


- If $(x-1)|f(x^m)$, prove that $(x^m - 1)|f(x^m)$.

<div class=note>

(1) $f(x^m) = (x-1)q(x) + f(1)$, we get $f(1) = 0$.
(2) $f(x) = (x-1)p(x) + f(1) = (x-1)p(x)$, substituting $x$ with $x^m$ yields the result.

</div>

- If the remainders of $f$ divided by $(x-1), (x-2), (x-3)$ are $4, 8, 16$ respectively. Find the remainder of $f$ divided by $(x-1)(x-2)(x-3)$.

<div class=note>

Suppose $f(x) = g(x)(x-1)(x-2)(x-3) + h(x)$, then $\operatorname{deg}(h) = 2$ and $h(1) = 4$, $h(2)=8$, $h(3)=16$. Then we get
$$ h(x) = 2x^2 -2 x + 4. $$

</div>

---

# Multiple Factors and Multiple Roots

---

## Key Points of Multiple Factors and Multiple Roots

- **Multiple Factors vs Roots**: Multiple roots implies multiple factors, converse not true.

<div class=note>

Example: $(x^2 + 1)^2$ has multiple factors in $\mathbb{C}, \mathbb{R}, \mathbb{Q}$, but only has multiple roots in $\mathbb{C}$.

</div>

- **Property**: $p(x)$ irreducible, $p(x)$ is $k$-fold factor of $f$, then it is $(k-1)$-fold factor of $f^{\prime}(x)$
- **Condition of Multiple Factor**: $f(x)$ doesn't have multiple factor iff $(f(x), f^{\prime}(x)) = 1$.


