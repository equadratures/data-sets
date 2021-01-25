This dataset contains simulation results for the von Karman Institute LS89 turbine blade. The stage pressure loss coefficient is measured for profiles deformed from the baseline profile with 20 FFD parameters. This data is used in the Blade Envelopes papers ([Part I](https://arxiv.org/abs/2011.11636) and [Part II](https://arxiv.org/abs/2012.15579)).

In addition, three collections of geometries are provided to demonstrate the formulation of the blade envelopes.

Data is obtained with the SU2 CFD solver. For more information on the boundary conditions and other parameters, please refer to Part I of the papers.

Data in file:

`X`:  A numpy ndarray with shape (1000, 20), containing the FFD amplitudes for each deformed turbine blade.

`loss`: A numpy ndarray with shape (1000), containing stage pressure loss coefficients for each design in X.

`x_coords`: A numpy ndarray with shape (240), containing x-coordinates of the deformed turbine profiles, measured at 240 stations. Since deformation is only in the y direction, these coordinates are the same for all profiles.

`train_y_coords`: A numpy ndarray with shape (5000,  240), containing the y-coordinates of 5000 samples drawn from the inactive subspace for loss, which is used to learn the blade envelope distribution parameters.

`y_coords_loss`: A numpy ndarray with shape (500,  1), containing the y-coordinates of 500 samples drawn from the inactive subspace for loss.

`y_coords_random`: A numpy ndarray with shape (1000,  1), containing the y-coordinates of 1000 samples from the whole design space (not necessarily loss invariant).
