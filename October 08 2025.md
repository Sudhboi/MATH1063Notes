## Example

Take $b(n)$ and $a(n)$ where $b(n)$ is $a(n)$ with zeroes intertwined.

$$
A_{n} = \sum_{k=1}^{n} a_{n} \text{ and }  B_{n} = \sum_{k=1}^{n} b(n)
$$

Let there be a catchup function $C: \mathbb{N} \to \mathbb{N}$

$$
A_{n} = B_{C(n)}
$$

$\sum a_{n} = L$ if for every $\epsilon$ there is some $N$ s.t. for all $n>N(\epsilon)$ s.t. $|A_{n} - L|<\epsilon$. For the same $\epsilon$ we can take $M=C(N(\epsilon))$ and $|B_{m} - L|<\epsilon$ for all $m>C(N(\epsilon))$. So, $\sum a_{n} = \sum b_{n}$.

## Conditional v.s. Absolute Convergence

If $\sum |a_{n}|$ converges, we say that $\sum a_{n}$ converges absolutely. In this case, we can rearrange the terms as we like and the result stays unchanged.

If $\sum a_{n}$ converges but $\sum |a_{n}|$ diverges, we say $\sum a_{n}$ converges conditionally.

Facts: If $\sum a_{n}$ passes the ratio test, then it converges absolutely.

## Root test

Take $\lim_{ n \to \infty } |a_{n}|^{1/n} = \rho$.

* If $0\leq\rho<1$ then it converges.
* If $\rho>1$ then it diverges.

"Proof": For $n\gg0$, $|a_{n}|\approx \rho^n$, compare with $\sum \rho^n$, which is a geometric series.

## Alternating Series Test

If $a_{n} \to 0$ and $a_{n}$ is positive and decreasing, then $\sum_{n=1}^{\infty}(-1)^na_{n}$ converges.

Example: $\sum_{n=1}^{\infty} \frac{(-1)^n}{n}$.

Since $\frac{1}{n} \to 0$ and is decreasing,
By the alternating series test, it converges.

(Note that $\left|\sum\frac{(-1)^n}{n}\right|$ does not converge.)

## Series as Jumps

Suppose we have an alternating series $\sum_{n=1}^{\infty}(-1)^na_{n}$ and $a_{n}$ decreases to 0. Drawing the graph, we can see a spiral.

The Partial sums $S_{0}, S_{2}, S_{4},\dots$ are decreasing but they are bounded below. Therefore, they must converge. Similar for the odd partials sums.

$$
S_{0}>S_{2}>S_{4}>\dots>L>\dots>S_{5}>S_{3}>S_{1}
$$

Note that $|S_{n} - S_{n-1}| = a_{n} \implies |L-S_{n}|<a_{n}$.

For example, the alternating harmonic series, $\sum_{n=1}^{\infty} \frac{(-1)^n}{n}$ we know that $|S_{n} - L| < \frac{1}{N}$.
So for 0.001 accuracy we take $S_{1000}$.

## Dirichlet Test (Not on the test)

$\sum_{n=1}^{\infty} a_{n}b_{n}$. If $a_{n} \to 0$ & $B_{N}=\sum_{n=1}^{N}b_{n}$ is bounded, then the series converges.

For example, 

$$
\sum_{n=1}^{\infty} \frac{1}{n} (-1)^n
$$
$$
a_{n}= \frac{1}{n} \quad b_{n}=(-1)^n
$$

For all $N$, $0\leq B_{N} \leq {1}$, so it is bounded, and $a_{n} \to 0$ So by Dirichlet's test, it converges.

Now we take $\sum_{n=1}^{\infty} \frac{\sin(n)}{n} = \sum_{n=1}^{\infty}a_{n}b_{n}$.

$a_{n} \to 0$, $b_{n} = \sin(n)$. $B_{N} = \sum_{n=1}^{N}\sin(n)$. 

Is $B_{N}$ bounded? There are three possibilites. It is bounded, or drifts to $\pm \infty$, or goes all over the place.

We are saved because there is a nice formula for $B_{n}$.

$$
e^{i\theta} = \cos(\theta) + i\sin(\theta) \text{ when } \theta \text{ is real.}
$$
$$
e^{i\alpha}\cdot e^{i\beta} = e^{i(\beta+\alpha)}
$$
$$
e = \cos(1) + i\sin(1)
$$
$$
(e^i)^n = \cos(n) + i\sin(n);\:z=e^i
$$
$$
1 + z + z^{2}+z^{3}+\dots+z^n = \sum_{k=0}^{n} \cos(k) + i\left[ \sum_{k=0}^{n} \sin(k) \right]
$$

Since it is a geometric series,

$$
1 + z + z^{2}+z^{3}+\dots+z^n = \frac{1-z^{n+1}}{1-z} = \frac{1-e^{i(n+1)}}{1-[\cos(1) + i\sin(1)]}$$

since $|e^{i(n+1)}| = 1$, it converges. (Taking the imaginary part and shit.)

Therefore, our initial series converges.


