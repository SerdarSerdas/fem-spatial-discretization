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



Spatial discretization of partial differential equations in mechanics can be carried out using various numerical frameworks, most prominently the finite difference method, the finite volume method, and the finite element method (FEM). Each of these approaches is based on a different discretization philosophy and exhibits distinct advantages and limitations when applied to problems in continuum mechanics and related fields.

The finite difference method, historically the earliest of the three, relies on structured grids and on the systematic use of Taylor-series expansions to approximate spatial derivatives. This inherently local construction is straightforward on regular meshes but tends to become cumbersome and less flexible when the underlying geometry involves complex shapes, curved boundaries, or highly heterogeneous domains. As a consequence, its applicability to multi-dimensional engineering problems with intricate geometrical features is often restricted.
