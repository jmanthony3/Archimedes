<!-- 211029 -->
# Solution and Second-Phase Strengthening

## Elastic Interactions
### Introduction
Our treatment of metals and the defects within them has been primarily concerned with pure metals.
The vast majority of "real" metals are alloys, and the role of alloying elements can be multi-faceted.
The way alloying elements interact with dislocations depends on their size, what position they take in the lattice, and the amount (concentration) of those elements.


### Substitutionals versus Interstitials
[[substitutionals]]
: The alloying element takes the lattice site of the matrix metal.
- Solvent: majority element in alloy.
- Solute: minority element(s) in alloy.
- | ![](../../../attachments/engr-839-001-mechanical-metallurgy/substitutional_versus_interstitials_211029_182341_EST.png) |
|:--:|
| For example, in Cu-Zn, the zinc atoms, [[solute]] take the place of copper, [[solvent]]. |

Alloying has a solid solution form, such that no precipitation of segregation of elements occur.
[[Hume-Rothery-Rules]] apply in guiding whether elements stay in solution, practically speaking.


### [Elastic Misfit](elastic-misfit.md)


### Stress Fields in Polar Coordinates
Recalling Fig. \ref{fig:edge_dislocation_stress_equation_example} for [[edge-dislocations]]: $\begin{bmatrix}
-\frac{G\vec{b}\chi_{2}(3\chi_{1}^{2} + \chi_{2}^{2})}{2\pi(1 - \nu)(\chi_{1}^{2} + \chi_{2}^{2})^{2}} & \frac{G\vec{b}\chi_{2}(\chi_{1}^{2} + \chi_{2}^{2})}{2\pi(1 - \nu)(\chi_{1}^{2} + \chi_{2}^{2})^{2}} & -\frac{G\vec{b}\chi_{2}\nu}{\pi(1 - \nu)(\chi_{1}^{2} + \chi_{2}^{2})} \\
\frac{G\vec{b}\chi_{1}(\chi_{1}^{2} + \chi_{2}^{2})}{2\pi(1 - \nu)(\chi_{1}^{2} + \chi_{2}^{2})^{2}}
\end{bmatrix}$ yields:

$$\begin{split}
\sigma_{rr} = \sigma_{\theta\theta} &= -\frac{G\vec{b}}{2\pi(1 - \nu)}\frac{\sin(\theta)}{r} \\
\sigma_{zz} &= -\frac{\nu G\vec{b}}{\pi(1 - \nu)}{\sin(\theta)}{r} \\
\sigma_{r\theta} &= -\frac{G\vec{b}}{2\pi(1 - \nu)}\frac{\cos(\theta)}{r} \\
\sigma_{\theta z} &= \sigma_{zr} = 0 \\
\sigma_{p} &= \frac{1 + \nu}{1 - \nu}\frac{G\vec{b}}{3\pi}{\sin(\theta)}{r}
\end{split}$$

| ![](../../../attachments/engr-839-001-mechanical-metallurgy/stress_field_in_polar_coordinates_211029_184041_EST.png) |
|:--:|
| Recall that the stress field is loosely related to $5\vec{b}$. If you can squish smaller atoms into the solute, then the smaller atoms want to rise to the top of the dislocation which minimizes the local stress to straighten the dislocation. |



### Interaction Energy
As described by Eshelby:
$$\begin{equation}
\begin{split}
U_{int} &= V\sigma_{ij}(\epsilon_{ij})_{T} \\
U_{misfit} &= \sigma_{p}\Delta V = \frac{1 + \nu}{1 - \nu}\frac{G\vec{b}}{3\pi}\frac{\sin(\theta)}{r}4\pi\epsilon r_{0}^{3} = A\frac{\sin(\theta)}{r} \\
A &= \frac{4}{3}\frac{1 + \nu}{1 - \nu}G\vec{b}\epsilon r_{0}^{3}
\end{split}
\end{equation}$$


### Interaction Force
$$\begin{equation}
\begin{split}
F &= -\frac{\partial U_{misfit}}{\partial r} \\
 &= A\frac{\sin(\theta)}{r^{2}}
\end{split}
\end{equation}$$

Force from derivative of energy wrt distance from dislocation (Eq. \eqref{eq:interaction_force}).
This is true for the area surrounding the [[dislocation-core]].

!!! tip [[interaction-energy]] is positiv above the [[slip-plane]].


