# Digesting the O(3) NLSM construction

This is an "open math" community effort to create a beautiful version of the construction of the 2d NLSM with target $S^2$.

Author: the community

## Organization

- Discord channel: https://discord.gg/bF8Hd2ahP
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


## Most interesting ingredients of the contruction

- **Mixing estimate:** obtained using noncommutative Mermin-Wagner idea, correlation inequalities, reflection positivity
- **Block spin transformation** with intrinsic rather than extrinsic coordinates: spins remain on the sphere and potential does not become a double well.
- **Large/small gradient decomposition** in the spirit of Gawedzki-Kupiainen and Balaban
- **Finite range fluctuation covariances** in the spirit of Brydges, but finite range condition seems to be implemented through explicit truncation rather than exact decomposition.
- **Nelson's 3/5 argument** is used to prove rotational invariance.

## General conventions and notation

- The complete analysis is on the unit lattice until the very end.
- Microscopic spins are denoted $q_x\in S^2$.
- $N_R(P)$ denotes radius $R$ neighborhood of $P \subset \mathbb{Z}^2$.
- Uses $L$-adic scales with distances $L^{-j}$. Scales are indexed by $j = N, \dots, 0$ with $N$ the UV scale and $0$ the unit scale.
- $H_j$ refers to the explicit solution of the second order truncation of the coupling constant recursion:
$$H_j = H+\gamma j.$$
- The true coupling constants are $b_j$ and definded in (6.1):
$$b_{j-1}=b_j+\alpha_{N-j}+\kappa_{N-j}/b_j + \Delta_j, \qquad \alpha \approx \frac{\log L}{2\pi}$$
- The symbol $h$ seems to stand for history. It seems to be something like the data along an RG flow.
Thus $h_j$ contains in particular the information $(b_{N-1}, \dots, b_j)$ so has length $N-j$. How precisely is it defined?
- Gaussian kinetic terms $K_h$ depend on the history $h$. They incorporate the infinite field strength renormalization. Initially $K_\varnothing=K_{h_N}=d^*d=-\Delta$ is the Laplacian and $K_{h_j}$
should look approximately like $-Z_j \Delta$ with $Z_j$ the field strength?

## General terminology

- seed anchors:
- seeds:
- cores: union of seeds within radius $50M$ of each other
- halo:
- retained density: is this something like a polymer representation?
- inverse window $\Omega_x$: this seems to be the finite range of the Gaussian fluctuation field.
- ...

## TODO

### Concrete exercises to work out

- Create a simple explicit version of the intrinsic-coordinates block spin transform (Lemma 5.2).
- Formulate polymer geometry is more standard framework.
- 

### Questions to clarify

- How does the nonlinear block spin transform get connected to the Gaussian one?
- How precisely does the finite-range truncation of the fluctuation covariance get handled?
- Is Section 7 the first time that the mixing estimate from Section 2 gets used?

## Notes

These notes focus on the fouth paper on the $O(3)$ continuum limit. It uses the other ones.

### General remarks

- Part I seems to concern the continuum limit for sufficiently large renormalized coupling $H$.
- Part II seems to be the extension to all renormalized couplings $H$.
- It is **not** established that the limit is scale covariant (only depends on $H$ through rescaling).
- It is **not** established that the field strength $B_N$ diverges like $N^{1/3}$ as expected from RG.

### Mixing estimate (Section 2)

- This section establishes the local a priori mixing estimate. No RG is involved.

### Gaussian block spins, polymers, norms (Section 3)

- This sections seems to set up a version of the polymer geometry and norms typical in RG.

#### Gaussian block spin transformations (Section 3.1-3.2)

- This section seems to do the linear block spin transformations in the Gaussian setting.
It should be elementary.
- Looks similar to Gawedezki--Kupiainen, see Section 2 of
***A Rigorous Block Spin Approach to Massless Lattice Theories***.

#### Large/small field decomposition (Section 3.3)

### TBC (Section 4)

### RG transformation (Section 5)

#### Introduction of the fluctuation field (Section 5.3)

- Intrinsic coordinates. Exact identity: ...
- $V_{[x]}$ seems to be the block spin field.

#### Fluctuation integration (Section 5.3)

- Fluctuation covariances have finite range $y \in \Omega_x$ with $\Omega_x  = E(P) \cap B_R(y)$ where $E(P)$ is the nonfrozen region.
- Thus not decoupling expansion (cluster expansion) is needed.
- Mayer expansion for exponentiating the small field action still present.

#### Mayer expansion (Section 5.4)

- Anything special?

#### Extraction of marginal coupling constants (Section 5.5)

### Tuning of the bare coupling constant (Section 6)

- Anything special compared to familiar RG constructions?


### Tilting estimate for rotational invariance (Section 8)

- I think this will be used in Nelson's 3/5 estimate to prove rotational invariance

### Local observables and correlation functions (Section 9)
