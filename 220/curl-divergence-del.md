# The del operator

###### In Cartesian Coordinates

$\nabla=\frac{\delta}{\delta x}\hat x+\frac{\delta}{\delta y}\hat y+\frac{\delta}{\delta z}\hat z$

**del** is an operator that you "apply" to a scalar or vector field. 
It can be multiplied with a scalar, OR it can be dot/cross producted with a 
vector. 

#### Scalar quantities (Gradient vector)

A gradient vector tells us which "direction" results in the greatest increase
of the given function. 
It can be thought of as the derivative of a function with respect to each 
coordinate direction (ie, xyz). Doing so would give the "rate of change" with
respect to each "direction". 

Example: given $T=5x^2yz$ (scalar quantity), we can apply the del operator, 
giving

$\nabla T=\frac{\delta}{\delta x}\hat x+\frac{\delta}{\delta y}\hat y+\frac{\delta}{\delta z}\hat z\cdot(5x^2yz)$

from here, we can directly distribute $T$ across the del operator. 
From there we simply carry out the partial derivative with respect to each 
variable, giving

$\nabla T=10xyz \hat x+5x^2z \hat y+5x^2y \hat z$

Now, if we knew where we were (given some x,y,z coordinates), we could use the 
gradient function to tell us that moving in the resulting vector direction would
increase the function $T$ the greatest. 
Furthermore, the **magnitude** of the gradient gives us the "rate of change" 
of the function IF we moved in the given direction.

#### Vector quantity: Divergence

Divergence tells you how much a vector field is "flowing" into or out of 
a point in space. 

Flow (or **flux**) can be thought of as the "amount" of a field that passes
**perpendicular** through a given surface. 

$Flux=\vec{E}_{\perp S}S$

where $\vec{E}_{\perp S}$ represents the average field over surface area $S$.
This can be rewritten in integral form, giving

$Flux=\int{\vec{E}\cdot\vec{ds}}$ 

where $\vec{ds}$ represents a differential surface area vector 
(normal to the surface)

**Divergence can be described as such**. Given an arbitrary vector field, and
a random point in space. Imagine a cube surrounding this point, with its $x,y,z$
vertecies approaching 0. For this cube, calculating the Flux would yield the
**divergence**. Hence, divergence can be given as 

$Divergence=\frac{flux}{small\, volume}$

Furthermore, the **divergence theorem** states that the total flux through any 
_closed surface_ can be found by breaking the surface's volume into little
cubes, finding the flux through each of those cubes, and adding them together.
Mathematically, this can be written as 

$\int{\vec{\nabla}\cdot\vec{E}dV}=\oint{\vec{E}\cdot\vec{ds}}$


Example: given $\vec{E}=5y\hat x+2x\hat y+3z\hat z$, we can dot product the nabla
operator, giving

$\nabla \cdot \vec{E}=\begin{pmatrix} 5y \\ 2x\\3z \end{pmatrix}\cdot \begin{pmatrix} \frac{\delta}{\delta x}\\ \frac{\delta}{\delta y} \\ \frac{\delta}{\delta z} \end{pmatrix}$

which can be simplified to 

$\frac{\delta}{\delta x}(5y)+\frac{\delta}{\delta y}(2x)+\frac{\delta}{\delta z}(3z)$

giving us the final answer of $3$. Remember the dot product of two vectors 
ALWAYS gives a scalar quantity. 

#### Vector quantity: curl 
Curl tells you how much a vector field "swirls" or "circulates" around a point 
in space. 

Given a closed loop in a vector field, the "circulation" would be determined
by taking the differential length of the path, $\vec{dl}$, and multiplying 
it by the component of the vector field that is paralell to $\vec{dl}$, and 
adding up all the components across the loop. This can mathematically be
represented as

$circulation=\oint_c{\vec{E}\cdot}{dl}$

where $c$ represents the close loop or "contour".

Similar to how the divergence is calculated, the curl is calculated by taking
curl in the $xy$, $xz$ and $zy$ planes around an point, and finding the 
magnitude of curl. 

$curl \,\vec{E}=\vec{\nabla}\times\vec{E}$

Furthermore, **Stokes Theorem** statkes that the circulation around the border 
of any surface can be computed by breaking the blanket into smaller surfaces, 
computing the circulation around each surface, and adding them together. 
Mathematically, this can be written as 

$\oint\vec{E}\cdot\vec{dl}=\int(\vec{\nabla}\times\vec{E})\cdot{\vec{ds}})$


