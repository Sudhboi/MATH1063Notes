If $S$ is finite, then we can assign $\mu(x_{i})$ for each $x_{i} \in S$.

Eg. for two six sided dice convolve stuff, for six sided die it's 1/6 for each event. ...

If $S = \mathbb{R}$, we can measure intervals as follows.

$$
\mu{ (a,b) } = \int_{a}^{b} p(x) \, dx 
$$

This gives a measure if both,
1. $p(x) \geq 0$ for all $x$.
2. $\int_{-\infty}^{\infty} p(x) \, dx = 1$.

If $p(x)$ satisfies these then $p$ is called a probability density function.

Interpretation: If an experiment with an uncertain outcome is performed repeatedly,
Eg.
- Measurement errors
- Genetics
If $E$ is an event, eg. the chicken is white
$$
\frac{\text{\# of times event occurs in } E }{\text{\# of experiments}} \to^{\text{almost surely}} \mu(E)
$$
We say $X$ is a random variable if it represents the outcome of an experiment and we write $p(X \in E)$ to be the probability that $X$ is in $E$. ($P(X\in E) = \mu(E)$).

Cumulative distribution function - 
$$
CDF(x) = \int_{-\infty}^{x} p(t) \, dt = P(X \leq x) = \mu((-\infty, x))
$$

(Cumulative distribution function is commonly written as $P(X)$).

Facts:

1. Is $P(x) = \int_{-\infty}^{x} p(t) \, dt$ ever decreasing?

$$
\mu{ ((-\infty, x)) } \text{ vs. } \mu((-\infty, y)) \text{, } x < y
$$

No. It is increasing all the time.

2. $\lim_{ x \to \infty }P(x) = \int_{-\infty}^{\infty} p(x) \, dx = 1$

Egs.
1. $\frac{1}{2}\chi_{[0,2]}(x) = p(x)$ where 

$$
\chi_{[0,2]}(x)\begin{cases}
1 \text{ if } x \in [0,2]\\ \\
0 \text{ if } x \not\in [0,2]
\end{cases}
$$
This represents picking a number in $[0, 2]$ uniformly at random.

$$
\int_{\frac{1}{2}}^{2} p(t) \, dt = \text{prob. of picking a number between } \frac{1}{2} \text{ and } 2 
$$
$$
\int_{3}^{4} p(x) \, dx = 0
$$
$$
P\left( x=\frac{1}{2} \right) = \int_{\frac{1}{2}}^{\frac{1}{2}} p(t) \, dt = 0 
$$

2. $f(x) = \frac{1}{1 + x^{2}}$. 
	1. $f(x) > 0$
	2. We see
$$\int_{0}^{a} \frac{1}{1+x^{2}} \, dx = \arctan(a) \implies \int_{0}^{\infty} \frac{1}{1+x^{2}} \, dx = \lim_{ a \to \infty } \arctan(a) = \frac{\pi}{2}$$
		similarly,
		$$
	\int_{-\infty}^{0} \frac{1}{1+x^{2}} \, dx = \frac{\pi}{2} 
$$
		Therefore,
		$$
\int_{-\infty}^{\infty} \frac{1}{1+x^{2}} \, dx = \pi
$$
		So,
		$$
p(x) = \frac{1}{\pi}f(x)
$$
		is a probability distribution function.

3. Another example,

$$
P(x) = \begin{cases}
0 \text{ if } x < 0\\ \\
e^{-x} \text{ if } x > 0
\end{cases}
$$
	Here, $P(x)$ is a probability distribution function.

## Expectation / Mean

If $X$ is a numerical random variable, then the mean or expectation is given by,

$$
\bar{X} = \int_{-\infty}^{\infty} xp(x) \, dx 
$$

in a continuous space.

If $S = \{ x_{1},\dots,x_{n} \} \in \#\text{'s}$, $\bar{X} = \sum_{i=1}^{n} x_{i}\mu(\{ x_{i} \})$

Eg. 6 sided die, $\bar{X} = \frac{1}{6} + \frac{2}{6} + \frac{3}{6} + \frac{4}{6} + \frac{5}{6} + \frac{6}{6}$ = $\frac{1}{6}\cdot \frac{6(7)}{2} = 3.5$




