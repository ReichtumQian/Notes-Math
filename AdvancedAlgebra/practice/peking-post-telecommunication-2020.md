
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

**Solution**. Since $r(A) = 1$, then the number of free variables in the fundamental solution system of $Ax = 0$ is $3$. Then
$$
  \begin{bmatrix}
    1 & 2 & 0 & 2\\
    -1 & -1 & 1 & a\\
    1 & -1 & a & 5\\
    2 & a & -3 & -5
  \end{bmatrix}
  \rightarrow
  \begin{bmatrix}
    1 & 2 & 0 & 2\\
    0 & 1 & 1 & 2+a\\
    0 & 0 & a+3 & 9+3a\\
    0 & 0 & 1-a & -a^2 + 2a - 1
  \end{bmatrix}
$$
has a rank of $3$, so $a = -3$ or $a = 1$. When $a = -3$, the general solution is
$$ x = \gamma_1 (1, 2, 0, 2)^T + \gamma_2 (0, 1, 1, -1)^T + \gamma_3(0, 0, 4, -4)^T.  $$
When $a = 1$, the general solution is
$$ x = \gamma_1 (1, 2, 0, 2)^T + \gamma_2 (0, 1, 1, 3)^T + \gamma_3(0, 0, 4, 12)^T.  $$


## Problem 5
