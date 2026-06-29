# From Minimality to Free Boundary Equations

This note is a short technical taster from Section 2 of the dissertation. It explains how the variational formulation of the Alt-Caffarelli problem leads to the PDE and free boundary conditions.

The starting point is the one-phase Alt-Caffarelli functional

$$J(v, \Omega) = \int_{\Omega} \left( |\nabla v|^2 + \chi_{{v > 0}} Q^2 \right).$$

A local minimizer is not assumed in advance to satisfy a classical PDE everywhere. Instead, the Euler-Lagrange conditions are extracted from the fact that small admissible perturbations cannot decrease the energy.

The goal is to justify, in progressively stronger senses, the formal conditions

$$u \geq 0, \qquad \Delta u = 0 \quad \text{in } \Omega \cap {u > 0}, \qquad |\nabla u| = Q \quad \text{weakly on } \Omega \cap \partial {u > 0}.$$

---

## Lemma 2.3: Subharmonicity of Local Minimizers

The first step is to show that a local minimizer is subharmonic. This is obtained by perturbing the minimizer downwards.

**Lemma 2.3.** If $u$ is a local minimizer, then $u$ is subharmonic, $\Delta u \geq 0$, in the sense of distributions, that is

$$\int_{\Omega} \nabla u \cdot \nabla \varphi \leq 0$$

for every $\varphi \in C_0^\infty(\Omega)$ such that $\varphi \geq 0$ on $\Omega$.

**Proof sketch.** Let $\varphi \in C_0^\infty(\Omega)$, with $\varphi \geq 0$, and consider the competitor

$$\tilde{u} = u - \varepsilon \varphi,$$

where $\varepsilon > 0$ is sufficiently small.

By local minimality,

$$J(u, \Omega) \leq J(u - \varepsilon \varphi, \Omega),$$

and hence

$$0 \leq J(u - \varepsilon \varphi, \Omega) - J(u, \Omega).$$

Expanding the Dirichlet energy gives

$$|\nabla(u - \varepsilon \varphi)|^2 - |\nabla u|^2 = -2\varepsilon \nabla u \cdot \nabla \varphi + \varepsilon^2 |\nabla \varphi|^2.$$

For the characteristic term, since $\varepsilon > 0$ and $\varphi \geq 0$, we have

$${u - \varepsilon \varphi > 0} = {u > \varepsilon \varphi} \subseteq {u > 0}.$$

Thus the change in the characteristic term is non-positive. Removing this non-positive contribution from the energy difference gives

$$0 \leq \int_{\Omega} \left(|\nabla(u - \varepsilon \varphi)|^2 - |\nabla u|^2\right).$$

Dividing by $2\varepsilon$ and taking the limit superior as $\varepsilon \to 0$, we obtain

$$0 \leq -\int_{\Omega} \nabla u \cdot \nabla \varphi.$$

Therefore,

$$\int_{\Omega} \nabla u \cdot \nabla \varphi \leq 0,$$

which proves that $u$ is subharmonic in the distributional sense.

---

## Theorem 2.12: Harmonicity on the Positivity Set

Lemma 2.3 gives one inequality. To obtain harmonicity, we restrict attention to the open positivity set ${u > 0}$, where small perturbations do not change the characteristic term.

**Theorem 2.12.** If $u$ is a local minimum, then $u$ is classically harmonic on the open set ${u > 0}$. Moreover, $u$ is smooth on ${u > 0}$.

Equivalently,

$$\Delta u = 0 \quad \text{in } \Omega \cap {u > 0}.$$

**Proof sketch.** By Lemma 2.3, $u$ is subharmonic on $\Omega$ in the distributional sense. Hence it remains to show that $u$ is superharmonic on the open set ${u > 0}$.

Let

$$\varphi \in C_0^\infty({u > 0}), \qquad \varphi \geq 0.$$

Consider the perturbation

$$\tilde{u} = u + \varepsilon \varphi,$$

where $\varepsilon < 0$ is sufficiently small.

Since the support of $\varphi$ is compactly contained in ${u > 0}$, the positivity set does not change under this perturbation for small $\varepsilon$. Thus the characteristic term contributes no first-order change.

By minimality,

$$0 \leq \limsup_{\varepsilon \to 0} \frac{1}{2\varepsilon} \left[J(u + \varepsilon \varphi, \Omega) - J(u, \Omega)\right] = \int_{\Omega} \nabla u \cdot \nabla \varphi.$$

