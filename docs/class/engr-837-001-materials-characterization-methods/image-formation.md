<!-- 20220907T09:38 -->
# Image Formation
## Objectives
* Determine the mechanism by which images are formed using an #electron-beam
* Determine beam conditions and their effects on imaging
* Discuss the beam-sample interaction and the information generated
* Identify the practical controls to optimize the [resolution](resolution.md)

## Probe Size and Resolution
Recall from #optical-microscopy that the wavelength of light determines the resolution for a given #NA: half the Airy disk diameter.
In #electron-microscopy, the probe diameter is now the limiting factor, as *it* is scanned across the surface.
The probe diameter is related to the probe current, $i_{p}$, beam brightness, $\beta$, and angle of convergence, $\alpha_{f}$.

| ![](../../../attachments/image-formation/probe_size_and_resolution_220907_140110_EST.png) |
|:--:|
| $d_{p} = \sqrt{\frac{4i_{p}}{\beta(\pi\alpha_{f})^{2}}}$ |

### Another way of looking at it
!!! question What if we decrease working distance and aperture size at the same time? How does this affect our [depth of field](depth-of-field.md)? <cite> #Mark-Atwater
    ![](../../../attachments/image-formation/another_way_of_looking_at_probe_size_and_resolution_220907_140613_EST.png)
    | ![](../../../attachments/image-formation/depth_of_field_visualized_for_working_distance_and_aperture_220907_141141_EST.png) |
    |:--:|
    | One of the key benefits of #SEM is high [depth of field](depth-of-field.md) for its magnification because the cone is already so narrow. |

## Probe brightness
The brightness of the beam is determined by the probe current, diameter, and #convergence-angle, as reorganized from the prior equation for beam size: units are $\frac{A}{m^{2}sr}$ (current density per unit solid angle).
Brightness is a constant based on source type, so the other variables must scale proportionally.

$$\begin{split}
\beta &= \frac{4i_{p}}{(\pi d \alpha_{f})^{2}} \\
\beta &\propto eV_{0}
\end{split}$$

## Aberrations and minimum resolution
We cannot simply increase the #convergence-angle without penalty.
High $\alpha_{f}$ values introduce greater degrees of [aberrations](aberrations.md).
At an optimized $\alpha_{f}$, the probe size is $d_{min} = KC_{s}^{\frac{1}{4}}(\frac{i_{p}}{\beta} + \lambda^{2})^{\frac{3}{8}}$.
$K$ is a constant $\sim 1$, $C_{s}$ is the #spherical-aberrations coefficient, and $\lambda$ is the wavelength.
The operating voltage and probe brightness are especially important.

## Gun type and settings
| ![](../../../attachments/image-formation/gun_type_and_settings_220907_141559_EST.png) |
|:--:|
| Probe diameter goes down with increased acceleration voltage. Probe diameter also goes down with source type. |

Why this is true is similar to comparing the ability to focus light from a standard filament bulb and a laser pointer.

## Emitter type
#cold-FEG have a very high brightness but relatively low probe current: a small tip area and small angle of departure.
#Schottky-FEG also have a high brightness, but they have a larger tip area and greater electron density energy spread.

## Signal generation
The beam must have sufficient current to produce usable signal, so lower current is not a means to better resolution.
The signal generated from the incident beam will be lower than that of the incident beam, and can be obstructed by noise at very low intensities.

| ![](../../../attachments/image-formation/signal_generation_220907_142031_EST.png) |
|:--:|
| Too much noise and you cannot differentiate what you are focusing on. |

## Signal to noise
The [Rose Visibility Criterion](rose-visibility-criterion.md) states that the signal must be fives times greater than the noise to distinguish objects.
The deviation can be determined from the square root of the mean of n counts of S: $\Delta S > 5N$ or $\Delta S > 5\sqrt{\bar{n}}$.
Contrast was defined as: $C = \frac{\Delta S}{S} > \frac{5\sqrt{\bar{n}}}{S} = \frac{5\sqrt{\bar{n}}}{\bar{n}}$ which yields $\bar{n} > (5/C)^{2}$.

## Probe current and signal
The number of counts is what is detected and is proportional to the electrons put into the sample and the dwell time: $i_{s} = \frac{\bar{n}e}{\tau}$.
A proportionality constant between the probe and signal current is applied with the contrast: $i_{p} = \frac{25e}{\epsilon C^{2}\tau}$.
Dwell time is often the frame rate, or time, $t_{f}$ to complete a scan of one frame with $n_{PE}$ pixels: $\tau = \frac{t_{f}}{n_{PE}}$.
Faster scan speeds reduce dwell time and things will not be as crisp and clear.

## Sources of contrast
[Contrast](contrast.md) is developed by varying signal, but the cause of signal variation can be from two primary sources:
1. Topography
2. Composition

Both can contribute simultaneously, but the electrons from each are different in character and can be optimally collected in different ways.
The beam interaction will be different in each case.

## [Interaction volume](interaction-volume.md)

## [Topographical contrast](topographical-contrast.md)

## [Composition contrast](compositional-contrast.md)

## Summary
- The beam is of critical importance to the image in #SEM
- The source will determine what is possible and practical for both image resolution and signal output
- The minimum probe size is achieved with a high brightness, low current, and high #convergence-angle, but only to a limit
- The beam doesn't just scan the surface, it goes into it, so signal is necessarily from a larger area
- The signal generated provides contrast through topographical and compositional factors which are both useful

!!! question What conditions are needed to get good contrast between phases? <cite> 
    Distinct phases and a good difference of Z number in sample composition.