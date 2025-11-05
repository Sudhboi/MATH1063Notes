## Making new Taylor Series 

Theorem A $C^\infty$ function hsa a unique power series expansion centered at $x=a$.
Corollary - No matter how you get it, the power series will be the same.

We can use substitution. For example,

$$
e^x= \sum_{n=0}^{\infty}  \frac{1}{n!}x^n
$$

for all $x \in \mathbb{R}$.

$$
\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n
$$

only for $|x|<1$. So,

$$
e^{-t^2} = \sum_{n=o}^{\infty} \frac{1}{n!}(-t^{2})^n=\sum_{n=0}^{\infty} \frac{(-1)^n}{n!}t^{2n}
$$

true for all $t$. So, this is the taylor series for $e^{-t^{2}}$.
Eg.

$$
\frac{d^{27}}{dt^{27}} e^{-t^2} = 0
$$

Since coefficient for $t^{27}$ is 0. (We see that from the power series derived before). This means that if you get any power series, it has to be equal to the taylor series of the function.

## Basic Taylor Power Series

$$
e^x= \sum_{n=0}^{\infty} \frac{1}{n!}x^n
$$
$$
\sin(x) = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)!}x^{2n+1}
$$
$$
\cos(x) = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n)!}x^{2n}
$$
$$
\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n, 
$$

## Sub:

$$
\frac{1}{1+x^2} = \frac{1}{1-(-x^2)} = \sum_{n=0}^{\infty} (-x^{2})^n = \sum_{n=0}^{\infty} (-1)^nx^{2n} 
$$

Warning:

$$
f(x) = e^{-1/x^{2}}
$$

as $x\to 0$, $-\frac{1}{x^2} \to -\infty$, $e^{-1/x^2} \to 0$

We can show that 

$$
f^{(n)}(0) = 0
$$

Therefore, the taylor expansion,

$$
P(x) = \sum_{n=0}^{\infty}  \frac{0}{n!}x^n
$$

Take Taylor Polynomials $P_{n}(x)$, the error does not go to 0.

Apparently Complex Analysis explains it very well. 

## Formal Derivatives and Integrals

$$
P(x) = \sum_{n=0}^{\infty} a_{n}(x-a)^n
$$
$$
FI(P(x)) = \sum_{n=0}^{\infty} \frac{a_{n}}{n+1}(x-a)^{n+1}
$$

Here, the degree 0 coefficient is zero.

$$
FD(P(x)) = \sum_{n=0}^{\infty} a_{n}(n)(x-a)^{n-1}
$$

Degree 0 is the $n=1$ term.

Theorem: On the open interval of convergence of $P(x)$,

$$
FI(P(x)) = \int_{a}^{x} P(t) \, dt 
$$
$$
FD(P(x)) = P'(x)
$$

Example:

$$
\frac{d}{dx} \arctan(x) = \frac{1}{1+x^2} = \sum_{n=0}^{\infty} (-1)^nx^{2n}
$$
$$
\int_{0}^{x} \frac{1}{1+t^2} \, dt = \int_{0}^{x} \sum_{n=0}^{\infty} (-1)^nt^{2n} \, dt = \sum_{n=0}^{\infty} \frac{(-1)^n}{2n+1}x^{2n+1} = \arctan(x) + C = \arctan(x)  
$$

## "Easy Fact"

$P'(x)$ and $\int_{a}^{x} P(t) \, dt$ have the same interval of convergence. (Do the ratio test)

$$
\arctan(1) = \frac{\pi}{4}
$$
$$
\frac{\pi}{4} = \sum_{n=0}^{\infty} (-1)^n \frac{1^{2n+1}}{2n+1} = 1 - \frac{1}{3} +\frac{1}{5} - \frac{1}{7} +\dots
$$