Combining this with Lemma 2.3 gives

$$\int_{\Omega} \nabla u \cdot \nabla \varphi = 0$$

for every non-negative $\varphi \in C_0^\infty({u > 0})$.

Therefore, $u$ is weakly harmonic on ${u > 0}$. By Weyl's lemma, $u$ is classically harmonic and smooth on ${u > 0}$.

---

## Theorem 2.14: Weak Free Boundary Condition

The previous theorem explains the PDE inside the positivity set. The next question is what condition holds on the free boundary $\partial {u > 0}$.

Formally, the expected Bernoulli-type condition is

$$|\nabla u| = Q \quad \text{on } \Omega \cap \partial {u > 0}.$$

This condition is more delicate because the boundary itself depends on the unknown minimizer $u$. The dissertation therefore formulates it in a weak limiting sense.

**Theorem 2.14.** Let $u$ be a local minimum and suppose that $Q^2 \in W^{1,1}(\Omega)$. Then

$$\lim_{\varepsilon \to 0} \int_{\partial {u > \varepsilon}} \left(|\nabla u|^2 - Q^2\right) \eta \cdot \nu = 0$$

for every admissible vector field $\eta$, where $\nu$ is the unit normal to the level set $\partial {u > \varepsilon}$.

**Proof sketch.** Instead of perturbing the values of $u$, we perturb the domain.

Let $\eta \in C_0^\infty(\Omega, \mathbb{R}^n)$, and for sufficiently small $\varepsilon > 0$, define

$$\tau_\varepsilon(x) = x + \varepsilon \eta(x).$$

For small $\varepsilon$, this map is a diffeomorphism. Define $u_\varepsilon$ by transporting $u$ through $\tau_\varepsilon$:

$$u_\varepsilon(\tau_\varepsilon(x)) = u(x).$$

By local minimality,

$$0 \leq J(u_\varepsilon, \Omega) - J(u, \Omega).$$

After changing variables, the energy difference can be expressed over the positivity set ${u > 0}$. The relevant first-order expansions are

$$D\tau_\varepsilon = I + \varepsilon D\eta + o(\varepsilon),$$

$$[D\tau_\varepsilon]^{-1} = I - \varepsilon D\eta + o(\varepsilon),$$

and

$$\det D\tau_\varepsilon = 1 + \varepsilon \nabla \cdot \eta + o(\varepsilon).$$

Using these expansions, the first variation contains the term

$$\int_{{u > 0}} \left((|\nabla u|^2 + Q^2)\nabla \cdot \eta - 2\nabla u D\eta \nabla u + \nabla Q^2 \cdot \eta\right).$$

Since $u$ is harmonic on ${u > 0}$ by Theorem 2.12, the interior contribution can be rewritten as a boundary term over the level surfaces $\partial {u > \varepsilon}$.

On such level surfaces, one has

$$\nabla u = |\nabla u|\nu,$$

where $\nu$ is the unit normal vector to the level set.

Substituting this identity into the boundary expression yields

$$0 = \lim_{\varepsilon \to 0} \int_{\partial {u > \varepsilon}} \left(Q^2 - |\nabla u|^2\right)(\eta \cdot \nu).$$

Equivalently,

$$\lim_{\varepsilon \to 0} \int_{\partial {u > \varepsilon}} \left(|\nabla u|^2 - Q^2\right)\eta \cdot \nu = 0.$$

This is the weak form of the free boundary condition

$$|\nabla u| = Q \quad \text{on } \Omega \cap \partial {u > 0}.$$

---

## Summary

These three results form the first bridge between the variational formulation and the PDE/free-boundary formulation.

| Result       | Interpretation                                           |
| ------------ | -------------------------------------------------------- |
| Lemma 2.3    | Minimality implies subharmonicity                        |
| Theorem 2.12 | Local minimizers are harmonic inside the positivity set  |
| Theorem 2.14 | Domain variations yield the weak free boundary condition |

Together, they justify the formal Euler-Lagrange conditions

$$u \geq 0, \qquad \Delta u = 0 \quad \text{in } \Omega \cap {u > 0}, \qquad |\nabla u| = Q \quad \text{weakly on } \Omega \cap \partial {u > 0}.$$

These conditions are the starting point for the later analysis of blow-up limits, Weiss' monotonicity formula, dimension reduction, stability, and low-dimensional regularity.
