---
layout: page
title: Computational Projects
permalink: /computational_projects/
---

## Data Analysis

During my PhD, I've written thousands of IPython/Jupyter notebooks to analyze different types
of data that I have encountered (i.e. images, tabular data, etc.). I have used many different python
packages for data analysis, but I must often use

1. `IPython/Jupyter notebook`
1. `matplotlib, seaborn`
1. `numpy, scipy`
1. `pandas`
1. `scikit-image` (for image processing)
1. `pymc3` (mostly for fitting parameters and estimating their likelihood with monte carlo techniques)
1. `cython` (when I need my analysis to go fast)

I have authored several packages for my own data analysis needs in the laboratory (see the below).

### Image Analysis for my Range Expansion Experiments

I developed my own pipeline to process images and extract relevant information. This code
was extensively used in my [first paper](https://www.biorxiv.org/content/early/2017/06/07/145631).

The pipeline begins with the [range_expansion_image_analysis_fiji](https://github.com/Range-Expansions/range_expansion_image_analysis_fiji)
repository where I used Fiji, and open-source image processing library, to  extract binary masks 
illustrating where different strains of fluorescent microbes were located in a colony. 
In the image below, the left was an experiment of mine where  multiple colors of *E. coli* expanded from 
a dense droplet and segregated into one color locally. The image  on the left is experiment, and the image 
on the right was the masks of each strain created using my script. The words "eYFP", "eCFP", and "mCherry" 
are labels for the strains corresponding to the fluroescent proteins that they produce.

 <p align="center">
<img src="../images/resized/expansion_vs_mask_bigger_text.jpg" width="600">
</p>

After using Fiji to create the fluorescent masks, I imported the masks into python  and developed
[range_expansion_image_analysis_python](https://github.com/Range-Expansions/range_expansion_image_analysis_python)
to extract relevant information. My code extensively utilizes `scikit-image`, a standard Python-based image 
processing library. My Python package could extract various quantities such as the spatial correlation between strains, 
the average fraction of each strain vs. colony radius, and was utilized to compare my experimental results 
to theoretical predictions. 

For example, I used the Python Package to plot the average fraction of three of the above competing strains
(red, yellow, and blue) as a function of colony radius during many experiments. In the plot below,
 the initial fraction composition is the red dot and the final composition is the blue one. As you can see, the 
fraction trajectories are very stochastic. In my 
[first paper](https://www.biorxiv.org/content/early/2017/06/07/145631), I developed a theory to predict the statistical properties of this motion. In order to create this plot, I helped to develop 
[python-ternary](https://github.com/marcharper/python-ternary) (I created a 
new technique to shade ternary diagrams that worked better for my data).

 <p align="center">
<img src="../images/resized/ternary_with_L.png" width="800">
</p>

### [expansion_powerlaw_fit](https://github.com/Range-Expansions/expansion_powerlaw_fit)

As a physicist, I am often interested in studying fluctuations 
around deterministic trends in time-traces. Based on the algorithm discussed in the materials and 
methods of [this paper](http://www.pnas.org/cgi/doi/10.1073/pnas.0710150104)

### Determining the Growth Rate of Microbes

In order to determine how fast microbes divide (most microbes don't have sex
to reproduce; they just create clones of themselves via "budding"), scientists usually grows 
microbes in a small glass filled with transparent nutritious media. 
As the microbes grow, the media becomes  "murky" and more opaque; it is thus possible to extract the 
growth rate of microbes in culture by measuring how much light is absorbed by the media vs. time.

My colleague @nwespe and I (Nichole is now an insight data science fellow!) wrote the Python package
[OD_growth_finder](https://github.com/btweinstein/OD_growth_finder) to 
extract growth rates of microbes from absorbance data. The package heavily utilized `pandas`
and `numpy`, as modern machines to obtain absorbance data ("Plate Readers") obtain data from many growing
cultures of microbes at once, resulting in data that is naturally tabular. See the linked
[IPython Notebook](https://github.com/btweinstein/OD_growth_finder/blob/master/OD_growth_analyzer_example.ipynb)
for an idea what the package can do. Below is a plot I created using the package illustrating
how adding an antibiotic (cyclohexamide) to a microbial culture will slow their growth and that,
unsurprisingly, adding the drug in higher concentration slows their growth more.

 <p align="center">
<img src="../images/resized/cyclo_room.png" width="600">
</p>

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