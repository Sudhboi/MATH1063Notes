## Last time

We saw that,
$$
\sum_{n=1}^{\infty} \frac{1}{n}
$$
$$
S_{N} = \sum_{n=1}^{N} \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \dots
$$
$$
S_{N} \geq \int_{1}^{N+1} \frac{1}{x} \, dx = \ln(N+1) 
$$
$$
\lim_{ N \to \infty } S_{N} = \infty
$$
So, $\sum_{n=1}^{\infty} \frac{1}{n}$ does not converge.

Takeaway:
Even if $a_{n} \to 0$, the series may not converge.

## Geometric Series

$$
\sum_{n=0}^{\infty} a^n;\: S_{N} = \frac{1-a^{N+1}}{1-a} 
$$
$$
S_{N} \to c \iff |a|<1 \text{ and } S_{N} \to \frac{1}{1-a}
$$
So,
$$
\sum_{n=0}^{\infty} a^n=\frac{1}{1-a} \text{ if } |a| < 1
$$
Definition: 
If $\sum_{n=n_{0}}^{\infty}a_{n}$ is a series, then $\sum_{n=k}^{\infty}a_{n}$ is called the $k$-tail of the series.

Fact: A series converges only if all of its $k$-tails converge.

Example:
$$
\sum_{n=3}^{\infty} \left( \frac{9}{10} \right)^n =\left( \frac{9}{10} \right)^3+\left( \frac{9}{10} \right)^4 + \dots
$$
$$
= \left( \frac{9}{10} \right)^3 \left[ 1 + \frac{9}{10} + \left( \frac{9}{10} \right)^2 + \dots \right]
$$
$$
= \left( \frac{9}{10} \right)^3\sum_{n=1}^{\infty} \left( \frac{9}{10} \right)^n
$$
$$
=7.29
$$
## Improper Integrals

For example,
$$
\int_{0}^{1} \frac{1}{\sqrt{ x }} \, dx
$$
Integral explodes at a bound; We can't plug 0 into the integral.

Instead, we need to take the limit,
$$
\lim_{ a \to 0^+ } \int_{a}^{1} \frac{1}{\sqrt{ x }} \, dx
$$
$$
= \lim_{ a \to 0^+ } \left[ \frac{x^{1/2}}{\frac{1}{2}} \right]^1_{a} = \lim_{ a \to 0^+ } [2\sqrt{ 1 } - 2\sqrt{ a }] = 2  
$$
Definition: An improper integral of the form,
$$
\int_{a}^{\infty} f(x) \, d \text{ or } \int_{-\infty}^{a} f(x) \, dx  
$$
where $f$ is continuous on $[a,\infty)$ or $(-\infty, a]$ is called a type-1 improper integral and by definition,
$$
\int_{a}^{\infty} f(x) \, dx =\lim_{ b \to \infty } \int_{a}^{b} f(x) \, dx 
$$
An improper integral of the form,
$$
\int_{-\infty}^{\infty} f(x) \, dx = \lim_{ c \to -\infty } \int_{c}^{a} f(x) \, d + \lim_{ b \to \infty } \int_{a}^{b} f(x) \, dx = \int_{-\infty}^{a} f(x) \, dx+\int_{a}^{\infty} f(x) \, dx   
$$
for some $a$.

If $f$ is continuous on $(a,b]$ but maybe not defined at $a$ then,
$$
\int_{a}^{b} f(x) \, dx = \lim_{ c \to a^+ } \int_{c}^{b} f(x) \, dx 
$$
The "approaching" of the limit is significant here. This is the type-2 integral.

Issues:
$$
\int_{-a}^{a} x \, dx = 0 
$$
$$
\int_{-\infty}^{\infty} x \, dx = \left[ \frac{x^2}{2} \right]^{\infty}_{\infty} = \frac{\infty^{2}}{2} -\frac{(-\infty)^{2}}{2}
$$
which should not be done.
$$
\lim_{ a \to \infty } \int_{-a}^{a} x \, dx = \lim_{ a \to \infty } \left[ \frac{x^2}{2} \right]^{a}_{a} =\lim_{ a \to \infty }  \frac{a^{2}}{2} -\frac{(-a)^{2}}{2} = 0 
$$
$$
\lim_{ a \to \infty } \int_{-a}^{a+1} x \, dx = \lim_{ a \to \infty } \left[ \frac{x^2}{2} \right]^{a+1}_{-a} = \lim_{ a \to \infty } \frac{(a+1)^{2}}{2} -\frac{(-a)^{2}}{2} = \lim_{ a \to \infty } a + \frac{1}{2} = \infty
$$
Using another way,
$$
\int_{-\infty}^{\infty} x \, dx = \lim_{ a \to -\infty } -\frac{a^{2}}{2} + \lim_{ b \to \infty } \frac{b^{2}}{2} = -\infty+\infty
$$
So, $\int_{-\infty}^{\infty} x \, dx$ is divergent.

$\infty-\infty$ is never well defined for integration. By splitting the integral up we made it clear that $\int_{-\infty}^{\infty} x \, dx$ is divergent.

Example: $\int_{0}^{\infty} \sin(x) \, dx = \infty-\infty$ (taking the positive areas and the negative areas.) 

Takeaway: For an improper integral $\int_{a}^{b} f(x) \, dx$ we need $|f(x)|$ to converge, i.e., the positive area and the negative area need to be finite.

## Kinetic Energy needed to escape Earth according to Newton

$$
r_{\text{earth}} = 6.4 \times 10^6\text{ m}
$$
$$
m_{\text{earth}} = 6 \times 10^{24} \text{ kg}
$$
$$
F_{g} = -\frac{Gm_{\text{earth}}m}{r^2}
$$
$$
\text{Work: } F \Delta r \text{ in J} 
$$
To lift an object to $\infty$ from surface,
$$
W = \int_{r_{\text{earth}}}^{\infty} F_{g}(r) \, dr = \int_{r_{earth}}^{\infty}  -\frac{Gm_{\text{earth}}m}{r^2}\, dr = A\int_{r_{earth}}^{\infty} \frac{1}{r^{2}} \, dr = \lim_{ a \to \infty } A\int_{r_{earth}}^{a} \frac{1}{r^{2}} \, dr 
$$
$$
=A\lim_{ a \to \infty } \left[ \frac{-1}{r} \right]^\infty_{r_{earth}} =\frac{A}{r_{earth}}
$$
$$
\therefore W = -\frac{Gm_{earth}m}{r^2} = K.E.
$$
