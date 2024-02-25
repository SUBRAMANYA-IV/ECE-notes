### Black body radiation

##### What is a black body?

When an _opaque_ body absorbs radiation, part of it is reflected and the rest
of it is absorbed. the color of bodies is given by the light they _reflect_.

Absorbtion can be described as follows 

1) Radiation absorbed leads to an increase in kinetic energy of its constituent 
  atoms
2) they oscillate about their equilibrium positions
3) average thermal/kinetic energy of the atoms of a body determines its 
  temperature, hence the temperature of the body increases. 
4) The electrons of the constituent atoms are accelerated by the oscillations. 
4) This increase in kinetic energy of the electrons could result in them 
   gaining enough energy to escape, releasing energy in the form of 
   electromagnetic radiation. 
5) Reduces the kinetic energy of the oscillations and leads to a lower temp

When this process is in equilibrium, ie the rate of absorption is equal to
the rate of emission, the body is in thermal equilibrium. hence _a good
absorber of radiation is also a good emitter_ 

The electromagnetic radiation emitted from this process is called _thermal 
radiation_. At normal temperatures (below 600 celcius), the emitted
radiation is not visible; mostly in the infrared and microwave spectrum 

As the temperature of the body increases, the proportion of _high frequency_ 
wavelenghts, ie the visible and UV band, increase. at the 600-700 degree range,
materials start glowing red.

A body that absorbs **all** radiation incident on it is called an **ideal black
body**. The relation between the power radiation by an ideal black body and
the temperature can be given by 

$R=\sigma T^4$

where

- $R$ is te power per unit area
- $T$ is the absolute temperature (kelvin)
- $\sigma=5.6703*10^{-8}\frac{W}{m^2K^4}$, Stefan's constant. 

This applies to black bodies, where **ONLY** the temperature matters. 
In reality, for non-ideal bodies, factors like color, composition and more
impact the rate at which energy is emmitted (or power, remember power=
$\frac{joules}{second})$ 

To account for all these factors, the constant $\epsilon$, or emissivity
is used to "scale" the power per area from a black body to a real body
(is ALWAYS less than 1). 

Furthermore, the _spectral distribution_ (ie which wavelenghts and how much)
of the radiation emitted by a blackbody is found to depnd **only** on the
absolute temperature $T$

![black-body-radiation](https://cdn.britannica.com/83/283-050-7701048B/energy-unit-area-second-wavelength-interval-temperatures.jpg)
**important notes**

- the x-axis measures the wavelength
- the y-axis measures TODO

The _emperically_ determined relation yields a function with the curve given 
above. some key properties that can be noted is that 

- the wavelength at which the distribution has its maximum value varies 
  invesrely with the temperature, given by
  
  $\lambda_m\propto \frac{1}{T}$
  
  or 
  
  $\lambda_m T=constant=2.898*10^{-3}m\cdot K$


# Rayleigh-Jeans equation

calculating Wiens distribution or $R(\lambda)$ requires the calculation of 
the _energy density of electromagnetic waves in a cavity_ (tf does this mean?)

An interesting way to simulate an ideal black body is a cavity, such as 
a keyhole in a closet door. The electromagnetic radiation that goes into 
the hole doesnt have the chance to be reflected, and if it does, it likely 
gets re-absrobed in the interoir of the object, making it a good approximation
to an ideal black body 

the power radiation _out_ of the hole is proportional to the total energy 
density $U$ (energy per unit volume of the radiation in the cavity), which
can be shown to be

$R=\frac{1}{4}cU$

(Remember, the unit of $R$ is $\frac{W}{m^3}$)

this principle can be extended as a function, given by 

$R(\lambda)=\frac{1}{4}cu(\lambda)$

where if $u(\lambda)d\lambda$ is the _fraction of energy per unit volume_ in 
the given range $d\lambda$ (remember, the proportion of a wavelenght cannot
be given as a SINGULAR wavelenght, instead a range of wavelenghts, hence
explaining the use of the $d\lambda$ expression).

The energy density distribution function $u(\lambda)$ can be calculated from 
classical physics in a straightfoward way. This involves finding the number of
modes of oscillation of the electromagnetic field in the cavity with 
wavelenghts in the interval $d(\lambda)$ and multiplying by the average
energy per mode
Hence, the number of modes of oscillation per unit volume, $n(\lambda)$
is independent of the shape of the cavity and is given by 

$n(\lambda)=8\pi\lambda^{-4}$

which is independent of the shape of the cavity, and only depends on the 
wavelength of the given radiation

The average energy per mode of oscillation is $kT$, where $k$ is the Boltzmann
constant. Hence, it can be stated that 

$u(\lambda)=kTn(\lambda)=8\pi kT\lambda^{-4}$

finally, this gives us the _Rayleigh-Jeans equation_. 

At long wavelenghts, the equation agrees with the experimentally determined
spectral distribution, but at short wavelenghts this equation predicts that 
$u(\lambda)$ becomes large, approaching infinity as $\lambda \rightarrow \infty$
whereas the experiment shows the opposite; it approaches 0. 
This conflict of theoretical and experimental observations was called the 
_ultraviolet catastrophe_. The solution? 

## Planck's Law

The fundamental assumtion is that, as the wavelength gets shorter, the
number of _modes_, or standing waves, possible will increase. therefor, as 
$\lambda\rightarrow\infty$ the number of modes of oscillation approach infinity
as seen by the equation $n(\lambda)=8 \pi \lambda^{-4}$, which gives
_the number of modes of oscillations (ie, the number of standing waves possible
per unit volume)_. 
For the energy density formula $u(\lambda)$ to approach zero as $\lambda\rightarrow 0$
According to classic physics, the EM waves in the cavity are produced by 
accelerated electric charges in the walls of the cavity vibrating as
simple harmonic oscillators. Recall that the radiation emitted by such
oscillators has the **SAME FREQUENCY** as the oscillation itself. 
This in the end leads to the same problem as before, ie the ultraviolet 
catastrophe

Plank managed to solve this by deriving an equation by calculating the average
energy $\bar{E}$ **assuming** that the energy of the oscillating charges, 
and hence the radiation that was emitted, was discrete; ie, that it 
could take on only the values of $0,\epsilon,2\epsilon...n\epsilon$ where $\epsilon$ represents the energy of each particle, which can be written as 

$E_n=n\epsilon=nhf$

The rest of the derivation is beyond the scope of this class, but the important
thing is 

Plank Tried to reconcile his new equation with classical physics, but was
unable to. This lead to the idea of _quantization of energy_, or that it could
only occur at integer multiples of a fundamental quantity, which was later
proven by einstein to explain the photoelectric effect and suggested that
rather than being a strange property of oscilators in the cavity walls
and blackbody radiation, quantization was a fundamental charecteristic of
light energy. 









**TODO: THE FUCK IS A MODE?**







