## Example

Find Taylor series for $f(x) = \ln(1+x)$ centered at $x=0$, i.e., the Maclauren Series.
$$
f'(x) = \frac{1}{1+x} = \frac{1}{1-(-x)} = \sum_{n=0}^{\infty} (-x)^n = \sum_{n=0}^{\infty} (-1)^nx^n
$$
This is good for $x \in (-1,1)$.
$$
\int_{0}^{x} \frac{1}{1+t} \, dt = F(x) 
$$
and,
$$
F(x) = \ln(1+x) + C
$$
(We avoid the absolute value cuz figure it out.)
$$
F(0) = \int_{0}^{o} \frac{1}{1+t} \, dt  = 0
$$
$$
\ln(1 + 0) = \ln(1) = 0
$$
Therefore,
$$
F(x) = \ln(1+x)
$$
To find the Taylor Series,
$$
\int_{0}^{x} \sum_{n=0}^{\infty} (-1)^nt^n \, dt 
$$
$$
= \sum_{n=0}^{\infty} \frac{(-1)^n}{n+1}x^{n+1}
$$
which is the Taylor Series for $\ln(1+x)$. (We can interchange integration and summation on the open interval of convergence.)

## Another Example

$$
f(x) = e^{-x^2}
$$
$$
erf(x) = \int_{0}^{x} e^{-t^{2}} \, dt 
$$
![[Pasted image 20251022115740.png]]
![[Pasted image 20251022115556.png]]
$$
e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}
$$
$$
e^{-t^{2}} = \sum_{n=0}^{\infty} \frac{(-1)^nx^{2n}}{n!}
$$
$$
erf(x) = \sum_{n=0}^{\infty}  \left[ \frac{(-1)^n}{n!(2n+1)} \right]x^{2n+1}
$$
## Power series algebra

$$
\frac{\sin(x)}{x} = \frac{1}{x} \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)!}x^{2n+1} = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)!}x^{2n}
$$
![[Pasted image 20251022120123.png]]
### Application 1:

$$
\lim_{ x \to o } \frac{\sin(x)}{x} = \lim_{ x \to 0 } P(x) = P(0) = 1
$$
## Multiplying Power Series
$$
f(x) = \frac{1}{x-\frac{\pi}{2}}\cos(x)
$$
expand at $\frac{\pi}{2}$.
$$
\cos(x) = -1\left( x-\frac{\pi}{2} \right) + \frac{1}{3!}\left( x-\frac{\pi}{2} \right)^3 - \frac{1}{5!}\left( x-\frac{\pi}{2} \right)^5 + \dots
$$
So,
$$
\frac{1}{x-\frac{\pi}{2}}\cos(x) = -1 + \frac{1}{3!}\left( x-\frac{\pi}{2} \right)^2 - \frac{1}{5!}\left( x-\frac{\pi}{2} \right)^4 + \dots
$$
Therefore,
$$
P\left( \frac{\pi}{2} \right) = -1 + 0 + 0+ \dots
$$
## Multiplying two power series.
1. Same center
2. Common open interval of convergence.

$$
[a_{0}+a_{1}(x-a) +a_{2}(x-a)^{2}+\dots][b_{0} + b_{1}(x-b) + b_{2}(x-b)^2 + \dots]
$$

