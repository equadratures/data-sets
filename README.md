# data-sets
This repository stores datasets intended for use with the [equadratures](https://github.com/Effective-Quadratures/equadratures) code. Many of the datasets involve problems commonly encountered in aeronautics and other areas of engineering. Some of the datasets are used in recent academic [publications](https://equadratures.org/_documentation/references.html), and/or [blog posts](https://discourse.equadratures.org/), involving the equadratures code.

## Summary of datasets

- **naca0012**: Aerodynamic performance data for an ensemble of deformed naca0012 aerofoils. The data is ideal for testing surrogate models intended for rapid flowfield estimation.

- **blade_envelopes**: Aerodynamic performance data for an ensemble of deformed von Karman Institute LS89 turbine blades. This data is used in the Blade Envelopes papers ([Part I](https://arxiv.org/abs/2011.11636) and [Part II](https://arxiv.org/abs/2012.15579)), which explore a novel approach to determining manufacturing tolerances via dimension reduction.

- **probes**: Temperature recovery and loss data for an ensemble of shrouded probes used to measure stagnation temperature in turbo-machinery applications. This data is used in the [ASME Turbo Expo paper](https://asmedigitalcollection.asme.org/GT/proceedings-abstract/GT2020/84089/V02CT35A057/1094558), which uses dimension reduction to explore the design of turbo-machinery temperature probes.

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
