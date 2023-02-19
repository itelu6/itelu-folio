---
layout: distill
title: 🚧 mathematical methods for physics and engineering (outline)
description: the outline for teaching mathematical methods for physics and engineering 
#img: https://cdn.pixabay.com/photo/2015/03/21/11/41/school-683550_1280.jpg
importance: 1
category: bud

authors:
  - name: I-Te Lu
    affiliations:
       name: MPSD, Germany


bibliography: books.bib

toc:
  - name: Series solutions of ordinary differential equations
    subsections: 
       - name: outline
       - name: selected exercises 
  - name: Sturm-Liouville form for differential equations
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
    subsections:
       - name: outline
       - name: selected exercises


---

<!-- assets/img/3.jpg -->

## Introduction 

Here we will mainly focus on the book: "Mathematical Methods for Physics and Engineering: A Comprehensive Guide" <d-cite key="riley2006mathematical"></d-cite>.

## Series solutions of ordinary differential equations

Here we look at how to find the homogeneous solutions for the 2nd order differential equation using the series expansion method for the linear independent solutions. 

* **What and why to learn**: to find the solutions for the 2nd order differential equations, which occurs very often in physics and engineering.

* **Analytical regime for the solutions? what are ordinary points and singular points [regular or irregular (essential)]?**

* **How should we find the solution at the regular singular points?** Frobenius series and the indicial equation. For the latter one, there are three senarios: differ by an non-integer, repeated, differ by an integer

* **How should we find the second solution?** The Wronskian method and The derivative method.

* **When does the series terminate?** polynominal solutions. This is very useful, especially, in quantum mechanics. 

### outline 

### selected exercises
Please use the RHB book <d-cite key="riley2006mathematical"></d-cite> and solve the following exercises in Chapter 16: 16.01, 16.03, 16.04, 16.05, 16.07, 16.08, 16.09, 16.12, 16.13, 16.15


## Sturm-Liouville form for differential equations

Here we look into a special form, so-called Sturm-Liouville (SL) form,  of the 2nd order differential equation (ODE): 
$$
p(x)\frac{d^{2}y}{dx^{2}} + r(x)\frac{dy}{dx} + q(x)y + \lambda\rho(x)y = 0,
$$
into which several well-known differential equations, such as Chebyshev, Legendre, Laguerre, or Hermite equations can be transformed.

Once we know how to solve the eigenvalue problem of the SL form imposed on the appropriate boundary conditions, then all the situations that statify the same boundary condition can be obtained from the superposition of the eigenfunctions. 


### outline 

* **What and why to learn**: to find the eigen functions to build up the solution of an ODE (with the weight functions)

* **Prepare some tools**: 1) Hilbert space with a set of infinite-dimensional functions, equipped with the inner product and the norm, 2) build up a function using the basis, and 3) Orthonormalize a basis, and 6) a few useful properties: Schwarz inequality, triangle inequality, and Bessel's inequality

* **What is a hermitian operator?** Adjoint, self-adjoint, and Hermitian operator; to prove a few statements for a Hermitian operator: 1) the real the eigenvalues; 2) the orthogonality and normalization of the eigenfunctions; 3) the completeness of the eigenfunctions; 4) the construction of real eigenfunctions (superposition)

* **What is the Sturm-Liouville (SL) equation?** 1) SL linear operator form; 2) SL operator is self-adjoint and Hermitian;

* **What is so special about SL form?** Transform other OEDs to the SL form and find the natural interval where $$p(x)$$ vanishes. Here are some examples: Legendre, associated Legendre, Chebyshe, Bessel, Laguerre, associated Laguerre, Hermite, Hypergeometric OED.

* **A powerful tool for solving OED**: Green's function, whose advantage is to include the boundary conditions from the start to build any f(x) that satisfies the boundary condition 

* **Final remark**: a useful generalization to include a constant shift (here we need an example) 


### selected exercises

Please use the RHB book <d-cite key="riley2006mathematical"></d-cite> and solve the following exercises in Chapter 17: 17.02, 17.03, 17.04, 17.05, 17.07, 17.09, 17.10, 17.11, 17.14, 17.15. 

