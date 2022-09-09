### Introduction
Plasticity is sometimes involved with engineering design. It may also prove integral to performance. This chapter explores the importance the stress-strain behavior and the effects thereof.
Materials always follow elastic to plastic deformation before ultimate failure. Most applications will operate within the elastic region (ceramics with narrow elastic regimes), but accommodations for work-hardening may be considered. Not all materials work-harden the same way. Two yield points in materials: *first yield* is the elastic limit, and *ultimate strength* is ultimate plasticity. **Plasticity** is imperative for processing and performance of materials.

!!! tip
    Think of Dr. Atwater's lawn mower!

**Mechanical Testing** Determines mechanical properties for materials: such as various tension or compression. Tension is the most popular, but all give same information: *stress-strain* curve.

#### Engineering and true stress and strain
Recall that [[engineering-stress]] is from $A_{0}$ and [[true-stress]] uses $A_{i}$. *Plastic deformation is volume conservative*, which allows calculating [[true-stress]] and [[true-strain]] from the engineering values. Stress-strain curves relates initial conditions to overall performance.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stress_strain_curve_comparisons_true_to_engineering_210913_183110_EST.png) |
|:--:|
| True stress-strain gives more accurate understanding of stress states, but can be more difficult to interpret. $\label{fig:stress_strain_curve_comparisons_true_to_engineering}$ |

!!! question Is conversion from engineering to true stress-strain meaningful with necking? <cite> DK
    It depends. We will discuss this later.

#### Work-Hardening Basics
*[[Ludwik-Hollomann]]* equations
: $$\begin{equation}\sigma = \sigma_{0} + K\epsilon^{n} \label{eq:ludwik_hollomann}\end{equation}$$ Where $\sigma_{0}$ is the yield stress, $K$ is experimentally found ($\frac{G}{100}-\frac{G}{1000}$); $\epsilon$ is true strain; and, $n$ is some work hardening coefficient (0.2-0.5).

!!! example Use the *[[Ludwik-Hollomann]]* equation (Eq. \eqref{eq:ludwik_hollomann}) to determine work hardening exponent, $n$ in an alloy of true strain at 0.1 and true stress = 415 MPa. Assume $K = 1035 MPa$ and $\sigma_{0} = 0$.
    $$\begin{split}
    \sigma &= \sigma_{0} + K\epsilon^{n} \\
    log[\sigma &= \sigma_{0} + K\epsilon^{n}] \\
    log(\sigma) &= log(K) + n*log(\epsilon) \\
    \frac{log(\sigma) - log(K)}{log(\epsilon)} &= n
    \end{split} \\
    \begin{split}
    \implies n &= \frac{log(415) - log(1035)}{log(0.1)} \\
    n &\approx 0.397
    \end{split}$$

    !!! note
        The greater, $n$, the more work-hardening can occur.

**Refined Methods**
*L=H* has limits; therefore, *Voce* equations adds asymmetry. *[[Johnson-Cook]]* expands with strain-rate and temperature dependence:

$$\begin{equation}
\sigma = (\sigma_{0} + K\epsilon^{n})\bigg(1 + C*ln(\frac{\dot{\epsilon}}{\dot{\epsilon_{0}}})\bigg)\bigg[1 - \bigg(\frac{T - T_{r}}{T_{m} - T_{r}}\bigg)^{m}\bigg]
\label{eq:johnson_cook}
\end{equation}$$

Each term in the *[[Johnson-Cook]]* equation represents a different failure mechanism.

**Volume Conservation**
Volume is assumed to be constant through deformation; however, volume is not always assumed constant in the elastic region. *[[poissons-ratio]]*, $\nu$ is constant in the elastic region, but varies in the plastic region. True and engineering stress-strains considered equivalent up to elastic limit.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stress_strain_jog_210913_185442_EST.png) |
|:--:|
| Steels have upper and lower yield limits to break dislocations apart. $\label{fig:stress_strain_jog}$ |

#### Summary
Plasticity introduces new requirements to calculate stress and strain. Elastic portion considered inconsequential and plastic deformation is volume constant.


---


*Lecture: September 15, 2021*

### Tensile Curve Parameters, Necking, and Strain Rate
Features of the stress-strain curve indicate when necking occurs, and give insight when correction factors apply: only when cylindrical samples neck. New equations for material behavior after necking. [[strain-rate]] affects material response as well.

#### Introduction
Tensile testing is the most basic form to determine material properties. Parameters of test affect outcome: temperature, etcetera.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/tensile_curve_features_210915_192748_EST.png) |
|:--:|
| *A:* $0.2\%$ strain offset yield stress. *B:* #upper-yield. *C:* #lower-yield. *D:* #proportional-limit. *D`:* #ultimate-tensile-strength (UTS). *E:* #rupture-stress. *F:* non-uniform plastic strain limit. *G:* #rupture-strain (strain to failure). *H:* lower yield region. The area under the elastic region is the *#modulus-of-resilience* and *#toughness* is area under entire curve. $\label{fig:tensile_curve_features}$ |

The more dislocations/impurities, the more local stresses exist, and more global force is required to overcome the sum of the internal stress: this is true for plain carbon steels.

