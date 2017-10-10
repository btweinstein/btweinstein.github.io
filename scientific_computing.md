---
layout: page
title: Scientific Computing
permalink: /computation/scientific_computing
exclude: true
---

My scientific computing projects have focused on both fluid mechanics, relevant to the second half of my thesis, or simulating microbial colony growth (i.e. interfacial growth due to autocatalytic reactions).

## Fluid Mechanics

### [An Award-Winning GPU-powered Lattice Boltzmann Simulation](https://github.com/btweinstein/2d-lb)

As I knew the second half of my PhD would focus on fluid mechanics (as I was growing microbes on an ultra-viscous liquid), I audited Sauro Succi's computational fluid mechanics course in hopes that I could create experimentally relevant simulations.  Sauro played a pivotal role in the development of the Lattice Boltzmann technique, a relatively new mesocopic technique that excels when simulating multiphase fluid flow and flows in complex geometries (such as porous media). 

Based on the material I had learned while auditing Sauro's class, I created my own GPU-powered 2-dimensional Lattice Boltzmann simulator in collaboration with @matheuscfernandes as the final project for CS205 (one of my required courses to obtain my minor in Computational Science and Engineering). Relative to naive Python, our GPU-powered simulation obtained a speedup of 650x, and, relative to single-threaded cython, a speedup of about 50x. Additional information about the Lattice Boltzmann technique, our simulation, and our procedure to optimize the speed of our package can be seen on the [**2d-LB website**](https://sites.google.com/site/latticeboltzmannmethodcs205/). The video illustrates a simulation of fluid flow around an obstacle at moderate Reynolds number, and the video below that is a rather humorous video that discusses our simulation in greater detail.

<p align="center">
<iframe src="https://docs.google.com/file/d/0ByRswVj1mkw-eFp2WDFfUVdnT0U/preview" width="560" height="300"></iframe>
</p>

<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/Py2hT0Y7gJ4" frameborder="0" allowfullscreen></iframe>
</p>


After completing the final project, I wrote a proposal to the [Institute for Applied Computational Sciences](https://iacs.seas.harvard.edu/) at Harvard asking them to fund work extending the simulation; I wanted to add real-time visualization of fluid flows with `vispy` and add the transport of passive scalars by fluid flow (a situation relevant to my experiments). IACS awarded me a $25,000 student scholarship to develop the simulation further and I completed those additions. This was one of my favorite projects during my PhD.




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
