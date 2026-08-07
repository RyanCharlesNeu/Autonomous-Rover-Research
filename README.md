## Autonomous Rover
**Wheeled Rover for Collaborative Off-Road Robot Teams**
<br>
**L3Harris HAV Lab**
<br>
**Advisor: Dr. Sun**
<br>
**Role: Undergraduate Research Assistant**

<!-- HERO IMAGE: full rover photo or render -->
<img src="assets/rover-hero.jpg" width="40%" />

## Overview

This project explores physical collaboration between robots in a heterogeneous, off-road team, specifically, how robots with different capabilities can support each other to move across terrain that would stop any one of them alone. The core idea: each robot in the team has different strengths, and by working together, they can lean on each other's strengths in situations where their own platform falls short, letting the team perform beyond what any single robot could do alone.

<img src="assets/AutonomousRobotTeam.png" width="49%" />

*Renderings of a heterogeneous robot team operating together.*

An early proof-of-concept demonstrated this directly: a wheeled robot, initially unable to move under an applied load, regains motion once a drone lifts a portion of that weight, reducing static friction enough for the robot to drive forward. As part of this work, I calibrated a RadioLink drone using ArduPilot and delivered a multi-robot coordination demonstration and presentation to the Army Research Lab.

<!-- PROOF OF CONCEPT VIDEO -->
https://github.com/user-attachments/assets/ae976bf7-49cf-4480-8de5-11d52da3f888

Building on that proof of concept, the current phase of the project is the wheeled rover itself, a purpose-built platform designed not just to move independently, but to physically pull and be pulled by other robots in the team. The sections below cover that build.

## Research Program

This work sits within a broader research effort, **Autonomous Vehicle Coordination on Complex and Extreme Terrains**, developing a multi-modality UGV-UAV team (wheeled, tracked, and legged ground robots, plus an aerial drone) that uses physical coordination and joint path planning to traverse terrain no single platform could cross alone.

My part in this: build and autonomize the wheeled rover first, then extend autonomy to a legged platform, then develop a mechanism that lets robots physically connect and push or pull each other autonomously.

## Design & CAD

<img src="assets/rover-cad-original.png" width="70%" />

*Early CAD design of the rover chassis. This is an earlier iteration, not the final design, shown here to document the design process.*

Before modeling anything, the rover's motor and material requirements were driven by the pull/be-pulled requirement: weight and torque calculations determined the motor sizing needed to both move the rover itself and tow another robot in the team. Those calculations set the material and component list that the CAD design was built around.

## Fabrication

**Chassis**

https://github.com/user-attachments/assets/ddc288d6-379b-4fef-987a-e665b07f313f

*Chassis assembly. The chassis was machined from aluminum.*

<img src="assets/rover-chassis-lid.jpg" width="55%" />

*Chassis with lid attached.*

The chassis was manufactured in aluminum based on the CAD design above. All machining was done in-house as part of the build.

**Motor Mounting**

<img src="assets/MotorMounting.jpeg" width="40%" />

*Motor mounting. Mounting holes were drill pressed directly into the aluminum chassis.*

**Battery Holder & ESC Mounts**

<img src="assets/battery-esc-mount-cad.png" width="55%" /> <img src="assets/battery-esc-mount-printed.jpg" width="39%" />

*CAD design (left) and the 3D-printed PETG battery holder and ESC mounts (right). Mounting holes were drill pressed and the parts secured to the chassis.*

**Wheel Attachment**

<img src="assets/wheel-attachment-render.png" width="55%" />

*Rendering of the wheel attachment design. The mating piece was lathed to attach to the wheel; wheel installation is in progress.*

## Electronics & Testing

The ESCs were soldered together and wired in parallel. This wiring was done without PWM signal splitting, a simpler approach that works for this stage of testing but isn't the most refined method; it's a known area for cleanup in a later iteration.

With wiring complete, the ESCs were configured, and the signal and ground wires were soldered onto the receiver pins to enable motor control testing with a receiver/transmitter pair.

<!-- DEMO VIDEO: wheels turning under receiver/transmitter control -->
<!-- [drag video file into editor here] -->

*Demo: motor control test showing the wheels turning under receiver/transmitter input.*

Controller responsiveness was confirmed through this test before moving on to sensing and autonomy.

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
