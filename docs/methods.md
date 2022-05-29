[Home](index) 
[Previous](examples.md)
[Next](FAQ.md)  
___
# Simulation and Analytical Methods
## Optical Geometry

**Fig. 1(a-c)** and **(d-f)** are the two common schematics of experimental geometries where the red and blue rays are the fundamental and second harmonic light, respectively. The plane of incidence is defined as the $L_1 - L_3$ plane, where $(L_1,L_2,L_3)$ are the lab coordinates as displayed in **Fig. 1a** and **d**.

While rotating the incident polarization ($E$$^i$($\phi$)), polarized SH intensities are collected as a function of the azimuthal angle . **Fig. 1b** depicts the collection of _p_ and _s_ polarized SH intensities ($I_p^{2\omega} (\psi)$ and $I_s^{2\omega} (\psi)$) and **Fig. 1e** illustrate the SH intensities polarized both parallel and perpendicular to the incident fundamental polarization ($I$$_\parallel$$^2$$^\omega$ ($\phi$) and $I$$_\perp$$^2$$^\omega$ ($\phi$)) if projected in $s - p$ plane. Here,  _s_ and _p_ describes the electrical fields of electromagnetic waves within and perpendicular to the plane of incidence ($L_1 - L_3$ plane), respectively.

The former geometry is commonly achieved with a rotating halfwave plate and fixed analyzer while the latter geometry can be achieved by simply rotating the crystal or rotating the halfwave plate and analyzer simultaneously. **Fig. 1c** and **f** demonstrate the SHG polar plots of GaAs (111) obtained at normal incident geometry which contain information of crystal symmetry, refractive indices at both  and  frequencies, and second-order nonlinear susceptibility.


>![V6_Figure1](img/V6_Figure1.png)
Figure 1. Two common types of experimental geometries for SHG polarimetry. **a-c** _p_- and _s_- polarized SHG intensities as a function of incident fundamental polarization. **d-f** SHG intensities polarized both parallel and perpendicular to the incident polarization projected in $s - p$ plane. Red and blue waves suggest a pump beam at $\omega$ and signal beam at $2\omega$ frequency, separately. $(L_1,L_2,L_3)$ is the lab coordinate system. The orange and dark grey planes are the sample surface and plane of incidence ($L_1 - L_3$ plane).  $\psi$ is the azimuthal angle. **b,e** Relations of incident polarization and SHG polarization projected in $s - p$ plane. **c,f** SHG polar plots of GaAs (111) in the normal incident geometries using two experimental configurations described in panels **a**,**b**, and **d**,**e**, separately.


## Coordinate System

Four different coordinate systems shown in **Fig. 2** are involved in fully describing the SHG measurement, and it is essential to establish their absolute and relative orientations.

On the lab scale, $(L_1,L_2,L_3)$ describe the _lab coordinate system_ (LCS) and $L_3$ corresponds to the normal to the surface; this coordinate system is always orthogonal. 

Looking at the atomic scale, the translation vectors of a unit cell of the crystal determine the _crystallographic coordinate system_(CCS) given by (_a_, _b_, _c_); these axes need _not_ be orthogonal.

The $(Z_1,Z_2,Z_3)$ represent the _crystal_ _physics coordinate system_ (ZCS) in which the material property tensors are represented; they are always orthogonal and their orientation relative to (_a_, _b_, _c_) follows Newnham’s convention.

The $(Z_1^{Principal},Z_2^{Principal},Z_3^{Principal})$ is the _principal coordinate system_ (PCS), where dielectric tensors or refractive index tensors are diagonalized; this coordinate system is also always orthogonal. For an isotropic or uniaxial structure, $(Z_1,Z_2,Z_3)\equiv (Z_1^{Principal},Z_2^{Principal},Z_3^{Principal})$ , which simplifies the overall problem. However, for a biaxial crystal, the PCS is _defined_ with the real part of the refractive indices along each axis following the ascending order, i.e.,$n(Z_1^{Principal})<n(Z_2^{Principal})<n(Z_3^{Principal})$ , while this is _not_ generally true in the crystal physics coordinate system. Henceforth, we will adopt the notation $n(Z_1^{Principal}) \equiv n_i^{\omega}$  for the Eigen values for the refractive index. In the PCS, the diagonal components of the complex _relative_ dielectric function can be conveniently written as $\epsilon^{Principal} \equiv \epsilon_i^{\omega}$ , where  is the vacuum permittivity. Therefore, the dielectric permittivity $\epsilon_i^{\omega}$ in the LCS can be expressed as
$$
\epsilon_i^{\omega} = a_{LZ}a_{ZP}\begin{pmatrix} n_1^{\omega}&0&0 \\\ 0&n_2^{\omega}&0 \\\ 0&0&n_3^{\omega}\end{pmatrix}^2(a_{LZ}a_{ZP})^{-1}
$$where  is the rotation matrix from ZCS to the LCS and  is the rotation matrix from the PCS to the ZCS, respectively.

>
>![Coordinate](img/Coordinate.png)
Schematic of four coordinate systems used for a monoclinic structure. , (_a_, _b_, _c_), , and  are the lab, crystallographic, crystal physics, and principal coordinate systems, respectively. Only the crystallographic coordinate system is non-orthogonal.

