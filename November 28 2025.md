## Centres of mass of thin metal plates

Total mass is $\rho\cdot$area. 
To describe 2d shapes, we consider regions bounded by graphs of functions. 

$$
M = \int_{1}^{e} \rho (x^{2}-\ln x) \, dx 
$$

To find center of mass $(\bar{x}, \bar{y})$,
$M_{y}$ is the moment relative to the $y$-axis.
Break region into vertical slivers.

For sliver at $x$, we look at,

$$
x\cdot\underbrace{\text{Infinitesimal mass}}_{\rho(f(x) - g(x))dx}
$$
$$
M_{y} = \rho \int_{a}^{b} x(f(x) - g(x)) \, dx 
$$
For center of mass,

$$
\frac{M_{y}}{M} = \frac{\sum x_{i}m_{i}}{\sum m_{i}} = \bar{x}
$$
where $M$ is the total mass.

$M_{x}$ is the moment relative to $x$-axis.
The moment of a rod of constant density and total mass $M$ is the same as a point mass at the $\frac{b^{2}-a^{2}}{2}$ of the rod with mass $M$.

$$
M = \int_{a}^{b} \rho \, dx = \rho(b-a)
$$
$$
M_{y} = \int_{a}^{b} \rho x \, dx = \frac{\rho (b^{2}-a^{2})}{2}
$$

To find $M_{x}$, integrate the moment of every vertical sliver.
Treat each sliver as an infinitesimaly thin rod. the contribution of $M_{x}$ to each sliver,

$$
M_{y(x)} 
$$
where $M$ is the mass of the sliver, $y(x)$ is the center of the sliver. 

$$
M = \rho(f(x) - g(x)) dx
$$
$$
y(x) = \frac{f(x)+g(x)}{2}
$$

so,

$$
M_{x} = \int_{a}^{b} \frac{\rho (f^{2}(x) - g^{2}(x))}{2} \, dx 
$$
$$
\bar{y}=\frac{M_{x}}{M}
$$

## The Theorem of Pappus

Let $R$ be a closed bounded region in the plane, and let $l$ be a line in the plane that is disjoint from $R$. The volume of the donut thing obtained by rotating $R$ around $l$ is,

$$
V = \text{Area}(R) \cdot \text{distance travelled by the centre of mass of \(R\) rotated around \(l\)}
$$
Proof: Socially construct $y$-axis to be $l$, pick $x$-axis so that $M_{x} = 0$.

$$
A = \int_{a}^{b} f(x) - g(x) \, dx
$$
$$
M_{y} = \int_{a}^{b} x(f(x) - g(x)) \, dx 
$$

Distance travelled by center of mass  = $2\pi \bar{x} = 2\pi\dots$ (Continued on Monday)
