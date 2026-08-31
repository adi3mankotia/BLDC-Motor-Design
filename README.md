BLDC Motor Design, Fabrication & Testing

Overview

This project documents the design, CAD modelling, fabrication, winding, assembly, and testing of a custom three-phase brushless DC (BLDC) motor developed as an electromechanical engineering project.

The motor was designed around a 15 V / 5 A electrical input constraint, with a target operating speed of 3,000 RPM and target torque of 0.12 N·m. The project combined electromagnetic design, SolidWorks CAD, 3D-printed components, N52 neodymium permanent magnets, copper windings, a Wye-connected three-phase stator, and physical prototype testing.

Note: The original detailed calculation worksheet is no longer available. The equations below reconstruct the key engineering relationships used in the design from the original project specifications. Values are presented transparently as design targets or reconstructed calculations rather than as preserved test measurements.

Final Prototype



The final prototype was physically fabricated, wound, assembled, mounted, and tested. The build used a custom stator/rotor geometry, hand-wound copper coils, permanent magnets, a central shaft, and 3D-printed structural components.

Project Objectives

The project was completed to demonstrate the full engineering workflow from electrical-machine theory to a physical prototype:

Requirements → calculations → electromagnetic configuration → CAD modelling → 3D printing → winding → assembly → testing → performance evaluation

The main objectives were to:

design a compact three-phase BLDC motor around a 15 V supply;

target approximately 3,000 RPM and 0.12 N·m torque;

calculate key motor-design relationships including angular velocity, mechanical power, torque constant, back-EMF relationships, and winding requirements;

model the motor components and assembly in SolidWorks;

fabricate the rotor/stator structure using 3D printing;

integrate N52 permanent magnets and copper windings;

connect the stator in a Wye configuration;

assemble and physically test the completed motor.

Design Specifications

Parameter

Design Value

Motor type

Three-phase BLDC

Supply voltage

15 V

Maximum design current

5 A

Maximum electrical input

75 W

Target speed

3,000 RPM

Target torque

0.12 N·m

Stator connection

Wye / Star

Permanent magnets

N52 Neodymium

CAD platform

SolidWorks

Fabrication

3D Printing + manual assembly

The 75 W value represents the electrical design limit implied by the 15 V, 5 A supply:

P_electrical,max = V × I
P_electrical,max = 15 × 5
P_electrical,max = 75 W

Engineering Design Relationships

1. Angular Velocity

Rotational speed in RPM can be converted to angular velocity using:

ω = 2πN / 60

For the 3,000 RPM design target:

ω = 2π(3000) / 60
ω ≈ 314.2 rad/s

2. Mechanical Output Power

Mechanical power is related to torque and angular velocity by:

P_mech = τω

Using the target torque and speed:

P_mech = 0.12 × 314.2
P_mech ≈ 37.7 W

This is the mechanical power corresponding to the simultaneous 3,000 RPM / 0.12 N·m target operating point.

3. Electrical Input Power

Electrical input power is:

P_in = VI

At the maximum 15 V / 5 A design constraint:

P_in = 15 × 5
P_in = 75 W

The electrical input limit and the target mechanical operating point are separate design quantities. Actual efficiency requires measured electrical input and mechanical output at the same operating condition.

4. Efficiency

Motor efficiency is calculated from:

η = (P_mech / P_in) × 100%

A verified efficiency value requires voltage, current, speed, and torque measurements taken at the same operating point. Because the original detailed test worksheet is no longer available, this repository does not claim a reconstructed efficiency as a measured result.

5. Torque Constant

The motor torque constant relates electromagnetic torque to current:

K_t = τ / I

The exact value depends on the current definition and operating condition used in the original design. The relationship was part of the motor-sizing process, but the original calculation sheet is unavailable.

6. Back-EMF Constant

Back electromotive force increases with rotor speed and can be represented by:

E = K_e ω

where:

E = back EMF

K_e = back-EMF constant

ω = angular velocity

A numerical back-EMF constant is not reconstructed here because the original measured/generated back-EMF value is unavailable.

CAD Design

