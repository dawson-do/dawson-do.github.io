---
layout: page
title: Spectral Ray Tracing
---
### CS 184/284A Spring 2024: Final Project

![Renders](/assets/spectral/images/final_renders.png)

[paper](/assets/spectral/Spectral_Raytracing.pdf) • [video](https://drive.google.com/file/d/1meLuPLVo5v9Gnn34_T2BAYmhlZy5Fjbu/view?usp=sharing) • [slides](/assets/spectral/CS284_FinalSlides_Team30.pdf)

##### Abstract
In this project, we write a ray tracer that includes spectral information about rays within the light field. A traditional ray tracer tracks RGB intensities along the ray and propagates the ray using RGB information about scene elements. In reality, light is distributed by wavelength in a continuous space, with visible light occupying the range approximately from 400 nm to 700 nm. Optical phenomena arise from wavelength-dependent interactions, including dispersion, iridescence, and reflection probability. In this project, we refactor the ray tracer we wrote in Homework 3 to incorporate wavelength dependence by adding a layer of wavelength sampling. We also implement scene elements that leverage this feature, including glass materials, mirror surfaces, microfacet surfaces, thin films, and black body emitters. With these, we can create striking photorealistic scenes accessible only through spectral information.

Out of ~80 other projects, we got an [honorable mention](https://cs184.eecs.berkeley.edu/sp24/docs/final_showcase)!

### Figures

| ![Two renders of a bunny, showing the effect of parameter B on the color of light refracted through glass.](/assets/spectral/images/bunny_compare.png) |
|:--:|
| Left, bunny rendered with non-dispersive glass. Right, bunny rendered with dispersive glass. |

| ![Example render showing the color differences between RGB rendering and spectral sampling for microfacet copper.](/assets/spectral/images/copper_dragon_compare.png) |
|:--:|
| CBdragon with copper surface. On the left, RGB upsampled microfacet BSDF. On the right, spectral microfacet BSDF. |

| ![Soap films on PVC and Copper with film thicknesses given on the left.](/assets/spectral/images/dragon_irid_pvc-cu.png) |
|:--:|
| Soap films on PVC and Copper with film thicknesses given on the left. |

| ![Actual colors of tempered steel at certain temperatures.](/assets/spectral/images/Tempering_standards_used_in_blacksmithing.jpg){: width="80%"} ![Dragons with a color gradient corresponding to the colors of tempered steel.](/assets/spectral/images/dragon_thin_fe_64.png){: width="40%"} ![Dragons with a color gradient corresponding to the colors of tempered steel.](/assets/spectral/images/dragon_cthin_fe_64.png){: width="40%"} |
|:--:|
| Iron oxide film on iron dragons, compared to a real reference of tempered steel [Wikipedia](https://en.wikipedia.org/wiki/Tempering_(metallurgy)). The left dragon uses varying refraction index from [RefractionIndex.info](https://refractiveindex.info/?shelf=main&book=Fe2O3), the right dragon uses constant refractive index, similar to Belcour and Barla, 2017.|

| ![Two soap bubbles against a white background with iridescent effects.](/assets/spectral/images/soap2_512.png){: width=""} |
|:--:|
| Soap bubbles modeled using a film on a vacuum. The foreground and background bubbles have a thickness of 500 nm and 350 nm, respectively. |

| ![Example render showing the color differences between black bodies at two different temperatures.](/assets/spectral/images/blackbody_compare.png){: width=""} |
|:--:|
| CBspheres with a black body area light temperature at 3000 K (left) and 12000 K (right). |

### Extras

![Metal bunny with bubbles and prism](/assets/spectral/images/prism_rab2.png){: width="48%"}
![Metal bunny with prism](/assets/spectral/images/prism_rab_2048.png){: width="48%"}
![Refractive diamond](/assets/spectral/images/diamond_cauchy_2048.png){: width="48%"}
![Refractive bunny](/assets/spectral/images/bunny_cauchy_1024.png){: width="48%"}
![Iridescent film on a metal dragon](/assets/spectral/images/dragon_thin750_water_128.png){: width="48%"}
![Iridescent film on a plastic dragon](/assets/spectral/images/dragon_cthin500_waterpvc.png){: width="48%"}
![Soap bubble and glass ball with film](/assets/spectral/images/soap_glass_1024.png){: width="48%"}
![Glass coil with film under 3000 K black body emitter](/assets/spectral/images/coil_thin550_glass_512.png){: width="48%"}
