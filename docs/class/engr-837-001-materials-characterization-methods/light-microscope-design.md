<!-- 20220829T13:05 -->
# Light Microscope Design
## Objectives
- Discuss the design and operation of light microscopes
- Identify key components and layout
- Detail the light path and critical illumination points
- Describe the way illumination and object focus achieved simultaneously
- Identify microscopy layout and the means for controlling image quality

## Microscopy Components
Components of optical microscope include:
- Illumination
- Objective lens
- Eyepiece
- Camera
- Specimen stage

## Illumination Source
The illumination can vary in type and the characteristic wavelength it emits (color, temperature) and the [total brightness](brightness.md).
(The light source can be very hot, so do not put a cover on a microscopy too quickly!)
The choice of illumination source is important as lens may be optimized for #chromatic-aberrations in that spectrum range or for the excitation of fluorophores.
LED sources can be tuned for a specific wavelength, which is especially useful in flourophore excitation.

## Illumination
Consists of a collector lens and condenser lens ( #Koehler-system ).
Collector lens focuses the light at the front focal plane of the condenser lens.
Condenser lens focuses light at the sample.
Defocuses the filament image at the sample for even illumination.

| ![](../../../attachments/engr-837-001-materials-characterization-methods/illumination_220830_154945_EST.png) |
|:--:|
| Light that is diverging from the focal plane and incident to the lens, the exiting light is collimated which is perfectly defocused but is helpful to provide light onto the specimen. |

## Conjugate Focal Planes
In the #Koehler-system, the same light path has two sets of conjugate focal planes: aperture planes are field planes.
The aperture planes are for illumination (filament image).
Light rays focused at the focal plane of the condenser are parallel after it.
The field planes are for specimen image formation.

| ![](../../../attachments/engr-837-001-materials-characterization-methods/conjugate_focal_planes_220830_155019_EST.png) |
|:--:|
| These two paths are in the same light source and path. These are not two different ways to diagram or map the light rays: this is the same system from the specimen. |

!!! note
    Think of the pinhole effect looking through a pinhole in a piece of paper by limiting the off-axis light.

## [Koehler diaphragms](koehler-diaphragms.md)

## Reflected light (epi-illumination) and filters
Reflected light microscope rely on a beam splitter to transmit light through the objective lens and back to the eyepiece or camera.
Light filters can be placed in the light path to regulate intensity or color compensation.

## Objective lens
Most important to image magnification and quality.
#NA between 0.16-1.4.

Highest dry lens #NA $\sim 0.95$.

Provide #chromatic-aberrations correction:
- Achromat (good)
- Semi-achromat (fluorite) (better)
- Apochromat (best)

## Aberration Correction Types
Achromat provide red and blue correction: must be illuminated green for black and white photography (old timey stuff).
Semi-achromat has higher #NA and better resolution, including some #spherical-aberrations correction.
Apochromat lenses have better #spherical-aberrations correction, higher #NA, much more complex design.

![](../../../attachments/engr-837-001-materials-characterization-methods/aberration_correction_types_220830_155213_EST.png)

## Lens identification
![](../../../attachments/engr-837-001-materials-characterization-methods/lens_identification_220830_155348_EST.png)

## Eyepiece
| ![](../../../attachments/engr-837-001-materials-characterization-methods/eyepiece_220830_155535_EST.png) |
|:--:|
| Provides magnification multiplier. May further correct [aberrations](aberrations.md). May provide a graticule for measurements of features. May incorporate independent focal adjustment (parfocal) to correspond to a separate camera. May include diopter adjustment. |

## Optimizing resolution
- Use an objective lens with the highest #NA possible
- Use high magnification
- Use an eyepiece compatible with the chosen objective lens
- Use the shortest possible wavelength light
- Keep the light system properly centered
- Use oil immersion lenses if available
- Adjust the #field-diaphragm for maximum [contrast](contrast.md) and the #aperture-diaphragm
- For maximum [resolution](resolution.md) and [contrast](contrast.md)
- Adjust [brightness](brightness.md) for best [resolution](resolution.md)

## Optimize depth of field
- Reduce #NA by closing the #aperture-diaphragm or use an objective lens with lower #NA
- Lower the magnification for a given #NA
- Use a high-powered eyepiece with a low-power, high- #NA objective lens
- Use the longest possible wavelength light

## Summary
- Light microscopes use a complex arrangement of lens to get quality images
- The lens quality is critical, but the design and adjustment of the microscope must be correct to get the performance from those lenses
- Proper illumination and defocused is achieved with the #field-diaphragm and #aperture-diaphragm
- The light quality (wavelength and dispersion) can be filtered for specific needs