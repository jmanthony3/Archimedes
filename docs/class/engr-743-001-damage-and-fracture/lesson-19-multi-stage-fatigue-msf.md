# Lesson 19: Multi-Stage Fatigue (MSF)

1. Bring in the boundary conditions.
   1. #fatigue uses the microstructure to predict #fatigue-life.
2. Flaws are assumed inclusions.
   1. Because #oxides at the front of molten metals nucleate faster, they become ceramic pores.
   2. Gases gather here and pores can become bigger.
   3. Notch root, edge effects are pores near the surface.
   4. #eutectic regions the last to form.
   5. Very complex defect sizes.
   6. "What if each these causes the failure?"
      1. Pregnancy: incubation of pores
      2. Smaller the crack, it incubates quicker and grows.
      3. Bigger pores take longer to become a crack.
      4. Cracks incubate faster at a smaller pores, but its crack is smaller.
      5. Bigger pores incubate slower, but the crack is bigger.
      6. This means the driving force of bigger pores is greater: the greater the growth.
   7. _Q: What is the underlying physics that drive smaller cracks to grow faster than large ones?_ 
   8. **A: only the spring constant between atoms resists the #crack-growth. Easier to grow at smaller distances than larger.**
   9. _Q: Is this where energy comes in (Gibb's or Holden's)?_
   10. **A: Yes. Dr. H thinks in dissipation of increasing #free-surface that identifies new #ISV. Baumann thinks of energy states.**
   11. _Q: Would a wrought or sintered metal incubate faster?_
   12. **A: Wrought will incubate sooner, but can live much longer with the crack. A sintered material can survive orders of magnitude more cycles (>possibly because of local plasticity <cite> JD), but will fail instantly with initiation of a single crack. The incubation time is longer in sintered, but #fatigue-life is longer for wrought. This follows the process-structure-properties logic.**
3. There is a transition point from #short-crack to #long-crack growth.
   1. After a critical crack length, the slopes are equivalent for various sized specimens, because they entered the #long-crack regime ( #fatigue ).
4. Rely on local, shear #plastic-strain ranges.
   1. Because, the inclusions move along #glide-planes or #shear-planes back and forth.
   2. Mode II/III deformation.
5. Fatigue Indicators
   1. The #beach-striations are #mesoscale indicators of #slip-plane (ex)intrusions.
   2. Switches to Mode I when #long-crack.
6. MSC versus LC
   1. #multisite-small-crack goes around the particles: $K_{max, elastic} < 6~MPa\sqrt{m}$.
   2. #long-crack goes straight through the particles: $K_{max, elastic} > 6~MPa\sqrt{m}$.
   3. The #edge-crack can give clues.
7. The size of the specimen dictates if particles or pores drive crack growth.
8. Cast metals have smooth, shiny pores. Cracks begin from here. 
   1. Wrought materials still exhibit this, sometimes, because the billet was cast.
   2. The thumbnail will have river marks that point to where the fatigue crack nucleated.
   3. Cracks move orthogonal to striations.
   4. Relies on geometry (strain) considerations, but some people will ask about load (stress) considerations with stress intensity and such.
9. $\frac{da}{dN}$ mechanics only: no microstructure considerations. Can include Mode-mixing.