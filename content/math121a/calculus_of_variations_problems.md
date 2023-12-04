+++
title = 'Calculus of Variations Problems'
date = 2023-12-04T14:07:38-08:00
+++

Problems with [Calculus of Variations](https://dev-undergrad.dev/math121a/calculus_of_variations) / Euler-Lagrange Differential Equations §9. Boas
<!--more-->

Make the following integrals ***stationary:***

### Problem 1
---

$$ \int_{x_1}^{x_2} \sqrt{x}\sqrt{1-y'^2} \\, dx. $$

In this problem, \\( F(x, \\, y, \\, y') = \sqrt{x}\sqrt{1 + y'^2} \\).
Therefore, 

$$ \frac{d }{d x} \frac{\partial F}{\partial y'} = 0, \qquad \frac{\partial F}{\partial y'} = \sqrt{x} \left(\frac{y'}{\sqrt{1+y'^2}} \right). $$ 

And so, 

$$ \frac{d }{d x} \left( \sqrt{x} \frac{y'}{\sqrt{1 + y'^2}} \right)
= 0  \Longrightarrow \sqrt{x}\frac{y'}{\sqrt{1+y'^2}} = c_1. $$

Rearranging and solving the differential equation yields: 

\begin{align*}
 y' &= \sqrt{\frac{-c_1}{c_1 - x} } \\\ 
\int dy &= \int \sqrt{\frac{-c_1}{c_1 - x} } \\,dx \\\
y &= 2\sqrt{c_1}\sqrt{x-c_1} + c_2 
\end{align*}

Simplying further we end up with the correct result, 

$$ \boxed{(y-c_2)^2 = 4c_1(x-c_1)} $$

 





 

 


 

 






