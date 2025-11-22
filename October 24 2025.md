## Series Division

$$
\tan(x) = \frac{\sin(x)}{\cos(x)}
$$

$\sin(x)$ and $\cos(x)$ must be expanded at the same point.

$$
\cos(x)\cdot \tan(x) = [1 -\frac{x^{2}}{2} + \frac{x^4}{4!} - \frac{x^6}{6!} +\dots ] [ a_{0}+a_{1}x+a_{2}x^2+\dots] = \left[ x-\frac{x^3}{3} + \frac{x^5}{5!} -\dots \right]
$$
$$
1a_{0} + (1a_{1})x + \left( a_{0} \frac{-1}{2} + a_{2} \right)x^{2} + \left( a_{3}-\frac{1}{2}a_{1} \right)x^{3}
$$
$$
0x^0+x + 0x^{2} - \frac{1}{3!}x^{3}+0x^4 + \frac{1}{5!}x^5
$$
$$
\therefore a_{0}=0, a_{1}=1, a_{2} = 0, a_{3} = \frac{1}{3}
$$
$$
\tan(x) = x + \frac{1}{3}x^{3} + \dots
$$

where the power series converges.
![image](attachments/Pasted%20image%2020251024114915.png)

## Binomial Series

$$
f(x) = (1+x)^r
$$

where $r$ is a fixed number $r\neq 0$.

$$
f'(x) = r(1+x)^{r-1}
$$
$$
f''(x) = r(r-1)(1+x)^{r-2}
$$
$$
.
$$
$$
.
$$
$$
f^{(n)}(x) = r(r-1)\dots(r-n+1) (1+x)^{r-n}
$$

When $x = 0$, the taylor series is,

$$
\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!} x^n
$$
$$
P(x) = \sum_{n=0}^{\infty} \frac{r(r-1)(r-2)\dots(r-n+1)}{n!} x^n
$$
$$
= \sum_{n=0}^{\infty} \begin{pmatrix}
r \\
n
\end{pmatrix}
x^n
$$

Interesting fact: If $r \in \mathbb{Z}_{>0}$, $\begin{pmatrix}r\\r+n\end{pmatrix} = 0$ ($n \in \mathbb{N}$). i.e., the series has finitely many terms since $(1+x)^r$ is a polynomial. Otherwise, the series has infinitely many terms.

## How Newton calculated $\pi$

$$
\frac{1}{1+x^2} = \sum_{n=0}^{\infty} (-1)^nx^2n
$$

We integrate,

$$
\arctan(x) = \sum_{n=0}^{\infty} \frac{(-1)^n}{2n+1} x^{2n+1}
$$

Interval of convergence is $(-1,1)$.

$$
\frac{\pi}{4} = \arctan(1) = \sum_{n=0}^{\infty} \frac{(-1)^n}{2n + 1} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \dots
$$

which converges very slowly.

$$
\arcsin(x), \arcsin\left(  \frac{1}{2} \right) = \frac{\pi}{6}
$$
$$
\frac{d}{dx} \arcsin(x) = (1-x^2)^{-1/2}
$$
$$
(1+t)^{-1/2} = \sum_{n=0}^{\infty} \begin{pmatrix}
-\frac{1}{2} \\
n
\end{pmatrix} t^n
$$
$$
(1 + (-x^{2}))^{-1/2} = \sum_{n=0}^{\infty} \begin{pmatrix}
-\frac{1}{2} \\
n
\end{pmatrix} (-1)^n x^{2n}
$$

We integrate this and sub $\frac{\pi}{6}$ in.

## Loose end

A function $f$ is Riemann integrable if integrals are well defined.

![image](attachments/Pasted%20image%2020251024122014.png)
(Editor's note: I couldn't get github to recognize these images. My bad. You should be able to go through the attachments folder to figure out what this image is)

Fact: $f$ is riemann integrable on $[a,b]$ exactly if it is bounded & only has finitely many discontinuities.

