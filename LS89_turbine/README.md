This dataset contains data about the dependence of the wall heat transfer of the LS89 turbine from the von Karman Institute as a function of some boundary conditions depending on the exit Mach number, exit Reynolds number and turbulence intensity. It consists of data obtained from an experimental campaign by Arts et al. (Aero-thermal performance of a two-dimensional highly loaded transonic turbine nozzle guide vane: A test case for inviscid and viscous flow computations, in Journal of Turbomachinery, 114 (1)), in addition to  CFD simulations of the same geometry using the open source CFD code SU2, under various boundary conditions.

Data in file:

`experimental_inputs`:  A numpy ndarray with shape (21, 3), containing the boundary condition variables for each data point in the experimental run.

`experimental_outputs`: A numpy ndarray with shape (21,), containing the wall heat transfer values for each data point in the experimental run.

`CFD_inputs`: A numpy ndarray with shape (64, 3), containing the boundary condition variables for each data point in the CFD simulations.

`CFD_outputs`: A numpy ndarray with shape (64,), containing the wall heat transfer values for each data point in the CFD simulations.
