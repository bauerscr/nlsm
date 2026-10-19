# Digesting the O(3) NLSM construction

This is an "open math" community effort to create a beautiful version of the construction of the 2d NLSM with target $S^2$.

Author: the community

## Organization

- <del>Discord channel: https://discord.gg/bF8Hd2ahP</del>
- Zulip channel: https://probabilistic-qft.zulipchat.com/join/whlijwfr75fksr5gxezhynp5/
- Mailing list: nlsm@probabilistic-qft.org (not in place yet)
- Catchup meetings: Mondays 4pm Amsterdam time

## Papers

1. [Exponential decay in two-dimensional classical $O(n)$ models](https://github.com/openai/math/blob/main/preprints/Exponential-decay-in-two-dimensional-classical-On-models-September-23-2026/paper.pdf)
   - Establishes exponential decay for lattice model without estimate on $m(\beta)>0$.
   - Result is not used in the subsequent papers, but related idea implemented there in a stronger way.
   - Understable, Lean available
2. [O(4) mass bounds](https://github.com/openai/math/blob/main/preprints/Sharp-mass-bounds-for-the-two-dimensional-O4-model-September-23-2026/paper.pdf)
   - Establishes $m(\beta) \asymp \sqrt{\beta}e^{-\pi\beta}$.
   - Gets referred to and adapted a lot in the $O(3)$ papers.
   - No Lean
3. [O(4) exact mass asymptotics](https://github.com/openai/math/blob/main/preprints/Exact-mass-asymptotics-for-the-two-dimensional-O4-lattice-model-October-5-2026/exact-mass-o4.pdf)
   - Establishes $m(\beta) \sim C\sqrt{\beta}e^{-\pi\beta}$ as $\beta\to\infty$ with explicit constant.
   - No Lean
4. [O(3) massive continuum limit](https://github.com/openai/math/blob/main/preprints/The-canonical-massive-continuum-limit-of-the-two-dimensional-O3-model-October-4-2026/massive-continuum-o3.pdf)
   - Establishes continuum limit and all OS axioms.
   - No Lean
5. [O(3) isolated particle pole](https://github.com/openai/math/blob/main/preprints/An-Isolated-Particle-Pole-for-the-Two-Dimensional-O3-Spin-Field-October-4-2026/o3-particle-pole.pdf)
   - Establishes isolated particle pole and upper mass gap.
   - No Lean


## Most interesting ingredients of the construction

- **Mixing estimate:** obtained using noncommutative Mermin-Wagner idea, correlation inequalities, reflection positivity
- **Block spin transformation** with intrinsic rather than extrinsic coordinates: spins remain on the sphere and potential does not become a double well.
- **Large/small gradient decomposition** in the spirit of Gawedzki-Kupiainen and Balaban
- **Finite range fluctuation covariances** in the spirit of Brydges, but finite range condition seems to be implemented through explicit truncation rather than exact decomposition.
- **Nelson's 3/5 argument** is used to prove rotational invariance.

## General conventions and notation

- The complete analysis is on the unit lattice until the very end.
- Uses $L$-adic scales with distances $L^{-j}$. Scales are indexed by $j = N, \dots, 0$ with $N$ the UV scale and $0$ the unit scale.
- $\Lambda_j$ denotes the block lattice, i.e., $\Lambda_{j-1}$ are the centers of the $L$-blocks in $\Lambda_j$.
- Microscopic spins are denoted $q_x\in S^2$.
- Block spins are denoted by $V_{[x]} \in S^2$ where $[x]$ is (...).
- $N_R(P)$ denotes radius $R$ neighborhood of $P \subset \mathbb{Z}^2$.
- $H_j$ refers to the explicit solution of the second order truncation of the coupling constant recursion:
$$H_j = H+\gamma j.$$
- The true coupling constants are $b_j$ and definded in (3.29) and (6.1):
$$b_{j-1}=b_j+\alpha_{N-j}+\kappa_{N-j}/b_j + \Delta_j, \qquad \alpha \approx \frac{\log L}{2\pi}$$
- The symbol $h_j$ stands for history. It is the sequence of block spin transforms done up scale $j$. The Gaussian kinetic terms $K_h$ depend on the history $h$. They do not incorporate field strength renormalization. Initially $K_\varnothing=K_{h_N}=d^*d=-\Delta$.
- The renormalized density at scale $j$ with respect to the product measure is represented in the stable form (3.29):
$$Z_j(q) = e^{v_j|\Lambda_j| - b_j E_j(q)} \exp\Big[-\sum_\alpha (...)\Big] \Xi_j(q).$$
- Here $v_j$ is the vacuum energy, $b_j$ the running coupling constant and the
sum over $\alpha$ contains further irrelevant (in RG sense) but lower order terms.
This is a familiar polymer representation in RG.
I expect the lower order term compensate for the fact that rescaling of the
kinetic term is only accurate to lowest order.

## General terminology

- chord: Euclidean distance between spins.
- fallback: the second case of the piecewise definition of block spins 
- seed anchors:
- seeds:
- cores: union of seeds within radius $50M$ of each other
- halo:
- retained density: is this something like a polymer representation?
- inverse window $\Omega_x$: this seems to be the finite range of the Gaussian fluctuation field.
- ...

## Notes

These notes focus on the fouth paper on the $O(3)$ continuum limit. It uses the other ones.

### General remarks

- Part I seems to concern the continuum limit for sufficiently large renormalized coupling $H$.
  - The mixing estimate of Section 2 only gets used in Section 8.
  - The small scale RG flow is self-contained in Sections 3-7. Better organization would be to have this first.
- Part II seems to be the extension to all renormalized couplings $H$.
  - Not sure yet if this requires an interesting idea.
- It is **not** established that the limit is scale covariant (only depends on $H$ through rescaling).
- It is **not** established that the field strength $B_N$ diverges like $N^{1/3}$ as expected from RG.

### Mixing estimate (Section 2)

- This section establishes the local a priori mixing estimate. No RG is involved.
- It does not seem to get used until Section 8. It would make sense to move it to after Section 7.

### Gaussian block spins, polymers, norms (Section 3)

- This sections seems to set up a version of the polymer geometry and norms typical in RG.

#### Gaussian block spin transformations (Section 3.1-3.2)

- This section seems to do the linear block spin transformations in the Gaussian setting.
It should be elementary.
- Looks similar to Gawedezki--Kupiainen, see Section 2 of
***A Rigorous Block Spin Approach to Massless Lattice Theories***.

#### Large/small field decomposition (Section 3.3)

- The form of the polymer decomposition / effective densitities seems to be defined here.

### Estimates on Gaussian block spins (Section 4)

- The first display in Section 4.1 seems to embedded the rotated lattice in the original one,
preparting for Nelson's 3/5 argument for rotational invariance in Section 10.

### RG transformation (Section 5)

- This is where the actual RG transformation is implemented.
- Can one make the output of this section a "black box" theorem?

#### Introduction of the fluctuation field (Section 5.3)

- Intrinsic coordinates. Exact identity: ...
- $V_{[x]}$ seems to be the block spin field.

#### Fluctuation integration (Section 5.3)

- Fluctuation covariances have finite range $y \in \Omega_x$ with $\Omega_x  = E(P) \cap B_R(y)$ where $E(P)$ is the nonfrozen region.
- Thus no decoupling expansion (cluster expansion) is needed.
- Mayer expansion for exponentiating the small field action still present.

#### Large field estimates (Section 5.4)

- How does this compare to Balaban's R operation?
- How exactly is it done?

#### Extraction of marginal coupling constants (Section 5.5)

- Is there anything else going on in this section?

### TBC (Section 7)

### Tuning of the bare coupling constant (Section 6)

- Anything special compared to familiar RG constructions?


### Tilting estimate for rotational invariance (Section 8)

- I think this will be used in Nelson's 3/5 estimate to prove rotational invariance

### Local observables and correlation functions (Section 9)


## TODO

### Concrete exercises to work out

- Create a simple explicit version of the intrinsic-coordinates block spin transform (Lemma 5.2).
- Formulate polymer geometry is more standard framework.
- Can we formulate Section 5 as a "black box" theorem that takes an a configuration as defined
in Section 3 to another such configuration at the next scale?
-

### Questions to clarify

- How does the nonlinear block spin transform get connected to the Gaussian one?
- How precisely does the finite-range truncation of the fluctuation covariance get handled?
- 

