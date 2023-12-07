+++
title = 'Fourier Series & Transform'
date = 2023-12-05T15:41:40-08:00
+++

Notes on Fourier Series & Transform -- §7. Boas

<!--more-->

### Fourier Series 
---

We will first start with functions that have a period of \\( 2\pi \\) 

I'm not gonna go into any derivations but the idea is that any curve and be
approximated as an infinite series of smaller sinusoidal curves.

##### \\( 2\pi \\) Period

\begin{align*} f(x) = \frac{ 1 }{ 2 } a_0 &+ a_1\cos(x) + a_2\cos(2x) + a_3 \cos(3x) + \cdots \\\ &+ b_1\sin(x) + b_2\sin(2x) + b_3\sin(3x) + \cdots \end{align*}

where the coefficients \\( a_n \\) and \\( b_n \\) 

$$ a_n = \frac{ 1 }{ \pi } \int_{ -\pi }^{ \pi } f(x) \cos(n x) \\, dx \qquad
b_n = \frac{ 1 }{ \pi } \int_{ -\pi }^{ \pi } f(x) \sin( nx ) \\, dx   $$ 

And since 

$$ \sin( nx ) = \frac{ e^{inx} - e^{-inx} }{ 2i }, \qquad \cos( nx ) = \frac{ e^{inx} + e^{-inx} }{ 2 }    $$

\\( f(x) \\) can also be defined as the following: 

$$ f(x) = c_0 + c_1e^{ ix } + c_{-1} e^{ -ix } + c_2e^{ 2ix } + c_{-2} e^{ -2ix } + \cdots + \sum_{n = -\infty}^{ \infty } c_n e^{ inx }        $$

where \\( c_n \\) 

$$ c_n = \frac{ 1 }{ 2\pi } \int_{ -\pi }^{ \pi } f(x) e^{ {-inx} } \\,  dx  $$

##### \\( 2l \\) Period

$$ f(x) = \frac{ 1 }{ 2 } a_0 + a_1 \cos\left( \frac{ \pi x }{ l }\right) + b_1 \sin\left( \frac{ \pi x}{ l }  \right)   + \cdots + \sum
\left( a_n \cos\left( \frac{ n\pi x }{ l }  \right) + b_n \sin\left( \frac{ n\pi x }{ l }  \right)      \right)   $$ 

$$ f(x) = \sum_{-\infty}^{ {\infty} } c_n e^{ -in\pi x / l }    $$

#### Parseval's Theorem for Fourier Series

Average of \\( |f(x)|^2 \\) (over a period) 

\begin{align*}
    \text{Average of } |f(x)|^2 \text{ (over a period) } &= \left( \frac{ 1 }{ 2 } a_0 \right) ^{ 2 } + \frac{ 1 }{ 2 } \sum_{1}^{ {\infty} } a_n^2 + \frac{ 1 }{ 2 } \sum_1^{ \infty } b_n^2 \\\ &= \sum_{-\infty}^{ \infty } |c_n|^2    
\end{align*}

### Fourier Transform 
--- 

\begin{align*}
    &f(x) = \int_{ -\infty }^{ \infty } g(\alpha) e^{ i\alpha x } \\, d\alpha \\\ &g(\alpha) = \frac{ 1 }{ 2\pi } \int_{ -\infty }^{ \infty } f(x) e^{ -i \alpha x } \\,  dx  
\end{align*}

With fourier transforms, \\( \alpha \\) is analogous to \\( n \\) with fourier series. \\( \alpha \\) is the **continuous** analog of \\( n, \\) as fourier series are with summations, but fourier transforms are with integrals. 

In the same sense, \\( g(\alpha) \\) is the same as \\( c_n \\) from the exponential form of a fourier series. \\( g(\alpha) \\) is a continuous function that has the same function as \\( c_n \\) at every point in space.

#### Parseval's Theorem for Fourier Transforms

$$ \int_{ -\infty }^{ \infty } |g(\alpha)|^2 \\,  d\alpha = \frac{ 1 }{ 2\pi } \int_{ -\infty }^{ \infty } |f(x)|^2\\, d\alpha $$ 

[Practice Problems on Fourier Series & Transforms](https://dev-undergrad.dev/math121a/fourier_series_transform_problems/)





 


 

 

 








