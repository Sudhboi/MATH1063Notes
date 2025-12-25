## Ordinary Differential Equations

- One independent variable $t$.
- Solve for functions $y$ that satisfy equations involving $y$, $y'$, $\dots$ and $t$.

Eg.

$$
y' = f(t)
$$
Solve for $y = y(t)$.

$$
\implies y = \int_{a}^{t} f(x) \, dx + C = \int f(t) dt
$$

Generally speaking, differential equations don't have unique solutions, there are parameters.

## Power Series Methods

$y'' + y = 0$

Implicit: $y''$ and $y$ exists. $y'' = -y$. $y$ is infinitely differentiable, so maybe it has a taylor series. Assume,

$y(t) = a_{0} + a_{1}t+a_{2}t^{2}+a_{3}t^{3}+\dots$

which is the taylor series expansion at $t = 0$.

$$
y''(t) = 2a_{2} + 6a_{3}t + 12a_{4}t^{2}
$$

Since $y'' = -y$,

$$
a_{0} = -2a_{2}
$$
$$
a_{1} = -6a_{3}
$$
$$
a_{m} = -(m+2)(m+1)a_{m+2}
$$

So we have relationships between the terms. So in particular, $a_{0}$ determines $a_{2n}$ for all $n$, and $a_{1}$ determines $a_{2n+1}$ for all $n$.

If $y(t) = \sum_{n=0}^{\infty}a_{n}t^{n}$, $a_{0} = y(0)$, $a_{1} = y'(0)$. Given $y'' + y = 0$ and values $y(0)$ and $y'(0)$, there is a unique solution.

$$
a_{m+2} = -\frac{a_{m}}{(m+2)(m+1)}
$$
$$
a_{0}, a_{2} = -\frac{a_{0}}{2}
$$