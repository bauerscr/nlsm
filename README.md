# Digesting the O(3) NLSM construction

Author: the community

## Organization

- Discord channel: https://discord.gg/bF8Hd2ahP
- Mailing list: nlsm@probabilistic-qft.org
- Catchup meetings: Mondays 4pm Amsterdam time

## Papers

1. [Exponential decay in two-dimensional classical $O(n)$ models](https://github.com/openai/math/blob/main/preprints/Exponential-decay-in-two-dimensional-classical-On-models-September-23-2026/paper.pdf)
   - Seems understandable, Lean available
   - Result is not used in the subsequent papers, but related idea implemented there in a stronger way
2. [$O(4)$ mass bounds](https://github.com/openai/math/blob/main/preprints/Sharp-mass-bounds-for-the-two-dimensional-O4-model-September-23-2026/paper.pdf)
   - Establishes $m(\beta) \asymp \sqrt{\beta}e^{-\pi\beta}$
   - Gets referred to and adapted a lot in the $O(3)$ papers
   - No Lean
3. [O(4) exact mass asymptotics](https://github.com/openai/math/blob/main/preprints/Exact-mass-asymptotics-for-the-two-dimensional-O4-lattice-model-October-5-2026/exact-mass-o4.pdf)
   - Establishes $m(\beta) \sim C\sqrt{\beta}e^{-\pi\beta}$ as $\beta\to\infty$ with explicit constant
   - No Lean
4. [$O(3)$ massive continuum limit](https://github.com/openai/math/blob/main/preprints/The-canonical-massive-continuum-limit-of-the-two-dimensional-O3-model-October-4-2026/massive-continuum-o3.pdf)
   - Establishes continuum limit and all OS axioms
   - No Lean
5. [$O(3)$ isolated particle pole](https://github.com/openai/math/blob/main/preprints/An-Isolated-Particle-Pole-for-the-Two-Dimensional-O3-Spin-Field-October-4-2026/o3-particle-pole.pdf)
   - Establishes isolated particle pole and upper mass gap
   - No Lean


## Most interesting ingredients of the contruction

- **Mixing estimate:** obtained using noncommutative Mermin-Wagner idea, correlation inequalities, reflection positivity
- **Block spin transformation** with **intrinsic** rather than **extrinsic** coordinates: spins remain on the sphere and potential does not become a double well.
- **Large/small gradient decomposition** in the spirit of Gawedzki-Kupiainen and Balaban
- **Finite range fluctuation covariances** in the spirit of Brydges, but finite range condition seems to be implemented through explicit truncation rather than exact decomposition.
- **Nelson's 3/5 argument** is used to prove rotational invariance.

## General conventions and notation

- The complete analysis is on the unit lattice until the very end.
- $N_R(P)$ denotes radius $R$ neighborhood of $P \subset \Z^2$

## General terminology

- seed anchors:
- seeds:
- cores: union of seeds within radius $50M$ of each other
- halo:
- ...


## Notes

These notes focus on the fouth paper on the $O(3)$ continuum limit. It uses the others ones.

### Mixing estimate (Section 2)

### Introduction of the fluctuation field (Section 5.3)

- Intrinsic coordinates. Exact identity: ...

### Fluctuation integration (Section 5.3)

- Fluctuation covariances have finite range $y \in \Omega_x$ with $\Omega_x  = E(P) \cap B_R(y)$ where $E(P)$ is the nonfrozen region.
- Thus not decoupling expansion (cluster expansion) is needed.
- Mayer expansion for exponentiating the small field action still present.

### Mayer expansion (Section 5.4)

- Anything special?

### Tuning of the bare coupling constant (Section 6)

- Anything special compared to familiar RG constructions?


### Tilting estimate for rotational invariance (Section 8)

- I think this will be used in Nelson's 3/5 estimate to prove rotational invariance

### Local observables and correlation functions (Section 9)
