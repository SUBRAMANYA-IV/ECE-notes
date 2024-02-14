# Diodes

Circuit element which **does not** follow a linear current-voltage relationship. 

## The Ideal Diode

The ideal diode has I-V charecteristics such that, when the voltage is negative
(reverse biased), it acts as an open circuit and doesnt allow any current
to flow. When the voltage is positive, the diode acts as a "short circuit"
allowing any current to flow with zero voltage drop. A **forward-biased** diode
is said to be "turned on". 

##### example use of dioes: rectifier

Diodes can be used in AC circuits to attenuate the negative portion of
sinusoidal signals that are supplied to a load. 

**TODO: insert rectifier diagram**

##### example use of diodes: Diode logic gates

Another use case of diodes is modelling OR and AND logic gates. 

**TODO: insert logic gate diagram**


## Terminal Chaecteristics of junction diodes. 

Diodes are most commonly implemented using a _pn_ junction, as seen in previous
chapters. due to the barrier-voltage of _pn_ junction,s this makes them ideal
at acting as diodes, due to them readily conducting current when a 
_reverse bias_ voltage is applied, and acting as an open circuit when a
_forward bias_ voltage is applied. 

**todo: insert IV graph of pn/diodes**

The operating regions of a diode can be broken down into 3 parts

1) Forward bias region, at $v>0$
1) Reverse bias region, at $v<0$
1) breakdown region, at $v<-V_{ZK}$


### The Forward Bias Region. 

the region defined by a positive-terminal voltage. The I-V relationship
can be closely approximated by 

$i=I_s(e^\frac{v}{V_T}-1)$

Note that this is the exact same equation used in _pn_ junctions at a 
**given temperature**. (keep in mind, $V_T$ is highly dependent on temperature)
$I_S$ in this case represents the **saturation curret** or **scale current**. 
This comes from the fact that $I_S$ is _directly proportional_ to the cross
sectional area of the diode. Hence, _doubling_ the diodes area will
double the value of $I_S$. $I_S$ is also strongly related to the temperature. 
as a rule of thumb, **I_S doubles in value fo every 5c rise in temperature**

The voltage %V_T$ (thermal voltage) is given by 

$V_T=\frac{kT}{q}$

where

* $k$ is Boltzmann's constant, $8.62*10^{-5}\frac{eV}{K}=1.38*10^{-23}\frac{joules}{kelvin}$
* $T$ is the absolute temperature in kelvins
* $q$ is the magnitude of electronic charge, $1.60*10^{-19}\, coulomb$

At room temperature, $V_T$ can be approximated to $25mV$

For apprexiable current $i$ in the forward direction, specifically for 
$i>>I_S$, the previous current-voltage equation can be approximated to 

$i\approx I_se^{\frac{v}{V_T}}$

Rearanging the equation to solve for $v$, we get 

$v=V_T ln{\frac{i}{I_S}}$


Another interesting property can be demonstrated by taking two voltages, 
$V_1$ and $V_2$, and their respective forward currents $I_1$ and $I_2$, and
finding the ratio of $I_2$ to $I_1$, which gives us 

$\frac{I_2}{I_1}=e^\frac{V_2-V_1}{V_T}$

Rearanging this expression and using $log$ instead of $ln$, we get

$V_2-V_1=2.3V_Tlog(\frac{I_2}{I_1})$

which states that for every 10-fold increase in forward current leads to a 
$2.3V_T$ increase in voltage-drop






