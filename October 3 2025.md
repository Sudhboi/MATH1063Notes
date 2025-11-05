## Integral Comparison Test

Given $\sum_{n=n_{0}}^{\infty}a_{n}$ and a function $f: [n_{0}, \infty)\to\mathbb{R}$ that is decreasing with $f(n) = a_{n}$ and $a_{n}\geq 0$, then $\sum_{n=n_{0}}^{\infty}a_{n}$ converges exactly if ($\iff$) $\int_{n_{0}}^{\infty} f(x) \, dx$ converges.

### Proof:

Taking an infinite histogram with width 1, and $f(n) = a_{n}$,

If $\int_{n_{0}}^{\infty} f(x) \, dx = \infty$, then $\sum_{n=n_{0}}^{\infty}a_{n}$ diverges. On the other hand, if $\int_{n_{0}}^{\infty} f(x) \, dx = L<\infty$,

$$
\int_{n_{0}+1}^{\infty} f(x-1)  \, dx > \sum_{n=n_{0}+1}^{\infty} a_{n} 
$$

So $\sum a_{n}$ converges. Example, $p$-series.

$\sum_{n=1}^{\infty} \frac{1}{n^p}$ with $0<p$, then $\frac{1}{n^p} \to 0$.

Does this converge? For which $p$ values?

Take $f(x) = \frac{1}{x^p}$, $f(n) = \frac{1}{n^p}$ and $f(x)$ is decreasing.

$$
\int_{1}^{\infty} \frac{1}{x^p} \, dx = \lim_{ a \to \infty } \left[ \frac{x^{1-p}}{1-p} \right]^\infty_{1} = \lim_{ a \to \infty } \frac{a^{1-p}}{1-p} - \frac{1}{1-p}
$$

When is this infinite?

If $1-p<0 \iff p<1$, then $\int_{0}^{\infty} \frac{1}{x^p} \, dx < \infty$.
If $1 - p > 0 \iff p>1$, then $\int_{0}^{\infty} \frac{1}{x^p} \, dx = \infty$.

However, if $p = 1$, if we take the limit,

$$
\lim_{ a \to \infty } \frac{a^{1-p}}{1-p} - \frac{1}{1-p} = \lim_{ a \to \infty } \frac{a^0}{0} - \frac{1}{0}
$$
$$
\int_{1}^{\infty} \frac{1}{x} \, dx = \lim_{ a \to \infty } \ln(a) = \infty
$$

## Series Comparison Test

Let $a_{n}\geq b_{n}$ and $a_{n},b_{n}\geq 0$. If $\sum a_{n}$ converges, so does $\sum b_{n}$. If $\sum b_{n}$ diverges, so does $\sum a_{n}$. 

## Limit Comparison Test

Let $a_{n}, b_{n} \geq 0$

* $\lim_{ n \to \infty } \frac{a_{n}}{b_{n}} = c < \infty$ then $\sum a_{n}$ converges precisely when $\sum b_{n}$ converges.
* $\lim_{ n \to \infty } \frac{a_{n}}{b_{n}} = 0$, we get that $b_{n}\gg a_{n}$. If $\sum b_{n}$ converges, then $\sum a_{n}$ converges as well.
* $\lim_{ n \to \infty } \frac{a_{n}}{b_{n}} = \infty$, conclude stuff on your own.

Example:

$$
S =\sum_{n=1}^{\infty} \frac{|\cos(n)|}{n^{2}}
$$

Does $S$ converge?
Since $S \leq \frac{1}{n^{2}}$ by comparison with $\sum_{n=1}^{\infty} \frac{1}{n^{2}}$ which converges. So we know $S$ converges.

## The Obvious Test

$a_{n}$ may be positive or negative.

If $\sum_{n=n_{0}}^{\infty}|a_{n}|$ converges, then so does $\sum_{n=n_{0}}^{\infty}a_{n}$ converges.

## Ratio Test

Assume all $a_{n} \neq 0$. Then consider

$$
\rho = \lim_{ n \to \infty } \frac{|a_{n+1}|}{|a_{n}|}
$$

If $0<\rho<1$, then the series converges.
If $p>1$, then the series diverges.
If $p=0$, use another test.

