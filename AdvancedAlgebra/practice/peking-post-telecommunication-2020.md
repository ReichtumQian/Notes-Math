
# Peking University of Posts and Telecommunications Advanced Algebra 2020

## Problem 1

Let the reduced rational number $\frac{p}{q}$ be a root of $f(x) = a_0x^k + a_1x^{k-1} + \cdots + a_{k-1}x + a_k$, where $a_i$ are all integers. Prove that for any integer $m$, $(p-mq)|f(m)$.

**Proof**. Since $\frac{p}{q}$ is a root of $f(x)$, then there exists an integer-coefficient polynomial $g(x)$ such that
$$ f(x) = (qx - p)g(x) \Rightarrow f(m) = (qm - p)g(m). $$
Since $g(m)$ must be an integer, then $(p-mq)|f(m)$.

## Problem 2

Ignored.

## Problem 3

Find all the $n$-order matrices $A$ such that $(A^{\ast})^{\ast} = A$.

**Solution**. According to the properties of adjugate matrix, we know 
$$(A^{\ast})^{\ast}A^{\ast} = |A^{\ast}| I = |A|^{n-1}I
\Rightarrow (A^{\ast})^{\ast}A^{\ast}A = |A|^{n-1}A
\Rightarrow (A^{\ast})^{\ast} = |A|^{n-2}A.
$$
The condition $A = (A^{\ast})^{\ast}$ implies $A = |A|^{n-2}A$. When $n = 2$, any matrix satisfies the condition. When $n > 2$, $|A| = 1$ or $A = O$.

## Problem 4

Let $A$ be a $3 \times 4$ matrix, $r(A) = 1$. If the vector sequence
$$ \alpha_1 = (1,2,0,2)^T, \alpha_2 = (-1,-1,1,a)^T, \alpha_3=(1,-1,a,5)^T, \alpha_4=(2,a,-3,-5)^T $$
is equivalent to the solution system of $AX = O$. Find the general solution of $AX = O$.

