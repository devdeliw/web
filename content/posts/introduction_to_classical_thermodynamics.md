+++
title = 'Classical Thermodynamics -- 01'
date = 2024-01-17T10:06:30-08:00
draft = false
+++

Note 1 -- Classical Thermodynamics, Chien-I Chiang
<!--more-->

### 1 Microstates and Macrostates

In nature we are often interested in systems that contain a large number of
**degrees of freedom**. For example, in a balloon there is an astronomical
number of air molecules. In these cases it is impossible to trace the motion of
each individual particle. Instead, we are often interested in the physical
quantities that describe the *collective* behavior of systems of many
particles, such as **volume, pressure,** etc. 

With that said, we know that the macroscopic properties of a system can often
be understood by the behavior of its microscopic constituents. The different
possible microscopic configurations of a macroscopic system that yield the same
macroscopic properties of the system are called **microstates** of the system. 

The goals of classical thermodynamics and statistical mechanics are to study
the relations between different macroscopic quantities and how to extract
information about macroscopic properties from the possible microscopic
configurations. 

### 2 Temperature and the Zeroth Law of Thermodynamics

To begin with, let us first describe the notion of **thermal equilibrium**.
When two systems of large degrees of freedom are brought together, we say they
are in _thermal contact_ if energy can be exchanged between two systems. This
energy can be transferred with intimate mechanical contact or via radiations
when they are separated by an empty space. 

When thermal equilibrium is reached, even though energy is still allowed to
transfer, the __probability of the two systems being in any given microstate
becomes time-independent__. Because the probability distribution of the
microstates is constant after equilibrium is reached, so are the macrostates of
the two systems. 

![test](/test.png)

With the notion of thermal equilibrium, the **zeroth law of thermodynamics**
states: 

_if system A and B are separately in thermal equilibrium with a third system C,
then A and B are also in thermal equilibrium with each other_

From the zeroth law of thermodynamics we see that being in thermal equilibrium
with a third reference system defines a state of the system. __Temperature__ is
then a __state variable__ that describes such a state. That is, _two systems
are in thermal equilibrium if they have the same temperature._ Note that temperature is a variable that is only relevant for systems with large degrees of freedom. It’s meaningless to talk about the temperature of a baseball if our concern is about its overall motion. In that case, there are only three degrees of freedom (it can move in three directions) and we can describe its motion precisely. However, if we are considering the matter molecules that make up the baseball, we then have a collection of particles with astronomical degrees of freedom, and we can talk about its temperature.

### 3 Thermal Expansion of Solids and Fluids

Roughly speaking, as temperature increases, the constituent particles move with
faster thermal speed and thus move further away from their average position.
This means that each particle requires larger space around and thus cause
thermal expansion. 

Suppose at a temperature _T_ the dimension of concern (such as the length of
a gold bar, the circumference of a disk, etc.) has a length _L_. Because each
part of the object expands proportionally due to thermal expansion, the longer
the dimension _L_, the longer the change \\( dL \\). As such it is physically
reasonable to write the changing rate of \\( L \\) under varying temperature as 

$$ \frac{ dL }{ dT } = \alpha(T) L $$ 

where \\( \alpha(T) \\) is called the __coefficient of thermal expansion__ at
temperature \\( T \\) . The above relation basically gives the definition of \\( \alpha(T) \\) . 

![01](/01.png)

If the temperature variation \\( \Delta T \\) isn't too large, we can then
approximate the coefficient \\( \alpha \\) to be a constant, and the change in
linear dimension \\( \Delta L \\) is then given by 

$$ \Delta L \simeq \alpha L \Delta T $$ 

For larger variations in temperature such that the temperature-dependence of \\( \alpha(T) \\) cannot be ignored, we solve the differential equation 

$$ \int_{ L_i }^{ L_f } \frac{ 1 }{ L } \\,  dL = \int_{ T_i }^{ T_f
} \alpha(T) \\,  dT  $$ 

##### Example

The coefficient of area expansion, denoted as \\( \alpha_A \\) is defined as 

$$ \alpha_A = \frac{ 1 }{ A } \frac{d A}{d T} $$ 

Consider a rectangular tile of dimensions \\( L_x \\) and \\( L_y \\) made by
material of linear expansion coefficient \\( \alpha \\) . Show that when the
expansion is small compared with the original dimension, the two expansion
coefficient are related by 

$$ \alpha_A = 2\alpha $$ 

##### Solution 

Both linear dimensions \\( L_x \\) and \\( L_y \\) expand according to the
above equations. Thus the expanded area of the tile is 

\begin{align*}
    A + dA &= (L_x + \alpha L_x dT)(L_y + \alpha L_y dT) \\\
           &= L_xL_y + 2\alpha(L_x L_y)dT + (L_xL_y)(\alpha dT)^{ 2 }  \\\
           & \simeq A + 2\alpha A dT
\end{align*}

We therefore get 

$$ dA = 2\alpha A dT $$ 

which gives

$$ \alpha_A = \frac{ 1 }{ A } \frac{d A}{d T}= 2\alpha $$ 


