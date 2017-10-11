---
layout: page
title: Research
permalink: /research/
weight: 1
---

My PhD focused on experimentally, theoretically, and numerically investigating how  different forms of transport impact the evolutionary dynamics of growing microbial colonies. As evolution is *random,* I extensively utilized probabilistic random-walk based techniques to model and describe my experiments. Stochastic processes are often modeled via stochastic differential equations (SDEs). 

My work required the use of *spatially extended* SDE's, as I had to take into account the transport  opposed to many stochastic processes that can be modeled via a stochastic differential equation, my problem was slightly more challenging: I had to take into account the *spatial* structure of the colony, and thus had to couple the local  

of  I learned how to work with stochastic differential equations and all sorts of probabilistic ideas and calculus. These were slightly harder, however; they were *spatial* stochastic differential equations!

# Range Expansions: Diffusive Growth and Evolution

The standard experiment I conducted was quite simple. I took multiple identical strains of *E. coli* differing only by the fluroescent protein they produced (their color), mixed them together in growth media, and deposited the media onto the surface of a nutritious agar plate in a small circular droplet roughly 2mm in diameter. Once on the agar surface, the *E. coli* use the local nutrients to grow and proliferate (*E. coli* reproduce by creating clones of themselves, or budding; they do not have sex). The growth of a population into virgin territory is called a **range expansion**.

The movie below show the growth of three strains of E. coli on an agar plate after initial inoculation. Naively, one would expect that as the colony grows, the different strains of E. coli would remain mixed resulting in a blend of all the colors. Surprisingly, past a certain radius, the colony segregates into one local color, forming beautiful patterns.What is the source of this phenomena? The *E. coli* are not doing anything strange: they simply grow and divide at roughly the same rate.

<p align="center">
<iframe src="https://drive.google.com/file/d/0ByRswVj1mkw-N29QMHM1Q2lWTXc/preview" width="600" height="350"></iframe>
</p>

Similar patterns can be seen in different geometries. In the below movie, I again inoculated three different colored strains of *E. coli* in equal proportions on a strip of filter paper. I placed the filter paper on an agar plate and imaged the colony growing. 

<p align="center">
<iframe src="https://drive.google.com/file/d/0ByRswVj1mkw-c3lYMHZ1b0JKUW8/preview" width="600" height="200"></iframe>
</p>

My PhD focused on understanding these patterns. I created many GitHub repositories and IPython Notebooks to quantify the results of my experiments (see the [Computation](/computation) page). Ultimately, it can be shown that these patterns are created because of the small population size in the thin growing layer at the front of the colony. A layer of about 5 to 10 cells are actively growing at the front of the colony at any time. If, by chance, several red cell divides before others nearby, there is a chance that the red cells will take over.


# Advection and its impact on Evolution


