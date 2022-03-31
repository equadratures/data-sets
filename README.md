# data-sets
This repository stores datasets intended for use with the [equadratures](https://github.com/Effective-Quadratures/equadratures) code. Many of the datasets involve problems commonly encountered in aeronautics and other areas of engineering. Some of the datasets are used in recent academic [publications](https://equadratures.org/_documentation/references.html), and/or [blog posts](https://discourse.equadratures.org/), involving the equadratures code.

## Summary of datasets

- **naca0012**: Aerodynamic performance data for an ensemble of deformed naca0012 aerofoils. The data is ideal for testing surrogate models intended for rapid flowfield estimation.

- **blade_envelopes**: Aerodynamic performance data for an ensemble of deformed von Karman Institute LS89 turbine blades. This data is used in the Blade Envelopes papers ([part I](https://arxiv.org/abs/2011.11636) and [part II](https://arxiv.org/abs/2012.15579)), which explore a novel approach to determining manufacturing tolerances via dimension reduction.

- **probes**: Temperature recovery and loss data for an ensemble of shrouded probes used to measure stagnation temperature in turbo-machinery applications. This data is used in the [this paper](https://asmedigitalcollection.asme.org/GT/proceedings-abstract/GT2020/84089/V02CT35A057/1094558), which uses dimension reduction to explore the design of turbo-machinery temperature probes.

- **3Dfan_blades**: Aerodynamic performance for three distinct 3D research fan blades. This data-set is ideal for evaluating the utility of similar subspaces. This data is used in [this paper](https://asmedigitalcollection.asme.org/turbomachinery/article-abstract/140/4/041003/378904/Turbomachinery-Active-Subspace-Performance-Maps?redirectedFrom=fulltext) on active subspace performance maps, and [this paper](https://www.cambridge.org/core/journals/aeronautical-journal/article/abs/supporting-multipoint-fan-design-with-dimension-reduction/3614035892B7EAC41DC8C486BA008A03) on multiple active subspaces.

- **LS89_turbine**: Heat transfer of the LS89 turbine as a function of boundary conditions (inlet Mach number, Reynolds number and turbulence intensity). This data-set consists of two input-output sets. The first one is obtained from [Arts et al.](https://asmedigitalcollection.asme.org/turbomachinery/article-abstract/114/1/147/419968/Aero-Thermal-Performance-of-a-Two-Dimensional?redirectedFrom=fulltext), and comprises experimental data obtained from wind tunnel measurements. The second one consists of simulation data of the same geometry, obtained from the [SU2 CFD suite](https://su2code.github.io). 

## To load datasets
The datasets can be loaded using the `datasets.load_eq_dataset()` function in equadratures. The requested dataset can either be downloaded directly by the code, or to minimise downloads this repo can be cloned once by the user, and the local repo directory can be given to the function. In both cases a summary of the requested dataset will be printed to screen, and a `NpzFile` object containing the data will be returned. The numpy arrays within this can be accessed in the usual way, e.g. `X = data['X']`.

### Direct download
To download the `naca0012` dataset:

```python
import equadratures as eq
data = eq.datasets.load_eq_dataset('naca0012')
```

### git clone

To avoid having to download the dataset each time `load_eq_dataset()` is called, this git repo can be cloned onto your local machine instead. For example:

```console
cd /Users/user/Documents/
git clone https://github.com/Effective-Quadratures/data-sets.git
```

The directory location of the local repo can then be given via the `data_dir` argument:

```python
import equadratures as eq
data = eq.datasets.load_eq_dataset('naca0012', data_dir='/Users/user/Documents/data-sets')
```
