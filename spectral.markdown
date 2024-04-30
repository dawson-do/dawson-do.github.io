---
layout: page
title: Spectral Ray Tracing
permalink: /spectral/
---
### CS 184/284A Spring 2024: Final Project

![Renders](/assets/spectral/images/final_renders.png)

[paper](/assets/spectral/Spectral_Raytracing.pdf) • [code]() • [video]() • [slides]()

##### Abstract
In this project, we write a ray tracer that includes spectral information about rays within the light field. A traditional ray tracer tracks RGB intensities along the ray and propagates the ray using RGB information about scene elements. In reality, light is distributed by wavelength in a continuous space, with visible light occupying the range approximately from 400 nm to 700 nm. Optical phenomena arise from wavelength-dependent interactions, including dispersion, iridescence, and reflection probability. In this project, we refactor the ray tracer we wrote in Homework 3 to incorporate wavelength dependence by adding a layer of wavelength sampling. We also implement scene elements that leverage this feature, including glass materials, mirror surfaces, microfacet surfaces, thin films, and black body emitters. With these, we can create striking photorealistic scenes accessible only through spectral information.

### Image Gallery
