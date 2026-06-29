# Free Boundary Problem

**2025 Cambridge Mathematics Master's dissertation overview on the Alt-Caffarelli one-phase free boundary problem, low-dimensional regularity, and stability methods.**

This repository provides a concise public-facing overview of my dissertation on the **Alt-Caffarelli one-phase free boundary problem**. The full dissertation was written in LaTeX and spans 45 pages. This repository is intended as a readable research summary rather than a complete reproduction of the dissertation.

## Overview

The dissertation studies the one-phase free boundary problem associated with the **Alt-Caffarelli functional**

$$J(v, \Omega) = \int_{\Omega} \left( |\nabla v|^2 + \chi_{{v > 0}} Q^2 \right).$$

Minimizers formally satisfy the Euler-Lagrange conditions

$$u \geq 0, \qquad \Delta u = 0 \quad \text{in } \Omega \cap {u > 0}, \qquad |\nabla u| = Q \quad \text{weakly on } \Omega \cap \partial {u > 0}.$$

The boundary condition is imposed on a set determined by the solution itself. This gives rise to a **free boundary problem**.

The main focus of the dissertation is the classification of global minimizers in low dimensions and its connection to the regularity of their free boundaries.

## Main Result Studied

The dissertation works towards the following regularity theorem.

> In dimensions $n \leq 4$, the free boundary of global minimizers to the Alt-Caffarelli functional is locally a $C^{1,\alpha}$-hypersurface. If $Q$ is smooth, then the free boundary is a smooth hypersurface.

This result is connected to the classification of homogeneous global minimizers and the analysis of possible singular free boundaries.

The higher-dimensional classification problem remains open. In particular, the critical dimension $k^*$ is known to satisfy

$$k^* \in {5, 6, 7}.$$

## Mathematical Context

Free boundary problems arise when the domain on which a PDE is solved is itself unknown and must be determined as part of the solution.

In this problem, the positivity set

$${u > 0}$$

is not fixed in advance. Its boundary,

$$\partial {u > 0},$$

is the **free boundary**.

The central regularity question is whether this free boundary is smooth, singular, or somewhere in between.

This dissertation sits at the intersection of:

* Calculus of variations
* Elliptic partial differential equations
* Geometric measure theory
* Free boundary regularity
* Blow-up analysis
* Stability methods
* Minimal surface theory analogues

## Dissertation Structure

The dissertation follows a roughly chronological development of the theory.

| Section    | Content                                                                           |
| ---------- | --------------------------------------------------------------------------------- |
| Section 1  | Problem setup and existence of minimizers                                         |
| Section 2  | Local minima and Euler-Lagrange conditions                                        |
| Section 3  | Blow-up sequences and blow-up limits                                              |
| Section 4  | Weiss' monotonicity formula and dimension reduction                               |
| Section 5  | Stability and the Caffarelli-Jerison-Kenig inequality                             |
| Section 6  | Jerison-Savin instability criterion and low-dimensional regularity                |
| Final part | Reformulation of the subsolution construction approach as an optimization problem |

## Key Ideas

### 1. Variational Formulation

The problem begins with the minimization of the functional

$$J(v, \Omega) = \int_{\Omega} \left( |\nabla v|^2 + \chi_{{v > 0}} Q^2 \right).$$

The Dirichlet energy term $|\nabla v|^2$ penalizes oscillation, while the characteristic term $\chi_{{v > 0}} Q^2$ penalizes the size of the positivity set.

The competition between these two terms allows minimizers to develop regions where they vanish identically. The boundary of such a region is not prescribed in advance, which is why the problem has a free boundary.

### 2. Existence and Local Minima

The dissertation begins by reviewing the variational setup introduced by Alt and Caffarelli.

Using Hilbert's direct method, together with compactness and coercivity tools such as the Rellich-Kondrachov compactness theorem and generalized Poincare-type inequalities, one obtains the existence of minimizers.

The next step is to study local minimizers and derive the Euler-Lagrange conditions they satisfy. These conditions include harmonicity in the positivity set and a Bernoulli-type condition on the free boundary.

### 3. Lipschitz Continuity and Non-Degeneracy

A major early part of the theory is to extract regularity information from the minimality of the functional.

Two important properties are:

* **Lipschitz continuity**, which gives upper control on how quickly a minimizer can grow
* **Non-degeneracy**, which prevents a minimizer from vanishing too slowly near the free boundary

