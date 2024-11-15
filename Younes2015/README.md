# Younes 2015

> **_Publication:_**
>
> Younes, A., Fahs, M., Zidane, A. et al. A new benchmark with high accurate solution for hot–cold fluids mixing. Heat Mass Transfer 51, 1321–1336 (2015). https://doi.org/10.1007/s00231-015-1500-z


Basically the Henry Problem transfered to Navier Stokes flow. The semi-analytical solution obtained with the Fourier-Galerkin method is compared with the model results. 

The model here corresponds to test case I as described in the publication. In accordance with the author the outlet velocity profile is adjusted to $\widetilde{u}_{out} = -0.18174 + 0.09137 y + 0.84642 y^2 + 1.31589 y^3 -1.37525 y^4$. This lowers the mass balance error from being around $3\%$ to around $3.75 \cdot 10^{-5} \%$. 

## How to run
1. Excecute blockMesh
2. If you changed the length scales: edit [funkySetFieldsDict](system/funkySetFieldsDict) such that the hydrostatic pressure is adjusted accordingly.
3. If you changed the mesh: edit [fvSolution](system/fvSolution) such that the reference pressure corresponds to the reference cell.
4. Make a copy of [0.orig](0.orig) with the name *0*
5. Excecute funkySetFields for time step *0*
6. Start the simulation using the *buoyantBoussinesqPimpleFoam* solver