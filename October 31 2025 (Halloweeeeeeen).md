## More integrating Trig Stuff

$$
\frac{d}{dx} \tan(x) = \frac{d}{dx} \frac{\sin(x)}{\cos(x)} = \frac{\cos ^{2}x+\sin ^{2}x}{\cos ^{2}x} = \sec ^{2}x
$$
Which means,
$$
\int \sec ^{2}x \, dx = \tan(x) + C
$$
$$
\frac{d}{dx} \sec(x) = \frac{d}{dx}[\cos(x)]^{-1} = -1[\cos(x)]^{-2}(-\sin x) = \sec x\tan x
$$
$$
\implies \int \sec x\tan x = \sec x + C
$$
$$
\int \tan x \, dx = \int \frac{\sin x}{\cos x} \, dx 
$$
$$
u = \cos x, du = -\sin x
$$
$$
\int \tan x \, dx = \int-\frac{du}{u} = -\ln |u| + C = \ln|\sec x| + C 
$$
So e.g. $\int\tan ^{4}x\sec ^{2}x \,dx$ is similar to the ones using  $\cos(x)$ and $\sin(x)$.
But,

$$
\int \tan ^{4}x\sec ^{4}x \, dx = \int \tan ^{4}x(1+\tan ^{2}x)\sec ^{2}x\, dx 
$$
What is $\int \sec(x)\,dx$ though?

Take this absolutely not random function - 
$$
\ln (\sec(x) + \tan(x))
$$
$$
\frac{d}{dx} \ln (\sec x+\tan x) = \frac{1}{\sec x+\tan x} (\sec x\tan x+\tan ^{2} x) = \sec x
$$

This integral is interesting because its raining outside (also mercador projections but whatever).

## Mercador Projection of the unit sphere

Rule 1 : Must preserve angles
Rule 2 : Longitudinal Lines must be vertical.

If in a boat, the compass always points in same direction, travel on straight line.

![[Pasted image 20251031115237.png]]
If you chop the sphere at $\theta$,
![[Pasted image 20251031115546.png]]
![[Pasted image 20251031115851.png]]
lower side of square with length $h$ takes
$$
\frac{h}{2\pi \cos \theta}
$$
of the latitudes, so length is $\frac{h}{\cos \theta}$ in projection.
![[Pasted image 20251031120122.png]]
The expansion factor varies with $\theta$ on unit space,
![[Pasted image 20251031120424.png]]

## Trig Substitution (inside out u-sub, actually)

$$
1-\sin ^{2}\theta = \cos ^{2}\theta \leftrightarrow  \sqrt{ a^{2}-x^{2} }
$$
$$
\tan ^{2}\theta + 1 = \sec ^{2}\theta \leftrightarrow \sqrt{x^{2} + a^{2}}
$$
$$
\sec ^{2}\theta -1 = \tan ^{2}\theta \leftrightarrow  \sqrt{ x^{2}-a^{2} }
$$

$$
\int_{0}^{4} \frac{dx}{\sqrt{ 16-x^{2} }} \, dx 
$$
$$
x = 4\sin \theta, dx = 4\cos \theta d\theta
$$
$$
x = 0 \implies \theta = 0
$$
$$
x = 4 \implies 4\sin \theta = 4 \implies \theta = \frac{\pi}{2}
$$
$$
= \int_{0}^{\pi/2} \frac{4\cos \theta}{\sqrt{ 16-16\sin ^{2}\theta }} \, d\theta = \int_{0}^{\pi/2} \, d\theta = \frac{\pi}{2} 
$$

There's improperness stuff but it all works out anyway.
