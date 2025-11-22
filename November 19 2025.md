## Volumes of revolution using Cylindrical Shells

![[Pasted image 20251119113709.png]]
![some image](attachments/Pasted%20image%2020251119113709.png)

![image](attachments/Pasted%20image%2020251119114144.png)

![image](attachments/Pasted%20image%2020251119114305.png)

![image](attachments/Pasted%20image%2020251119114415.png)

The volume of the cylinder is,

$$
V = \underbrace{f(x^*_{i})}_{\text{height}}\cdot\underbrace{\pi(x_{i+1}^{2} - x_{i}^{2})}_{\text{Base Area}}
$$

## Approximation with n-shells

![image](attachments/Pasted%20image%2020251119114756.png)

$$
A_{n} = \sum_{i=0}^{n-1} f(x^*_{i})\cdot \pi(x_{i+1}^{2}-x_{i}^{2})
$$

## Tangent - Riemann Sum

$$
S_{n} = \sum_{i=0}^{n} f(x_{i}^*) \Delta x_{i}
$$

Have partition ${x_{0},x_{1},\dots,x_{n}}$. $\Delta x_{i} = x_{i+1} - x_{i}$, $x_{i} \leq x_{i}^* \leq x_{i+1}$, which is the Sample Point.

## Coming Back

$$
A_{n} = \sum_{i=0}^{n-1} f(x^{\*}_{i})\cdot \pi(x_{i+1}^{2}-x_{i}^{2})
$$
$$
A_{n} = \sum_{i=0}^{n-1} f(x^{\*}_{i})\cdot \pi(x_{i+1} + x_{i})(x_{i + 1} - x_{i})
$$
$$
A_{n} = \sum_{i=0}^{n-1} f(x^{\*}_{i})\cdot \pi(x_{i+1} + x_{i})\Delta x_{i}
$$
$$
A_{n} = \sum_{i=0}^{n-1} f(x^{\*}_{i})\cdot 2\pi \frac{x_{i+1} + x_{i}}{2} \Delta x_{i}
$$

Take sampling $x_{i}^{\*}$ as the mid point.

$$
A_{n} = \sum_{i=0}^{n-1} 2\pi f(x^{\*}_{i})\cdot x_{i}^* \Delta x_{i}
$$

This is a riemann approximation that gives,

$$
\lim_{ n \to \infty } A_{n} = \int_{x_{\text{min}}}^{x_{\text{max}}} 2\pi x f(x) \, dx 
$$

Which is the volume.

(Fact: If $f(x)$ is integrable, so is $2\pi xf(x)$)

## Example

What is the volume of rotating this around the $y$-axis?

![image](attachments/Pasted%20image%2020251119115930.png)

$$
= \int_{1}^{2} 2\pi x \frac{1}{x^{2}} \, dx  = [2\pi \ln x]^2_{1} = 2\pi \ln 2
$$

# Arc Length

How long is a curve?

![image](attachments/Pasted%20image%2020251119120440.png)

## Integral Mean Value Theorem

$$
\int_{a}^{b} f(x) \, dx = (b-a)f(x^\*)
$$

for some $x^* \in [a, b]$

## How to approximate arc length?

![image](attachments/Pasted%20image%2020251119121139.png)

$$
A_{n} = \sum l_{i}
$$

![image](attachments/Pasted%20image%2020251119121307.png)

By the MVT there is a sample point $x^{\*}_{i} \in [x_{i}, x_{{i+1}}]$ s.t.

$$
\frac{\Delta y_{i}}{\Delta x_{i}} = f'(x_{i}^{\*})
$$
$$
A_{n} = \sum_{i=0}^{n-1} l_{i} = \sum_{i=0}^{n-1} \sqrt{ \Delta x^{2}_{i}+\Delta y^{2}_{i} }
$$
$$
= \sum_{i=0}^{n-1}  \sqrt{ 1 + \frac{\Delta y_{i}^{2}}{\Delta x_{i}^{2}} } \Delta x_{i}
$$
$$
= \sum_{i=0}^{n-1} \sqrt{ 1 + [f'(x_{i}^*)]^{2} } \Delta x_{i}
$$

Therefore,

$$
\lim_{ n \to \infty } A_{n} = \int_{x_{\text{min}}}^{x_{\text{max}}} \sqrt{ 1 + (f'(x))^{2} } \, dx 
$$