!!! note Items of Note
    1. Yielding is preceded by *micro-yielding*, where  [[dislocation-motion]] can occur below traditional yield stress.
    2. Upper-lower yield behavior is largely seen in plain, low-carbon steels.
    3. Vacancy and dislocation pinning resist initial yielding.
    4. [[strain-rate]] will modify the tensile curve and can obscure the upper-lower yield phenomenon when present.

#### Necking
Occurs when localized deformation begins to dominate the strain: *void nucleation, coalescence, and growth*. This is also known as *[[plastic-instability]]* and is defined by **[[Considere-Criterion]]**: increase in stress relative to strain (work-hardening) reaching a maximum in the engineering stress-strain curve. *The higher the strain exponent, the more strain you get out of the material.* Using this criterion, substituting true stress-strain into the derivative and apply Eq. \eqref{eq:ludwik_hollomann}, you get the relationship $\epsilon_{u} = n$, where $\epsilon_{n}$ is maximum, uniform plastic strain.

Work-hardening exponent from *engineering* stress-strain curve. [[work-hardening]] decreases during increase of plastic strain until that point at which necking occurs. A metal unable to work-harden immediately reaches the point of necking after yielding, which is consistent with equations.

[[work-softening]]
: The more it deforms, the easier it can be deformed (not necessarily from reduced area)--is possible under extreme conditions.

!!! tip
    Think of void nucleation, coalescence, and growth!

#### Stress-strain and Necking
After necking, instantaneous cross-sectional area must be continuously determined. Neck acts as a "second", miniature tensile specimen, so it's strain-rate is higher from shorter length. Irregular geometry of neck also introduces triaxial flow stress. Magnitude of transverse stresses depends on sample and neck geometry and strain-rate.

##### Bridgman Correction
This only applies to *cylindrical* samples, because sample area and neck radius must be known.

$$\begin{equation}
\sigma = \frac{\sigma_{avg}}{(1 + 2\frac{R}{r_{n}})ln(1 + \frac{r_{n}}{2R})}
\label{eq:bridgmann_correction}
\end{equation}$$

$R$ is radius of curvature of the neck, and $r_{n}$ is the cross-sectional radius at thinnest part of neck. The further away from necking (higher strains), this correction factor increases.

##### State of Stress in Deformation
Necking is onset of failure in a non-uniform fashion. Applies only to tensile testing, because compression samples *barrel*. Necking can be suppressed to achieve higher strains in more complex stress states.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/wire_drawing_example_210915_193440_EST.png) |
|:--:|
| Wire drawing shows ability to achieve 7.4 true strain of copper. $\label{fig:wire_drawing_example}$ |

#### Strain Rate
Increasing [[strain-rate]] work-hardens faster: **void nucleation controls**!! This parameter is part of stress-strain-rate relationship: $\sigma = K\dot{\epsilon}^{m}$. $m$ can be found from a jump test between two strain-rates using the [[Ludwik-Hollomann]] equation: $m = \frac{ln(\frac{\sigma_{2}}{\sigma_{1}})}{ln(\frac{\dot{\epsilon_{2}}}{\dot{\epsilon_{1}}})}$.

**Strain-rate In Practice**
Strain-rate can vary from $10^{-6}s^{-1}$ to $10^{6}s^{-1}$. Tensile tests usually within $10^{-4}s^{-1}$ to $10^{-1}s^{-1}$. High [[strain-rate]] (Hoppy bar) and creep or stress relaxation tests invaluable to determine material behavior under extreme conditions. Creep and stress relaxation tests incorporate higher temperatures, which is important to material performance.

Strain-rate affects material behavior. Increasing [[strain-rate]] often increases yield stress and the [[work-hardening]] rate. Typically, $0.02<m<0.2$ for $0-0.9T_{H}$.

**Super-plastic Behavior** Effective [[strain-rate]] in necking area increases. Positive [[strain-rate]] sensitivity implies an increased stress and the yield point will shift to the weaker section. Same concept that assists in distributing strain across tensile specimen length in [[work-hardening]].

#### Summary
Stress-strain curve contains much information, but not all can be known from only the engineering curve. Necking changes specimen geometry, which affects test results. Stress states may control onset and progression of necking, which may allow for much higher strains before failure. [[strain-rate]] affects material response and is dependent on processing and performance applications.


---


*Lecture: September 17, 2021*

### Compression and Hardness
#### Introduction
Many applications use compressive stresses; therefore, testing for compression is more relevant. Some materials perform well under compression and not tension. Simpler and more cost-effective to perform compression tests; therefore, metal alloy research heavily utilizes this method.

#### Practical Considerations
Compression is simple but requires care to ensure good data. Plate alignment and sample parallelism and flatness are imperative. Lubricant between plates and sample reduce barreling. Machine compliance must be removed from measured stress-strain curve, especially at lower strains. Can also measure strain from video recordings and point markers on sample.

!!! tip
    Plates should be much harder than the sample.