## Waves in Nonlinear Medium

When a monochromatic plane wave at frequency  is incident upon the interface, two refracted rays at frequency $\omega$ will propagate inside the medium with two orthogonal dielectric displacement vectors $D^{T,e,\omega}$ and $D^{T,o,\omega}$. The two waves can be both ordinary, or one ordinary and one extraordinary, depending on the optical class of the material and the propagation direction. Without loss of generality, we denote the two refracted waves by superscripts _T_, as shown in green in **Fig. 3**. The two fundamental waves correspond to the Eigen solutions of the wave equation at the linear frequency, $\omega$ , given in the LCS as

$$
\begin{align}
\nabla\times\nabla\times E^{T,\omega}
\begin{pmatrix} \varepsilon_{L_1L_1}^{\omega}&\varepsilon_{L_1L_2}^{\omega}&\varepsilon_{L_1L_3}^{\omega} \\\ \varepsilon_{L_2L_1}^{\omega}&\varepsilon_{L_2L_2}^{\omega}&\varepsilon_{L_2L_3}^{\omega} \\\ \varepsilon_{L_3L_1}^{\omega}&\varepsilon_{L_3L_2}^{\omega}&\varepsilon_{L_3L_3}^{\omega}
\end{pmatrix}
\mu^{\omega}
\frac{\partial^2}{\partial t^2}
E^{T,\omega}=0
\end{align}
$$
where $\varepsilon_{L_iL_j}^{\omega}$ represents the dielectric permittivity tensor at frequency $\omega$ in the LCS, and the $\mu^{\omega}$ represents the magnetic permeability tensor in the LCS at $\omega$. Typically $\mu^{\omega}\approx\mu_0$, the vacuum permittivity is assumed, but this is not a requirement; the above formulation is quite general and can accommodate the full anisotropic magnetic permeability tensor of the material if so desired. In general, the anisotropic dielectric permittivity and magnetic permeability tensors of the medium are not diagonalized in the lab coordinates (LCS). Therefore, the non-collinearity between $\pmb{E}$ and $\pmb{D}$, as well as $\pmb{B}$ and $\pmb{H}$ results in two non-overlapping orthogonal relations ($\pmb{k}$, $\pmb{D}$, $\pmb{B}$) and ($\pmb{S}$, $\pmb{E}$, $\pmb{H}$). Here, $\pmb{k}$, $\pmb{D}$, $\pmb{B}$, $\pmb{S}$, $\pmb{E}$, and $\pmb{H}$ are wavevector, dielectric displacement, magnetic induction, Poynting vector, electric field and magnetic field intensity. Note that $\pmb{E}$ and $\pmb{H}$ are not necessarily normal to the wavevector $\pmb{k}$ inside the medium.

The second-order nonlinear susceptibility induces a nonlinear polarization and thus radiates nonlinear source waves at  frequency. The source wave at  frequency can be written as,

where , ,  are the nonlinear polarization, the electric field of the refracted  waves, and the second-order nonlinear susceptibility. The term  is the wavevector of the source wave (superscript _S_) that combines two linear wavevectors9, i.e., . The electric fields radiated by the nonlinear polarization can then be calculated in the LCS using the wave equation9,22,23,

where  represents the dielectric permittivity tensor at frequency 2 in the LCS, and the  represents the magnetic permeability tensor in the LCS at .19 Again, typically , the vacuum permittivity is assumed, but this is not a requirement; the above formulation is quite general and can accommodate the full anisotropic magnetic permeability tensor of the material if so desired. The homogeneous wave and inhomogeneous waves radiated by the nonlinear polarization correspond to the general and particular solutions of **Eq. (4)**, respectively. The former component is also known as the “free wave”, and the latter is the radiated wave by the nonlinear polarization known as the “bound wave.”11,14 The total nonlinear wave can be expressed as a superposition of the general and particular solutions. To solve the homogeneous wave at both linear (**Eq. 2**) and nonlinear (**Eq. 4**) frequencies, the _congruence transformation,_ and _generalized Eigen equation_ are employed.24 The two eigenvalues and eigenvectors correspond to effective refractive indices and electric field directions for the two homogeneous _e_ and _o_ waves at the corresponding frequencies. Three inhomogeneous waves , will be generated according to **Eq. 3**, as shown in **Fig. 1a**, due to the three-wave mixing process. Therefore, in principle, five waves at  will be generated, as shown in **Fig. 1a**, where blue and red correspond to homogeneous and inhomogeneous waves, respectively. The inhomogeneous SHG fields can be written in the following form:

where **C** is the field strength to be determined from **Equation (4)** for a given . By substituting **Eq. (3)** and **(5)** into **Eq. (4)**, the field strengths of the three inhomogeneous waves can be explicitly calculated with the associated second-order optical susceptibilities. Accordingly, the  for the three inhomogeneous waves can be obtained by

## Calculation at $2\omega$ Frequency

___
[Home](index) 
[Previous](examples.md)
[Next](FAQ.md)  