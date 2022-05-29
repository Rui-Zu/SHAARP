[Home](index) 
[Previous](install.md)
[Next](output.md)
___

# Input Parameters
This section introduces each subpanel of the input panel. Each subpanel is folderable and can be expanded of collapsed bysingle- clicking the bottum ![[img/Pasted image 20220529090158.png]] or ![[img/Pasted image 20220529090221.png]] at the upper left corner. 
## Functionality
>![[img/Pasted image 20220529085914.png]]
>**Functionality subpanel**

This subpanel contains four tabs corresponding to three different modes 
- User Guide shows the Welcome Page and a quick start example of SHAARP. 
- SHG Simulation directs to the tab for numerical simulation of SHG polarometry. 
- Partial Analytical Expression directs to the tab for deriving the analytical expression of reflective SHG intensity with _some_ input parameters to be unknown and symbolic and others known with numerical values. 
- Full Analytical Expression directions to the tab for showing the full analytical expression of reflective SHG intensity with _all_ input parameters to be unknown. 
## Polarimetry Settings
>![[img/Pasted image 20220529090657.png]]
>**Polarimetry subpanel**

This subpanel input parameters related to the geometric setup for the virtual polarimetry experiment. 
- Incident Angle specifies the incidenent angle of the incident wave with respect to the out-of-plane of the single surface. 
	- The unit is in `Degree`
	- A few "common" incident angles are provided (0, 15, ..., 75) which can be evaluated by clicking. 
- Incident Field desribes the electric field vector of the incident wave which can be specified by the following parameters. 
	- Incident Polarization Angle $\varphi$  
		- The unit is in `Degree`
		- Two modes of setting up for $\varphi$  
			- Rotate Polarizer: ==?==  
			- Fix Polarizer: ==?==  
				- If this mode is chose, there is a pop-up setup for Fixed Incident Polarization Angle 
			- Which mode to use can be determined [[Polarizer Mode]] 
	- Incidenet Elllipticity $\Delta \delta$ 
		- The unit is in `Degree`
	- Output Polarization 
		- Two modes of setting up for $\varphi$  
			- Rotate Polarizer: ==?==  
				- If this mode is chose, there is a pop-up setup for Analyzer-Polarizer Angle Offset (unit in degree)
			- Fix Polarizer: ==?==  
				- If this mode is chose, there is a pop-up setup for Fixed Analyzer Angle 
		- Which mode to use can be determined [[Analyzer Mode]] 
- Schematics 
	- One can choose showing either 2D Schematics or 3D Schematics for the geometric setup and the visual definitions of the angles. 
>![[img/Pasted image 20220529092357.png]]
>**2D schematics of Polarimetry setup**
>![[img/Pasted image 20220529092403.png]]
>**3D schematics of Polarimetry setup** 

## Crystal Structure
>![[img/Pasted image 20220529092912.png]]
>**Crystal Structure subpanel** 

This subpanel specifies the crystallography of the material of interest. 
- Point Group is a drop-down menu specifying the point group of the material of interest. 
- The rest input parameters specify the six lattice constants of the crystal. 

## Crystal Orientation
>![[img/Pasted image 20220529093244.png]]
>**Setup crystal orientation using crystal physics directions** 
>![[img/Pasted image 20220529112919.png]]
>**Setup crystal orientation using crystal physics directions**

This subpanel specifies the crystal orientation of the material of interest in the geometry of SHG experiments.
There are two modes to setup the orientation: 
- Use Miller Indices (hkl) 
- Use Crystal Physics Direction 
- 


## Dielectric Tensors
>![[img/Pasted image 20220529094040.png]]
>**Dielectric Tensor subpanel** 

This subpanel specifies the dielectric permittivity in matrix form for the fundamental $\omega$ and SHG $2\omega$ waves. 
- Note that each entry can be input with a complex number so both the real and imaginary parts of $\varepsilon_{ij}$ can be sepcified.  
## Second Harmonic Generation (SHG) Tensors
>![[img/Pasted image 20220529094104.png]]
>**SHG Tensor subpanel**

This subpanel specifies the SHG tensor (in Voigt notation matrix form)
- Note that constraints due to symmetry (specified via Point Group in the subpanel `Crystal Structure`) are imposed automatically. 
## Case Studies 
>!![[img/Pasted image 20220529094133.png]]
>**Case Studies subpanel** 

This subpanel provides a few case studies for reflective SHG experiments on common nonlinear optical crystals.
- Cases in Manuscript contain the four examples in our manuscript [doi to manuscript](manuscript) 
- Complex SHG Coefficients contain one example with absorption term in the SHG tensor. 
- Deep UV NLO contain nonlinear optical crystals in the deep ultraviolet spectrum (==?==). 
- Polar Metals contain crystals with an purely imginary dielectric permittivity (characteristic of metal ==?==). 
- Other Crystals  

## Material Properties Preset Values
>![[img/Pasted image 20220529094218.png]]
>**Material Properties Preset Values** 

This subpanel helps to store a set of user-defined materials properties (including lattice constants, dielectric tensors, and SHG tensors) for up to four different materials. 
- First provide inputs to all the properties for Materials 1, click update to compute and store the results into Preset 1. 
- Then provide inputs to all the properties for Materials 2, click update to compute and store the results into Preset 2. 
- And so on for Materials 3, 4 and Preset 3, 4. 
 