+++
image = "img/blog.jpeg"
showonlyimage = true
date = "2025-03-22T00:00:00+00:00"
title = "Singular statistical models"
draft = true
weight = 999
+++w

<!--more-->

singular : Fisher information is degenerate.
- relates to non-identification problems. $\theta \to p(x|\theta)$
- cause several problems in statistics and machine learning
- ex. Gaussian mixture model, Hidden markov model
- differential geometric (like dually flat manifold) cannot be directly applied. -->


### Legendre duality 

z = f'(x0) + f(x0) - f'(x0)   
p = f'(x)    
φ(p) = xp - f(x)

=> when f is convex, a point <-> a tangent line 

=> when f is non-convex in general, the relationship betweeen hypersurfaces (wavefronts)
- hypersurfaces admitting singularity is larger than wavefronts. (ex. Whitney umbrella)

### Legendre submanifold L
- Lf := {(x, x', f(x))} is an example of Legendre submanifold.
- generalization of the graph of functions (x,f(x)).
- regular modelの定義は, π1とπ'1の写像が両方とも準同型であること.

x <- Base space (x,z) <-π- (x,p,z) -π'-> (p,z') Fiber space -> p


### Coherent tangent bandles E, E'
- prior studies from mathematicians


### Dually flat structure of singular models
- $\nabla^E, \nabla^{E'}$


### Canonical divergence
- The canonical divergence on L is deifined by D_L(p,q) = z(p) + z'(q) - x(p)^T p(q)
    - if L is regular, it reduces to Bregman divergence.
- The generalized Pythagorean theorem on Legendre submanifolds also holds!
    - introduce e-curve and m-curve. The orthogonaliy is not defined via metrics but between affine structures. (reduces to metrics version on regular models.) -->