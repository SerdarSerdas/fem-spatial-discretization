# Spatial Discretization via Least-Squares Finite Elements

**Dr.-Ing. Serdar Serdas**

## Notation

| Symbol | Meaning |
|--------|---------|
| $\mathcal{B}, \mathcal{B}_0$ | Physical domain (current, reference configuration) |
| $\mathcal{B}^h, \mathcal{B}_0^h$ | Discretized domain (union of all finite elements) |
| $\mathcal{B}_e, \mathcal{B}_0^e$ | Physical domain of element $e$ (current, reference) |
| $\hat{\mathcal{B}}_e$ | Reference (isoparametric) element of element $e$ |
| $\partial\mathcal{B}$ | Boundary of domain $\mathcal{B}$ |
| $n_{\mathrm{elem}}$ | Number of finite elements in the mesh |
| $N$ or $n_{\mathrm{en}}$ | Number of element nodes (local degrees of freedom) |
| $N_I, N^I$ | Shape (interpolation) function associated with node $I$ |
| $\boldsymbol{\xi}$ | Natural / isoparametric coordinates, e.g. $(\xi,\eta,\zeta)$ |
| $\boldsymbol{X}, \boldsymbol{x}$ | Material (reference) and spatial (current) coordinates |
| $\boldsymbol{X}_I, \boldsymbol{x}_I$ | Nodal coordinates in reference and current configuration |
| $\boldsymbol{J}_e$ | Jacobian of mapping $\hat{\mathcal{B}}_e \rightarrow \mathcal{B}_0^e$ |
| $\boldsymbol{j}_e$ | Jacobian of mapping $\hat{\mathcal{B}}_e \rightarrow \mathcal{B}_e$ |
| $\boldsymbol{F}$ | Deformation gradient $\boldsymbol{F} = \partial\boldsymbol{x}/\partial\boldsymbol{X}$ |
| $\nabla_{\boldsymbol{\xi}}$ | Gradient w.r.t. natural coordinates $\boldsymbol{\xi}$ |
| $\nabla_{\boldsymbol{X}}, \nabla_{\boldsymbol{x}}$ | Gradients w.r.t. material and spatial coordinates |
| $\mathrm{Grad}, \mathrm{grad}$ | Material and spatial gradients of vector fields |
| $f$ | Generic scalar integrand on an element |
| $w_{GP}$ | Gauss quadrature weight associated with Gauss point $GP$ |
| $n_{\mathrm{GP}}$ | Number of Gauss points per element |
| $L^p(\mathcal{B})$ | Lebesgue space of $p$-integrable functions on $\mathcal{B}$ |
| $W^{k,p}(\mathcal{B})$ | Sobolev space of order $k$ with integrability exponent $p$ |
| $H^k(\mathcal{B})$ | Sobolev (Hilbert) space $W^{k,2}(\mathcal{B})$ |
| $P_r, Q_r$ | Lagrange elements of degree $r$ (triangular / 1D, quadrilateral) |
