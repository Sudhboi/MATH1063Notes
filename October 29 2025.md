## Strategy for choosing $u$

1. Logarithumz
2. Inverse Trig
3. Algebraic
4. Trigonometric
5. Exponential

## Example

$$
\int t^{2}e^{3t} \, dt 
$$
$$
u = t^{2}, du = 2tdt
$$
$$
dv = e^{3t}dt, v = \frac{1}{3}e^{3t}
$$
$$
= \frac{1}{3}t^{2}e^{3t} - \int \frac{1}{3}e^{3t}2t \, dt 
$$
Detouring,
$$
\int te^{3t} \, dt 
$$
$$
u = t, du = dt
$$
$$
dv =e^{3t}dt, v = \frac{1}{3}e^{3t}
$$
$$
= \frac{1}{3}te^{3t} - \frac{1}{3}\int e^{3t} \, dt 
$$
$$
= \frac{1}{3}te^{3t} - \frac{1}{9}e^{3t} + C
$$
Coming Back,
$$
= \frac{1}{3}t^{2}e^{3t} - \frac{2}{3}\left[ \frac{1}{3}te^{3t} - \frac{1}{9}e^{3t} + C \right]
$$
$$
 = \frac{1}{3}t^{2}e^{3t} - \frac{2}{9}te^{3t} + \frac{2}{27}e^{3t} + C
$$
# Another Example

$$
\int t^{3}e^{t^{2}} \, dt 
$$
$$
u = t^{2}, du = 2t
$$
$$
dv = e^{t^{2}}tdt, v = \frac{1}{2}e^{t^{2}}
$$
$$
= \frac{1}{2}t^{2}e^{t^{2}} - \int \frac{1}{2}e^{t^{2}}2t \, dt 
$$
$$
= \frac{1}{2}t^{2}e^{t^{2}} - \frac{1}{2}\int e^{t^{2}}2tdt
$$
$$
= \frac{1}{2}t^{2}e^{t^{2}} - \frac{1}{2}e^{t^{2}} + C
$$
## Trigonometric Integrals

$$
\int \sin ^{5}x\cos ^{3}x \, dx 
$$
$$
=\int \sin ^{5}x(1-\sin ^{2}x)\cos(x) dx
$$
Let $$
u = \sin(x), du = \cos(x)dx
$$Subbing $u$ in,
$$
=\int u^{5}(1-u^{2})du
$$
$$
= \int u^{5} - u^{7}du
$$
$$
= \frac{u^{6}}{6} - \frac{u^8}{8} + C
$$
$$
= \frac{\sin^6(x)}{6} - \frac{\sin^8(x)}{8} + C
$$
# Yet another example

$$
\int \sin ^{4}x\cos ^{2}x \, dx 
$$
$$
\int \left[ \frac{1-\cos(2x)}{2} \right]^2 \left( \frac{1+\cos(2x)}{2} \right)dx
$$
$$
=\frac{1}{8} \int(1-\cos(2x))(1-\cos ^{2}(2x))dx
$$
$$
\int 1 - \cos ^{2}(2x) - \cos(2x) + \cos ^{3}(2x)dx
$$
You then do some other stuff that I'm too lazy to type out.
(Use the reduction formula from the tutorial)

## Angle Sum formulas

If $\theta \in \mathbb{R}$,
$$
e^{i\theta} = \cos(\theta) + i\sin(\theta)
$$
and,
$$
e^{i\alpha}\cdot e^{i\beta} = e^{i(\alpha+\beta)}
$$
$$
\implies (\cos \alpha + i\sin \alpha)(\cos \beta + i \sin \beta) = \cos(\alpha + \beta) + i\sin(\alpha+\beta)
$$
$$
\implies \cos \alpha \cos \beta + \cos \alpha \cdot i\sin \beta + i \sin \alpha \cos \beta + i\sin \alpha\cdot i\sin \beta
$$
$$
\implies [\cos \alpha \cos \beta - \sin \alpha \sin \beta] + i[\cos \alpha \sin \beta + \cos \beta \sin \alpha]
$$
Equating the real and imaginary parts,
$$
\cos(\alpha + \beta) = \cos \alpha \cos \beta - \sin \alpha \sin \beta
$$
$$
\sin(\alpha+\beta) = \cos \alpha \sin \beta + \cos \beta \sin \alpha
$$
We can derive any identity from this.
For instance,
$$
\cos(2\theta) = \cos(\theta + \theta) = \cos \theta \cos \theta - \sin \theta \sin \theta
$$
$$
= 2\cos ^{2}\theta - 1
$$
Which implies,
$$
\cos ^{2}\theta = \frac{1 + \cos(2\theta)}{2}
$$
Also,
$$
\cos(\alpha + \beta) + \cos(\alpha-\beta)
$$
$$
= \cos \alpha \cos \beta - \sin \alpha \sin \beta + \cos \alpha \cos(-\beta) - \sin \alpha \sin(-\beta)
$$
$$
= \cos \alpha \cos \beta - \sin \alpha \sin \beta + \cos \alpha \cos(\beta) + \sin \alpha \sin(\beta)
$$
$$
 = 2\cos \alpha \cos \beta 
$$
Therefore,
$$
\cos \alpha \cos \beta = \frac{\cos(\alpha+\beta) + \cos(\alpha-\beta)}{2}
$$
This shows up in Fourier Theory on signal processing. For example,
$$
\int_{0}^{2\pi} \cos(px)\cos(qx) \, dx 
$$
Here, $p,q \in \mathbb{Z}$, and $p \neq q$.
$$
\frac{1}{2}\int_{0}^{2\pi} \cos(px + qx) + \cos(px-qx) \, dx 
$$
Case 1: $p = q$
$$
\frac{1}{2}\int_{0}^{2\pi} \cos(2px) + \cos(0x) \, dx  = \frac{1}{2}\int_{0}^{2\pi} \cos(2px) + 1 \, dx 
$$
$$
=\frac{1}{2}\left[ \frac{\sin(2px)}{2p} +x\right]^{2\pi}_{0} = \frac{1}{2}2\pi = \pi
$$

