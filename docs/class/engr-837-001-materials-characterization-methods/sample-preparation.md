# Sample Preparation

In some cases, an object of interest can be viewed without any alteration: e.g. a dead bug.
In most research effort, the examination of materials will require extensive sample preparation.
A typical sequence of steps will consist of:
- [Sample Preparation](#sample-preparation)
    - [Sectioning](#sectioning)
    - [Microtomy](#microtomy)
    - [Mounting](#mounting)
    - [Grinding](#grinding)
    - [Polishing](#polishing)
    - [Etching](#etching)

### Sectioning
To make a sample easier to image, it is often cut down to a smaller size.
There may be a portion of interest that is not readily visible without sectioning (i.e. interior).
The sample can be roughly cut with an appropriate method[^1]:
* High-speed saw (fast, high damage)
* Low-speed saw (medium speed and damage)
* Electrical discharge machining ( #EDM ): slow, precise, causes surface melting, only for conductive materials
* #water-jet: requires programming and set up, cutting is fast, modest damage without heating

[^1]: For more information about #EDM and water jet, see this [link](https://www.accessengineeringlibrary.com/content/book/9781260122312/toc-chapter/chapter22/section/section1).

### Microtomy
Primarily used for soft materials: such as, polymers and biological samples.
Uses a very sharp knife to slice thin section from a sample: like a mandolin used in the kitchen.
#ultramicrotomy creates *very* thin ($20-150 nm$) sections for #TEM.

### Mounting
Holds a specimen in place for [sectioning](#sectioning), [grinding](#grinding), and [polishing](#polishing): many automated techniques rely on the standardized shape and size.
Can be hot or cold-mounted.
* Hot mounting used heat and pressure to mold a polymer (typically phenolic), around the sample: heat is unacceptable for some samples with heat-sensitive features.
* Cold mounting uses a two-part resin/hardener mixer to create mold around the sample and cures over time (minutes to hours).
  * Often epoxy or polyester, hardness and clarity vary.
  * Vacuum infiltration will aid in removing air bubbles and created a good bond.
* Additives such as glass filler or conductive powders can be added.

Samples can also be mounted by clamping or adhering to a surface.

### Grinding
The surface created during sectioning is rarely acceptable for analysis.
Abrasive smoothing is used to progressively remove #damage and generate a flat surface.
Each step of grinding/polishing is only intended to remove the #damage of a previous step of similar magnitude: a sequence of abrasives is used to incrementally prepare the surface.
The grinding process should be done with alternating sample orientations to provide a clear indication of the progress:
- Rotate sample $90\degree$ between grinding steps.
- Automated polishers will provide randomized grinding orientations so that the sample is uniformly processed: this removes artifacts such as comet tailing.

!!! info Storing Sand Paper
    Finer grits should be stored above the coarser grits so that the finer grits are not scratched by the coarser grit which could happen if a coarse grit fell onto a finer grit.

### Polishing
Instead of an abrasive paper, final polishing will use a pad to which the abrasive particles are added: the style of the pad will determine the proper polishing #particle-size.
Polishing steps should following a similar process of progressively reducing the coarseness of grind.
Excessive pressure at polishing can cause #plastic-deformation and "smear" our the surface features.
#vibratory-polishing uses a fine slurry with vibration to reduce surface #damage.
#electropolishing and #ion-polishing provide damage-free surfaces.

### Etching
To highlight certain features, etching can be used.
Etching uses a chemically active solution to selectively remove areas of a sample.
The material being etched will determine the appropriate etchant.
#grain-boundary and #grain-contrast are commonly examined by etching: the etch rate is faster at #grain-boundary and for certain #grain-orientation.