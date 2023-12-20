+++
title = 'Complex Analysis'
date = 2023-12-04T17:56:35-08:00
+++

Notes on Complex Analysis & Functions of Complex Variables -- §14. Boas
<!--more--> 

### Functions of a Complex Variable
--- 

Any complex function of \\( z \\) , \\( f(z) \\), can be written as \\( u(x,y) + iv(x,y) \\). 

The derivative of \\( f(z) \\) , 

$$ f'(z) = \frac{d f}{d z} = \lim_{\Delta z \to 0} \frac{ \Delta f }{ \Delta z }  $$.

where \\( \Delta f = f(z + \Delta z) - f(z) \\) and \\( \Delta z = \Delta
x + i \Delta y \\).  

A function is ***analytic*** in a region \\( C \\) if it has a continuous derivative at every point within \\( C \\) . We can verify whether functions are analytic using the following equations: 

#### Cauchy-Riemann Conditions 


$$ \boxed{\frac{\partial u}{\partial x}  = \frac{\partial v}{\partial y} , \quad \frac{\partial v}{\partial x} = -\frac{\partial u}{\partial y}} $$

The functions \\( u \\)  and \\( v \\) are also harmonic, in that they satisfy
***Laplace's Equation*** within C. 

$$ \nabla^2 u = 0 \quad \nabla^2 v = 0 $$ 



### Contour Integrals
---

If \\( C \\) is a simple curve with a continuously turning tangent except at
a finite # of points. If \\( f(z) \\) is analytic on and inside \\( C \\), then 

