---
title: Literature Review of Numerical Simulation and Optimisation of the Shot Peening Process
author: Jun S. Chen, Dawood A. Desai, Stephan P. Heyns, Francesco Pietra
date: March 2019
site: https://doi.org/10.1177/1687814018818277
tags: review numerical-model hardening residual-stress-field
bibliography: biblio.bib
link-citations: true
---
<script type="text/javascript"
        src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS_CHTML">
</script>
<script type="text/x-mathjax-config">
	MathJax.Ajax.config.path["Extra"] = "https://jmanthony3.github.io/Codes/MathJax/extensions/TeX",
	MathJax.Hub.Config({
		TeX: {
			equationNumbers: {
				autoNumber: "AMS"
			},
			extensions: [
				"[Extra]/Taylor.js",
				"[Extra]/NumericalMethods.js"
			]
		},
		tex2jax: {
			inlineMath: [["$", "$"], ["\\(", "\\)"]],
			blockMath: [["$$", "$$"], ["\\[", "\\]"]],
		},
});
</script>
<!-- %%%%%%%% Document Metadata %%%%%%%% -->
# Literature Review of Numerical Simulation and Optimisation of the Shot Peening Process

Date Created: October 07, 2021

- [Literature Review of Numerical Simulation and Optimisation of the Shot Peening Process](#literature-review-of-numerical-simulation-and-optimisation-of-the-shot-peening-process)
	- [Annotations](#annotations)
	- [Figures](#figures)
	- [Abstract](#abstract)
	- [Notes](#notes)
		- [Source Subtitle](#source-subtitle)
<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->





<!-- START WRITING BELOW -->





<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->
## Annotations
Simulations recently done well to include randomness of shot and not exclude consideration for [[strain-rate]] sensitivity, cyclic behaviors ([[fatigue]]), and the [[Bauschinger-Effect]]; however, models exclude special focus on [[material-hardening]]. Review believes combination of genetic algorithms to optimize parameters and [[residual-stress]] approximations may soon converge. **Appropriate to apply [[elastoviscoplastic]] [[work-hardening]] effects.** [[friction]] effects have yet to be discussed?? **Area-averaging numerical evaluations of [[residual-stress]] most accurate!!** Each method for [[strain-hardening]] are context specific: their validity is not universal. Numerical optimizations have focused on [[surface-roughness]] and [[cold-working]].

<dl>
<dt><strong>Material Hardening</strong></dt>
<dd>Material hardness enhancement, which has yet to be set as an objective function to optimize [[residual-stress]].</dd>
</dl>

>The models used in simulation are generally different from those in optimisation. <cite> chen2019

>**We want to simulate the actual experiment!** <cite> JMA3

Sources of Note:
- *insert text here $\dots$*

## Figures

## Abstract
This work provides a comprehensive review of numerical simulation and optimisation of the shot peening found in the existing literature over the past 10 years. The review found that the developed numerical models coupling finite elements with discrete elements became increasingly mature and showed their advantages in incorporating flow behaviour and randomness of shots. High emphasis must be placed on the constitutive equations of target material where its strain-rate sensitivity, cyclic behaviour and Bauschinger effects are recommended to be incorporated in the numerical material model simultaneously since considering one of them in isolation may lead to unreliable distribution of residual stresses. Furthermore, material hardening is a critical benefit of shot peening; however, it has not received its deserved attention from the existing investigations, neither in simulation nor in optimisation. The study found that intensity and coverage are two critical control parameters recommended to be constraints for optimisation of shot peening. Finally, this work also found that developed heuristic algorithms, such as genetic algorithms have recently showed their advantages for searching optimal combinations of peening parameters. It is plausible that in the near future, the synergy of combining these algorithms with approximation models can be expected to gain more attention by researchers.

## Notes
*insert text here$\dots$*

### Source Subtitle
*insert text here$\dots$*

\bibliography
<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->





<!-- %%%%%%%% End Document %%%%%%%% -->