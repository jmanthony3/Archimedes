# Lesson 19: Multi-Stage Fatigue (MSF)

1. Bring in the #boundary-conditions.
   1. #fatigue uses the #microstructure to predict #fatigue-life.
2. Flaws are assumed inclusions.
   1. Because #oxides at the front of molten metals #nucleation faster, they become ceramic #pores.
   2. Gases gather here and #pores can become bigger.
   3. #notch-root-radius, edge effects are #pores near the surface.
   4. #eutectic regions the last to form.
   5. Very complex defect sizes.
   6. "What if each these causes the #failure?"
      1. #pregnancy: #pore-incubation
      2. Smaller the #cracks, #crack-incubation quicker and higher #crack-growth-rate
      3. Bigger #pores take longer to become #cracks.
      4. #crack-incubation faster at smaller #pores, but #cracks are smaller.
      5. Bigger #pores incubate slower, but the #cracks are bigger.
      6. This means the driving force of bigger #pores is greater: the greater the growth.

!!! question What is the underlying physics that drive smaller #cracks to grow faster than large ones?
    Only the spring constant between atoms resists the #crack-growth.
    Easier to grow at smaller distances than larger.

!!! question Is this where energy comes in ( #Gibbs-Free-Energy or Holden's)? <cite> 
    Yes.
    #Mark-F-Horstemeyer thinks in dissipation of increasing #free-surface that identifies new #ISV.
    #Doug-Baumann thinks of energy states.

!!! question Would a wrought or sintered metal have faster #crack-incubation? <cite> 
    Wrought will incubate sooner, but can live much longer with the #cracks.
    A sintered material can survive orders of magnitude more cycles, but will fail instantly with a single #crack-initiation.

    !!! quote #Jared-Darius
        Possibly because of local [plasticity](../engr-839-001-mechanical-metallurgy/plasticity.md).

    The incubation time is longer in sintered, but #fatigue-life is longer for wrought.
    This follows the #CPSPP logic.

1. There is a transition point from #short-crack to #long-crack growth.
   1. After a [critical crack length](critical-crack-length.md), the slopes are equivalent for various sized specimens, because they entered the #long-crack regime ( #fatigue ).
2. Rely on local, shear #plastic-strain ranges.
   1. Because, the inclusions move along #glide-planes or #shear-planes back and forth.
   2. #Mode-II / #Mode-III deformation.
3. Fatigue Indicators
   1. The #beach-striations are #mesoscale indicators of #slip-plane (ex)intrusions.
   2. Switches to #Mode-I when #long-crack.
4. #microstructure-crack versus #long-crack
   1. #multisite-small-crack goes around the particles: $K_{max, elastic} < 6~MPa\sqrt{m}$.
   2. #long-crack goes straight through the particles: $K_{max, elastic} > 6~MPa\sqrt{m}$.
   3. The #edge-crack can give clues.
5. The size of the specimen dictates if particles or #pores drive #crack-growth.
6. Cast metals have smooth, shiny #pores. #cracks begin from here. 
   1. Wrought materials still exhibit this, sometimes, because the billet was cast.
   2. The thumbnail will have #river-marks that point to where the #fatigue-cracks nucleated.
   3. #cracks move #orthogonal to [striations](striations.md).
   4. Relies on geometry (strain) considerations, but some people will ask about load (stress) considerations with #stress-intensity and such.
7.  $\frac{da}{dN}$ mechanics only: no #microstructure considerations. Can include #mode-mixing.