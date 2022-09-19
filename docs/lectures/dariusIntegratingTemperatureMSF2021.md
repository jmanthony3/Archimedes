<script type='text/javascript'
    src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS_CHTML'>
</script>
<script type='text/x-mathjax-config'>
    MathJax.Ajax.config.path['Extra'] = 'https://jmanthony3.github.io/Codes/MathJax/extensions/TeX',
    MathJax.Hub.Queue(['Typeset',MathJax.Hub]);
    MathJax.Hub.Config({
        TeX: {
            equationNumbers: {
                autoNumber: 'AMS'
            },
            extensions: [
                '[Extra]/MechanicalMetallurgy.js',
                '[Extra]/NumericalMethods.js'
            ]
        },
        tex2jax: {
            inlineMath: [['$', '$'], ['\\(', '\\)']],
            blockMath: [['$$', '$$'], ['\\[', '\\]']]
        },
    });
</script>
= Integrating Temperature Dependence into a Microstructure-Sensitive Fatigue Model for #titanium Alloys
*Presenter:#Jared-Darius*

_Advisor: Dr. Marcos Lugo_

Committee:
* Dr. Mark Horstemeyer
* Dr. Heechen Cho
* Dr. Brian Jordon

== Abstract
Abstract:

This work seeks to integrate temperature dependence into a microstructure-sensitive fatigue model for #titanium alloys produced by both extrusion and electron beam melting (EBM) additive manufacturing, revising and enhancing the MultiStage Fatigue (MSF) model as the foundational model framework. Traditional fatigue modeling has required design engineers to conservatively use a lower-bound estimate of fatigue life predictions given a statistically significant spread of experimental data that can span up to two or sometimes three orders of magnitude for a given test condition. This variation in fatigue data has since been accounted for with the advent of the MSF model, linking individual microstructures to their influence on fatigue life in three distinct stages: incubation, small crack growth, and long crack growth. Since the inception of the MSF model in 2003 by McDowell et al. [1] where it was applied to a cast aluminum alloy, its application has been expanded to a wide range of aluminum alloys, #magnesium alloys, steels, polymers, and even one #titanium alloy made by laser engineered net shaping (LENS). The MSF model correlates a set of parameters to unify model constants for a given material chemistry across a range of alloys and processing methods. Currently, the Ti-6Al-4V (Ti64) alloy is being implemented in aircraft and spacecraft as a corrosion-resistant lightweight structural metal with good strength retention at elevated temperatures. However, the MSF model lacks any temperature dependence. Therefore, this work integrates a temperature dependence to the MSF model for the first time, applying the model to the Ti64 alloy in two new processing methods. First the microstructure of both materials is characterized. Next, monotonic and fatigue experiments are conducted with both extruded and EBM Ti64 at room temperature and at elevated temperatures (150, 300, and 500 °C). Subsequent fractographic analysis reveals the most deleterious microstructures and failure mechanisms. The experimental work informed the model development for both materials, implementing a revised version of the MSF model that refines and formalizes the changes and additions that have been made over the past two decades.

== Slides
1. Outline
    1. Why is this important, what is missing, how will this be filled, what results fill that?
    2. Q&A
2. Bridging the Gap
    1. Fatigue: cyclic damage to microstructure over time.
    2. **Well-defined and explained the history (from 1900's) and definition of fatigue.**
    3. **Good job explaining what is required to move forward.**
3. Intellectual Merit (ums - 5)
    1. Why EDM: reduce weight and greater control of geometry and structure.
    2. The updated MSF model can fill the void of understanding these EDM manufactured components.
    3. _Can be applied to other metal microstructures?_
4. Justification (ums - 1)
    1. MSF better fits experiments over Coffin-Manson and Ramberg-OSgood.
    2. **Gestured to presented material, but not indicative to TEAMs attendees)
5. Why Ti64? (ums - 1)
    1. _Previously misunderstood metal now covers over half the manufactured #titanium?_
6. CPSPP (ums - 3)
    1. **Good covering the "TTT"-esqueness of $\beta$ to $\alpha$ phases.**
    2. **Good explaining what "creep" is.**
    3. _Recrystallization not seen in performance life?_
7. ICME
8. Foundations of MSF
    1. **Good introducing concepts and inputs.**
9. Temperature Influences
    1. **I love butter!! Good example!**
    2. **What is monotonic?Gave an analogy for non-engineering audience, then used an engineering keyword.**
10. Arrhenius Equations (ums - 1)
    1. Typically, increasing temperature increases chemical reaction rates (just as learned in high school chemistry).
11. 4 Objectives
12. Methodology
    1. **Lots of specimens!!**
13. Experiment Machines
14. Microstructure Characterization
15. EBM Surface (ums - 2)
    1. _Fatigue has been considered a surface phenomenon, does updating this MSF model require considering internal fatigue cracks?_
    2. **Comparing to mirror finish was helpful for understanding just how "rough" EBM is to microstructure.**
16. Polished and Etched
    1. _Is the band at the edge an example of gradient-structured grains from cooling during EBM manufacture?_
17. Characterizing Microstructure (ums - 1)
18. cont... (ums - 3)
    1. **Who cares what 10x is? What length scale??**
19. cont...
20. Statistics (ums - 5)
    1. **Good explaining the normal distribution of EBM particle size before and after build. I felt that I gained more understanding here.**
21. Monotonic Behavior
22. EBM and Extruded (ums - 2)
23. Fractography (ums - 2)
24. Lack of Fusion
25. Temperature-Dependent Behaviors (ums - 3)
26. Fracture Surface at 4 Temps. (ums - 2)
    1. **Void nucleation, coalescence, and growth!**
27. Cyclic Behavior
28. Room Temps
    1. **Appreciated drawing out the key point from the graph.**