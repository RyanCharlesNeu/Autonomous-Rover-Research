# Autonomous-Rover-Research
**Wheeled Rover for Collaborative Off-Road Robot Teams**
<br>
**L3Harris HAV Lab**
<br>
**Advisor: Dr. Sun**

<!-- HERO IMAGE: full rover photo or render -->
<img src="assets/rover-hero.jpg" width="40%" />

## Overview

This project is an autonomous wheeled rover designed to operate as part of a heterogeneous, off-road robot team. Unlike a standalone rover, this design has to do double duty: it needs to move independently across rough terrain, and it needs to be able to physically pull and be pulled by other robots in the team. That second requirement drove the entire design process, since it meant the chassis, motors, and drivetrain all had to be sized around real towing loads, not just the rover's own weight.

The sections below walk through the build in the order it actually happened: from load calculations, to CAD, to fabrication, to the current state of the electronics.

## Design & CAD

<img src="assets/rover-cad-original.png" width="70%" />

*Early CAD design of the rover chassis. This is an earlier iteration, not the final design, shown here to document the design process.*

Before modeling anything, the rover's motor and material requirements were driven by the pull/be-pulled requirement: weight and torque calculations determined the motor sizing needed to both move the rover itself and tow another robot in the team. Those calculations set the material and component list that the CAD design was built around.

## Fabrication

<img src="assets/rover-chassis-assembly.jpg" width="70%" />

*Chassis assembly. The chassis was machined from aluminum.*

The chassis was manufactured in aluminum based on the CAD design above. All machining was done in-house as part of the build.

## Electronics & Testing

With the chassis built, the electrical build followed in this order: motors installed onto the chassis, full system wiring completed, ESC (electronic speed controller) holders built and mounted, and ground/signal wires soldered onto the ESCs. Controller responsiveness was then tested to confirm the drivetrain responds correctly to input before moving on to sensing and autonomy.

<details>
<summary><strong>Coming soon: wheels, LiDAR & autonomy (click to expand)</strong></summary>

<br>

The next stage of the build, expected within the next few days, adds:

- **Wheels** mounted to the completed chassis and drivetrain
- **LiDAR** for terrain and obstacle sensing
- **Raspberry Pi** running simple optical detection

This section will be updated with photos, video, and results once that stage is complete.

</details>

## Status

The rover is under active development. Chassis fabrication and core drivetrain electronics (motors, wiring, ESCs) are complete and tested. Wheels, LiDAR, and Raspberry Pi-based optical detection are the immediate next steps.

## Future Work

- **Wheel mounting** and drivetrain integration
- **LiDAR-based terrain sensing**
- **Raspberry Pi optical detection** for basic obstacle/object recognition
- **Autonomous navigation** within the broader heterogeneous robot team
- **Field testing** of pull/tow capability with other team members
