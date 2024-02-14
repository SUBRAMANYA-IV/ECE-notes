# Differential equations

The parameters of a differential equation tell us a lot about the behavior of 
the system. 

Given the general form of a differential equation, given by 

$\sum_{k=0}^Na_k\frac{d^k}{dt^k}y(t)=\sum_{k=0}^Mb_k\frac{d^k}{dt^k}x(t)$

where $x(t)$ is the input function, and $y(t)$ is the output function

by summarizing the entire history of the system prior to $t=0$, nothing
more needs to be known about the past to determine current and future output.

ie, if the initial conditions are zero, the system is at rest. 
if not, they represent the "energy" stored in the system due to past
inputs. 

An analytical approach or solving differential equations gives insights into
the relationship between coefficients {$b_0,...b_M,a_0...a_N$} and the system
response. We assume that the input is applied at time $t=0$

The **difference equation** is linear so the output can be written as a sum
of two terms, given by 

$y(t)=y_s(t)+y_t(t)$

where $y_s(t)$ represents the steady state response, or _what the function would
be if the input was applied "forever"_

and transient response $y_t(t)$, which represents _the transition from initial
conditions to steady state behavior_

##### Steady State Response $y_s(t)$

assume the input is a sum of complex exponential signals 

$x(t)=\sum_{i=0}^P\alpha_ie^{s_it}$

where $s_i$ is a complex number

However, we only need the output for an input of $x(t)=e^{st}$. The output is
$H(s)e^{st}$ where 

$H(s)=\frac{\sum_{k=0}^Mb_ks^k}{\sum_{k=0}^Na_ks^k}$

then, using linearity

$y_s(t)=\sum_{i=1}^P\alpha_iH(s_i)e^{s_it}$

$H(s)$ is called the transfer function of the system. 


