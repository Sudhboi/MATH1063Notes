## Theorem of Pappus (contd.)

The volume obtained by rotating a region $R$ around a line $l$ is equal to,

$$
V = L\cdot \text{area}(R)
$$

where $L$ is the distance travelled by the centre of mass as it is rotated around $l$.

$$
L = 2\pi r
$$

where $r$ is the distance from centre of mass to the axis.

Proof: Assume $\rho = 1$. Align $l$ with $y$-axis

$$
\bar{x} = \frac{M_{y}}{M} = \frac{\int_{a}^{b} x(f(x) - g(x)) \, dx }{\int_{a}^{b} f(x) - g(x) \, dx } = \frac{M_{y}}{A}
$$

$$
L = 2\pi \bar{x}
$$
$$
L \cdot \text{Area}(R) = 2\pi \bar{x} \cdot \text{Area}(R)
$$
$$
= 2\pi \left[\frac{\int_{a}^{b} x(f(x) - g(x)) \, dx }{\int_{a}^{b} f(x) - g(x) \, dx }\right] \cdot \int_{a}^{b} f(x) - g(x) \, dx 
$$
$$
l \cdot \text{Area}(R) = \int_{a}^{b} 2\pi x(f(x)-g(x)) \, dx 
$$

which is the same as the volume of rotation calculated using cylindrical shells.

Fact: Have two conjoined regions s.t. $\bar{x_{i}}$ is the C.M. of $R_{i}$, and $M_{i}$ be the mass of $R_{i}$. The overall C.M. $\bar{x}$,

$$
\bar{x} = \frac{M_{1}\bar{x_{1}} + M_{2}\bar{x}_{2}}{M_{1}+M_{2}}
$$

$$
\bar{x}_{1} = \frac{\int_{a}^{b} x(f(x)-g(x)) \, dx }{\int_{a}^{b} f(x) - g(x) \, dx } = \frac{M_{y_{1}}}{M_{1}}
$$
$$
\bar{x}_{2} = \frac{\int_{b}^{c} x(f(x)-g(x)) \, dx }{\int_{b}^{c} f(x) - g(x) \, dx } = \frac{M_{y_{2}}}{M_{2}}
$$

You know what to do next.
## Probability

Have $S$, which is a space of outcomes.

Eg. 
- Dice roll (d6), $S$ = {1, 2, 3, ... ,6}
- Position of an electron in 1D, $S$ = $\mathbb{R}$.

An event $E$ is a subset of $S$.

Eg. 
- Roll an even number on a d6, $E$ = {2, 4, 6}
- Electron has $x$-position between (-1, 1), $E$ = (-1,1)

A probability measure $\mu$ on $S$ assigns a number between 0 and 1 to events in $E$. There are the following rules.

1. $\mu(S) = 1$
2. If $A \cap B = \phi,$ $\mu(A \cup B) = \mu(A) + \mu(B)$, in general, $\mu(A \cup B) = \mu(A) + \mu(B) - \mu(A\cap B)$.
3. If $\{ A_{i} \}_{i=1}^\infty$ is a collection of disjoint events,

$$
\mu\left( \bigcup_{i=1}^\infty A_{i} \right) = \sum_{i=1}^{\infty} \mu(A_{i}) \leq 1
$$

Eg. consider picking a real number at random with uniform probability inside \[0, 1] (Using a 10 sided coin obviously). Take $E = \left\\{  \frac{1}{2}  \right\\}$. $\mu(E) = 0$. 

$\mathbb{Q} = \left\\{  \frac{n}{q} :n, q \in \mathbb{Z}, q \neq 0 \right\\}$. $\mathbb{Q}$ is countable. $\mathbb{Q} = \{ q_{0},q_{1},q_{2}\dots \}$, $\mathbb{Q} = \bigcup_{i=1}^{\infty}{q_{i}}$. 
