$$
\frac{P(x)}{Q(x)}
$$
Step 0: If $deg(P(x)) \geq deg(Q(x))$, do long division $P(x) = D(x)Q(x) + R(x)$, $deg(R(x)) < deg(Q(x))$.

$$
\frac{P(x)}{Q(x)} = D(x) + \frac{R(x)}{Q(x)}
$$

Step 1: Factor $Q(x) = l_{1}(x)^{n_{1}}\dots l_{r}(x)^{n_{r}}\cdot q_{1}(x)^{m_{1}}\dots q_{s}(x)^{m_{s}}$ where the $l_{i}(x)$ are linear factors and $q_{j}(x)$ are irreducible quadratic factors. Exponents $n_{i}, m_{j}$ are called multiplicities.

$$
\frac{R(x)}{Q(x)} = \underbrace {\frac{A_{11}}{l_{1}(x)} + \dots + \frac{A_{1n_{1}}}{l_{1}(x)^{n_{1}}}+ \dots}_{\text{Linear part. All numerators are constant.}  }+ \underbrace{\frac{B_{11}x + C_{11}}{q_{1}(x)} + \dots + \frac{B_{1m_{1}}x + C_{1m_{1}}}{q_{1}x^{m_{1}}}}_{\text{Quadratic Factors part. All numerators are } Bx + C \text{ So linear factors/deg1 polynomials}}
$$

Step 3. Add fractions on RHS. Numerator equals $R(x)$. Equate coefficients and solve for $A_{ij}, B_{pq}, C_{pq}$. 

## Example

$$
\frac{x^{3}}{(x-1)(x+2)}
$$
$$
\frac{x^{3}}{(x-1)(x+2)} = x - 1 + \frac{3x - 2}{(x-1)(x-2)}
$$
$$
\frac{3x-2}{(x-1)(x+2)} = \frac{A}{(x-1)} + \frac{B}{(x-2)}
$$

Direct Method:

$$
\frac{A}{x-1} + \frac{B}{x+2} = \frac{A(x+2) + B(x-1)}{(x-1)(x+2)}
$$
$$
 = \frac{(A+B)x + (2A-B)}{(x-1)(x+2)}
$$

Which implies,

$$
A + B = 3
$$
$$
2A - B = -2
$$

You solve for $A$ and $B$ and plug into the equations, and then integrate as usual.

Less Direct Method.

$$
\frac{A(x+2) + B(x-1)}{(x-1)(x+2)} = \frac{3x-2}{(x-1)(x-2)}
$$
$$
A(x+2) + B(x-1) = 3x-2
$$

Sub $x = 2$ to kill $(x+2)$. This gives us,

$$
A(0) + B(-2-1) = 3(-2)-2
$$
$$
B = \frac{8}{3}
$$

Subbing $x=1$ gives $A = \frac{1}{3}$.
Therefore,

$$
\frac{x^{3}}{(x-1)(x+2)} = x -1 + \frac{1}{3} \frac{1}{x-1} + \frac{8}{3} \frac{1}{x + 2}
$$
$$
\int \frac{x^{3}}{(x-1)(x+2)} = \frac{x^{2}}{2} - x + \frac{1}{3}\ln |x-1| + \frac{8}{3}\ln |x + 2| + C
$$

The sub-to-kill trick works with linear factors with multiplicities all 1.

## Another Example

$$
\frac{x^{3}}{x(x-1)(x-2)^{2}} = \frac{B}{x-1} + \frac{C}{x-2} = \frac{D}{(x-2)^{2}}
$$

Yea I'm not typing this out. Just use your brain.

