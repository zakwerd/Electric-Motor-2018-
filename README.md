# Electric Motor Project (2019)
Designing and Building an Electric Motor Optimized for High RPM with [Ethan Zhang](https://www.linkedin.com/in/ethnzhng/)

## Abstract
This paper describes the design process and results of a two-phase, four pole, brushless, DC electric motor that was optimized for rotational speed (RPM). Speed optimization was primarily in the form of a robust, compact exterior for maximum stability and minimal vibrations. The motor reached a top speed of 13,140 RPM and averaged 12,120 RPM, both under 28.1 Watts of power. The static torque measured was 0.00019 N⋅m and the dynamic torque was 0.00010 N⋅m. The motor’s efficiency was only 0.163%. Despite the low torque, the high rotational speed gives this motor promise for being used as a vacuum motor (or another type of motor that relies on speed and not torque). 

## Final RPM Results
**Top RPM:** 13,140 RPM  
**Avg. RPM:** 12,120 RPM   
**Awards:** 4th highest RPM in our high school's history!!!

## Design

### Design Overview
The motor is a simplistic two phase, four pole motor that uses a lightweight wooden dowel as its rotor. It has a compact, sturdy shape constructed from 2x4 wood which houses the electromagnets. The rotor is supported by a single steel ball bearing epoxied into ¼ inch plywood. The electromagnets are controlled with two unipolar Hall effect sensors (or simply Hall chips), each angled at 45 degrees towards the rotor and, along with the electromagnets, they are placed as close to the rotor as possible.

![Motor Design](https://user-images.githubusercontent.com/59108656/89957939-90b90c80-dbed-11ea-84a7-c0ea9ff91acc.png)  
*Figure 1. Front and back angle photos of the final motor*

### Design Choices and Reasoning
**Two-Phase Motor Decision**  
Two-phase motors are mechanically and electrically simple, allowing for more time to test and perfect the motor. The simple design narrowed the room for possible errors and unexpected roadblocks (both mechanically and electrically). 

**Electromagnets Embedded Entirely in 2x4 Wood**  
The robust electromagnet holds minimized vibration, maximized stability, and made the motor more compact.

**Wood Dowel Rotor**  
The rotor’s moment of inertia (dependent on mass) directly corresponds to its angular velocity. A lighter rotor enabled a higher RPM.

**Compact 3D Printed Rotor**  
The moment of inertia of a cylinder increases with its radius. Minimizing the size of the rotor minimized its moment of inertia, thus maximizing RPM.

**Single Ball Bearing**  
Testing revealed that two ball bearings dramatically increased the friction of the rotor, reducing RPM significantly. Using one ball bearing came with the cost of a less stable rotor.

![CAD MOTOR](https://user-images.githubusercontent.com/59108656/89958454-bc88c200-dbee-11ea-8d35-1d921f4f19bc.png)  
*Figure 2. CAD displaying front, side, top, and isometric views of the motor (units: inches)*

## Theory of Operation
![Motor Circuit_schem](https://user-images.githubusercontent.com/59108656/89958620-2d2fde80-dbef-11ea-965f-dc8346eea354.png)  *Figure 3. Motor Circuit Diagram*

### Primary Circuit Component Overview:
**NPN Transistors**  
NPN transistors function as switches, allowing current to flow when more than 0.7 V is applied to the base. An NPN transistor works by having three silicon layers sandwiched together. P-layers are doped - meaning other elements are added to the silicon crystal lattice - with elements, typically aluminum, containing three valence electrons (the amount silicon has), resulting in free electron “holes” to be created in the crystal lattice. N-layers are doped with an element, typically phosphorus, containing five valence electrons, creating extra free electrons in the lattice. Free electrons easily move from the p to n layer when a voltage is applied to the base to “saturate” it (meaning the base-emitter and base-collector junctions become forward biased). Once this occurs, current can flow from the collector to emitter.

**Unipolar Hall Chips**  
Unipolar Hall Chips work under the Hall Effect: on the chip’s p-layer, when a magnetic force is present, the holes (positive charges) are polarized to one side (see Diagram 2). As current is applied, the Lorentz force - a force exerted by a magnetic field on a moving charge - also polarizes the charges. The separation of charges creates a potential difference in the p-layer (labeled as V_H in Diagram 2), resulting in current to flow through the connected, polarized ends (Hall Chip output).

![skykhPXZAp5eLY8OijnQQ9g](https://user-images.githubusercontent.com/59108656/89958783-a8919000-dbef-11ea-81fe-7724f4affe32.png)  
*Diagram 2. Visual of a unipolar Hall Chip’s internals when a magnetic field is present* 

**Electromagnets**  
As current flows through a wire, a magnetic field is generated. When a current passes through a coiled wire, or solenoid, a magnetic field is generated through the inside and around the outside of the wire in a figure-eight shape (displayed by Diagram 3). The magnetic field is strongest directly in front of the solenoid (green bar on Diagram 3) and is unapparent when perpendicular to the solenoid (red bar on Diagram 3). Ampere’s Law says the strength of a solenoid’s magnetic field can be approximated by B=unI where u is a constant multiplied by the solenoid core’s relative permeability, n is the number of coils divided by the wire length, and I is the current through the wire. With the solenoids’ generated magnetic fields, the fixed, rotor magnets can be attracted or repelled, spinning the rotor.  
![sOraYdnCH3j2xQVmOM6hviw](https://user-images.githubusercontent.com/59108656/89958876-e8587780-dbef-11ea-8db1-c6db472c0d49.png)  
*Diagram 3. Visual of the magnetic field generated as an electric current passes through a solenoid*

## Next Steps and Motor Improvements

  Although it is occasionally unstable and is very inefficient, in its current state, the motor can achieve a very high RPM. While it’s fast enough to get on the Hall of Fame, there are a number of improvements that could be made. 
	Firstly, the coils could have been precisely wounded (in numbers of turns) to have their magnet strength perfectly balanced, reducing the rotor’s wobbling. More precise tests could have been conducted to optimize the motor’s RPM based on the coil length, wire gauge, number of turns, etc. The frame also could have been cut more precisely, increasing stability and reducing vibrations. The minute errors in the wood cuts propagated into large problems when at high RPMs. A low friction, ceramic ball bearing could have been used in replacement of the steel ball bearing to increase the RPM and efficiency. The wooden rotor had many imperfections that were noticeable at when at high RPM. Using a precisely shaped material, like carbon fiber tubing, for the rotor would reduce wobbling while still maintaining the rotor’s low moment of inertia.