#### Compression Curve
Stress-strain opposite from tensile curve. Barreling is source of non-uniform plastic strain.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/compression_stress_strain_curve_with_barreling_210917_184501_EST.png) |
|:--:|
| True stress-strain moves the curve down and to the right from the engineering stress-strain curve, which is opposite that seen for tension testing. $\label{fig:compression_stress_strain_curve_with_barreling}$ |

Effects of barreling most pronounced at strains exceeding 0.4; therefore, compression testing usually limited to less than that. Friction is very important when initial $\frac{height}{diameter}$ is reduced: if too tall and thin, the specimen will buckle first.

#### Compression Failure
If perfectly striked, stress state greatly varies through specimen. Although extreme, ductility allows for stress-strain behavior off the central axis. Non-uniform stress occurs, then, across top and bottom surfaces (friction hill).

$$\begin{equation}
p = \sigma_{0}\exp(\frac{2\mu(a - r)}{h})
\label{eq:friction_hill_pressure}
\end{equation}$$

$\mu$ is coefficient of friction, $r$ is distance from center, $a$ is radius of sample, and $h$ is height of sample.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/compression_failure_friction_hill_210917_185143_EST.png) |
|:--:|
| Friction hill seen at top and bottom surfaces of sample when barreling. $\label{fig:compression_failure_friction_hill}$ |

!!! example If $\frac{height}{diameter} = 2$, then what is $p_{max}$?
    $$\begin{split}
    \frac{l}{d} 	&= 2 \\
    p 	&= \sigma_{0}\exp(\frac{2\mu(a - r)}{h})
    \end{split} \\
    \begin{split}
    p &= \sigma_{0}\exp(2(0.15)(\frac{a}{h})), \frac{d}{h} = \frac{1}{2}(\frac{\frac{a}{2}}{h}) = \frac{1}{2} \longrightarrow \frac{a}{h} = \frac{1}{4} \\
    \implies p 	&= \sigma_{0}\exp(2(0.15)(\frac{1}{4})) \\
    &= \sigma_{0}\exp(\frac{0.3}{4})
    \end{split}$$

#### Bauschinger Effect
If you pull something in tension, then switch to compression, the yield point will lower from tension to compression. The strain in the material from tension weakens the material and causes a lower yield point: the *[[Bauschinger-Effect]]*.

#### Hardness Testing
**Hardness is a material's resistance to plastic flow by indentation.** Scale of indentation varies with load, which is standardized with the indenter while its displacement is measured.

Brinell
: Uses a hard sphere of known dimension and known force to measure the size of indent. Amount of applied force changes size of indention.
$$\begin{equation}
HB = \frac{P}{\pi Dh} = \frac{2P}{\pi D(D - \sqrt{D^{2} - d^{2}})}
\label{eq:brinell_hardness_number}
\end{equation}$$

Rockwell
: Testing is simple, provides direct, arbitrary hardness reading, but relatable to known values.
$$\begin{equation}
HB_{Meyer} = \frac{4P}{\pi d^{2}}
\label{eq:meyer_hardness_number}
\end{equation}$$
: Useful on a wide range of materials.
: *Testing Process:*
: - Apply pre-load.
: - Apply indentation load.
: - Remove "major" load from specific indenter and load.
: - Measure depth read on scale: 0-100.

Indenter geometry will determine scale: A, B, or C. *Rockwell-C* is best for harder steels and metals of similar properties. Superficial scales for thin samples with lower loads to avoid anvil effects.

Vickers
: Also known as *Diamond Pyramid*, because indenter is pyramid with $136\degree$, which is based on $d_{Brinell} = 0.375D$ relationship. Can be used on any material. Indentation size measured by average length across diagonals. Hardness computed by...
$$\begin{equation}
HV = \frac{2Psin(\frac{\alpha}{2})}{d^{2}} \approx = \frac{1.8544P}{d^{2}}
\label{eq:vickers_hardness}
\end{equation}$$

#### Hardness-Yield Relationship
For Vickers hardness, measured value is related to yield stress through Tabor's relation (Eq. \eqreftabor_relation{eq:tabor_relation}):

$$\begin{equation}
H = 3\sigma_{y}
\label{eq:tabor_relation}
\end{equation}$$

This assumes no [[work-hardening]]; therefore, use $\epsilon_{p} = \frac{d'}{5D} \approx 0.075$ for $d = 0.375D$ with a flow stress, $\tau = 8-10 \%$ in hardness conversions.	

#### Micro-Indentation Testing
Creates indent that 10's of microns in size.

!!! note
    Vickers is macro- and micro-indent test method: wherein, anything below $200g$ force is considered micro-testing.

Allows testing of small features: particles or areas of grain. Ability to probe microscale features limited if larger scale features dominate material.

$$\begin{equation}
KHN = \frac{14.228}{L}
\label{eq:knoop_hardness}
\end{equation}$$

#### Nano-Indentation Testing
Highly sensitive force-displacement device, which allows for general microstructural investigation at lowest length scales. Examine small volume of material with *Berkovich* indenter.

$$\begin{equation}
H = \frac{P_{max}}{A}
\label{eq:berkovich_hardness}
\end{equation}$$

### Summary
Compression testing is opposite tension. Equations of true stress-strain are same, but have different effects. Hardness provides simple means...