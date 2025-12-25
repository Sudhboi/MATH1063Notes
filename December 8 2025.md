## Existence and Uniqueness of ODEs

$$
F: \mathbb{R}^{n+2} \to \mathbb{R}
$$
$$
F (x_{0},x_{1},\dots,x_{n},t)
$$
Initial condition $c_{0},\dots,c_{n,t_{0}}$ all in $\mathbb{R}$. If $\frac{ \partial F }{ \partial x_{i} }(x_{0}, \dots,t)$ and $\frac{ \partial F }{ \partial t }(x_{0},\dots,t)$ are continuous at $(c_{0}, \dots, c_{n}, t_{0})$. Then $F(y, y',\dots,y^n,t) = 0$ has a unique solution with $y^{(m)}(t_{0}) = C_{m}$ defined on some small $[t_{0}-\delta, t + \delta]$.

Eg. $y''+ty=0 \implies y'' = -ty$
$$
y'' = F(y, y', t)
$$
$$
F(x_{0}, x_{1}, t) = -tx_{0}
$$
$$\frac{ \partial F }{ \partial x_{0} } = -t$$
$$
\frac{ \partial F }{ \partial t } = -x_{1} 
$$

## Separation of Variables.

Method:

Write $y'$ as $\frac{dy}{dx}$ and pretend its a function. If can set to $h(y)dy = g(x)dx$, integrate both sides and solve for constants.

## Eg. Falling with air resistance.
$v$ is velocity.
$$
v' = -g -kv \, (k > 0)
$$
($-kv$ makes air resistance in opposite direction as velocity.)
$k$ is the air resitance coefficient.

Standard Form

$$v' +kv = -g$$

Use an integrating factor $\mu(t)$.

$$\implies \mu v' + \mu kv = -\mu g$$

Things we want

$$
\frac{d}{dt}[\mu v] = \mu v' + \mu kv
$$
 On the one hand,
$$
\frac{d}{dt}[\mu v] = \mu v' + \mu'v
$$
We need,
$$
\mu' = \mu k
$$
to get our wish. Note,

$$
\frac{d\mu}{dt} = \mu k
$$
This is separable so,

$$
\frac{d\mu}{\mu} = kdt
$$
$$
\implies \ln |\mu| = kt + C_{1}
$$
$$
\implies |\mu| = e^{kt + C_{1}} = e^{kt}C_{2}
$$
$$
\implies \mu = e^{kt}C_{3}
$$
where $C_{3}$ can be positive/negative.

Coming back,

$$
\mu v' + \mu kv = -\mu g
$$

By our choice of $\mu$, LHS is nice.

$$
\implies \frac{d}{dt}[\mu v] = -\mu g
$$

Solve for $v$ by integrating both sides.

$$
\mu v = \int -\mu g \, dt 
$$
$$
v = \frac{1}{\mu}\int -\mu g \, dt 
$$
$$
\implies v = -\frac{1}{e^{kt}C_{3}}\int -e^{kt}C_{3} \, dt 
$$
$$
= \frac{1}{e^{kt}}\left( -\frac{g}{k} \right)[e^{kt} + C]
$$
$$
= -\frac{g}{k}[1 + Ce^{-kt}]
$$
Some Initial Conditions.
$v(0) = 0$ is "Just Dropped Case"
$$
v(0) = \left( -\frac{g}{k} \right)[1 + Ce^{0}] = 0
$$
$$
\implies C = -1
$$
$$
v(t) = \left( -\frac{g}{k} \right)[1-e^{-kt}]
$$

Coming hot from space

$v(0) = -1000$
$$
-\frac{g}{k}[1 + C] = -1000
$$
$$
C = \frac{1000k}{g} - 1
$$
Already going at terminal velocity.

$v(0) = -\frac{g}{k}$
$$
-\frac{g}{k}=-\frac{g}{k}[1 + C] \implies C =0
$$
$$
v(t) = -\frac{g}{k}
$$
## Generalized First Order Linear Differential Equation

$$
a(x)y' + b(x)y = c(x)
$$
Standardize.

$$
y' + p(x)y = q(x)
$$
$$
\mu(x) = e^{\int p(x)dx}
$$
$$
y = \frac{1}{\mu(x)}\int \mu(x)q(x)dx
$$