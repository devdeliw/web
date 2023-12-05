+++
title = 'Complex Analysis Problems'
date = 2023-12-05T13:01:05-08:00
+++

Practice Problems on [Complex Analysis](https://dev-undergrad.dev/math121a/complex_analysis/) -- Contour Integration & Laurent Series 
<!--more--> 

## Contour Integration
---

1. Let \\( C \\) be a contour defined by \\( |z| = 10 \\). Solve the following
   contour integral.

$$ \oint_C \frac{ 1 }{ 1+z^2 } \\, dz $$ 

Here, \\( f(z) = \frac{ 1 }{ 1+z^2 }  \\) and the poles of \\( f(z) \\) occur
at \\( z = \pm i \\). We calculate the residues at both poles: 

$$ \text{Res}\_{z\to i} f(z) = \lim\_{z\to i} (z-i) f(z) = \lim\_{z\to i}
(z-i)\frac{ 1 }{ (z+i)(z-i) }  = \frac{ 1 }{ 2i }  $$

$$ \text{Res}\_{z\to -i} f(z) = \lim\_{z\to -i} (z+i) f(z) = \lim\_{z\to -i} (z+i) \frac{ 1 }{ (z+i)(z-i) } = -\frac{ 1 }{ 2i }  $$

Implementing Residue Theorem, 

$$ \oint_C \frac{ 1 }{ 1+z^2 } \\,  dz = 2\pi i \cdot \left(\frac{ 1 }{ 2i } - \frac{ 1 }{ 2i } \right) = 0$$

Keep in mind, we only choose to calculate the residues and implement residue
theorem for **poles that are inside the contour**

2. Another example, with the same contour \\( C \\) defined by \\( |z| < 10 \\): 

  
$$ \oint_C  \frac{ z }{ 1 + z^2 } dz $$ 

The poles of this function are the same as last problems -- **both within the
contour**. We calculate the residues: 

$$ \text{Res}\_{z \to i} f(z) = \lim\_{z \to i} (z-i) \frac{ z }{ (z+i)(z-i) }  = \frac{ z }{ z+i } \Big|\_{z=i} = \frac{ i }{ 2i } = \frac{ 1 }{ 2 }  $$

$$ \text{Res}\_{z\to -i} f(z) = \lim\_{z\to -i} (z+i) \frac{ z }{ (z+i)(z-i) } = \frac{ z }{ z-i } \Big|\_{z=-i} = \frac{ -i }{ -2i } = \frac{ 1 }{ 2 }  $$

Therefore, implementing Residue Theorem, 

$$ \oint_C \frac{ z }{ 1+z^2 } dz = 2\pi i \sum \text{Res} f(z) = 2\pi i \left( \frac{ 1 }{ 2 } + \frac{ 1 }{ 2 } \right) = 2\pi i. $$ 


## Laurent Series 
---

Let us solve the Laurent Series for \\( f(z) = \frac{ 12 }{ z(2-z)(1+z) }  \\) for the other two regions: 

\begin{align*}
    &R_2 = {1 < |z| < 2} \\\
    &R_3 = { |z| > 2 }
\end{align*}

### \\( R_2 \\) 
---


As shown in the notes,

$$ f(z) = \frac{ 12 }{ z(2-z)(1+z) } = \frac{ 4}{ z } \left( \frac{ 1 }{ 1+z } + \frac{ 1 }{ 2-z }  \right). $$

For \\( R_2 = {1 < |z| < 2} \\), we need to find the series for \\( f(z) \\)
that converges \\( > 1 \\) and converges \\( < 2 \\). Using the formulas in the
notes, we know for a \\( |z| < \alpha \\) we expand in terms of \\( z^n \\), and
for a \\( |z| > \alpha \\) we expand in terms of \\( \left( \frac{ 1 }{ z }  \right)^n  \\). Therefore, we need to alter the forms for each term of \\( f(z) \\) respectively. 

Since the region has \\( |z| > 1 \\) , we convert \\( \frac{ 1 }{ 1+z }  \\)
into a form that converges for \\( |z| > 1 \\) -- in other words we put it so
we can get a taylor series in powers of \\( \left( \frac{ 1 }{ z }  \right)^n \\).

$$ \frac{ 1 }{ 1+z } = \frac{ 1 }{ z - (-1) } = \frac{ 1 }{ z } \frac{ 1 }{ 1- \left( -\frac{ 1 }{ z }  \right)} = \frac{ 1 }{ z } \sum \left( -\frac{ 1 }{ z }  \right)^n.   $$

Since the region also has \\( |z| < 2 \\) we convert \\( \frac{ 1 }{ 2-z }  \\) into a form that converges for \\( |z| < 2 \\) -- in other words we put it so we can get a taylor series in powers of \\( \left( z \right) ^n \\) 

$$ \frac{ 1 }{ 2-z } = \frac{ 1 }{ 2 } \frac{ 1 }{ 1 - \frac{ z }{ 2 }  } = \frac{ 1 }{ 2 } \sum \left( \frac{ z }{ 2 }  \right) ^n.  $$

We plug in both series into \\( f(z) = \frac{ 4 }{ z } \left( \frac{ 1 }{ 1+z } + \frac{ 1 }{ 2-z }  \right)  \\): 

$$ f(z) = \frac{ 4 }{ z } \left( \frac{ 1 }{ 1+z } + \frac{ 1 }{ 2-z }  \right) = \frac{ 4 }{ z } \left( \frac{ 1 }{ z } \sum \left( -\frac{ 1 }{ z }  \right) ^n  + \frac{ 1 }{ 2 } \sum \left( \frac{ z }{ 2 }  \right) ^n \right).$$

This is the laurent series for \\( f(z) \\) in the region \\( R_2 \\) where \\( 1 < |z| < 2 \\). 

### \\( R_3 \\) 
---

For \\( R_3 \\) where \\( |z| > 2 \\), we need to find the individual series
where both \\( |z| > 1 \\) and \\( |z| > 2 \\) . 

Therefore, 

$$ \frac{ 1 }{ 1+z } = \frac{ 1 }{ z - (-1) } = \frac{ 1 }{ z } \frac{ 1 }{ 1 - \left( \frac{ -1 }{ z }  \right)  } = \frac{ 1 }{ z } \sum \left( -\frac{ 1 }{ z }  \right) ^n.  $$

$$ \frac{ 1 }{ 2-z } = -\frac{ 1 }{ z } \frac{ 1 }{ -\frac{ 2 }{ z } + 1 } = -\frac{ 1 }{ z } \frac{ 1 }{ 1-\frac{ 2 }{ z }  } = -\frac{ 1 }{ z } \sum \left( \frac{ 2 }{ z }  \right) ^n.  $$ 

Plugging this back into \\( f(z) \\) yields

$$ f(z) = \frac{ 4 }{ z } \left( \frac{ 1 }{ 1+z } + \frac{ 1 }{ 2-z }  \right) = \frac{ 4 }{ z } \left( -\frac{ 1 }{ z } \sum \left( \frac{ 2 }{ z }  \right) ^n + \frac{ 1 }{ z } \sum \left( -\frac{ 1 }{ z }  \right) ^n \right).  $$

This is the laurent series for \\( f(z) \\) in the region \\( R_3 \\) where \\( |z| > 2 \\). 



 

 

 

 

 

 


 

 



 





