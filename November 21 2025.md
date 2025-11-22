## Computing Surface Area

![image](attachments/Pasted%20image%2020251121113305.png)

![image](attachments/Pasted%20image%2020251121114728.png)

Area of a Frustum:
$$
A = \pi(r_{1}+r_{2})l
$$

![image](attachments/Pasted%20image%2020251121115158.png)

Area:

$$
r_{1}=f(x_{i}),\text{ } r_{2} = f(x_{i +1})
$$
$$
l = \sqrt{ \Delta x_{i}^{2} + \Delta y_{i}^{2} }
$$
$$
A = \pi(f(x_{i}) + f(x_{i+1}))\sqrt{ \Delta x_{i}^{2} + \Delta y_{i}^{2} }
$$
$$
A_{n} = \sum_{i=0}^{n-1} \pi(f(x_{i}) + f(x_{i + 1}))\sqrt{ 1 + \left( \frac{\Delta x_{i}}{\Delta y_{i}}\right)^{2} } \Delta x_{i}
$$

We have,

$$
\exists x_{i} \leq x_{i}^*\leq x_{i+1} \text{ s.t. } f'(x_{i}^*) = \frac{\Delta y_{i}}{\Delta x_{i}}
$$

by MVT, and,

$$
\exists x_{i} \leq x_{i}^{**}\leq x_{i+1} \text{ s.t. } f(x_{i}^{**} = Avg(f(x_{i}), f(x_{i+1})))
$$

by Intermediate Value Theorem.

$$
A_{n} = \sum_{i=0}^{n-1} 2\pi f(x^{**}_{i}) \sqrt{ 1 + f'(x)^{2} } \Delta x_{i}
$$
$$
\lim_{ n \to \infty } A_{n} = \int_{x_{\text{min}}}^{x_{{max}}} 2\pi f(x)\sqrt{ 1 + f'(x)^{2} } \, dx 
$$

which is the surface area.

## Surface Area of Sphere

$$
y = f(x) = \sqrt{ r^{2}-x^{2} }
$$
$$
A = \int_{-r}^{r} 2\pi \sqrt{ r^{2}-x^{2} } \sqrt{ 1 + \left[ \frac{-x}{\sqrt{ r^{2}-x^{2} }} \right]^{2} } \, dx 
$$
$$
A = \int_{-r}^{r} 2\pi r \, dx = [2\pi rx]^r_{-r} = 2\pi r \cdot 2r = 4\pi r^{2}
$$

## Physical Applications

1. If a linear rod has linear density $\rho (x)$,

![image](attachments/Pasted%20image%2020251121121146.png)

then its mass is $M  = \int_{x_{\text{min}}}^{x_{\text{max}}} \rho(x) \, dx$. Integrand is the mass of an infinitesimal piece of rod.

2. Mass of a radially symmetric disc.

$$
M = \int_{0}^{R} 2\pi r \rho(r) \, dr 
$$

![image](attachments/Pasted%20image%2020251121121757.png)

Example: A pirate has a 10m dangling over their boat for crossfit. The linear density of the chain is 4 kg/m.
