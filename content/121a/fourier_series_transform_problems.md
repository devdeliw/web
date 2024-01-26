+++
title = 'Fourier Series & Transform Problems'
date = 2023-12-05T17:21:00-08:00
+++

Practice Problems on [Fourier Series
& Transforms](https://dev-undergrad.dev/math121a/fourier_series_transform) / Calculating \\( g(\alpha) \\) 
<!--more-->

## Convention 

\begin{align*}
    & f(x) = \int_{ -\infty }^{ \infty } g(\alpha) e^{ i\alpha x } \\, d\alpha \\\ 
    & g(\alpha) = \frac{ 1 }{ 2\pi } \int_{ -\infty }^{ \infty } f(x) e^{-i\alpha x } \\, dx
\end{align*}



##### Problem 1
---

Calculate the fourier transform, \\( g(\alpha) \\) for 

$$ f(x) = \begin{cases} 1 &\quad 0 < x < 1 \\\ 0 &\quad \text{else} \end{cases} $$ 

\begin{align*}
    g(\alpha) &= \frac{ 1 }{ 2\pi } \int_{ -infty }^{ \infty } f(x) e^{ -i\alpha x } dx \\\
    &= \frac{ 1 }{ 2\pi } \int_{ 0 }^{ 1 } e^{ -i\alpha x } dx = \frac{ 1 }{ 2\pi } \left( -\frac{ e^{ -i\alpha x }    }{ i\alpha }  \right)_0^{ 1 }  = \frac{ 1 }{ 2\pi } \left( -\frac{ e^{ -i\alpha }   }{ i\alpha } + \frac{ 1 }{ i\alpha }  \right)   
\end{align*}

##### Problem 2
---

Calculate the inverse fourier transform, \\( f(x) \\) for 

$$ g(\alpha) = \pi e^{ -|\alpha| }   $$

Since \\( g(\alpha) = \pi e^{ -|\alpha| }   \\), that's the same thing as 


\begin{align*}
    g(\alpha) = \pi e^{ \alpha } &\qquad \alpha < 0 \\\
    g(\alpha) = \pi^{ -\alpha } &\qquad \alpha > 0 
\end{align*}

So we have two integrals to solve: 

$$ f(x) = \int_{ -\infty }^{ \infty } g(\alpha)e^{ i\alpha x } \\, d\alpha = \int_{ -\infty }^{ 0 } \pi e^{ \alpha } e^{ i\alpha x } \\,  d\alpha + \int_{ 0 }^{ \infty } \pi e^{ -\alpha } e^{ i\alpha x } \\,  d\alpha      $$

Let us first tackle the first integral, \\( \int_{ -\infty }^{ 0 }  \pi e^{ \alpha } e^{ i \alpha x } \\,  d\alpha  \\) 

$$ \int_{ -\infty }^{ 0 } \pi e^{ \alpha }    e^{ i\alpha x } \\,  d\alpha =    \pi\int_{ -\infty }^{ 0 } e^{ \alpha(1+ix) }\\, d\alpha = \pi\frac{ e^{ \alpha(1+ix) }   }{ 1+ix } \Big|_{-\infty}^{ 0 } = \frac{ \pi }{ 1 + ix }     $$

The second integral, 

$$ \int_{ 0 }^{ \infty } \pi e^{ -\alpha } e^{ i\alpha x } \\,  d\alpha = \pi \int_{ 0 }^{ \infty } e^{ \alpha(-1+ix) } \\,  d\alpha = \pi \frac{ e^{ \alpha(-1+ix) }   }{ -1+ix  } \Big|_0^{ \infty } = -\frac{ \pi }{ -1 + ix }      $$ 

Adding these solved integrals together, 

$$ f(x) = \pi \left( \frac{ 1 }{ 1+ix } - \frac{ 1 }{ ix - 1}  \right) = \pi \left( \frac{1 - ix + 1 + ix}{1-(ix)^{ 2 }} \right) = \frac{ 2\pi }{ 1+x^2 }   $$ 




 

 





 




 



