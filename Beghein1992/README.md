# Béghein et al., 1992

> **_Publication:_**
>
> C. Béghein, F. Haghighat, F. Allard, Numerical study of double-diffusive natural convection in a square cavity. International Journal of Heat and Mass Transfer 35(4), 833-46 (1992). https://doi.org/10.1016/0017-9310(92)90251-M.

Double-diffusive convection problem in a cavity. Different horizontal temperature and concentration gradients lead to different thermosolutal convection patterns that range from being fully enhanced aided by both gradients to nullified when both gradients cancel out. A numerical solution of the steady-state is to be compared. Note, the mathematical model comprises the Boussinesq assumption.

The model here corresponds to the test case of opposing flows with $\beta_s$ or $Ra_s$ $> 0$, see fig. 2.d in the publication. Disclaimer: The values of the physical quantities are arbitarily set to just fullfill the dimensionless requirements, any similarities to real values on this planet is coincidental.

## How to run
1. Excecute blockMesh
2. If you changed the length scales: edit [funkySetFieldsDict](system/funkySetFieldsDict) such that the hydrostatic pressure is adjusted accordingly.
3. If you changed the mesh: edit [fvSolution](system/fvSolution) such that the reference pressure corresponds to the reference cell.
4. Make a copy of [0.orig](0.orig) with the name *0*
5. Excecute funkySetFields for time step *0*
6. Start the simulation using the modified *buoyantBoussinesqPimpleFoam* solver