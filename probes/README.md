## Summary
This dataset contains temperature recovery and loss data for a set of 128 probe designs, used in the 2020 ASME Turbo Expo [paper](https://asmedigitalcollection.asme.org/GT/proceedings-abstract/GT2020/84089/V02CT35A057/1094558):

"Design space exploration of stagnation temperature probes via dimension reduction" (GT2020-16277)

Each design is obtained by deforming a baseline design parameterised with seven design parameters. The baseline design is representative of a single-shrouded stagnation temperature probe used aero-engines. Data is obtained with the SU2 CFD solver, with the freestream Mach number varied from 0.3 to 0.8. All input and output data has been standardised to lie within the interval [-1,1].

## Description of Data
There are $N=128$ designs and $d=7$ design parameters. The input design vectors are stored in $\mathbf{X}\in \mathbb{R}^{N\times d}$, while the three design objectives are stored in $y_1,y_2,y_3 \in \mathbb{R}^{N \times 1}$.

The design objectives are the following (see Sections 2 and 6 in the paper for more details):
1) $y_1$: Stagnation pressure loss coefficient $Y_p$ averaged across the Mach number range. 

2) $y_2$: Gradient of recovery ratio w.r.t to Mach number $\partial R_r/\partial M$.

3) $y_3$: Recovery ratio $R_r$ at Mach 0.8. 

As in the paper, $X$ is standardised to lie within the interval $[-1,1]$. Unlike in the paper, for commerical privacy reasons, $y_1$, $y_2$ and $y_3$ are also standarised here. 

Data in file:

`X`:  A numpy ndarray with shape (128, 7), containing the 7 non-dimensionalised design parameters of each probe.

`y1`: A numpy ndarray with shape (120,1), containing the $y_1$ design objective for each probe.

`y2`: A numpy ndarray with shape (120,1), containing the $y_2$ design objective for each probe.

`y3`: A numpy ndarray with shape (120,1), containing the $y_3$ design objective for each probe.
