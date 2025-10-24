## Ratio Test

Let $\lim_{ n \to \infty } \frac{|a_{n_{1}}|}{|a_{n}|} = \rho$,
* If $0\leq \rho < 1$ then the series converges.
* If $\rho>1$ then $\sum a_{n}$ diverges.
* If $\rho=1$ or $D.N.E$, then the test is inconclusive.
This is super important for power series.

Also take non-zero terms. (they don't do anything, so just ignore them lol)

Examples:

$\sum_{n=1}^{\infty} \frac{1}{n^{2}}$, comparison with $\int_{1}^{\infty} \frac{1}{x^{2}} \, dx$ says it converges.

$$
a_{n} = \frac{1}{n^2}
$$
Ratio Test:
$$
\lim_{ n \to \infty } \frac{|a_{n+1}|}{|a_{n}|} =\lim_{ n \to \infty } \frac{(n)^{2}}{(n+1)^{2}} = \lim_{ n \to \infty } \frac{1}{1+\frac{2}{n}+\frac{1}{n^{2}}} = 1
$$
So the Ratio test does not work.

Another Example.
$$\sum_{n=0}^{\infty} \frac{2^n(-1)^n}{n!}$$
$$
\lim_{ n \to \infty } \frac{|a_{n+1}|}{|a_{n}|} = \lim_{ n \to \infty } \frac{2^{n+1}}{(n+1)!}\cdot \frac{n!}{2^n} = \lim_{ n \to \infty } \frac{2}{n+1} = 0
$$
Therefore the series converges.

## Proof of Ratio Test

Let $\rho=\lim_{ n \to \infty } \frac{|a_{n+1}|}{|a_{n}|}$ & suppose $0\leq \rho<1$. We can take $\epsilon$ so that $\epsilon +\rho < 1$. By definition of $\lim_{ n \to \infty } \frac{|a_{n+1}|}{|a_{n}|}$ there is a large $N$ so that if $n>N$, then 

$$
\rho-\epsilon < \frac{|a_{n+1}|}{|a_{n}|} < \rho + \epsilon <1
$$
Take $r = \rho + \epsilon < 1$.

Notice,
$$
\frac{|a_{N+1}|}{|a_{N}|} < r \implies |a_{N+1}| < |a_{N}|r
$$
$$
\frac{|a_{N+2}|}{|a_{N+1}|} < r \implies |a_{N+2}| < |a_{N+1}|r < |a_{N}|r^2
$$
$$
\dots
$$
$$
\implies |a_{N+k}| < |a_{N}|r^k
$$
Consider the series $\sum_{k=0}^{\infty} |a_{N}|r^k = |a_{N}|\sum_{k=0}^{\infty}r^k$, which we know converges (geometric series, $r<1$). Now, compare this with $\sum_{k=0}^{\infty}|a_{n+k}|$. Since,
$$
|a_{N+j}| \leq |a_{N}|r^j
$$
Therefore, by the comparison test, since the larger series converges, the smaller one does as well. And since $\sum |a_{n}|$ converges, so does $\sum a_{n}$ converges as well.

## More examples

$$
\sum_{n=1}^{\infty} \frac{|\sin(n)|}{n} \text{ v.s. } \sum_{n=1}^{\infty} \frac{\sin(n)}{n}
$$
Take $|\sin(n)|$. For $n =1, 2, 3\dots$

We group into blocks of 7 numbers. For each 7, we go around a bit more once since $7>2\pi$. So for each 7, at least twice,
$$
|\sin(n)| \geq \frac{\sqrt{ 2 }}{2}
$$
(think about $\sin(x)$ when $x=\frac{\pi}{4}$ and $\frac{\pi}{4} +\frac{\pi}{2}$).

Idea: Take another series that is guaranteed to diverge but will be less.
$$
\frac{\sin(1)}{1}+\dots +\frac{|\sin(7)|}{7} + \dots +\frac{|\sin(14)|}{14}
$$
$$
0+\dots+\frac{\sqrt{ 2 }}{7} + 0 + \dots + \frac{\sqrt{ 2 }}{14} + \dots
$$
So our lower series is 
$$
\sum_{n=1}^{k} \frac{\sqrt{ 2 }}{7n} = A_{k} \text{ and } S_{k} =\sum_{n=1}^{k} \frac{\sin(n)}{n}
$$
We know that $A_{\left\lfloor  \frac{k}{7}  \right\rfloor} <S_{k}$. Since $A_{k} = \frac{\sqrt{ 2 }}{7}\sum_{n=1}^{L} \frac{1}{n} \to \infty$.
So, $\lim_{ k \to \infty } S_{k} = \infty$. 
$$
\implies \sum_{n=1}^{\infty} \frac{|\sin(n)|}{n} \text{ diverges.}
$$
