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

$$ R_1 = \\{ |z| < 1 \\} $$
$$ R_2 = \\{ 1 < |z| < 2 \\} $$ 
$$ R_3 = \\{ |z| > 2 \\} $$ 


 




  

 

 

 
 




 




