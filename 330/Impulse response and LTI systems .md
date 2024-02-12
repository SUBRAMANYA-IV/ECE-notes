Impulse Response
=================

* Example: An LTI system has an impulse response of $h[n]={\frac{1}{3}}^n u[n] $
Solution: write the input $x[n]=2\delta[n]-\delta[n-1]+\delta[n-3]$

1) time invariance: $\delta[n-k]\rightarrow h[n-k]$ 
2) 
   So, $\delta[n-1]\rightarrow {\frac{1}{3}}^n-1u[n-1]$ and $\delta[n-3]\rightarrow {\frac{1}{3}}^n-3u[n-3]$




BIBO and Stability
====================

* Example: A system has impulse response $h[n]=(-\frac{1}{2})^n u[n] $  

solution: for a system to be stable, or _bounded input bounded output_, it must
follow the statment


$\sum_{n=-\infty}^{\infty}|h[n]|<\infty$

For the example above, we get 

$\sum_{n=-\infty}^{\infty} (-\frac{1}{2})^n u[n]$  

The absolute value ignores the negative, and $u[n]$ term sets the limit from 
0 to $\infty $. This gives the expression 

$\sum_{n=0}^{\infty} (\frac{1}{2})^n$

which gives 

$\frac{1}{1-\frac{1}{2}}=2$


