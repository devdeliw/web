+++
title = 'Complex Analysis Problems'
date = 2023-12-05T13:01:05-08:00
+++

Practice Problems on [Complex Analysis](https://dev-undergrad.dev/math121a/complex_analysis/) -- Contour Integration & Laurent Series 
<!--more--> 

### Contour Integration
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

$$ \oint_C \frac{ z }{ 1+z^2 } dz = 2\pi i \sum \text{Res} f(z) = 2\pi i \left( \frac{ 1 }{ 2 } + \frac{ 1 }{ 2 } \right) = 2\pi i  $$ 



 

 



 





