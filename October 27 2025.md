## Integration by Parts

$$
df = f'(x) \,dx,\, \int df=f(x) + C, \int_{a}^{b} df = f(b) - f(a)
$$
General Stokes Theorem (for fun): 
$$
\int_{\Omega}^{}  \, df = \int_{d\Omega}^{} f  
$$
For function $u,v$,
$$
d(uv) = udv + vdu
$$
$$
\implies \int d(uv) = \int udv + \int vdu
$$
$$
\implies uv = \int udv + \int vdu
$$
$$
\implies \int udv = uv - \int vdu
$$
The $+C$ is hiding in the integral.
$$
\int_{a}^{b} u \, dv = uv|^b_{a} + \int_{a}^{b} v \, du =u(b)v(b) - u(a)u(b) - \int_{a}^{b} v \, du 
$$
## Strategy

1. Recognize the integrand as $\int u\:dv$
2. Know $v = \int dv$
3. Deal with $\int v\:du$
4. Repeat? End? 

## Examples

$$
\int \ln(x) \, dx 
$$
$$
u = \ln(x)\quad du = \frac{1}{x}dx
$$
$$
dv = dx\quad v = x
$$
$$
\int \ln(x) \, dx  = x\ln(x) - \int x\cdot \frac{1}{x} \, dx = x\ln(x) - \int  \, dx  = x\ln(x) - x + C = x(\ln(x) - 1) + C
$$
## Doing it definite integral style:

$$
\int_{0}^{1} \ln(x) \, dx  = \lim_{ a \to 0^+ } \int_{a}^{1} \ln(x) \, dx 
$$
$$
\int_{a}^{1} \ln(x) \, dx 
$$
$$
u = \ln(x)\quad du = \frac{1}{x}dx
$$
$$
dv = dx\quad v =x
$$
$$
=x\ln(x)|^1_{a} - \int_{a}^{1} \frac{x}{x} \, dx
$$
$$
= 0 - a\ln(a) - [1-a]
$$
$$
= -a\ln(a) + a - 1
$$
Now,
$$
\int_{0}^{1} \ln(x) \, dx = \lim_{ a \to 0^+ } -a\ln(a) + a -1 
$$
$$
= \lim_{ a \to o^+ } -a\ln(a) - 1
$$
Taking the limit.
$$
\lim_{ a \to 0^+ } -a\ln(a): -0^+\cdot \infty
$$
$$
=\lim_{ a \to 0^+ } \frac{\ln(a)}{\left( -\frac{1}{a} \right)} \implies \frac{-\infty}{-\infty} 
$$
Using L'Hopital's rule,
$$
=\lim_{ a \to 0^+  } \frac{\frac{1}{a}}{\left( -\frac{1}{a^2}\cdot-1 \right)} = \lim_{ a \to 0^+ } \frac{a^{2}}{a} = \lim_{ a \to 0^+ } a = 0  
$$
Coming back,
$$
= \lim_{ a \to o^+ } -a\ln(a) - 1=0-1=-1
$$
## Example

$$
\int_{-1}^{1} x^2\sin(3x) \, dx  = 0
$$
Bruh.
Taking,
$$
\int x^{2}\sin(3x) \, dx 
$$
$$
 u = x^{2}\quad du = 2x\:dx
$$
$$
dv = \sin(3x)\:dx\quad v = -\frac{1}{3}\cos(3x)
$$
$$
=-\frac{1}{3}x^{2}\cos(3x)+\frac{1}{3}\int 2x\cos(3x) \, dx = -\frac{1}{3}x^{2}\cos(3x) + \frac{2}{3}\int x\cos(3x) \, dx 
$$
Doing the side quest,
$$
\int x\cos(3x) \, dx 
$$
$$
u = x\quad du = dx
$$
$$
dv = \cos(3x)dx\quad v = \frac{1}{3}\sin(3x)
$$
$$
\frac{1}{3}x\sin(3x) - \frac{1}{3}\int \sin(3x)\:dx
$$
$$
\frac{1}{3}x\sin(3x) + \frac{1}{9}\cos(3x) + C
$$
Taking it back,
$$
=-\frac{1}{3}x^{2}\cos(3x)+\frac{2}{3}\left[ \frac{1}{3}x\sin(3x) + \frac{1}{9}\cos(3x) + C \right]
$$
$$
=-\frac{1}{3}x^{2}\cos(3x) + \frac{2}{9}x\sin(3x) + \frac{2}{27}\cos(3x) + C
$$
