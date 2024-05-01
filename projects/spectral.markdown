---
layout: page
title: Spectral Ray Tracing
---
### CS 184/284A Spring 2024: Final Project

![Renders](/assets/spectral/images/final_renders.png)

[paper](/assets/spectral/Spectral_Raytracing.pdf) • [video]() • [slides]()

##### Abstract
In this project, we write a ray tracer that includes spectral information about rays within the light field. A traditional ray tracer tracks RGB intensities along the ray and propagates the ray using RGB information about scene elements. In reality, light is distributed by wavelength in a continuous space, with visible light occupying the range approximately from 400 nm to 700 nm. Optical phenomena arise from wavelength-dependent interactions, including dispersion, iridescence, and reflection probability. In this project, we refactor the ray tracer we wrote in Homework 3 to incorporate wavelength dependence by adding a layer of wavelength sampling. We also implement scene elements that leverage this feature, including glass materials, mirror surfaces, microfacet surfaces, thin films, and black body emitters. With these, we can create striking photorealistic scenes accessible only through spectral information.

### Figures

| ![Two renders of a bunny, showing the effect of parameter B on the color of light refracted through glass.](/assets/spectral/images/bunny_compare.png){: width="33%" } |
|:--:|
| Top, bunny rendered with non-dispersive glass. Bottom, bunny rendered with dispersive glass. |

<figure>
  <img src="{{site.url}}/assets/spectral/images/copper_dragon_compare.png" alt="Example render showing the color differences between RGB rendering and spectral sampling for microfacet copper."  width="33%"/>
  <figcaption>CBdragon with copper surface. On the left, RGB up-sampled microfacet BSDF. On the right, spectral microfacet BSDF.</figcaption>
</figure>

<figure>
  <img src="{{site.url}}/assets/spectral/images/dragon_irid_pvc-cu.png" alt="Soap films on PVC and Copper with film thicknesses given on the left."  width="33%"/>
  <figcaption>CBdragon with copper surface. On the left, RGB up-sampled microfacet BSDF. On the right, spectral microfacet BSDF.</figcaption>
</figure>

<figure>
  <img src="{{site.url}}/assets/spectral/images/soap2_512.png" alt="Two soap bubbles against a white background with iridescent effects."  width="33%"/>
  <figcaption>Soap bubbles modeled using a film on a vacuum. The foreground and background bubbles have a thickness of 500 nm and 350 nm, respectively.</figcaption>
</figure>

<figure>
  <img src="{{site.url}}/assets/spectral/images/blackbody_compare.png" alt="Example render showing the color differences between black bodies at two different temperatures."  width="33%"/>
  <figcaption>CBspheres with a black body area light temperature at 3000 K (left) and 12000 K (right).</figcaption>
</figure>

### Extras
