# ♯SHAARP._si_
## Simulation and analytical derivation for nonlinear optics

![GitHub release version](https://img.shields.io/github/v/release/Rui-Zu/SHAARP?color=%2350C878&include_prereleases)
![License](https://img.shields.io/github/license/Rui-Zu/SHAARP)
![GitHub Size](https://img.shields.io/github/repo-size/Rui-Zu/SHAARP)

**♯SHAARP**._si_ is an open-source package for deriving and simulating reflected optical second harmonic generation (SHG) from a single interface (_si_), typically the surface of a single crystal. Optical SHG describes the process where two photons of frequency interact with a nonlinear medium (a crystal) to create a photon at 2$\omega$, so called the SHG process.  (A followup package for multiple interfaces is currently being developed).

This package builds in the most general approach to both analytically and numerically solving the surface SHG response of a single crystal surface with arbitrary crystal symmetry, arbitrary orientation and a complex dielectric function (complex refractive indices).

As a very brief primer, the SHG interaction is given by $P_i^{2\omega} = d_{ijk}E_j^{\omega}E_k^{\omega}$, where _E_ are the fundamental electric fields of photons at $\omega$ frequency, _P_ is the nonlinear polarization at $2\omega$ frequency created inside the crystal, and $d_{ijk}$ is a third rank polar tensor describing the nonlinear optical property of the crystal. The subscripts _i, j, k_ are dummy subscripts denoting the polarization directions of the respective quantities; each of these indices can be 1, 2, or 3, that represent the orthogonal _crystal physics_ axes denoted in ♯SHAARP as $(Z_1,Z_2,Z_3)$. The SHG tensor, $d_{ijk}$, thus has 3x3x3=27 terms; however crystal symmetry can significantly reduce the number of non-zero terms in the tensor. As described in the manual in detail, besides the _crystal physics_ axes, there are four other sets of axes we will use in this package, namely, the crystallographic axes $(a,b,c)$, the lab axes, $(L_1,L_2,L_3)$, principal axes, $(Z_1^{princial},Z_2^{principal},Z_3^{principal})$ and the polarization axes (_s_, _p_); relationships between them is important to understand in order to usefully employ this package in experiments.

One important application of the code is to provide analytical expressions to fit experimentally measured polar plots for a nonlinear single crystal.  By such fitting, one can determine the point group symmetry, as well as determine the various nonlinear coefficients by comparing with a standard crystal whose nonlinear coefficients are known. A second application is to quickly generate the expected SHG polarimetry response from crystals whose linear and nonlinear properties are already known.

Follow the steps below to get started with the package. For more detailed information on ♯SHAARP._si_, please refer to the [manual](https://shaarp.readthedocs.io/en/latest/).

## Installation 
♯SHAARP._si_ is written as a notebook using Wolfram Language and need to run with _Mathematica®_
### _Mathematica®_ Notebook
- To install Mathematica, please refer to the [Installing Mathematica](https://reference.wolfram.com/language/tutorial/InstallingMathematica.html)
- If you already have a Wolfram account, you can log in through the [portal](https://account.wolfram.com/login) and download the software.
### Wolfram Player
-  Wolfram Player is a free software offered by _Mathematica®_ to interact with _Mathematica®_ Notebook.
- The download page can be accessed [here](https://www.wolfram.com/player/)
- Note: Wolfram Player provides access to most of the capabilities of ♯SHAARP._si_ except for [Full Analytical expressions](<install.md#Linear Optical Tensors>).

## Open the ♯SHAARP._si_.nb in the _Mathematica®_ software on your computer
1. Unzip the file and open the `SHAARP_si.nb`. 
	- Note: It is recommended to keep all the files in the same directory to access the full features of `♯SHAARP.si`
	- Make sure that the Dynamic Evaluation has been enbled (it is enabled by default).
2. From the menu `Evaluate` -> `Evaluate Notebook`
	- Note: This process will clear out all the definitions from other notebooks and enable the "Notation" package for the analytical solutions.
3. After ~30s waiting time for initialization, you will see the main panel: 
   ![Interface.png](<docs/img/install-GUI.png>)
4. The main panel contains four parts
	- [Input panels](https://shaarp.readthedocs.io/en/latest/input/) specify all the input parameters 
	- [Output panels](https://shaarp.readthedocs.io/en/latest/input/) give the output diagrams and equations 
	- Progress bar show the progress after clicking the Update button 
	- Update button execute the program by clicking it  

## Try preset demos
- On the left-hand panel (LHP), scroll down to “`Case Studies`”.
- Click on <span style="background-color: #D3D3D3">LiNbO<sub>3</sub> (11<span style="text-decoration:overline">2</span>0) MTI X-cut</span>. All the parameters will be autofilled for this case.
- In the “`Functionality`”, select “`SHG Simulation`”. Leave the other LHP settings in their default settings.
- At the top R.H. corner, click “<span style="background-color: #9CCC65">Update</span>". (Please be patient, it may take a few seconds; Watch the progress bar on the top to track when the calculation is done.)
- The second row of the right-hand panel (RHP) should depict the SHG polar plots, $I^{2\omega}(\varphi,\psi)$ and $I^{2\omega}(\varphi,\psi+\pi/2)$ for the default settings of polarization and plane of incidence (PoI) in the LHP.
- Placing the cursor on the polar plots,and you can view a detailed description of the plots.

Now you have obtained your first numerical simulation of SHG polarimetry from a single interface. Next, let’s explore various polarization settings for the fundamental $\omega$ and SHG $2\omega$ waves.

## Polarization Settings
- The definition of the incident polarization at frequency $\omega$ is given as $E=(E_p,E_s)=E_0(\cos\varphi, \sin\psi e^{i\Delta\delta})$, $E=(E_p,E_s)=E_0(\cos\varphi)$, $\sin\psi$, $\sin$, $\psi$, $e^{i\Delta\delta}$
- 
- where $E_p$ and $E_s$ are the _p_ and _s_ polarization components that are, respectively, parallel to and perpendicular to the PoI. The PoI is a plane formed by the incident wavevector, $\pmb{k}^{\omega}$, and the normal to the crystal surface. The polarization of the SHG wave (at frequency $2\omega$ is measured using a linear polarizer at an angle $\psi$, where $\psi=0^o$ and $90^o$ corresponds to the _p_-polarized and _s_-polarized SHG light, respectively.
- In the “<span style="background-color: #D3D3D3">Polarimetry Settings</span>”, you can vary
	1. the incident angle ( $\theta^i$, in the range between $0-90^o$ ),
	2. the incident ( $\omega$ ) polarization direction ( $\varphi$ )
	3. output ( $2\omega$ ) polarization direction ( $\psi$ ), and
	4. the ellipticity of incident wave ( $\Delta\delta$ )
- In the “<span style="background-color: #D3D3D3">Incident Angle &theta;<sup>i</sup>(<sup>o</sup>)</span>”, set incident angle (at frequency $\omega$)  to $0^o$, and press “<span style="background-color: #9CCC65">Update</span>” to evaluate the changes. In the first row on the RHP, the polarized SHG response will change. The change of incident angle will also be revealed in the “**Probing Geometry**” plot in the second row of the RHP.
- Now set the “<span style="background-color: #D3D3D3">Output SHG Polarization</span>” to “<span style="background-color: #D3D3D3">Fix Analyzer</span>”. A “<span style="background-color: #D3D3D3">Fixed Analyzer Angle</span>” option will appear, allowing you to select a specific output polarization direction. Keep the angle at $0^o$ for now (corresponding to _p_-polarization), and click “<span style="background-color: #9CCC65">Update</span>”. The SHG polar plots will change accordingly, and you can view the change to the polarization setting in the **Polarization Relations** plot in the second row of the RHP.
- Now click "<span style="background-color: #D3D3D3">3D Schematic</span>" and then “<span style="background-color: #9CCC65">Update</span>”. The <span style="background-color: #D3D3D3">3D Schematic</span> option will allow you to visualize the **Probing Geometry** and **Polarization Relations** in 3D, and you can change the view direction by dragging the plots.
- You can also change the incident polarization. Try playing with the polarization settings and press “<span style="background-color: #9CCC65">Update</span>” to generate new plots.

Now you have some experience in setting up the polarization conditions for both fundamental and the SHG waves, in viewing your polarization settings using Probing Geometry and Polarization Relations plots, and generating different SHG polarimetry plots. Next, we will play with the crystal settings.

## Crystal Structure and Crystal Orientation
- In the “<span style="background-color: #D3D3D3"><b>Crystal Structure Section</b></span>”, the user has to specify the point group symmetry and the lattice parameters in order to properly determine the nonvanishing SHG coefficients as well the relevant crystal plane orientations. As an example, LiNbO<sub>3</sub> has the point group _3m_ and its lattice parameters have been well studied. Presently, leave the default settings as they are from selecting the Case Studies “<span style="background-color: #D3D3D3">LiNbO<sub>3</sub> (11<span style="text-decoration:overline">2</span>0) MTI X-cut</span>”.
- “<span style="background-color: #D3D3D3"><b>Crystal Orientations</b></span>” determines how the single crystal is oriented for the study with respect to the lab coordinates. It requires two user inputs:
	1. The orientation of the crystal plane of surface
	2. The orientation of the plane of incidence(PoI)
- These two pieces of information can be input in one of two ways: (a) By using Miller indices, (hkl), by clicking “<span style="background-color: #D3D3D3">Use Miller Indices (hkl)</span>”. (b) By specifying the crystal physics axes with respect to the lab coordinates by clicking “<span style="background-color: #D3D3D3">Use crystal physics direction</span>.”
Note that $L_2$ lab axis is always fixed be perpendicular to the PoI.
- For the “<span style="background-color: #D3D3D3">LiNbO<sub>3</sub> (11<span style="text-decoration:overline">2</span>0) MTI X-cut</span>” case, the default orientation under “<span style="background-color: #D3D3D3">Use Miller Indices (hkl)</span>” is set such that $(110)$ is the surface plane, and $[1 \overline{1} 0]$ is perpendicular to the PoI. Hovering your mouse over <span style="background-color: #D3D3D3">?(hkl)</span> describes the relation between 4-index and 3-index Miller indices for the trigonal and hexagonal systems.
- The “<span style="background-color: #D3D3D3">Use crystal physics direction</span>” should be automatically populated for the preset “<span style="background-color: #D3D3D3">LiNbO<sub>3</sub> (11<span style="text-decoration:overline">2</span>0) MTI X-cut</span>”.  Otherwise, by hovering over the <span style="background-color: #D3D3D3">?crystal physics</span> specifies the relationship between the crystal physics and crystallographic axes for the selected point group. You can use this information to directly evaluate and input this information as well.
- Select <span style="background-color: #D3D3D3">3D Schematic</span> in the “<span style="background-color: #D3D3D3">Polarimetry Settings</span> and press “<span style="background-color: #9CCC65">Update</span>”. You can then view the crystal orientations $(Z_1,Z_2,Z_3)$ in relation to the lab frame $(L_1,L_2,L_3)$ in the 3D **Probing Geometry** plot. You can click, hold and rotate the 3D schematics to get a 3D perspective.
!!! note
	 Note that for the “<span style="background-color: #D3D3D3">LiNbO<sub>3</sub> (11<span style="text-decoration:overline">2</span>0) MTI X-cut</span>” case, $Z_3$ is parallel to $L_1$ in 3D **Probing Geometry** plot.
- Next, change the h,k, and l under the “<span style="background-color: #D3D3D3">[hkl] -> Direction Perpendicular to the Plane of Incidence</span>” to 0, 0, and 1. Press “<span style="background-color: #9CCC65">Update</span>” to update the calculation. The change means that you have rotated your crystal 90 degrees in-plane.
!!! note
	 Note that $Z_3$ is now parallel to $L_2$ in the 3D **Probing Geometry** plot.	 
 
Now you have finished the tutorial on the orientations. Detailed discussions about various coordinate systems and orientations can be found in the manual. Question marks next to “<span style="background-color: #D3D3D3">Use Miller Indices (hkl)</span>” can help you quickly refer to the definition of $(Z_1,Z_2,Z_3)$ based on the point group you have selected.

## Linear Optical Tensors
In this section, you will need to provide either complex refractive index $\widetilde{n}$ or the complex relative dielectric permittivity $\widetilde\varepsilon$ for both the $\omega$ and $2\omega$ frequencies.
!!! note
	 These tensors are property tensors specificed in the crystal physics coordinates and _do not_ need to be changed when changing the crystal orientation.

- You can change the <span style="background-color: #D3D3D3">complex refractive index</span> at $2\omega$ to complex values. You can change  $2.2529$,  $2.2529$ and $2.1604$ to $2.2529+I$,  $2.2529+I$ and $2.1604+2I$. Press “<span style="background-color: #9CCC65">Update</span>” to update the calculation.
!!! note
	 Note, use capital $I$ to represent the imaginary part in Mathematica.
- Now the polar plots are updated with a real refractive index tensor at $\omega$ but a complex refractive tensor at $2\omega$. Next, try making the dielectric tensor at $\omega$ to be complex as well.

## SHG Tensor (<i>d<sub>ijk</sub></i>)
- Based on the point group symmetry you have selected in the “<span style="background-color: #D3D3D3">Crystal Structure</span>”, the nonvanishing terms in the SHG tensor can be uniquely determined and provided in the Voigt notation<sup>1</sup>.
- The default setting for the “<span style="background-color: #D3D3D3">LiNbO<sub>3</sub> (11<span style="text-decoration:overline">2</span>0) MTI X-cut</span>”provides the nonlinear coefficients of LiNbO<sub>3</sub> measured using the fundamental wavelength at 800nm. You can try to change those values and press “<span style="background-color: #9CCC65">Update</span>” to evaluate the influence on the SHG polar plots.

Now you have finished a quick tutorial on the input panels and performing the SHG simulation. ♯SHAARP not only provides simulations of the polarized SHG response but also features in generating analytical expressions for fitting experimentally polar plots for determining nonlinear SHG coefficients and the crystal symmetry.

## Partial Analytical Expressions/ Full Analytical Expressions
<span style="background-color: #D3D3D3"><b>Partial analytical expressions</b></span> generate analytical expressions with only SHG coefficients as the unknown variables, providing a reliable way to experimentally determine SHG coefficients by fitting these expressions to the experimental polar plots. In this function, the numerical values of linear optical tensors, orientation, and the incident angle will be provided by the user and assumed to be known while the unknown SHG coefficients are left as variables.
On the other hand, the <span style="background-color: #D3D3D3"><b>Full analytical expressions</b></span> provides the complete variables-based analytical expressions where the linear and nonlinear optical properties, as well as the various polarization and incidence angles of measurement are assumed to be variables. This method will provide a comprehensive expression for the wave mixing in the nonlinear medium.

### Partial Analytical Expressions
- Taking LiNbO<sub>3</sub> as an example. Click <span style="background-color: #D3D3D3"><b>LiNbO<sub>3</sub> (11<span style="text-decoration:overline">2</span>0) MTI X-cut</b></span> in the <span style="background-color: #D3D3D3"><b>Case Study</b></span>, in order to to use the default parameters.
- Click <span style="background-color: #D3D3D3"><b>Partial Analytical Expressions</b></span> in the <span style="background-color: #D3D3D3"><b>Functionality</b></span> section. Press “<span style="background-color: #9CCC65">Update</span>” to initiate the calculation.
- The RHP will display the final intensity expressions of $I^{2\omega}(\varphi,\psi)$, and $I^{2\omega}(\varphi,\psi+\pi/2)$.
- The <span style="background-color: #D3D3D3"><b>Copy</b></span> button to the left of the expressions will allow you directly copy the expression and paste it into another document such as a Mathematica notebook, or Microsoft files.

### Full Analytical Expressions
- Taking LiNbO<sub>3</sub> as an example. Click <span style="background-color: #D3D3D3"><b>LiNbO<sub>3</sub> (11<span style="text-decoration:overline">2</span>0) MTI X-cut</b></span> in the <span style="background-color: #D3D3D3"><b>Case Study</b></span>, in order to to use the default parameters.
- Click <span style="background-color: #D3D3D3"><b>Full Analytical Expressions</b></span> in the <span style="background-color: #D3D3D3"><b>Functionality</b></span> section. Press “<span style="background-color: #9CCC65">Update</span>” to initiate the calculation.
!!! note
	This calculation could take up to a few minutes due to the amount of calculations involved. Please be patient! The progress bar shown at the top of the GUI helps keep track of the progress in the calculation.
- The RHP will display the equations for reflected electric fields at $2\omega$ frequency ($E^{2\omega}(\varphi,\psi)$ and $E^{2\omega}(\varphi,\psi+pi/2)$) and provide the complete set of equations in a separate notebook file, **Full Analytical Expressions.nb**,in the same directory of ♯SHAARP._si_.
- The <span style="background-color: #D3D3D3"><b>Copy</b></span> button to the left of the expressions will allow you directly copy the expression and paste it into another document such as a Mathematica notebook, or Microsoft files.
!!! note
	In the RHP, you can still use <span style="background-color: #D3D3D3"><b>Copy</b></span> to copy equations though the equations are not displayed.
- The analytical expressions are provided in sequence. For example, $E^{2\omega}(\varphi,\psi)$ is expressed using <span style="color:red"><i>C<sup>T,ee,2&omega;</sup></i></span> and <span style="color:blue"><i>E<sup>T,e,2&omega;</sup></i></span>_._ The expressions for the <span style="color:red"><i>C<sup>T,ee,2&omega;</sup></i></span> and <span style="color:blue"><i>E<sup>T,e,2&omega;</sup></i></span> will also be provided in the output expressions as a function of the material property coefficients and the measurement geometry.

## Defining New Presets
 <span style="background-color: #D3D3D3"><b>Materials Properties Preset Values</b></span>provides a way to store your input information so that you can review those input later. It works similarly to buttons in the  <span style="background-color: #D3D3D3"><b>Case Study</b></span> but allows users to customize input settings based on the need. This setting is particularly useful if you are varying some input settings to explore the influence and changes towards SHG response.
- Take LiNbO<sub>3</sub> as an example. Click <span style="background-color: #D3D3D3"><b>LiNbO<sub>3</sub> (11<span style="text-decoration:overline">2</span>0) MTI X-cut</b></span> in the <span style="background-color: #D3D3D3"><b>Case Study</b></span>, to use the default parameters. Click <span style="background-color: #D3D3D3"><b>SHG Simulations</b></span> in the Functionality section. Press “<span style="background-color: #9CCC65">Update</span>” to initiate the calculation.
- Click “<span style="background-color: #D3D3D3"><b>Preset 1</b></span>” to store the input information including orientations, crystal structure, linear optical tensor values, and SHG tensor values. You can set labels for your presets and enter “LNO” in the “<span style="background-color: #D3D3D3"><b>Preset 1 Label</b></span>”. Use “<span style="background-color: #9CCC65">Update</span>” to secure the settings. Hovering cursors on preset buttons will provide more information about preset values.
- Now, you can click <span style="background-color: #D3D3D3"><b>GaAs(111)</b></span> in the <span style="background-color: #D3D3D3"><b>Case Study</b></span> and press “<span style="background-color: #9CCC65">Update</span>” to evaluate different materials. Go to “<span style="background-color: #D3D3D3"><b>Preset 2</b></span>” and use “<span style="background-color: #9CCC65">Update</span>” to make changes to the settings.
- By pressing “<span style="background-color: #D3D3D3"><b>Preset 1</b></span>”, the input information will direct you back to the settings for preset 1. You can also click “<span style="background-color: #D3D3D3"><b>Preset 2</b></span>” to return to saved settings for preset 2.
- If you click “<span style="background-color: #D3D3D3"><b>Clear Presets</b></span>”, this process will erase all saved settings for all four presets. You can redefine presets after clearing the definition.

## More resources 
- Detailed description of the method can be found [here](methods.md)  
- Some specific cases can be found [here](examples.md)  


## Reference
1. Denev, S. A., Lummen, T. T. A., Barnes, E., Kumar, A. & Gopalan, V. Probing Ferroelectrics Using Optical Second Harmonic Generation. _Journal of the American Ceramic Society_ **94**, 2699–2727 (2011). 
