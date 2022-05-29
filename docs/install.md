[Home](index) 
[Previous](index)
[Next](input.md)
___

# Getting Started
## Installation 
`#SHAARP_SI` is written as a notebook using Wolfram Language and need to run with Mathematica 
- OS: Windows 10/Mac ==?== 
- [Mathematica 12.0+](https://user.wolfram.com/portal/myProducts.html) 

## Run SHAARP
1. Unzip the file and open the `SHAARP_SI_Vxx.nb` where `Vxx` denotes the version number. 
	- Make sure if the Dynamic Evaluation has been enbled (it is enabled by default). 
2. From the menu `Evaluation` -> `Evaluate Notebooke` 
	- Note 1: This process will execute `SHAARP_Init.nb`. So make sure the initialization notebooke `SHAARP_Init.nb` is inside the same folder of `SHAARP_SI_Vxx.nb`. 
	- Note 2: This process will clear out all the definitions from other notebooks and enable the "Notation" package for the analytical solutions.
3. After ~30s waiting time for initialization (==we need to improve it!==), you will see the main panel: 
   ![[img/Pasted image 20220529085626.png]]
4. The main panel contains four parts
	- [Input panels](input.md) specify all the input parameters 
	- [Output panels](output.md) give the output diagrams and equations 
	- Progress bar show the progress after clicking the Update button 
	- Update button execute the program by clicking it  

## More resources 
- Detailed description of the method can be found [here](methods.md)  
- Some specific cases can be found [here](examples.md)  


## [Frequently asked questions](FAQ.md) 

___ 
[Home](index) 
[Previous](index)
[Next](input.md)