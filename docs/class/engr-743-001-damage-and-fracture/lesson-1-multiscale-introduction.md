# Lesson 1: Multiscale Introduction

## What is #failure?
Examples:
- Ford designs for yield and GM goes to fracture
- However, it could be environmental
- Fracture
- Excessive Yielding
- Environmental
  - Corrosion
  - UV Attack
  - Oxygenation
- Discoloration

>"It is the inability of a component to function as intended." <cite> Dr. Mark Horstemeyer

## What is Analysis?
- Asking questions:
  - What caused it?
    - Poor initial design
    - Inadequate design info
    - Change in use
  - How many affected?
  - Can it be tolerated until repair?
  - How can it be fixed?
- Doing analysis.
- Observation
- Simulation is for insight.
- Sometimes, just do nothing except sit back through forensic study.

## How Do Materials Break?
- #ductile-brittle-fracture
- Principles of #fracture-mechanics
- #fatigue (Cyclic stresses)
  - Cyclic stresses, S-N curve
  - #crack-initiation/#crack-propagation
  - Factors to affect fatigue behavior
- #creep (time dependent deformation)
  - Stress/Temperature effects 
    - More temperature -> More creep
    - Like old, glass windows
  - Alloys for high-temperature use
- Must understand material structures and phase transitions.
  - Based on structure from chemistry
  - Can be categorized as some basic properties

## Engineering Materials
- Metals and Alloys
  - Metallic or crystalline
  - Strong, ductile, conductive
  - Fracture and fatigue
- Ceramics, Glass, and Glass-Ceramic
  - Ionic and covalent bonds
  - Crystalline and amorphous
  - Strong/Hard which resists corrosion/temperature
  - Brittle
- Polymers
  - Covalent or chain molecules
  - Cheap, lightweight and corrosion resistant
  - Weak and creep
- Composites
  - Various materials
  - Matrix fibers
  - Strong and lightweight
  - Expensive and delamination

## Ideal vs. Real Materials
- Every material has behavior according to its constitution
- Stress-strain for physical, solid materials
  - Davinci studied this (500 yrs. ago) with wire:
    - The longer wire failed at smaller loads than shorter wire of equal gage
    - **More volume = More possible void locations and growth**
  - _insert image later_

## What is Failure Prevention?
- Learning from mistakes.
>"Failure is success if learned from." <cite> MH
- Key to design

## How Do We Make Our Design Come Alive?
- Design
  - Performance/Economy
  - Safety/Durability
  - **Know the Boundary conditions. Know the normal and extreme environments.**
- Complexity
  - State of stress: uni(bi)(tri)-axial
    - More loading directions = Higher void growth rate
    - >_**Opposite to [von Mises](https://en.wikipedia.org/wiki/Von_Mises_yield_criterion)**_ <cite>DK :=
      - Scalar value (average) of all loading directions
      - Yield point is failure criterion
      - **Failure is often past yield point**
- Failure is not exclusively [von Mises](../engr-727-001-advanced-mechanics-of-materials/distortion-energy-theory-von-mises.md)
- Failure occurs when a component no longer functions as intended, which usually occurs at fracture.
  - Flaws and cracks exist initially
  - Period of applied loads
  - Cyclic loadings
- Objective
  - *Know the modes of failure for materials*
  - Relationship between mechanical behaviors

## Selection of Materials
>"Never assume a material behaves as intended." <cite> MH
- Classification
- Merits
  - Cost
  - Strength
- Case Studies (fancy name for a _report_)
  - Summary of events
  - Documentation/Analysis
  - Ramifications

## Case Study: Tin Can
1795. Napoleon to preserve food
1809. Nicolas Appert
1810. Peter Durand got patent from King George III by adding tin for corrosion resistance
1824. William Perry's Arctic Expedition
1866. E. M. Lang got patent
1876. Hume "Floater"
1890. _asdf_
Materials: originally tin, but not recyclable
1891. Coors made recyclable aluminum cans
Mechanics of opening used an old "church key"
1963. Pop Top invented, but litter and hazard
1975. It is what it is today

### Summary
- Pop top must fail, on demand, in a certain way
- Form followed function as developed
- Inherent problems still exist
- Failures advanced design