+++
title = 'Calculus of Variations'
date = 2023-12-03T14:17:36-08:00
description = "Notes on Calculus of Variations -- §9 Boas"
+++

### Introduction
---

The goal of calculus of variations is akin to finding maximum and minimum
values of $f(x)$ in ordinary calculus. 

You find $f'(x)$ and set it equal to 0. The values of $x$ correspond to the
maximum, minimum, or points of inflection with a horizontal tangent. Finding $f'(x) = 0$ therefore is necessary step, but not a sufficient condition in solving a problem where you specifically want the maximum or minimum. We have to then rely on the physics of the problem to filter out the rest of the points

We use the general term *stationary point* to mean simply that at $x$, $f'(x)
= 0$ there. 

In the calculus of variations, we state problems by saying that there exists
a certain quantity to be *minimized*. What we actually do is something similar
to putting $f'(x) = 0$ -- we make the quantity itself stationary. Fortunately,
in many calculus of variations problems, "stationary" is all that is required
by Fermat's principle. 

We wish to make an *integral* stationary: 
$$ I = \int_{x_1}^{x_2} F(x, y, y')\,dx \quad \left(\text{where } y'
= \frac{dy}{dx} \right) $$

