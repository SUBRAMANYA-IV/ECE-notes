# Convolution of Continuous time signals 

given an input and output relationship of 

$x(t)\rightarrow LTI\rightarrow y(t)$

for a continous time signal $x(t)$, it can be stated that

$\int_{-\infty}^{\infty}h(\tau)x(t-\tau)$

where $h(\tau)$ represents the impulse response of the signal. The same steps
used in the convolution of discrete time signals can be used to evaluate the
result of a continous time signal. 

1) reflect the function $x(\tau)$ along the $x$ axis
1) shift the function $x(\tau)$ $t$ units, treating $t$ as the "independent" 
   variable (represents the time at which the convolution is being evaluated)
3) multiply $x(t-\tau)$ with $h(\tau)$ and evaluate the signal over all values 
   that $\tau$ (usually taken from $-\infty$ to $\infty$)