Together, these properties provide the compactness and growth control needed for blow-up analysis.

### 4. Blow-Up Analysis

To understand the local structure of the free boundary near a point $x_0$, one studies rescaled functions of the form

$$u_r(x) = \frac{u(x_0 + rx)}{r}.$$

As $r \to 0$, subsequential limits of $u_r$ are called **blow-up limits**.

These blow-up limits capture the infinitesimal geometry of the free boundary near $x_0$. Classifying possible blow-up limits is therefore central to understanding the regularity of the free boundary itself.

### 5. Weiss' Monotonicity Formula

Weiss' monotonicity formula is used to show that blow-up limits are homogeneous of degree one.

That is, a blow-up limit $u_0$ satisfies

$$u_0(\lambda x) = \lambda u_0(x) \qquad \text{for all } \lambda > 0.$$

This reduces the local regularity problem to the classification of homogeneous global minimizers.

### 6. Dimension Reduction

The dissertation introduces the critical dimension $k^*$, which is the lowest dimension in which singular minimizing cones may exist.

Weiss' dimension reduction technique shows why low-dimensional classification results are powerful. If singular minimizers cannot occur in low dimensions, then the free boundary must be regular in those dimensions.

The classification in dimensions $n \leq 4$ implies regularity of the free boundary in those dimensions.

### 7. Stability and Instability

A key part of the dissertation studies stability of homogeneous degree-one solutions for the modified Weiss problem.

The Caffarelli-Jerison-Kenig integral inequality provides a stability condition. The Jerison-Savin approach then gives an instability criterion through the construction of appropriate subsolutions.

This framework is used to analyze the relevant homogeneous solutions in dimensions

$$n = 3 \qquad \text{and} \qquad n = 4.$$

The resulting lower bound on the critical dimension is

$$k^* \geq 5.$$

### 8. Optimization Reformulation

The final part of the dissertation reformulates the subsolution construction approach as an optimization problem.

This perspective provides a different way to view the instability argument and connects the analytic construction of subsolutions with an optimization-based formulation.

## Main Techniques

The dissertation reviews and reconstructs the following mathematical tools.

| Technique                         | Purpose                                                        |
| --------------------------------- | -------------------------------------------------------------- |
| Hilbert's direct method           | Proves existence of minimizers                                 |
| Rellich-Kondrachov compactness    | Provides compactness for minimizing sequences                  |
| Generalized Poincare inequalities | Supports coercivity and compactness arguments                  |
| Euler-Lagrange analysis           | Derives PDE and free boundary conditions                       |
| Lipschitz estimates               | Controls growth of minimizers                                  |
| Non-degeneracy estimates          | Prevents excessive flattening near the free boundary           |
| Blow-up analysis                  | Studies local free boundary geometry                           |
| Weiss' monotonicity formula       | Establishes homogeneity of blow-up limits                      |
| Dimension reduction               | Relates singularities to lower-dimensional cones               |
| Stability inequalities            | Characterizes stability of homogeneous solutions               |
| Subsolution construction          | Proves instability in selected dimensions                      |
| Optimization reformulation        | Recasts part of the instability argument in optimization terms |

## Main References

The dissertation draws on foundational work in the theory of free boundary problems, including:

| Authors                          | Contribution                                                  |
| -------------------------------- | ------------------------------------------------------------- |
| Alt and Caffarelli               | One-phase free boundary framework                             |
| Alt, Caffarelli, and Friedman    | Two-phase free boundary theory and applications               |
| Aguilera, Caffarelli, and Spruck | Variational formulations in heat conduction problems          |
| Weiss                            | Monotonicity formula and dimension reduction methods          |
| Caffarelli, Jerison, and Kenig   | Stability inequalities for free boundary problems             |
| Jerison and Savin                | Instability criterion and low-dimensional regularity analysis |
| De Silva and Jerison             | Singular energy-minimizing free boundaries                    |

## Skills Demonstrated

This dissertation demonstrates experience with:

* Advanced mathematical exposition
* Variational methods
* Elliptic PDE theory
* Free boundary regularity
* Blow-up and compactness arguments
* Stability analysis
* Reading and synthesizing research papers
* Technical writing in LaTeX
* Reformulating mathematical arguments from an optimization perspective

## Note

This repository is intended for academic and professional reference. It provides a concise overview of the dissertation's mathematical content without reproducing the full document.
