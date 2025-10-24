## Last time -

$$f(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2}(x-a)^2+\dots+\frac{f^{(n)}(a)}{n!}(x-a)^n + E_{n+1}(x)$$
and,
$$
|E_{n+1}(x)| \leq \frac{M}{(n+1)!}|x-a|^{n+1} 
$$
where M is an upper bound for $|f^{(n+1)}(x)|$ on $[x, a]$ or $[a,x]$.

Observations:
* Often you can take $M$ to be a conservative upper estimate (e.g. $e<100$) of $f^{(n+1)}$ instead of finding the exact maximum or minimum.
* As $n \to \infty$, $E_{n+1}(x) \to 0$ quite often.

# Numerical Series

$$
0 = (1-1) + (1-1) + \dots
$$
$$
0 = 1 + (-1 + 1) + (-1 + 1)
$$
$$
\therefore 0 =1
$$
Therefore, we use convergence.

Let $(a_{n})^{\infty}_{n=n_{0}}$ be a sequence. We can now make a new sequence of partial sums.

$$
S_{N} = \sum_{n=n_{0}}^{N} a_{n} = a_{1}+a_{2}+a_{3}+\dots+a_{N}
$$
The series with terms $(a_{n})$ is,
$$
\sum_{n=n_{0}}^{\infty} a_{n} = \lim_{ N \to \infty } \sum_{n=n_{0}}^{N} a_{n}=\lim_{ N \to \infty }S_{N}  
$$
We say the series converges if the limit exists and diverges otherwise. $\text{series} \equiv \text{infinite sum}$.

The main question we want to ask about a series is if it converges. Example:

$$
(a_{n})_{n=0}^\infty, \: a_{n} = (-1)^n
$$
$$
S_{N} = \sum_{n=0}^{N} (-1)^n
$$
$$
S_{1}=(-1)^0 + (-1)^1 = 0, \: S_{2} = 1 -1 + 1 = 1
$$
Therefore, $S_{N}$ is 1 if $N$ is even and 0 if $N$ is odd. This implies,
$$
\lim_{ N \to \infty } S_{N} \text{ DNE}
$$
Since $S$ doesn't get and stay close to any value.  So,
$$
\sum_{n=0}^{\infty} (-1)^n \text{ diverges and is therefore garbage.}
$$
## Most "important" math

If $|a|<1$, consider $a_{n} = a^n$.

$$
\sum_{n=0}^{N} a^n = 1 + a + a^2 + a^{3} + \dots
$$
Formula for $S_{N}$:

$$
(1-a)(1 +a + a^{2}+\dots+a^n) = (1 + a + a^{2} + a^{3} +\dots + a^N) - (a +a^{2} + a^{3} + a^{4} + \dots + a^{N+1})
$$
$$
(1-a)(1 +a + a^{2}+\dots+a^n) = 1 - a^{N+1}
$$
$$
(1 +a + a^{2}+\dots+a^n) = \frac{1 - a^{N+1}}{1 -a}
$$
Therefore,
$$
\sum_{n=0}^{\infty} a^n = \lim_{ N \to \infty } \frac{1-a^{N+1}}{1-a} = \frac{1}{1-a} 
$$
For example,

$$
\sum_{n=1}^{\infty} \left( \frac{-1}{2} \right)^n = \frac{1}{1-(-\frac{1}{2})} = \frac{2}{3}
$$
If we take $|a| \geq 1$, the series doesn't converge.

Take a car loan for example. 
* $D = 30000$ dollars
* $R = 1.05$ interest/year
* $P =$ Annual Payment
So, 
$$
D_{} = 30000
$$
$$
D_{1} = D_{0}(R) - P
$$
$$
D_{2}=D_{1}(R) - P = (D_{0}(R) - P)(R) - P = D_{0}R^{2}-PR-P
$$
$$
\dots
$$
$$
D_{N} = D_{0}R^N-P\left(\sum_{n=o}^{N-1} R^N\right)
$$
$$
D_{N} = D_{0}R^N - P \frac{1-R^N}{1-R}
$$
Suppose you want to pay off in $N = 6$ years,

$$
P = \left(\frac{1-R}{1-R^6}D_{0}R^6\right)
$$
## Visualising Series

We can visualise $\sum_{n=1}^{\infty} \frac{1}{n}$ as the area of an infinite histogram. Consider the graph $y = \frac{1}{x}$. Think of the histogram in your mind (I don't have a pen yet.)

$$
S_{2} > \int_{1}^{3} \frac{1}{x} \, dx 
$$
$$
S_{N} > \int_{1}^{N+1} \frac{1}{x} \, dx = \ln(N+1)
$$
$$
S_{N} > \ln(N+1)
$$
$$
\lim_{ N \to \infty } \ln(N + 1) = \infty 
$$
$$
\implies \lim_{ N \to \infty } S_{N} = \infty
$$
Therefore, the series diverges.