### Dislocation Pinning
The number of [[solute]] atoms near the dislocation determines how strongly the dislocation is prevented from moving.
Using the [[Peach-Koehler-Equation]] (Eq. \eqref{eq:peach_koehler_equation}) with solute spacing, $L$ and distance from dislocation, $b$, then $$\Delta\tau = \frac{F_{max}{bL}} = A\frac{\sin(\theta)}{r^{2}bL}$$
The linear dispersion of solute preferred along [[dislocation-density]], $\rho$... 


### Screw Dislocations and Interstitials
!!! attention
    No [[hydrostatic-stress]] on [[screw-dislocations]].

$$\begin{equation}
U_{misfit} = \dots
\end{split}
\end{equation}$$
\label{eq:screw_dislocation_misfit}

[[interstitials]] do not dilate the structure like [[substitutionals]] where $\epsilon_{11} = \epsilon_{22} = \epsilon_{33} = 0$.
Instead, interstitial misfit is found by ...


### Example from Research
Dr. Atwater found by experiment that placing antimony at the grain boundary of copper lost the nanograins to the boundary near $400^{\circ}C$ and not the $900^{\circ}C$ from numerical simulations (Thermal Stability of Nanocrystalline Copper Alloyed with Antimony).

$$\begin{split}
\Delta H_{el, vol} &= \frac{-2N_{Av}K_{Sb}G_{Cu}(V_{Sb} - V_{Cu})^{2}}{3K_{Sb}V_{Cu} + 4G_{Cu}V_{Sb}} \\
\Delta H_{el, rad} &= \frac{-24\pi N_{Av}K_{Sb}G_{Cu}r_{Cu}r_{Sb}(r_{Sb} - r_{Cu})^{2}}{\dots 3K_{Sb}V_{Cu} + 4G_{Cu}V_{Sb}}
\end{split}$$


### Summary
Solid solution strengthening is an important benefit of alloying.
The concentration of solute ...



<!-- 211105 -->
## Dislocation-Solute Interactions
Solutes affect [[dislocation-mobility]].
[[stress-strain]] curves may be useful to determine the bulk effect and importance to processing.
Phenomena of [[dislocation-solute-interaction]] and their parameters determine the magnitude of their influence.


### Introduction
Every impoerfection in a crystal has some stress field associated with it.
Pure, single crystals are "perfect", but could still include other dislocations.
Point defects are [[interstitials]].
Overall energy can be lowered by [[diffusion]] to tensile side of dislocation.
This enriched area is a localized "atmosphere" that causes a dislocation to be "trapped".
The usefuleness and drawbacks of this behavior can be understood through alloy and processing decisions.


### Upper/Lower Yield Phenomenon
Low carbon steels exhibit a differential yield stress, characterized by a lower stress plateau (not a common curve).
This is caused by a Cottrell atmosphere around a dislocation that locks the dislocation in place: [[interstitials]] diffuse to the [[dislocation-core]] to reduce stress.
The effect is most pronounced when the mobility of solute atoms and dislocations is similar: modest temperature required for [[diffusion]] to occur, but not rapidly.

| ![](../../../attachments/engr-839-001-mechanical-metallurgy/solute_motion_211108_214228_EST.png) |
|:--:|
| The stress required to break them must exceed the yield strength; therefore, the stress will reduce once broken. However, this stress is higher than that required to move them. A solute will want to stick with the dislocation. This could be thought of as [[work-softening]]. |

If they do are not locked together, then the yield would be the typical yield stress of material.
The book often refers to "removing the yield point" does not mean there is no yielding, only that there is upper-yield point.
==Solutes pin dislocations because of overlapping stress fields.==
Solutes need time to diffuse to dislocation for this to work.
Once the solute breaks free, it will not immediately go to another dislocation during motion.
Once stopped and given sufficient time, then the solute will diffuse.

Aging
: Typically means that some material was precipitate hardened.

The applied stress is greater than required to move dislocations, but is less than what is needed to unlock the dislocation from the solute: think similarly to other [[dislocation-obstacles]] where the dislocation would move if it could.
The effect of [[substitutionals]] is limited in this regard and requires higher temperature to permit reasonable [[diffusion-rate]].
A solute "atmosphere" may also be called something similar: e.g. [[Cottrell-Bilby-Cloud]].
These solutes have no reason to remain orderly which is essentially an [[interstitials]] problem: think [[Second-Law-of-Thermodynamics]].


