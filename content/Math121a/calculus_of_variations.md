+++
title = 'Calculus of Variations'
date = 2023-12-03T14:17:36-08:00
description = "Notes on Calculus of Variations -- §9 Boas"
+++

Notes on Calculus of Variations -- §9 Boas
<!--more-->

## Introduction
---

The goal of calculus of variations is akin to finding maximum and minimum
values of \\( f'(x) \\) in ordinary calculus. 

You find \\( f'(x) \\) and set it equal to 0. The values of \\(x\\) correspond to the
maximum, minimum, or points of inflection with a horizontal tangent. Finding \\(f'(x) = 0\\) therefore is necessary step, but not a sufficient condition in solving a problem where you specifically want the maximum or minimum. We have to then rely on the physics of the problem to filter out the rest of the points

We use the general term *stationary point* to mean simply that at \\(x\\), \\(f'(x)
= 0\\) there. 

In the calculus of variations, we state problems by saying that there exists
a certain quantity to be *minimized*. What we actually do is something similar
to putting \\(f'(x) = 0\\) -- we make the quantity itself stationary. Fortunately,
in many calculus of variations problems, "stationary" is all that is required
by Fermat's principle. 

### Calculus of Variations Integral

We wish to make an *integral* stationary: 
$$\boxed{ I = \int_{x_1}^{x_2} F(x, \\,y, \\,y')\\, dx \quad \left(\text{where } y' = \frac{dy}{dx} \right)} $$

---

#### Example 1: ***Geodesics*** 

Find the equation \\( y = y(x) \\) of a curve joining two points \\( (x_1, y_1) \\)
and \\( (x_2, y_2) \\) in the plane so that the distance between the points
measured along the curve is a minimum. We therefore want to minimize


$$I = \int_{x_1}^{x_2} \sqrt{dx^2 + dy^2}\\, dx. $$

which is equivalent to 

$$I = \int_{x_1}^{x_2} \sqrt{1 + y'^2}\\,  dx$$

In this scenario, \\( F(x, \\,y, \\,y') = \sqrt{1 + y'^2} \\)

If you go through the steps manually, by defining a theoretical curve \\( Y(x)
= y(x) + \epsilon \nu(x)\\) that makes 

$$I = \int_{x^1}^{x_2} \sqrt{ 1 + Y'^2} \\, dx$$ 

a minimum which ultimately means 

$$ \frac{dI}{dx} = 0 \quad \text{when } \epsilon = 0$$

you end up with an equation that applies to all calculus of variations
problems known as the

#### Euler-Lagrange Differential Equation

$$\boxed{ \frac{d}{dx} \frac{\partial F}{\partial y'} - \frac{\partial
F}{\partial y} = 0}$$ 

Using this equation with the Geodesic Example, we are to minimize 

$$\int_{x_1}^{x_2} \sqrt{1 + y'^2} \\, dx$$

so we have \\( F = \sqrt{1+y'^2} \\). Then 

$$\frac{\partial F}{\partial y'} = \frac{y'}{\sqrt{1+y'^2}} \quad
\frac{\partial F}{\partial y} = 0 $$ 


and the Euler-Lagrange equation gives 

$$ \frac{d}{dx} \left( \frac{y'}{\sqrt{1+y'^2}} \right)= 0 $$

which is a straight line. 