The motor components and full assembly were modelled in SolidWorks before fabrication. The CAD stage was used to define the motor geometry and evaluate component fit, shaft alignment, rotor/stator spacing, and assembly feasibility.

Full Assembly



Stator / Internal Geometry



Side View



The repository includes the original native SolidWorks files:

cad/solidworks/
├── BLDC_Motor_Assembly.SLDASM
├── Rotor.SLDPRT
├── StatorTop.SLDPRT
└── StatorBottom.SLDPRT

Electromagnetic Configuration

The motor used a three-phase stator with copper windings and N52 neodymium permanent magnets in the rotor. The stator phases were connected in a Wye (Star) configuration.

The electromagnetic design process considered target torque and speed, supply-voltage/current constraints, winding turns and available slot space, permanent-magnet strength and placement, rotor/stator geometry, air-gap control, back-EMF behaviour, and mechanical fit/alignment.

Fabrication & Assembly

After the CAD design was completed, the major structural components were 3D printed and assembled into the physical motor.

The build process included CAD modelling, 3D printing, stator winding, N52 magnet installation, three-phase Wye connection, shaft/mechanical assembly, full motor assembly, mounting, and pre-test checks.



Testing

The completed motor was physically tested after assembly.

Before operation, the prototype was checked for rotor/stator clearance, shaft alignment, winding continuity, phase connections, magnet placement, mechanical interference, secure mounting, and supply-voltage/current limits.

Testing was used to evaluate the prototype as a complete electromechanical system and to identify differences between theoretical design targets and real-world performance.

Because the original detailed measurement sheet is no longer available, this repository distinguishes design targets from verified measurements and avoids presenting reconstructed values as experimental data.

Engineering Lessons Learned

This project demonstrated that successful electric-machine design depends on more than analytical calculations. Physical performance is also affected by manufacturing tolerances, winding feasibility, air-gap control, magnet placement, shaft alignment, friction, material properties, and assembly quality.

The project provided hands-on experience connecting:

electromagnetic theory + electrical calculations + CAD + fabrication + wiring + mechanical assembly + testing

into one complete engineering system.

Repository Structure

BLDC-Motor-Design-and-Fabrication/
│
├── README.md
├── cad/
│   ├── solidworks/
│   │   ├── Rotor.SLDPRT
│   │   ├── StatorTop.SLDPRT
│   │   ├── StatorBottom.SLDPRT
│   │   └── BLDC_Motor_Assembly.SLDASM
│   ├── step/
│   └── stl/
├── images/
│   ├── physical_motor.jpg
│   ├── full_assembly.png
│   ├── stator_design.png
│   └── side_view.png
├── calculations/
│   └── design_calculations.md
├── testing/
│   └── test_results.md
└── report/

Tools & Skills Demonstrated

Electrical Engineering: BLDC Motor Design, Electric Machines, Electromagnetic Design, Three-Phase Windings, Wye Connection, Back-EMF, Torque/Speed Relationships

CAD & Fabrication: SolidWorks, 3D Printing, Component Design, Assembly Modelling, Prototype Fabrication

Hardware: N52 Neodymium Magnets, Copper Windings, Shaft/Mechanical Assembly

Engineering Process: Requirements Definition, Design Calculations, CAD Modelling, Fabrication, Assembly, Testing, Design Evaluation

Future Improvements

Future development could include quantitative characterization of the motor using a tachometer, current/voltage sensing, torque measurement, and back-EMF measurements. The CAD could also be refined to reduce the rotor-stator air gap, improve shaft/bearing alignment, increase winding space, and improve manufacturing tolerances.

Additional testing could produce verified speed-torque curves, efficiency maps, current measurements, thermal data, and comparisons between theoretical predictions and measured performance.

Project Summary

This project involved the complete design and physical construction of a custom three-phase BLDC motor. Starting from electrical and mechanical requirements, the motor was modelled in SolidWorks, fabricated using 3D-printed components, wound by hand, assembled with N52 permanent magnets in a Wye-connected configuration, and physically tested.

The project demonstrates practical experience in electric-machine design, electromagnetic calculations, CAD, prototyping, fabrication, and engineering testing.
