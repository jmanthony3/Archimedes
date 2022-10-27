# Depth of Field

...is the distance from the lens to the object: the longitudinal distance between two points measured from the point of view.

$D_{f}$ is the range of position over which the sharpness of an object does not change.
Outside this range, the object is out of focus.
Since light is diffraction limited.
The [resolution](../engr-743-001-damage-and-fracture/resolution.md) will not change across some range of distance.
Note that $R$ and $D_{f}$ are proportional (high [resolution](../engr-743-001-damage-and-fracture/resolution.md)) will have a small $D_{f}$): $$D_{f} = \frac{d}{\tan(\alpha)} = \frac{2R}{\tan(\alpha)} = \frac{1.22\lambda}{\mu\sin(\alpha)\tan(\alpha)}$$
==Therefore, depth of field can be increased with a longer #working-distance or smaller #aperture-size.==

![](../../../attachments/lecture-3-resolution-and-aberrations/depth_of_field_221027_160337_EST.png)

!!! question What if we decrease #working-distance and #aperture-size at the same time? How does this affect our depth of field? <cite> #Mark-Atwater
    ![](../../../attachments/image-formation/another_way_of_looking_at_probe_size_and_resolution_220907_140613_EST.png)
    | ![](../../../attachments/image-formation/depth_of_field_visualized_for_working_distance_and_aperture_220907_141141_EST.png) |
    |:--:|
    | One of the key benefits of #SEM is high depth of field for its magnification because the cone is already so narrow. |

## Optimizing in Optical Microscopy
- Reduce [NA](numerical-aperture.md) by closing the #aperture-diaphragm or use an objective lens with lower [NA](numerical-aperture.md)
- Lower the magnification for a given [NA](numerical-aperture.md)
- Use a high-powered eyepiece with a low-power, high-[NA](numerical-aperture.md) objective lens
- Use the longest possible wavelength light

## SEM
The large $D_{f}$ in #SEM is a consequence of the very small beam size and angle.
The beam is small enough to sufficiently resolve features over a large z-height, especially at low magnification.

$$\begin{split}
D_{f} &= \frac{2R}{\tan(\alpha)} \\
 &\cong \frac{200}{\alpha_{f}M} \\
 &\cong \frac{200 D_{W}}{R_{fap}M}
\end{split}$$

| ![](../../../attachments/lecture-8-sem-operations/depth_of_field_in_sem_221027_193650_EST.png) |
|:--:|
| The over- and under-focus conditions are still in focus. |