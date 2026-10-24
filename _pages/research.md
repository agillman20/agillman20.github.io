---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<style>
  .research-gallery { display: flex; flex-wrap: wrap; gap: 1.5em; margin: 1em 0 1.5em; align-items: flex-start; }
  .research-gallery figure { margin: 0; flex: 1 1 280px; max-width: 100%; }
  .research-gallery figure.wide { flex-basis: 100%; }
  .research-gallery img { display: block; width: 100%; height: auto; border-radius: 0.25rem; box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12); }
  .research-gallery figure:not(.wide) img { max-width: 400px; }
  .research-gallery figcaption { font-size: 0.8em; margin-top: 0.5em; }
</style>

Boundary Integral Equation Solvers
======

Boundary integral equation formulations recast a partial differential equation as an equation posed only on the boundary of the domain. This reduces the dimension of the problem, handles unbounded domains naturally, and leads to well-conditioned linear systems. Our work develops fast direct solvers and high order discretizations for these equations, with applications to wave scattering, periodic and multilayered media, geometries with corners or local perturbations, and multiphase flows.

<div class="research-gallery">
  <figure class="wide">
    <img src="/images/gifs/vesicles.gif" alt="Animation of vesicles flowing through a periodic channel" loading="lazy">
    <figcaption>Vesicle suspension flowing through a periodic channel.</figcaption>
  </figure>
</div>

**Selected publications**

* [A direct solver with O(N) complexity for integral equations on one-dimensional domains](https://doi.org/10.1007/s11464-012-0188-3) (2012)
* [A fast direct solver for quasi-periodic scattering problems](https://doi.org/10.1016/j.jcp.2013.04.015) (2013)
* [A simplified technique for the efficient and highly accurate discretization of boundary integral equations in 2D on domains with corners](https://doi.org/10.1016/j.jcp.2013.08.049) (2014)
* [A high-order accurate accelerated direct solver for acoustic scattering from surfaces](https://doi.org/10.1007/s10543-014-0508-y) (2015)
* [A fast algorithm for simulating multiphase flows through periodic geometries of arbitrary shape](https://doi.org/10.1137/15m1043066) (2016)
* [High resolution inverse scattering in two dimensions using recursive linearization](https://doi.org/10.1137/16m1093562) (2017)
* [An integral equation technique for scattering problems with mixed boundary conditions](https://doi.org/10.1007/s10444-016-9488-6) (2017)
* [A fast direct solver for boundary value problems on locally perturbed geometries](https://doi.org/10.1016/j.jcp.2017.12.013) (2018)
* [A fast direct solver for two dimensional quasi-periodic multilayered media scattering problems](https://doi.org/10.1007/s10543-020-00818-z) (2021), [Part II](https://doi.org/10.48550/arXiv.2204.06629) (2022)
* [An alternative extended linear system for boundary value problems on locally perturbed geometries](https://doi.org/10.1016/j.jcp.2021.110182) (2021)
* [A fast direct solver for integral equations on locally refined boundary discretizations and its application to multiphase flow simulations](https://doi.org/10.1007/s10444-022-09974-y) (2022)
* [An efficient boundary integral equation solution technique for solving aperiodic scattering problems from two-dimensional, periodic boundaries](https://arxiv.org/abs/2511.04424) (2025)

Hierarchical Poincaré–Steklov (HPS) Method
======

The HPS method is a high order discretization technique for variable coefficient elliptic partial differential equations that comes with a fast direct solver. The domain is split into a hierarchy of boxes, each discretized with a spectral collocation method, and the boxes are glued together via Poincaré–Steklov (Dirichlet-to-Neumann type) operators. Our work includes adaptive and parallel versions of the method, solvers for highly oscillatory Helmholtz problems in variable media, and iterative solvers for three dimensional problems. Demo codes are available on [GitHub](https://github.com/agillman20/HPS_Demos).

<div class="research-gallery">
  <figure>
    <img src="/images/gifs/bumps.gif" alt="Animation of a wave scattering through a medium of random bumps" loading="lazy">
    <figcaption>Wave scattering through a variable medium.</figcaption>
  </figure>
  <figure>
    <img src="/images/gifs/lens.gif" alt="Animation of a wave scattering from a lens as the incident direction rotates" loading="lazy">
    <figcaption>Scattering from a lens as the direction of the incident wave rotates.</figcaption>
  </figure>
  <figure>
    <img src="/images/gifs/brain.gif" alt="Animation of an inverse scattering reconstruction converging to the true image" loading="lazy">
    <figcaption>High resolution inverse scattering: the reconstruction (left) converging to the true scatterer (right).</figcaption>
  </figure>
</div>

**Selected publications**

* [A direct solver with O(N) complexity for variable coefficient elliptic PDEs discretized via a high-order composite spectral collocation method](https://doi.org/10.1137/130918988) (2014)
* [An O(N) algorithm for constructing the solution operator to 2D elliptic boundary value problems in the absence of body loads](https://doi.org/10.1007/s10444-013-9326-z) (2014)
* [A spectrally accurate direct solution technique for frequency-domain scattering problems with variable media](https://doi.org/10.1007/s10543-014-0499-8) (2015)
* [An accelerated Poisson solver based on multidomain spectral discretization](https://doi.org/10.1007/s10543-018-0714-0) (2018)
* [An adaptive high order direct solution technique for elliptic boundary value problems](https://doi.org/10.1137/17m1156320) (2019)
* [A parallel shared-memory implementation of a high-order accurate solution technique for variable coefficient Helmholtz problems](https://doi.org/10.1016/j.camwa.2019.08.019) (2020)
* [An iterative solver for the HPS discretization applied to three dimensional Helmholtz problems](https://doi.org/10.1137/21m1463380) (2024)

Extensions to Other PDE Solver Communities
======

The ideas behind fast direct solvers, such as exploiting low rank structure and hierarchical decompositions, apply well beyond integral equations and spectral methods. We bring these techniques to other discretizations and application areas, including finite element and finite volume methods, difference equations on lattices, numerical homogenization, kinetic models and quantum systems. Our randomized linear algebra library, [librla](https://github.com/agillman20/librla), makes the underlying low rank techniques available in Python, MATLAB/Octave and Julia.

**Selected publications**

* [Fast and accurate numerical methods for solving elliptic difference equations defined on lattices](https://doi.org/10.1016/j.jcp.2010.07.024) (2010)
* [Numerical homogenization via approximation of the solution operator](https://doi.org/10.1007/978-3-642-21943-6_9) (2011)
* [A fast solver for Poisson problems on infinite regular lattices](https://doi.org/10.1016/j.cam.2013.09.003) (2014)
* [Study of discrete scattering operators for some linear kinetic models](https://doi.org/10.1007/978-1-4939-6399-7_5) (2016)
* Construction and profiling of a fast direct solver for distributed finite-element computations (2026)
* [Generating entangled steady states in multistable open quantum systems via initial state control](https://doi.org/10.1103/s8kc-crf3) (2026)
* [librla: A library of randomized linear algebra routines](https://doi.org/10.48550/arXiv.2607.20732) (2026)
