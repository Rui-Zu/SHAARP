# Welcome to ♯SHAARP._si_ 
![GitHub release version](https://img.shields.io/github/v/release/Rui-Zu/SHAARP?color=%2350C878&include_prereleases)
![License](https://img.shields.io/github/license/Rui-Zu/SHAARP)
![GitHub Size](https://img.shields.io/github/repo-size/Rui-Zu/SHAARP)

**♯SHAARP**._si_ is an open-source package for deriving and simulating reflected optical second harmonic generation (SHG) from a single interface (_si_), typically the surface of a single crystal. Optical SHG describes the process where two photons of frequency $\omega$ interact with a nonlinear medium (a crystal) to create a photon at 2$\omega$, so called the SHG process.  (A follow up package for multiple interfaces is currently being developed).

This package builds in the most general approach to both analytically and numerically solving the surface SHG response of a single crystal surface with arbitrary crystal symmetry, arbitrary orientation and a complex dielectric function (complex refractive indices).

As a very brief primer, the SHG interaction is given by $P_i^{2\omega} = d_{ijk}E_j^{\omega}E_k^{\omega}$, where $E$ are the fundamental electric fields of photons at $\omega$ frequency, $P$ is the nonlinear polarization at $2\omega$ frequency created inside the crystal, and $d_{ijk}$ is a third rank polar tensor describing the nonlinear optical property of the crystal. The subscripts _i, j, k_ are dummy subscripts denoting the polarization directions of the respective quantities; each of these indices can be 1, 2, or 3, that represent the orthogonal _crystal physics_ axes denoted in ♯SHAARP as $(Z_1,Z_2,Z_3)$. The SHG tensor, $d_{ijk}$, thus has 3x3x3=27 terms; however, crystal symmetry can significantly reduce the number of non-zero terms in the tensor. As described in the manual in detail, besides the _crystal physics_ axes, there are four other sets of axes we will use in this package, namely, the crystallographic axes $(a,b,c)$, the lab axes, $(L_1,L_2,L_3)$, principal axes, $(Z_1^{principal},Z_2^{principal},Z_3^{principal})$ and the polarization axes (_s_, _p_); relationships between them are important to understand in order to usefully employ this package in experiments.

One critical application of the code is to provide analytical expressions to provide insight of intrinsic properties through the experimental observation. By such fitting, one can obtain structural information, polarization direction, as well as nonlinear optical susceptibilities. A second application is to simulate SHG response under various polarization states of incident photons, orientations and geometric considerations.

!!! note
	This project is under active development.

## Referencing
We request that you cite the following technical reference in any work for which you used ♯SHAARP:
1. R. Zu, B. Wang, J. He, J.-J. Wang, L. Weber, L.-Q. Chen, and V. Gopalan, SHAARP: An Open-Source Package for Analytical and Numerical Modeling of Optical Second Harmonic Generation in Anisotropic Crystals, (2022).

## Project outline

### [Getting Started with ♯SHAARP._si_](install.md)
### [Methods](methods.md)
### [Inputs](input.md)
### [Outputs](output.md)
### [Examples](examples.md)
### [Frequently Asked Questions](FAQ.md)
### [Table of Symbols](table.md)

## Acknowledgement
This development of the software was supported as part of the Computational Materials Sciences Program funded by the U.S. Department of Energy, Office of Science, Basic Energy Sciences, under Award No. DE-SC0020145.