### Luders Banding
The lower yield plateau exhibits an irregular stress, fluctuating around an average value.
The strain during this stage is referred to as yield point elongations.
This behavior is governed by the formation of [[deformation-bands]] ([[Luders-bands]]) where the material yields locally.
As the strain increases, the bands multiply and the yielded volume extend through the sample.
www.vimeo.com/4586024
*Starts off all clean, smooth, and polished, but these bands began to form under deformation along the preferential shear directions.
These bands extend across the whole cross-section.
Does not matter if angled down-left versus down-right: once one band forms, the stress field resolves to the same direction.*

Once fully accumulated, the [[stress-strain]] behavior takes a more normal [[strain-hardening]] character.
This behavior is problematic for the geometrical perturbations it causes, especially in thin components.
It can be reduced through 1) alloying: adding elements that will react with [[interstitials]] and bind them in a compound, or 2) pre-straining: deforming the material past the lower yield point so that is behaves uniformly in further deformation.


### Strain Aging
When you break free of the solute but not quite totally.
Dislocations have moved, but there is a hardening effect: usually in terms of precipitates present in alloys by heating and then giving time for diffusion of precipitation.
This is the return of solutes through strain so far past the yield point, but then relax from loading.
While the component sits on the shelf, carbon has time to diffuse to dislocations which hardens the material again.
If held under constant stress, then this process happens much quicker to enhance diffusion.
Pre-strained materials cannot be left that way for a long time: the material must be strained again.


### Dynamic Strain Aging
Dislocations broke free, but carbon caught up over time.
In this instance, the solute atoms can actually keep up with the dislocations: the dislocations are not moving that fast.
The solutes have higher mobility than the dislocations which are repeatedly pinned hardening and leading to higher tensile strength.
Higher temperatures for higher diffusion rates that the solute moves with the dislocation.
This does not affect yield, per se, mainly the ultimate tensile strength.

!!! summary Solute-Dislocation Motion Relationships
    - Solutes are pinned to dislocations which break free at the lower yield.
    - Dislocations freed from pinning solutes, but the solutes return over time: strain aging.
    - Solutes keep up with dislocation: dynamic strain aging.
    - Or some mix of these.


### Stress-Strain Serration
The "serrated" appearance in a [[stress-strain]] curve (sometimes seen in twinning experiments) can be described by various mechanisms of deformation: [[twinning]], martensitic transformation, and intermittent pinning of dislocations.
This is known at the [[Portevin-Le-Chatelier-Effect]].
This depends on [[dislocation-density]], [[solute-concentration]], [[strain-rate]], etcetera.


### Snoek Effect
This describes the effect of uniaxial stress on [[interstitials]] (internal friction).
With [[poissons-ratio]] in mind, a stress on one axis will result in different stresses on the other axes.
A *z-axis* stress will increase the *z-axis* [[interstitial-volume]] and contract the *x* and *y*.
This only occurs for loading that results in differential effect: e.g. not for $(111)$ loading.
[[interstitials]], which are regular site atoms and not those pinning dislocations, will then move to the more spacious location on *z*.
Can be measured with torsional pendulum:

$$\begin{split}
\tan(\delta) &= \frac{\log(\text{decrement})}{\pi} = Q^{-1} \\
 &= \frac{\ln(\frac{1}{n})}{\pi vt}
\end{split}$$

| ![](../../../attachments/engr-839-001-mechanical-metallurgy/snoek_effect_with_torsional_pendulum_example_211109_132842_EST.png) |
|:--:|
| Contractions within the *xy-plane* forces [[interstitials]] to the larger spaces along the *z-axis*: internal friction. This is similar to [[hydrogen-embrittlement]] or cast metals. Distributions of carbon vary when material is stressed. The number of cycles and rate of decay goes into the $\ln(\text{decrement})$. |


### Blue Brittleness
Dislocations are moving and solutes pin them, but the dislocations break free (similar to dynamic aging).
However, this is a special case: within a specific temperature range the solute atoms will outpace the dislocations and induce dynamic strain aging.
This lowers the ductility and increases the yield strength by dynamically pinning the dislocations.
This is a special case of [[Portevin-Le-Chatelier-Effect]].


### Summary
Dislocation and solute interactions of alloys have decisive effects on the mechanical properties.
Temperature affects diffusion rate and strain rate determine rate of dislocation motion versus solute motion.
**If, in the formulation of your *Critical Review*, you make an outline of what you want to say, then you can simply plug-n-play.**



<!-- 211108 -->
## Precipitation and Dispersion Strengthening
*(Absolutely no math in this section.)*