$$ \oint_\text{around \\( C \\)} f(z) dz = 0 \qquad \textbf{Cauchy's Theorem}  $$

The value of \\( f(z) \\) at \\( z = a \\) is also 

$$ f(a) = \frac{ 1 }{ 2\pi i  } \oint \frac{ f(a) }{ z-a } \\,dz $$

We can therefore calculate a contour integral for any function with the
following formula 

#### Residue Theorem 

$$ \oint_{\gamma} f(z) \\, dz = 2\pi i \cdot \sum \text{Res}_{z\to z_0} f(z) $$

where \\( \text{Res}_{z \to z_0} f(z) \\) is the ***Residue*** of \\( f \\) at
\\( z_0 \\).

This Residue is calculated a number of ways which I will
eventually go through, but the most useful method is with the following
formula:
 
$$ \text{Res}_{z\to z_0} f(z) = \lim (z-z_0)f(z) $$ 

as \\( z \to z_0 \\)  where \\( z_0 \\) is a unique pole / singularity of the function. 

#### Laurent Series 

let \\( C_1 \\) and \\( C_2 \\) be two circles centered at \\( z_0 \\). If \\( f(z) \\) is analytic in between them, 

$$ f(z) = a_0 + a_1(z-z_0) + a_2(z-z_0)^2 + ... + \frac{ b_1 }{ z-z_0 } + \frac{ b_2 }{ (z-z_0)^2 } + ...  $$

The \\( b_1 \\) term is equal to the residue of \\( f(z) \\) at \\( z_0 \\).
The coefficients \\( a_1 \\) and \\( b_1 \\) are equal to 

$$ a_1 = \frac{ 1 }{ 2\pi i }  \oint_C \frac{ f(z) }{ (z-z_0)^{n+1} } \\,  dz \qquad
b_n = \frac{ 1 }{ 2\pi i } \oint_C \frac{ f(z) }{ (z-z_0)^{-n+1}  }  \\, dz $$

##### Calculating Laurent Series 


**Example 1**

$$ f(z) = \frac{ 12 }{ z(2-z)(1+z) }  $$ 

There exist 3 singular points of this function: \\( z = 0 \\), \\( z = 2 \\),
\\( z = -1 \\). This means that there exist 2 circles who together make
3 different laurent series, each in the region

\begin{align*}
&R_1 = \\{ 0 < |z| < 1 \\} \\\
&R_2 = \\{ 1 < |z| < 2 \\} \\\
&R_3 = \\{ |z| > 2 \\} 
\end{align*}

Let us calculate the Laurent Series for \\( R_1  = \\{ 0 < |z| < 1 \\} \\)

We first have to alter \\( f(z) \\) into a form that we can do work with and
use known taylor series to our advantage. Implementing partial fractions, 

\begin{align*}
    f(z) &= \frac{ 12 }{ z(2-z)(1+z) } = \frac{ \alpha }{ z } \left(\frac{ 1 }{ 2-z } + \frac{ 1 }{ 1+z } \right) 
\end{align*}

Solving for \\( \alpha \\) yields \\( \alpha = 4 \\), so 

$$ \frac{ 12 }{ z(2-z)(1+z) } = \frac{ 4 }{ z } \left( \frac{ 1 }{ 1+z } + \frac{ 1 }{ 2-z } \right)$$

In \\( R_1 \\), \\( |z| < 2 \\) and \\( |z| < 1 \\). Thus we need to find two series
that converge where \\( |z| < 2 \\) and where \\( |z| < 1 \\). Adding them
together yields the Laurent Series for \\( f(z) \\) in \\( R_1 \\). 

For any series that we want to converge where \\( |z| < \alpha \\) for the
singularity \\( \alpha \\), we want to put the term that has a singularity at
\\( \alpha \\) in the following form to allow us to use basic taylor series: 

$$ \boxed{\frac{ 1 }{ z-\alpha } = -\frac{ 1 }{ \alpha } \frac{ 1 }{ 1 - \frac{ z }{ \alpha }  } = -\frac{ 1 }{ \alpha } \sum_n \left(\frac{ z }{ \alpha } \right)^n \qquad |z| < \alpha}  $$

Therefore, since \\( f(z) = \frac{ 4 }{ z }  \left( \frac{ 1 }{ 1+z } + \frac{ 1 }{ 2-z } \right) \\), solving for \\( |z| < 2 \\): 

$$ \frac{ 1 }{ 2-z } = \frac{ 1 }{ -z - (-2) } = -\frac{ 1 }{ -2 } \frac{ 1 }{ 1 - \frac{ -z }{ -2 }  } = \frac{ 1 }{ 2 } \frac{ 1 }{ 1 - \frac{ z }{ 2 }  }  = \frac{ 1 }{ 2 } \sum_n \left(\frac{ z }{ 2 } \right)^n $$ 

Doing the same for \\( |z| < 1 \\), 

$$ \frac{ 1 }{ 1 + z } = \frac{ 1 }{ z - (-1) } = \sum_n (-z)^n $$

And therefore, 

$$ f(z) = \frac{ 4 }{ z } \left( \frac{ 1 }{ 1+z } + \frac{ 1 }{ 2-z } \right) = \frac{ 4 }{ z } \left( \sum_n (-z)^n + \frac{ 1 }{ 2 } \sum_n \left(\frac{ z }{ 2 } \right)^n \right)  $$

This results in the following series: 

$$ f(z) = -3 + 9\frac{ z }{ 2 } - 15 \frac{ z^2 }{ 4 } + 33\frac{ z^3  }{ 8 } + ... + \frac{ 6 }{ z }  .$$ 
This is the laurent series for \\( f(z) \\) which is valid in the region \\( 0 < |z| < 1 \\). 

If we want to obtain Laurent Series in regions between \\( \alpha < |z| < \beta \\), we do a similar procedure. However for \\( |z| > \alpha \\) we have to put \\( f(z) \\) into a different form for it to converge and to allow us to use a taylor series in a similar way.

$$ \boxed{ \frac{ 1 }{ z - \alpha }  = \frac{ 1 }{ z } \frac{ 1 }{ 1 - \frac{ \alpha }{ z }  } = \frac{ 1 }{ z } \sum_n \left(\frac{ \alpha }{ z } \right)^n \qquad |z| > \alpha } $$ 

We then do the same, determine which separate series we need to calculate and add them together. 

For example if we are tasked to find the laurent series of \\( f(z) \\) that is valid in the range \\( 1 < |z| < 2 \\), we have to find the series from the term with the pole of 1 using the formula for \\( |z| > 1 \\). Then find the series from the term with the pole of 2 using the formula for \\( |z| < 2 \\), then substitute their series in to \\( f(z) \\) to get the final laurent series.

#### Laurent Series Procedure

1. Partial Fractions
2. Determine range of Laurent Series
3. Implement Taylor Series Formulae for each range 
4. Add resulting Series into the original \\( f(z) \\) 


[Complex Analysis Problems -- Contour Integration & Laurent
Series](https://dev-undergrad.dev/math121a/complex_analysis_problems/)

 











 




  

 

 

 
 




 




