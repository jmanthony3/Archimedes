<!-- 20221012T09:36 -->
# Defect Imaging
## Objectives
- Identify the importance of imaging of defects in TEM
- Describe common imaging effects related to bulk structure
- Discuss the causes for contrast in lattice defects and common examples
- Highlight high-resolution TEM and the need to carefully interpret the results

## Defects
Defects
: Imperfections in crystal structures wherein the pattern is neither uniform nor repeated.

TEM is an important tool for studying defects in materials because it is one of the few that can resolve the features.
Dislocations, stacking faults, twins, grain boundaries, etcetera are all visible under TEM.
The mechanisms for their appearance is difference than mass-density contrast, but it may appear similar.

### Wedge fringe
TEM samples are often prepared as thin wedges.
The continuously changing thickness can cause interference effects that appear as light and dark stripes perpendicular to the direction of increasing thickness.
This can be confused with mass-density contrast, but it is a geometrical effect dependent on the beam interactions in the material.

| ![](../../../attachments/defect-imaging/wedge_fringes_in_grain_boundaries_221012_135940_EST.png) |
|:--:|
| In grain boundaries, a Wedge Fringe could indicate a boundary, but it is not a direct representation of the boundary because the grains overlap wherein the beam destructively interacts with itself. |

## Deviation from Bragg's Law
The thickness change results in a change in diffraction intensity.
The kinematic theory of diffraction predicts this intensity ($I_{d}$) change (deviation , $\mathbf{s}$) for a thickness ($t$).
$$I_{d}\propto \Bigg(\frac{\sin(\pi st)}{\pi s}\Bigg)^{2}$$
"s" is the component of $\mathbf{s}$ parallel to the beam.
This results in an oscillation of intensity as thickness increases.

| ![](../../../attachments/defect-imaging/deviation_from_braggs_law_221012_140335_EST.png) |
|:--:|
| A bright firnge occurs at $t = ns^{-2}$ and a dark fringe at $t = n + (2s)^{-1}$. |

## STacking faults
Any wedge-shaped feature may produce these fringes, and stacking faults at an angle to the beam are no different.
The stacking faults are bounded by the partial dislocations.

| ![](../../attachments/defect-imaging/wedge_fringes_and_stacking_faults_221012_140541_EST.png) |
|:--:|
| Because this is a mostly uniform contrast and these fringes occur within the material itself, it is safe to assume these are actually Wedge fringes. |

## Bending contours
If the sample is bent, there will be a certain points at which the lattice planes satisfy Bragg diffraction.
They often occur as poaris given a symmetry contour.
Bend contours are highly sensitive to tilting, and they can be identified that way.
The bending does not need to be drastic, as the diffraction angles are often within a few degrees of the beam axis.

## Dislocations
Dislocations are created by the presence of an extra half-plane of atoms above or below the dislocation line.
The interruption of the crystal structure results in a lattice distortion that diffracts the beam at certain angles.
The dislocation will not be visible if it is perpendicular to the beam.

!!! question How do you tell the difference between dislocation and bending contours? <cite> Atwater
    Tilt the sample and see if the lines disappear because defects are not as sensitive to tilt as bending contours.

Dislocation appear as short lines because they terminate at the surface.
The projected image does not capture the thickness (third dimension )of the sample.
In-situ mechanical testing can be used to visualize the motion of dislocations.
v=EXbiEopDJ_g

## High-resolution TEM
HRTEM is a high-magnification, atomic resolution imaging technique.
The resulting images must be carefully interpreted to avoid assigning imaging artifacts with the actual structure.
Moire fringes are an example where overlapping crystals result in fringes that are not related to the actual structure.
Spacing can be an artifact, suggesting that atomic patterns are from different orientations, etcetera.
This is a highly developed topic in itself.

| ![](../../../attachments/defect-imaging/high-resolution_tem_and_moire_fringes_221012_141347_EST.png) |
|:--:|
| A Moire fringe is not an actual dislocation because it exaggerates and visually changes the representation of the pattern from the dislocation. Therefore, be carefully when looking at images. |

!!! example
    [Microstructural evolution of Alloy 709 during aging](https://www.sciencedirect.com/science/article/pii/S1044580319310514)