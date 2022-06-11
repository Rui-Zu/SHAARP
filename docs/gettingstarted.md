# Getting Started with # SHAARP.si

## What is Second Harmonic Generation (SHG)?

As a very brief primer, the SHG interaction is given by $P_i^{2\omega} = d_{ijk}E_j^{\omega}E_k^{\omega}$, where $E$ are the fundamental electric fields of photons at $\omega$ frequency, $P$ is the nonlinear polarization at $2\omega$ frequency created inside the crystal, and $d_{ijk}$ is a third rank polar tensor describing the nonlinear optical property of the crystal. The subscripts _i, j, k_ are dummy subscripts denoting the polarization directions of the respective quantities; each of these indices can be 1, 2, or 3, that represent the orthogonal _crystal physics_ axes denoted in SHAARP as $(Z_1,Z_2,Z_3)$. The SHG tensor, $d_{ijk}$, thus has 3x3x3=27 terms; however crystal symmetry can significantly reduce the number of non-zero terms in the tensor. As described in the manual in detail, besides the _crystal physics_ axes, there are four other sets of axes we will use in this package, namely, the crystallographic axes $(a,b,c)$, the lab axes, $(L_1,L_2,L_3)$, principal axes, $(Z_1^{princial},Z_2^{principal},Z_3^{principal})$ and the polarization axes (_s_, _p_); relationships between them is important to understand in order to usefully employ this package in experiments.

One important application of the code is to provide analytical expressions to fit experimentally measured polar plots for a nonlinear single crystal.  By such fitting, one can determine the point group symmetry, as well as determine the various nonlinear coefficients by comparing with a standard crystal whose nonlinear coefficients are known. A second application is to quickly generate the expected SHG polarimetry response from crystals whose linear and nonlinear properties are already known.


