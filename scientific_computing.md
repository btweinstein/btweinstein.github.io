---
layout: page
title: Scientific Computing
permalink: /computation/scientific_computing
---

During my PhD, I've written thousands of IPython/Jupyter notebooks to analyze different types
of data that I have encountered (i.e. images, tabular data, etc.). I have used many different python
packages for data analysis, but I must often use

1. `IPython/Jupyter notebook`
1. `matplotlib, seaborn`
1. `numpy, scipy`
1. `pandas`
1. `scikit-image` (for image processing)
1. `pymc3` (mostly for fitting parameters and estimating their likelihood with monte carlo techniques)
1. `cython` and the gnu-scientific library `cython_gsl` (when I need my analysis to go fast)
1. `PyOpenCL` (when I need my analysis to go *even* faster!)

I have authored several packages for my own data analysis needs in the laboratory (see the below).

## Fluid Mechanics

### [2d-lb](https://github.com/btweinstein/2d-lb)

### [stokesBuoyantSoluteFoam](https://github.com/btweinstein/stokesBuoyantSoluteFoam)

## Random Walk Theory and Applications to Evolution

I authored most of the code in the "[Range Expansion](https://github.com/range-expansions)" Github organization. I will summarize some of the projects below.

### [annihilating_coalescing_walks](https://github.com/Range-Expansions/annihilating_coalescing_walks)

The Cython-based simulation package developed for my [first paper](https://www.biorxiv.org/content/early/2017/06/07/145631). 
It simulates random walkers constrained on a ring and was calibrated to experiment.

<p align="center">
<img src="../images/resized/annihilating_coalescing_random_walkers.png" width="600">
</p>

### [expansion_optics](https://github.com/Range-Expansions/expansion_optics)

Determines how a perfectly smooth range expansion with strains that have
 differing growth rates would propagate forwards in time using the fast marching
 method ([scikit-fmm](https://github.com/scikit-fmm/scikit-fmm)) 
 
 <p align="center">
<img src="../images/resized/geo_optics_alone.png" width="600">
</p>

### [stepping_stone_expansions](https://github.com/Range-Expansions/stepping_stone_expansions/blob/master/docs/examples_of_use.ipynb)

### [rough_front_expansion](https://github.com/Range-Expansions/rough_front_expansion)

### [particle_populations_in_flow](https://github.com/Range-Expansions/particle_populations_in_flow)
