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

![half-rectifier](https://madpcb.com/wp-content/uploads/2020/11/Half-wave-Rectifier.jpg)

##### example use of diodes: Diode logic gates

Another use case of diodes is modelling OR and AND logic gates. 

**TODO: insert logic gate diagram**
![diode-logic-gate](https://i.ytimg.com/vi/OORpgCdyJlE/maxresdefault.jpg)


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

![diode-current-voltage](https://cdn.sparkfun.com/assets/4/4/a/5/b/5175b518ce395f2d49000000.png)

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

The voltage $V_T$ (thermal voltage) is given by 

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


### Reverse-Bias region

Reverse-bias region is the region of operation when the diode voltage
is _negative_ 

The equation

$i=I_s(e^\frac{v}{V_T}-1)$

Demonstrates how, when the reverse voltage $v$ becomes a few times larger than
$V_T$, the exponential term becomes negligibly small, and the diode current
becomes

$i\approx-I_s$

where $I_S$ represents the drift current, inline with the theory behind
current in _pn junctions_
Despite theory stating $I_S$ is quiet small, **it is still much larger than 
$I_S$ in reality**, AND the magnitude of this current is still impacted
by the reverse voltage, due to **leakage effects**.
These **leakage currents** are proportional to the **junction area**, same as 
the drift current $I_S$ is. 
**however**, their dependence on temperature is different. 

- $I_S$ doubles for every 5 degrees increase in temeprature. 
- Reverse current doubles for every 10 degrees increase in temperature. 

### Breakdown Region

The region defined by when the reverse voltage exceeds a threshold value
that is specific to the particular diode, called the **breakdown voltage**,
denotated by $V_{ZK}$, where $Z$ stands for _zener_ and $K$ stands for knee

The diagram above shows how, for a given change in voltage, the current 
increases significantly, indicating that the diode has started to act like 
an _shorted circuit_ again. 


## Modeling the diode forward charecteristic 

As seen above, the diode can be modelled in two distinct ways;
ideal and exponential. 

The symbols used will be 

- DC Source: $V_{DD}$
- Resistr: $R$
- Diode Voltage: $V_D$
- Diode Current: $I_D$



### Exponential Model

This represents the most accurate description of the diode in the _forward
region_, but its non-linear, making it difficult to work with. 

###### Example

![diode-example](https://miro.medium.com/v2/resize:fit:432/1*mijJgpHdt7DDmrPsb7tOcg.png)

Analyzing the figure above, given that $V_DD$ is greater than $0.5 V$, we can
use the approximated $I-V$ relationship, given by 

$I_D=I_S e^{\frac{V_D}{V_R}}$

Utilizing kirchoffs loop rule, we also get the equation

$I_D=\frac{V_{DD}-V_D}{R}$

given these two equations, and assuming $I_S$ is known, $I_D$ and $V_D$ can
be determined through a system of equations

### Graphical Analysis with exponential model 

Graphing these two relationships can give us a more intuitive understanding
as to _why_ it makes sense. 

Given that the above circuit is linear, the current through all elements must
be the same, and so the intersection between these two curves must be the
operating voltage of the diode

![diode-load-iv-graph](https://upload.wikimedia.org/wikipedia/commons/e/ed/Load_line_diode.png)

The graph above demonstrates this. **assuming the diode doesnt have an internal
resistance**, 

- the exponential curve represents the diode IV relationship
  - the IV curve of the circuit if only the diode was there 
- the straight line represents the **load line**
  - the I-V relationship of the circuit if the diode wasn't there
- vertical axis represents the current through the whole circuit
- horizontal axis represents voltage across various elements, such as 
  - $V_D$: across the diode
  - $V_DD$ across the voltage source (or total voltage)
    - fromt his, it can be deduced that the voltage across the load is given by 
      $V_R=V_{DD}-V_D$

Though this method is good for visualizing the basic relationship, its useless
in more complex circutits. For that, we use 


### Iterative analysis Using the exponential model

The principle of iteration is to use an approximation to get initial values,
and then use those initial values to determine a more exact value of the initial
approximation

When using iteration, we're usually given the operating voltage of the diode
at a given current. 

###### Example

Determine the current $I_D$ and the diode voltage $V_D$ with $V_{DD}=5V$ and
$R=1 k\Omega$. _Assume that the diode has a current of $1mA$ at $0.7V$_

###### Reasoning
First, we assume that $V_D$ is still 0.7 at the operating current of the circuit.
This makes sense because when operating in the forward-bias region of a diodes
IV, large changes in current result in small changes in the voltage across
the diode, hence allowing for approximation.
   

$I_D=\frac{V_{DD}-V_D}{R}$

$=\frac{5-0.7}{1*10^3}=4.3mA$

with this, we 1 complete coordinate on the I-V plot, given by $(0.7V,1mA)$ 
and another incomplete one, given by $(V_2,4.3mA)$

Using the diode equation, we can get a better estimate for $V_D$. 

$V_2-V_1=2.3V_Tlog(\frac{I_2}{I_1})$

Substituting all constants and rearanging for $V_2$, we get $V_2=0.738V$
This process can be repeated to get a more accurate value, but (though not shown)
the _second iterative process_ yields a voltage very close to the one above. 

### Constant Voltage Drop Model

![exponential-vs-constant-diode](https://www.physicsforums.com/attachments/diode-constant-voltage-drop-model-jpg.225896/)

The constant voltage drop model assumes that for forward conducting diodes
usually have a voltage drop in the narrow range, around 0.6 to 0.8




## Small Signal Model

Diodes can be bias to operate at a point in the forward I-V range and a small
AC signalis superimposed on the DC quantity. 
in essence, the diode acts as a variable resistor, where its resistance is
determined by its forward bias or "point of operation", ie where on its IV curve
is it "operating".

![small-signal-model](https://2.bp.blogspot.com/-bemFicfFoRw/UVz0kDkDuCI/AAAAAAAAAmk/LhyypCFTk6U/s1600/small+signal+diode2.bmp)

Assuming the "input signal" (ie AC Voltage signal) is sufficiently small, 
its _current_ operating range can be approximated to be linear. 
This relationship is given above, where 

- $v_d(t)$ represents the input AC signal voltage 
- $V_D$ represents the applied bias (to get the desired "resistance")
- $I_D$ is the DC component of the current (ie, the current drawn if a AC 
  source wasn't applied)
- $i_d(t)$ represents the output AC current (including $I_D$)

For reference purpose, the original diode IV equation is given by 

$I_D=I_Se^{\frac{V_D}{V_T}}$

superimposing the two voltages, we get 

$v_D(t)=V_D+v_d(t)$

given this, $v_d$ can be substituted into the diode-voltage-current equation
to give 

$i_D(t)=I_Se^{\frac{(V_D+v_d)}{V_T}}$

which can be expanded to 

$i_D(t)=I_Se^{\frac{V_D}{V_T}}e^{\frac{v_d}{V_T}}$

Referencing the original diode IV equation, the above equation can be simplified
to

$i_D(t)=I_De^{\frac{v_d}{V_T}}$

This **small-signal approximation** is valid for signals whose amplitudes
are smaller than around $5mV$, as this operates in the "exponential" region 
of a diodes forward-bias region. 

Using a **taylor-series expansion**, we can expand the equation to 

$i_D\approx I_D(1+\frac{v_d}{V_T})$

Given that This is the _superimposed_ currents, ie 

$i_D=I_D+i_d$

we finally get

$i_d=\frac{I_D}{V_T}v_d$





The quantity relating the _signal current_ $i_d$ to the signal voltage $v_d$
is called the **conductance**. The inverse (or reciprocal) of this symbol
is the **resistance**, given by $\Omega$

$r_d=\frac{V_T}{I_D}$

graphically, it can be interpreted that, because the input signal is
sufficiently small such that the change _along_ the diode IV curve is small
enough to approximate it to a linear relationship, similar to how a derivative
works (or literally how a derivative works lol)

given this information, it can also be stated that 

$r_d=\frac{1}{\frac{di_D}{dv_D}}$

some important points that can be inferred from above derivations are that

- the dc bias point is called the **quiescent point**
- small signal analysis can be performed seperately from the dc bias
  - ie, once the DC analysis is done, the small signal analysis can be done by 
    ignoring (shorting) all DC components and replacing the diode with an 
    equivalent resistance as calculated above 





## use of diode forward drop in voltage regulation

A voltage regulator is a circuit whose purpose is to provide a **constant 
DC voltage between its output terminals**

the output must remain constant despite 

- changes to the load current drawn from the regulator's output terminal
- changes in the DC power supply voltage that feeds the regulator circuit

using the property of dioes that 

- the voltage drop is almost constant at 0.7 volts
- but the current flowing through it varies


# Rectifier Circuits

## Half-Wave Rectifier

Given a realistic diode, when given an AC input voltage, the output voltage
can be given by

$v_o=0,v_s<V_D$
$v_o=v_s-V_D\,v_s>V_t$








