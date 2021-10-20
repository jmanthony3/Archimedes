# Meeting Minutes
## 210930
*Dr. Atwater Office (CERE)*

Opening comments:
- Inducing compressive stress improves fatigue life: that is why people do it.
- Compare ISV to DAMASK codes, to know the competing theories. DAMASK is younger.
- Very few papers on single-impact in the processing regime. We are not going up to $10^{6}$, but may be worth exploring one or two.
- Do static indenters truly make the same residual stress as dynamic shot? Can explore Brinell/Vickers indent at lower velocity (quasi-static) up to shot for higher velocity.
- Current indenter on Sam's could be set to surface and applied with air pressure behind; however, the force sensor requires a high enough strain rate to actually read data: impact.
- Annealed grains can be quick large, and exploring with nano-indenters are too specific. We could examine with care the changes in microstructures.

>**Q: Dissertation: How doe we explore?** <cite> Dr. Atwater
*A: Compare Brinell indent to shot impact.* 

### Dissertation Proposal Topic Versions
- "Hitting metal with other metal to improve the first metal."
- ISV with ICME modeling of multiscale modeling of deformation and surface nanocrystallization.
- Multiscale modeling of deformation and surface nanocrystallization via ICME Horizontal Bridging Coupled with ISV Theory and Recrystallization Codes
- *Abstract: Single-site impacts for air blast shot peening (ABSP) has been explored to observe changes of the local microstructure according to recrystallization by *

Title and abstract of proposal topic.

The more you read, the more that shapes what you wanna do or what you feel is relevant.

Deformation to grain refinement is not part of original proposal for this work, but these are critical features for performance. Proposal like this is going a step beyond the funding proposal with the experiment; therefore, shot peening research has been done rather broadly, but few include site-specific impact. People get distracted with multiple, random impacts. Slow, quasi-static indents are relevant and more interesting to other, but we want to see how the control of impact changes the material performance.

Does the DAMASK code look at cyclic structure change under strain? E.g. strains by some increment, then outputs that as a initial state for next loop?

>**Q: What is recrystallization?** <cite> Me
*A: If a material has a texture with it and there is much strain in the grains, which may be larger, then grain can reduce its stress by creating boundaries: i.e. breaking into smaller pieces when under elevated temperature. Tempered glass is like this, when struck it shatters into tiny pieces. When given energy, those grains will fracture into smaller ones, which can subsequently grow. Typically 0.4 the melting point; although, this depends on the impurities in the material. The more impure, the greater the temperature required to recrystallize.*

Reverse phase transformation from tetragonal [[bcc]] to [[fcc]]. Austenite is meta-stable. Retained austenite when quenching to form martensite, but austenite volatile at room temperature; therefore, quenched to freezing to convert remaining austenite to martensite. Martensite has weird needles that interferes with austenite transformation. Austenitic stainless is stable at room because of alloying elements. 

Temperature increasing at impact site? Discussion in ball milling particles of metal there exists a temperature spike, because of the kinetic energy transfer. Ball mill vials can come out hundreds of Kelvin.

>**Q: what is with temperature and recrystallization?** <cite> JMA3
*A: Dislocation density begin forming dislocation cells within grains, which get locked together. Low angle grain boundaries can be thought of as coordination of dislocation. More dislocations can form more grain boundaries. Temperature could prevent that from happening. Cryo-milling develops grin structure faster; more heat allows strain release from in the grains. Higher temperature cryo-milling loses ductility. Heat erases internal strain in material, which starts with dislocations, void, and grain boundaries.*

Martensite laths are brittle. If something ductile is put between them, is there more ductility? This sounds like refining, because the grains are being reshaped. Local temperature rises (generally $> \{300, 400, 500, 1000\}\text{\textdegree}C$). Collect thermal imaging of specimen: copper dissipates very quickly.

>**Q: How do we tie deformation to microstructural changes** <cite> MA
*A: Strain rate, total deformation, temperature. What variables are import? What available models incorporate those variables? What approach can be sued to connect all these dots? This is the proposal: not knowing what works best, but asking which one does best. ISV or DAMASK? Compare or incorporate data between these models. A way to improve material performance needs to be quantified, because some works have done so but not in a cohesive way. We present a model/method to show how to connect all these dots. Compare this and verify with experiment: linear ball peening.*

Can include low and high strain rate events. Not necessarily the ballistic level. But what is the limit? We may not need to worry about the mechanisms of deformation for our application, but we should say the limit before another method is required. Coerce experiment simulation and highlight the kepypoints in the abstract.


---


## 