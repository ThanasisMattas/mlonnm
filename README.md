# MLonNM

MLonNM (Machine Learning on Numerical methods) is an ongoing project, investigating how ML can be utilized to  
accelerate numerical methods.  
___

The Successive Over Relaxation (SOR) method on a 2D grid is selected as a first approach. SOR solves elliptic partial  
differential equations, like the Laplace or the Poisson’s equation. For this project, the weak (variable-coefficient)  
form of the Poisson’s equation is used. More info at the ```MLonNM_report.pdf``` at the current directory.

## Features

The features of the analysis are the configuration parameters of the simulation (Initial/Boundary conditions, domain  
sizing, discretization steps, etc), as long as the coefficients of the polynomials that represent the source and the  
permittivity functions.

## Data-point activator

The activator of each datapoint is going to be the optimum relaxation factor ω (omega) of the corresponding case;  
namely, the ω that leads to the fastest solution at the specific configuration, under a pre-defined precision.

## Data mining

The data mining is an automated process of generating the combinations of the different simulation configurations  
and, subsequently, running all of the simulations at a range of ω values, picking the optimum one as the activator of  
each datapoint.

This procedure is handled by the ```mlonnmDataMining.py``` script.

## Next

Next step of the project is the implementation of a ML algorithm (probably neural network) that hopefully will predict  
the ompimum relaxation factor at an unseen test set.  

Noting some further progress of the project, in some cases the optimum ω isn't constant during
the whole simulation.  
Thus, a prediction of a vector of the optimum ω values and the rate of change or the changing iteration marks would be  
an optimized goal for this project.

>(C) 2019, Thanasis Mattas  
>atmattas@physics.auth.gr