### Precipitation Hardening
Formation of a second phase by the separation or concentration of elements from the homogeneous mixture.
Only select alloys can precipitation hardene, and the most important commercial alloys are based on aluminum and nick
Aluminum alloys yield lightweight yet strong structural materials, and nickel alloys provide strong, heat-resistant options.
The way elements separate from the mix (size, shape, location, etcetera) is determined by chemistry and processing, and the mechanical properties follow suit.


### Precipitation Process
Basic process of [[precipitation-hardening]] involves three steps:
1. Solutionizing (Solubilization)
2. Quenching
3. Aging: reheating after quenching.

The time and temperature of these steps is determined by the alloy system, and both are important to the maximum hardness.


### Precipitation Mechanisms
The rejection of a solute from a super-saturated solution will progress through various stages.
Using Al-Cu as the archetype, the Cu will first form in clusters along Al $\{100\}$ planes: aka [[Guinier-Preston-Zones]] (#GPZ).
The zones do not have a distinct crystallographic structure at first and are coherent with the matrix lattice, though a stress field is introduced.
As the zones grow, the lattice mismatch increases until the planes are no longer fully coherent, and this required the formation of dislocations to accommodate the structure.
As the precipitates grow and assume a distinct crystallography, all coherency may be lost.
High temperature treatment may rapidly progress growth, such that early stages are effectively skipped. **This will normally happen outside of our control!**

*[GPZ]: Guinier-Preston Zone


### Composition and Temperature Effects
Additional Cu will result in more #GPZ.
Higher temperatures will accelerate precipitation.
#GPZ are quickly transformed to precipitates.
Those precipitates grow and become larger and farther apart.
This allows for [[dislocation-bowing]] around them more easily.
==Lower temperatures allow for more uniform distribution of precipitates.==


### Coherency
A second phase can exhibit varying degrees of coherency with the matrix.
The lattice spacing must be exact to exhibit full coherency (unlikely).
The more similar the phases are, the greater the degree of coherency and the greater the elastic strain is.


### Preferential Precipitate
To accommodate strain more readily, grain boundaries may be preferred sites for precipitation, thereby depleting the surrounding material from solute.
This leads to variability in properties, possibly leading to enhanced grain boundary corrosion or loss of strength.
An example is given of the consequences of solute depletion and plan ol' bad design with de Havilland Comet.



## Dispersion Strengthening
Unlike precipitates, dispersions are second particles added to a metal that are often completely different in properties and structures.
Much like other composites, the amount and characteristics of the second phase will determine the overall properties.
A dilute dispersion will maintain the metallic nature of the mixture, but it will have added strength through dislocation obstacles.
These should be small and uniformly dispersed: can be mixed in or created in situ by chemical reaction. Dispersions...



<!-- 211110 -->
## Dislocation-Particle Interactions
Introducing basic concepts of [[dislocation-particle-interactions]] and determining the primary parameters that determine how dislocations will interact with particles.
[[dislocation-bowing]] and [[dislocation-shearing]] have factors that determine the mode of passage.
Processing considerations and variations within and across compositions may be relevant to [[dislocation-particle-interactions]].


### Introduction
The inclusion of precipitates and particle dispersions is an effective way to strengthen an alloy (especially non-ferrous alloys).
Form of particles is determined by composition and processing, and that will determine the mechanical performance.
The primary factors that determine degree of strengthening are the [[particle-size]], [[volume-fraction]], and [[shear-strength]].
There is a way to minimize [[dislocation-motion]] by the presence and size of particles.


### Dislocation (Orowan) Bowing
If particles are within [[slip-plane]] of a dislocation, the dislocation will be impeded by their presence. 

\eqlab

*insert image*

Assume particles are impenetrable obstacles as basis for Orowan-model of strengthening.
Particles are incoherent with matrix such that dislocations cannot pass through any glide-plane.
Total shear stress to yield the material is then a combination of the pure matrix strength, $\tau_{m}$ and the dislocation-pinning:

\eqlabe

A more explicit treatment was subsequently developed by Ashby, where the particle radius is considered and predicts strengthening of $\sim0.5$ of the Orowan value: 

\eqlabe


### Particle Shearing
This mechanism of strengthening assumes [[dislocation-motion]] may pass through particles.
This will occur if the stress necessary to pass a dislocation through the particle is less than the stress required to bow the dislocation around the particle: a function of the particle properties and the spacing of the particles.

\eqlab

This indicates that small, hard particles (e.g. oxides, carbides, nitrides, etcetera) within a softer, metallic matrix will be more likely to be controlled by particle spacing than particle shearing.
Precipitation occurs....


### Shear Stress in Particle Cutting
IF the dislocation-glide-plane is coherent with the precipitate, then the stress needed to shear the particle will be determined by the energy of the surface created by passage of the dislocation.
Assuming a sphereical particle, the work to cut the particle in two is equivalent ot the creation of the new surface: 

\eqalign

*insert imgae*


### Volume Fraction
The higher the concentrated of the second phase, the more volume fraction there will be.
The volume fraction is determined by composition and precoessing, and size and spacing are inversley proportional.
With a uniform, cubic distribution, the volume fraction , $f$ will: 

\eqalign

*insert image*


### Considerations in Precipitation
During precipitation, there are various conformations as the solute phase(s) come out of the solution during aging.
As more particles are formed and grow, the relative abundance of them at these stages will control overall performance.
The general behavior follows the relationship: $\tau \propto \sqrt{rf}$.
As aging progresses, the radii of particles increases and the balance between bowing and shear changes: i.e.g Ostwald ripening.
The critical radius is that where the transition from shear to bowing occurs.

*insert image*

!!! note (The thermal stability of nanocrystalline copper cryogenically milled with tungsten)[https://www.sciencedirect.com/science/article/pii/S092150931201101X?via%3Dihub]
    With some leftover, "pure" copper, its hardness drops dramatically with greater annealing temperatures but less so when tungsten is allowed precipitate into the copper.
    The characterization class next fall goes into this.

    $$\begin{split}
    P &= \frac{2\gamma}{R} \\
    P_{z} &= \frac{3f\gamma}{2r} \\
    D &= \frac{4r}{3f}
    \end{split}$$

    The more heating, the more the particles want to grow.
    ==Particles directly contribute to hardness or through dislocation blocking.==
    Ideally, particles would be aligned along the major axis to the grain boundary.


### Summary
Dislocations can bow between bow or shear through particles.
Small particles and those with coherency are more likely to be sheared.
Incoherent, very hard, and larger particles are less likely to be sheared.
The spacing of particles is also critical, as bowing is easier around widely spaced particles.
The process of precipitation hardening ...
==Particles will either shear or bow, whichever is more favorable.==

!!! tip Critical Review
    Any topic covered can be discussed more than the others: not all topics need the same amount of explanation. Demonstrate your knowledge in those topics.


---


*Lecture: November 12, 2021*

!!! example (10.16) An aluminum alloy is strengthened by diffused, alumina particles with radius, $d = 15 \mu m$ at $3\\% Al_{2}O_{3}$ (weight-percent). Estimate the strength if $G_{Al} = 28 GPa$, $\rho_{Al} = 2700 \frac{kg}{m^{3}}$, and $\rho_{Al_{2}O_{3}} = 3960 \frac{kg}{m^{3}}$. Assume that there is no particle cutting.

    We want to find [[volume-fraction]]. Recall $V = \frac{m^{*}}{\rho}$.

    $$\begin{split}
    f &= \frac{(\frac{m^{*}}{\rho})_{\text{solute}}}{(\frac{m^{*}}{\rho})_{\text{solvent}} + (\frac{m^{*}}{\rho})_{\text{solute}}} \\
    &= \frac{(\frac{0.03}{3.96})}{(\frac{0.97}{2.70}) + (\frac{0.03}{3.96})} = 0.0207 \\
    \text{Recall: } f &= \frac{4\pi}{3}\frac{r^{3}}{x^{3}} \\
    \implies x &= \bigg(\frac{4\pi}{3f}r^{3}\bigg)^{\frac{1}{3}} \\
    &= \bigg(\frac{4\pi}{3(0.0207)}(15e-6)^{3}\bigg)^{\frac{1}{3}} \\
    &= \bigg(6.83e-13)^{\frac{1}{3}} \\
    &= 8.81e-5 [m] \\
    \text{Recall: } \tau &= \frac{G\vec{b}}{x} = \frac{(28e9)(0.286e-9)}{8.81e-5} \\
    &= \frac{8.008}{8.81e-5} \\
    &= 9.09e4 Pa \\
    \boxed{\tau} &\approx \boxed{91 kPa}
    \end{split}$$

    This $\tau$ is not necessarily the shear stress of the material, but is the contribution of the particles to the overall shear stress.