Note: Everything here is a polynomial.
## Partial Fractions

A rational function is a function 

$$
f(x) = \frac{P(x)}{Q(x)}
$$

where $P(x)$ and $Q(x)$ are polynomials. 
Goal: Find antiderivatives of all rational functions. (We can always find an elementary antiderivative for rational functions.)

$\mathbb{R} [x]$ the set of $\mathbb{R}$-polynomials. Eg, $x^{2} + 3x - 7$, or $\sqrt{ 2 }x^{17} - e$, where $x$ is always raised to a natural number. 

## Degree Formula

$$
deg(f(x)g(x)) = deg(f(x)) + deg(g(x))
$$
$$
deg(C) = 0
$$

## Division Algorithm

Given $f(x)$ and $p(x)$ there are polynomials $q(x)$, $r(x)$ with 

$$
f(x) = p(x)q(x) + r(x)
$$

with $deg(r(x)) < deg(p(x))$. Here, $r(x)$ is the remainder of the division of $\frac{f(x)}{p(x)}$. 

## Example:

$$
f(x) = x^{3}, p(x) = x -1
$$

Here, remainder will be a number.

![image](attachments/Pasted%20image%2020251105114230.png)

$$
\therefore x^{3} = (x-1)(x^{2}+x+1) + 1
$$

Note: $p$ does not divide $f$.
Take,
![image](attachments/Pasted%20image%2020251105114458.png)

$$
\therefore x^{3} = (x^{2}-1)(x) + x
$$

As we can see, the remainder has degree 1.

Theorem: If $f(x)$ is a polynomial, and $f(a) = 0$, then $f(x) = (x-a)g(a)$.

Proof 1: Taylor series - trivial but inefficient.

Proof 2: 

$$
f(x) = (x-a)g(x) + r(x)
$$
$$
= (x-a)g(x) + C
$$
$$
f(a) = (a-a)g(a) + C = 0
$$

Therefore, $C = 0$.

A polynomial $f$ is irreducible if $f$ is not the product of two polynomials of strictly lower degree.

Eg. 

$$
x^{2} -1 = (x+1)(x-1)
$$
$$
x^{2} + 1 = x^{2} + 1
$$

Theorem: The irreducible polynomials in $\mathbb{R}[x]$ are 

$$
ax + b; a,b\in \mathbb{R}
$$
$$
ax^{2} + bx + c; \Delta = b^{2} - 4ac < 0
$$

That's it. It follows from the fundamental theorem of Algebra and some more algebra. 

Fun Fact: Irreducible polynomials are like prime numbers.

A polynomial has a factorization into powers of irreducibles. What follows is,

$$
\frac{1}{(x-2)(x-3)} = \frac{A}{x-2} + \frac{B}{x-3}
$$

Claim: $A$ and $B$ exist. (proof: trust me bro).
To find them, we re-add the fraction. 

$$
\frac{A}{(x-2)} + \frac{B}{(x-3)} = \frac{A(x-3) + B(x-2)}{(x-2)(x-3)} = \frac{(A + B)x + (-3A - 2B)}{(x-2)(x-3)}
$$

Therefore,

$$
(A + B)x + (-3A - 2B) = 1
$$
$$
\implies A + B = 0, (-3A - 2B) = 1
$$

We can solve this system of linear equations to find $A$ and $B$.
We get $B = 1$ and $A = -1$.

Therefore,

$$
\frac{1}{(x-2)(x-3)} = \frac{-1}{x-2} + \frac{1}{x-3}
$$

So,

$$
\int \frac{1}{x^{2}-5x+6} dx = \int \frac{-1}{x-2} + \frac{1}{x-3}dx = -\ln |x-2| + \ln |x-3| + C = \ln | \frac{x-3}{x-2} | + C
$$

Two polynomials are relatively prime if they have no common proper factors.

Theorem: If $r, s \in \mathbb{Z}$ are coprime then there are integers $u, v$ s.t.

$$
1 = ur +  vs
$$

Theorem: If $f, g \in \mathbb{R}[x]$ are coprime, and $h \in \mathbb{R}[x]$ then there are polynomials $u, v$ s.t.

$$
h = uf + vg
$$

So,

$$
\frac{h}{f\cdot g} = \frac{u}{g} + \frac{v}{f}
$$

If $f$ or $g$ are reducible, we can carry on.

If $deg(h) < deg(f^n)$ then,

$$
h = r_{1} + r_{2}f + \dots + r_{n}f^{n-1}
$$

with $deg(r_{i}) < deg(f)$.

$$
h = r_{1} + fP_{1}
$$
$$
P_{1} = r_{1} + fP_{2}
$$

or:

$$
\frac{x^{7}+13x+1}{(x^{2}+1)^{4}} = \frac{A_{1}x + B_{1}}{x^{2}+1} + \dots + \frac{A_{4}x + B_{4}}{(x^{2}+1)^{4}}
$$




