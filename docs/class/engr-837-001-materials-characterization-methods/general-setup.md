<!-- 20220905T13:17 -->
# General Setup

This differs from reflected (epi-illuminated) light that reflects off the surface of a specimen. The content here dips into Ch. 3 but mostly with Ch. 4 with electromagnetic lenses and transmission microscopy.

## Objectives
* describe thebasic difference sbetween optical oelecton miscropy
* highlight the functional espects of electron miscropy
* detail the major components of a sem
* determine some of the key performance factuors in electon microscopy

## Introduction
* SEM is a versatile technique for imaging samples
* there are concepts from light microscopy that will carry over, but in a much different form
* the primary difference is the use of electrons, instead of photons, to form images: closest analogue is a confocal leaser scanning microscopy (CLSM)
* The implications of this allow a greater range of magnification and new possiblilitues in chemical analysis and other anlaytical techniques.

## Comparison to optical microscopy
* source in OM the source is a heated filament or LED producing a specific light spectrum (wavelength dispersion): in EM, the source is a filament (often heated) that produces "free" electrons that are given a specific energy (wavelength).
* In OM, the light is collected, focused, and magnificed through a series of lenses: EM is the same
* In OM, the lenses are glass, fixed, and subject to aberrations.
  * In Em, the lenses are electromagnetic, adjustable, and also subject to aberrations.
  * Some aberrations can be easily corrected, such as astigmatism

!!! note Some SEM machines require evacuating the imaging chamber.
    Keep in mind that not all things behave the same under vacuous conditions: i.e. water will boil at low pressures.

## General SEM "optics"
* The SEM uses an electron "gun" to generate electrons which are acclerated by high voltage down the column
* the electrons pass through electromagnatic lenses to condense and focus the beam
* the beam is rastered across the sample to generate signal that is converted to an image

![](../../attachments/scanning-electron-microscopy-general-setup/general_sem_optics_220905_173348_EST.png)

## Electron source
* the way electrons are generated is important to the resolution of the SEM
* to generate an electron beam, the work function of source must be overcome.
* the source (cathode) is combined with a Wehnelt cap
* the two main categories are thermionic and field emission
* The cost and capability of these sources are inversely proportional, and the system changes can also rapidly increase the cost.

![](../../attachments/scanning-electron-microscopy-general-setup/electron_source_220905_173718_EST.png)

![](../../attachments/scanning-electron-microscopy-general-setup/electron_source_220905_173718_EST.png)

### Thermionic source
Thermionic sources heat a filament to high temperature to "boil" off electrons. The lowest cost version is a tungsten wire. A lanthanum hexaboride ($LaxB_{6}$) emitter has a lower work function (less than half that of $W$). $LaB_{6}$ has a higher brightness (10X) and longer lifetime (10X) but high cost (10X). $LaB_{6}$ also requires higher vacuum and that raises the complexity and cost of the microscope.

### Field emission sources
Field emission gun (FEG) SEMs use a strong electrostatic field to draw electrons off the tip of the emitter. A tip that is not heated is considered a cold-FEG and requires an extremely sharp tip. Schottky FEGs uses lower temperature heating that thermionic sources and a $ZrO$ coating to reduce the work function of a single crystal $W$ emitter. Cold FEGs produce the best resolution, but Shottky tips provide greater analytical capability and stability: cold FEGs require extermely high vacuum and may need to be "flashed" to remove surface contamination.

## Electromagnatic lenses
* electrons will move perpendicular to a magnetic field.
* By changing the strength of the field, the electron beam can be manipulated.
* the magnetic field is altered through current in the lens, and by incorporating numerous sections, beam shape can be changed as well.
* the beam is focused to a fine point by these lenses and rastered by *scan coils*.

## Detecting Electrons
* Electrons interact with the sampel surface, and this produces a signal that can be detected.
* The common electron detector is the Everhart-Thornley detector, which applies a biased grid to attract (or reject) electron produced inelastically in the sample (secondary electrons)
* a positive grid bias allows electrons to be collected that are generated in areas with line-of-sight to the E-T detector.

!!! note 3D Perspective in SEM images
    Images appear to be 3D, which is correct, but is only an artifact of the rastering process and the shadows behinds crevices and ledges. Unlike in a confocal microscope, the objective lens does not move azimuthally to scan at various depths.

* Some electrons from the source interact inelastically with the sample, and these are called backscattered electrons (BSEs)
* these are high-energy electrons and not susceptible to the small grid bias on the E-T detector.
* The majority of these electrons are reflected toward the pole piece (objective lens), and a separate detector can be placed there to detect BSEs.
* SE provide topographical contrast and BSEs provide compositional contrast.