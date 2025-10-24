## Power Series centered at $x=a$

$$
P(x) = \sum_{n=0}^{\infty} a_{n}(x-a)^n;\, (x-a)^0 \equiv 1
$$
$$
a_{n}(x-a)^n <- \text{ term}
$$
where $a_{n}$ is the degree $n$ coefficient, $a$ is the centre.

### Example
$$
P(x) = \sum_{n=0}^{\infty}x^n=1 + x+x^{2}+\dots 
$$
Here, the centre is $0$, terms are $x^n$ and the coefficients are 1.

Subbing in an $x$ value gives us a numerical series.

$$
P\left( \frac{1}{3} \right) = \sum_{n=0}^{\infty} \left( \frac{1}{3} \right)^n = \frac{1}{1-\frac{1}{3}} = \frac{3}{2}
$$
$$
P(2) = \sum_{n=0}^{\infty} 2^n = 1 + 2 + 4 + \dots = \infty / D.N.E
$$
$P(x)$ gives a function s.t. $\frac{1}{3} \in Dom(P)$, $2 \not\in Dom(P)$. Given a $P(x)$, what is its domain?

Use the ratio test, result depends on $x$. Compute the limit of ratio of consecutive non-zero terms. For $P(x)$, compute,
$$
\lim_{ n \to \infty } \frac{|a_{n+1}|}{|a_{n}|} = \frac{|a_{n+1}(x-a)^{n+1}|}{|a_{n}(x-a)^n|} = \lim_{ n \to \infty } \frac{|x|^{n+1}}{|x|^n} =|x| =\rho
$$
The ratio test says,
* $0\leq \rho<1 \implies$ convergence,
* $\rho=1 \implies$ we dont know lol
* $\rho >1 \implies$ diverges.
By the ratio test, $P(x)$ converges when $|x| = \rho<1$
Verify endpoint cases where $|x| = 1$.
* When $x = 1$, $P(1) = 1+1+1+\dots$ which diverges.
* When $x=-1$, $P(-1) = 1 -1 +1 \mp\dots$ which also diverges.
All together, $Dom(P) = (-1,1)$.

### Example 2,
$$
\sum_{n=0}^{\infty} \frac{(-1)^n\cdot(x-3)^{2n}}{3^n}
$$
Figure out the open interval convergence first. Doing the ratio test,

$$
\lim_{ n \to \infty } \frac{|x-3|^{2(n+1)}}{3^{n+1}}\cdot \frac{3^{n}}{|x-3|^{2n}} = \frac{|x-3|^2}{3} = \rho
$$
Solving for $\rho<1$,
$$
\frac{|x-3|^2}{3} < 1
$$
$$
-\sqrt{ 3 } < x-3<\sqrt{ 3 }
$$
$$
3-\sqrt{ 3 }<x<3+\sqrt{ 3 }
$$
Therefore, it converges for $x \in (3-\sqrt{ 3 }, 3+\sqrt{ 3 })$

Our endpoints are when $x -3 = \pm \sqrt{ 3 }$.
$$
\sum_{n=0}^{\infty} \frac{(-1)^n\cdot(x-3)^{2n}}{3^n} = \sum_{n=0}^{\infty} (-1)^n\cdot \frac{3^n}{3^n} = \sum_{n=0}^{\infty} (-1)^n=1-1+1 \dots
$$
So they diverge.

## Convergence of Power Series

If a power series converges on the interval $(a-r,a+r)$ (open interval convergence), $r$ is called the radius of convergence. At endpoints, convergence is checked separately. Outside explodes. (I wish I had a pen so I could draw the diagram.)

