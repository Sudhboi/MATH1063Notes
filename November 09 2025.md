# Applications
## Computing Volumes and Stuff

Basic Volume is a generalized cylinder.

![[Pasted image 20251117113356.png]]

## Approach 1: Slicing

Take a solid $S$ and slice it into 2d slices that are perpendicular/orthogonal to some axis.

Eg.
![[Pasted image 20251117113748.png]]

Coordinatize - base is in $xy$-plane, Slices perpendicular to the $z$

$z$-Range for slices.

$$
0\leq z \leq 5
$$
Base at $z = 0$, tip $z = 5$

Areas of slices.

$A(z)$ area of slice at height $z$.
$A(0) = 2\times 3=6$ area of base.
$A(5) = 0$

Consider 2 sides.
![[Pasted image 20251117114922.png]]

are similar triangles.

Full triangle height 5 and base 3. Base of triangle at height $z$ is,

$$
b = \frac{5-z}{5}\cdot 3
$$
Viewed from the other side,

$$
b = \frac{5-z}{z}\cdot 2
$$

$$
A(z) = \frac{3(5-z)}{5}\cdot \frac{2(5-z)}{5} = \frac{6}{25}(5-z)^{2}
$$

## Volume Formula (General)

$$
\int_{z_{min}}^{z_{max}} \underbrace{A(z)}_{\text{Area of slice}} \, \underbrace{dz}_{\text{Infinitesimally small height}} 
$$
The integrand times $dz$ is the volume of an infinitesimally short "cylinder".

Volume: 

$$
\int_{0}^{5} \frac{6}{25}(5-z)^{2} \, dz 
$$
$$
= -\frac{(5-z)^{3}}{3}\cdot \frac{6}{25}|^5_{0} = 10
$$
## Volume of the sphere

![[Pasted image 20251117120058.png]]

Axis perpendicular to slices: $x$

Slice range: $-r \leq x\leq r$

![[Pasted image 20251117120148.png]]

$$
A(x) = \pi(r^{2}-x^{2})
$$
So,

$$
V = \int_{-r}^{r} \pi r^{2} - \pi x^{2}\, dx = 2 \int_{0}^{r} \pi r^{2}-\pi x^{2} \, dx  
$$
$$
= 2\left[ \pi r^{2}x- \frac{\pi x^{3}}{3} \right]^r_{0} = 2\left( \frac{2\pi r^{3}}{3} \right) = \frac{4}{3}\pi r^{3}
$$

## Special Case: Solids of Revolution.

Eg. $f(x) = \frac{1}{x}$. Take region beneath curve starting at $x = 1$ and form a solid by rotating around $x$-axis.

![[Pasted image 20251117120849.png]]

Calculate Volume

Slices are discs perpendicular to $x$-axis.

$$
A(x) = \pi r^{2}, r = f(x)
$$
$$
= \pi(f(x))^{2}
$$
Volume = 

$$
\int_{1}^{\infty} \pi\frac{1}{x^{2}} \, dx 
$$
## Washers

Example: Volume of sphere of radius 4 with cylinder of radius 1 drilled out.
![[Pasted image 20251117121714.png]]

Axis: $x$
$x$-range

$$
1=\sqrt{ 4^{2}-x^{2} }
$$
$$
x = \pm \sqrt{ 15 }
$$

Area of a slice (washer)

![[Pasted image 20251117121911.png]]

Area = 

$$
A(x) = \pi r_{\text{out}}^{2} - \pi r_{\text{in}}^{2}
$$
$$
A(x) = \pi(16-x^{2})-\pi = \pi(15-x^{2})
$$

Volume =

$$
\int_{-\sqrt{ 15 }}^{\sqrt{ 15 }} \pi(15-x^{2}) \, dx 
$$
