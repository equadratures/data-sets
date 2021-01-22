This dataset contains aerodynamic data for a set of 2100 aerofoils. Each aerofoil is obtained by deforming a NACA0012 aerofoil using 50 Hicks-Henne functions. 

Data is obtained with the SU2 CFD solver, which each case run at an angle of incidence of 0deg and Reynolds number of 6M.

Data in file:
X:  A numpy ndarray with shape (2100, 50), containing the bump function amplitudes for each aerofoil.
Cp: A numpy ndarray with shape (2100,200), containing static pressure coefficient data at 200 points around each aerofoil.
Cl: A numpy ndarray with shape (2100,  1), containing the lift coefficient for each aerofoil.
Cd: A numpy ndarray with shape (2100,  1), containing the drag coefficient for each aerofoil.
