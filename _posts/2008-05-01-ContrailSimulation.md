---
layout: post
title: Contrail Simulation
description: Numerical simulation of a condensation trail evolution and its interaction with the atmospheric turbulence  
thumbnail: "/data/ContrailSimulation/contrailSimulation_thumbnail2.png"
tags: [modelling]
---

{% include image.html file="/data/ContrailSimulation/contrail_example.jpg" alt="contrail Boeing 747" caption= "example of the formation of a contrail behind a Boeing 747." %}

This is an overview of the work I did during my PhD which was on a complete different scientific topic than the current wildfire related works I am involved in. The subject of my PhD was the simulation of condensation trail (contrail) formed behind cruising aircraft. References related to this work are listed at the end of this page.

Due to the rapid growth of commercial air traffic started in the 90's, the environmental impact of aircraft emissions has become now a topic of academic research and practical interest in the community of atmospheric chemistry modelers. The incorporation of these emissions into climate models is a difficult task because of the complex physical and
chemical transformations occurring in the plume of the aircraft, and the large range of
scales involved. The objective of my PhD was two-fold : the first one is to contribute to the elaboration of a new parameterization that models the effect of non-linear aircraft plume NOx chemistry on atmospheric ozone. The second objective is to evaluate the distribution of ice particles within the contrails in order to quantify their radiative impact.
To this end, I developed with the help of my supervisors Daniel Cariolle and Roberto Paoli a numerical model of the dynamical and microphysical processes of a generic contrail, from its early phase of formation up to its interaction with the atmosphere. It is based on the MesoNH model coupled with a specific microphysical module. Afterwards, we analyzed in detail the vortex regime up to 340 s after emission time, and performed the first simulation to date of the following diffusion regime where the plume interacts with atmospheric turbulence.

In the first vortex regime, the model reproduces the main features of the wake dynamics (such as formation of vorticity ring, linear growth of the short and long wavelength instabilities, formation of a secondary wake induced by the baroclinic torque) and an evolution of the ice particle distribution in good agreement with the measurements obtained for young contrail (see animation below).
{% include youtubePlayer.html id="i3ZMzEAqxqY" label="evolution of ice particle during the vortex regime"%}

In the diffusion regime, we force the model simulation with a synthetic sustained turbulent flow that mimics the real atmospheric turbulence at the tropopause level. The contrail simulation was run up to 30 min, and the results are in good agreement with the available experimental data, which validates, a posteriori, the simulation strategy adopted through this work. (see animation below)
{% include youtubePlayer.html id="3arAiORYG1U" label="evolution of ice supersaturation during the diffusion regime"%}

Finally, it is concluded that our model is suitable to evaluate in the future the impacts of aircraft emission on the atmospheric chemistry and radiative balance.

### References:
- Paugam, R., Paoli, R., and Cariolle, D.: Influence of vortex dynamics and atmospheric turbulence on the early evolution of a contrail, Atmos. Chem. Phys., 10, 3933-3952, [doi](https://doi.org/10.5194/acp-10-3933-2010), 2010.
- Paugam,  R.: Simulation numerique de l’ ́evolution d’une traınee de condensation et de son interaction avec la turbulence atmospherique, Ph.D. thesis, Ecole Centrale Paris - CERFACS, 2008. [link](https://tel.archives-ouvertes.fr/tel-01666360)
