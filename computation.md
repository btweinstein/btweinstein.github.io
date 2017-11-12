---
layout: page
title: Computation
permalink: /computation/
weight: 2
---

<p align="center">
<img src="../images/resized/mutational_meltdown.png" width="450">
</p>


## GitHub Projects

During my PhD, I wrote hundreds of IPython/Jupyter notebooks and created over 30 GitHub repositories to solve all sorts of interesting problems related to my research. In the links below (blue), I discuss and illustrate the usage of several of my projects. The repositories that I created can roughly be separated into two categories:

### 1. [Data Analysis Repositories](./data_analysis) 

These repositories help me analyze and parse my experimental data. They focus on extracting data from thousands of images and large tabular datasets. In general, the experiments I studied displayed many stochastic features, so I had to analyze my data and extract probabilistic information such as correlations, various moments, etc. I believe such probabilistic analysis will be useful in my future career. Most of the repositories utilize object oriented code.

### 2. [Scientific Computing Repositories](./scientific_computing)

These repositories are fast numerical simulations to help me gain an understanding of the physics governing my experiments. In these repositories, I extensively utilized GPU computing and efficient single-threaded code. The Harvard [Institute for Applied Computational Sciences](https://iacs.seas.harvard.edu/) awarded me a $25,000 scholarship to further develop one of my favorite scientific computing projects, a [2-dimensional GPU-powered Lattice Boltzmann Fluid Mechanics Simulator](./scientific_computing). Like the above, almost all repositories use object-oriented code.

## My Favorite Programming Tools

I have used many different scientific computing tools over the years but Python-based tools are consistently my favorite. Python is easy to use and is easy to link to faster languages such as C, C++, and OpenCL/CUDA. During my thesis, virtually every project I used included some combination of the below tools (see the above repositories for concrete examples):

1. `IPython/Jupyter notebook`
1. `matplotlib`, `seaborn`
1. `numpy`, `scipy`
1. `pandas` (tabular data)
1. `scikit-image` (for image processing)
1. `pymc3` (mostly for fitting parameters and estimating their likelihood with monte carlo techniques)
1. `cython` and the GNU Scientific Library `cython_gsl`  (when I need my analysis to go fast)
1. `PyOpenCL` and `PyCuda` for GPU and multi-threaded computing (when I need my analysis to go *even* faster!)

I am experienced C, C++, Java, Matlab, and Mathematica programmer as well.
