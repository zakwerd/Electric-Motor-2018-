# Electric Motor Project (2019)
Designing and Building an Electric Motor Optimized for High RPM with [Ethan Zhang](https://www.linkedin.com/in/ethnzhng/)

## Abstract
This paper describes the design process and results of a two-phase, four pole, brushless, DC electric motor that was optimized for rotational speed (RPM). Speed optimization was primarily in the form of a robust, compact exterior for maximum stability and minimal vibrations. The motor reached a top speed of 13,140 RPM and averaged 12,120 RPM, both under 28.1 Watts of power. The static torque measured was 0.00019 N⋅m and the dynamic torque was 0.00010 N⋅m. The motor’s efficiency was only 0.163%. Despite the low torque, the high rotational speed gives this motor promise for being used as a vacuum motor (or another type of motor that relies on speed and not torque). 

## Final RPM Results
**Top RPM:** 13,140 RPM  
**Avg. RPM:** 12,120 RPM   

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
