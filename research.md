---
layout: page
title: Research
permalink: /research/
weight: 1
---

My PhD focused on experimentally, analytically, and numerically investigating how  different forms of transport impact the evolutionary dynamics of growing microbial colonies. As evolution is *random,* I extensively utilized probabilistic techniques to analytically model and numerically simulate my experiments. The GitHub repositories and IPython Notebooks that I developed to analyze my experimental data and create scientific simulations can be seen on the [Computation](/computation) page.

<p align="center">
<img src="../images/resized/me_pipetting_cropped.jpg" width="300">
</p>


## Diffusive Growth and Evolution

### Experimental Setup

The standard experiment I conducted in the laboratory was quite simple. I took multiple identical strains of *E. coli* differing only by the fluroescent protein they produced (their color), mixed them together in growth media, and deposited the media onto the surface of a nutritious agar plate in a small circular droplet roughly 2mm in diameter. Once on the agar surface, the *E. coli* use the local nutrients to grow and proliferate (*E. coli* reproduce by creating clones of themselves, or budding; they do not have sex). The growth of a population into virgin territory is called a *range expansion*. 

The wiggling (i.e. diffusion) of the *E. coli* on the agar plate coupled with their growth results in the colony expanding. The movie below show the growth of three strains of E. coli on an agar plate after initial inoculation. Naively, one would expect that as the colony grows, the different strains of E. coli would remain mixed resulting in a blend of all the colors. Surprisingly, past a certain radius, the colony segregates into one local color, forming beautiful patterns. My PhD focused on understanding these patterns and consequently the evolutionary dynamics of microbial colonies. I created many GitHub repositories and IPython Notebooks to quantify the results of my experiments (see the [Data Analysis](/computation/data_analysis) page).

<p align="center">
<iframe src="https://drive.google.com/file/d/0ByRswVj1mkw-N29QMHM1Q2lWTXc/preview" width="600" height="350"></iframe>
</p>

Similar patterns can be seen in different geometries. In the below movie, I again inoculated three different colored strains of *E. coli* in equal proportions on a strip of filter paper. I placed the filter paper on an agar plate and imaged the colony growing. 

<p align="center">
<iframe src="https://drive.google.com/file/d/0ByRswVj1mkw-c3lYMHZ1b0JKUW8/preview" width="600" height="200"></iframe>
</p>

### Models of Growth 

Why do these patterns form? The *E. coli* in our experiments are not doing anything strange: they simply grow and divide at roughly the same rate. Ultimately, it can be shown that the patterns are created because the small population size of the thin growing layer at the front of the colony magnifies stochastic number fluctuations. 

A layer of about 5 to 10 cells are actively growing at the front of the colony at any time. If, by chance, several red cell divides before others nearby, there is a good that the red cells will take over if the local population size is small. A standard mathematical model to describe two competing strains (i.e. the red and blue color) in a colony is the "Stochastic Fisher-Kolmogorov-Petrovsky-Piscounov" (FKPP) equation and can be expressed as

$$ \frac{\partial}{\partial t} f(\vec{x},t) = D \nabla^2 f(\vec{x},t) + sf(1-f) + \sqrt{\frac{f(1-f)}{N}} \zeta(\vec{x}, t)$$

$$f$$ describes the population density of one of the two strains as a function of space $$\vec{x}$$ and time $$t$$. The population, due to the wiggling of *E. coli*, diffuses with a diffusion constant $$D$$ and grows at a rate specified by $$s$$. Due to overcrowding, the population saturates at a density of $$f=1$$. The final term is the most interesting and describes how *stochasticity* impacts the evolution of the colony. $$N$$ describes how many cells locally compete at the front of a colony, and $$\zeta(\vec{x},t)$$ is Gaussian white noise with mean zero and variance 1 and is distributed over space with the property that 

$$\langle \zeta(\vec{x},t) \zeta(\vec{x}',t') \rangle = \delta(\vec{x} - \vec{x}') \delta(t - t')$$

As $$N$$ decreases, i.e. the growing colony layer becomes more thin, the stochastic term on the farm right becomes larger and larger. If stochastic term on the far right is large, fluctuations in the local population density of a certain strain color will be large, and the absorbing points $$f=0$$ or $$f=1$$ will be randomly reached, resulting in the total dominance or exctinction of a color locally. 


An image from a numerical simulation of the SKFPP equation that I created is shown below. I used this equation and various model analogs through my PhD to model my experiments; my simulation GitHub repositories can seen in the [Scientific Computing](/computation/scientific_computing) page. The SKFPP equation is trickier to work with than typical stochastic differential equations because of the *spatial diffusion* term ($$D$$); the local growth and competition between the strains is coupled with their diffusive transport. 

<p align="center">
<img src="../images/resized/random_undulation_expansion.png" width="300">
</p>

### My first paper: Many Colored Strains with Differing Growth Velocities in a Range Expansion

See it [here](https://www.biorxiv.org/content/early/2017/06/07/145631). It is submitted and we are working on some revisions now.

## Advective Transport and Evolution

### Experiments with a Viscous Fluid

Many organisms do not live on solid surfaces; they instead live in liquid environments, such as fish or phytoplankton in the ocean. In the ocean, a new form of transport is introduced: *advection*, or the transport of material by fluid flow. How does advection couple with the diffusive-induced growth discussed above to alter the evolutionary dynamics of populations?

To the best of my knowledge, nobody has created an easy-to-use, well-controlled laboratory system to study this question. I teamed up with my colleague [Severine Atis](https://scholar.harvard.edu/atis) to solve this problem. We created a viscous fluid with a viscosity 20 times that of honey (roughly $$50 \hspace{1pt}  \mathrm{Pa} \cdot \mathrm{s}$$). The fluid was viscous enough that environmental perturbations (i.e. accidentally bumping the container) did not cause it to appreciably move. It was also viscous enough that we could pump it using syringe pumps in a controlled manner at the speed at which microbes expanded (roughly 30 $$\mathrm{\mu m / hour}$$). An image of the fluid slowly creeping down the side of a bottle can be seen below. 

<p align="center">
<img src="../images/resized/viscous_media.jpg" width="200">
</p>

 
We repeated the same protocol as before: we poured the viscous media in a petri dish and inoculated different colored strains of microbes on its surface; we then imaged the microbes growing. For these experiments, we used the Baker's yeast *Saccharomyces cerevisiae*. The media was so viscous that the deposited microbes settled to its bottom over the course of weeks; they effectively lived on the surface of the media.

As expected, the morphology of growth was impacted by growing on a fluid rather than a solid. Surprisingly, however, colonies growing on our fluid  
