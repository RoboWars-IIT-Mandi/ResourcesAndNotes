# **Upgrading Your 8KG Combat Robot: A Technical Guide for Student Teams**

## **1\. Introduction: Gearing Up for the 8KG Challenge**

Leading a college combat robot team presents a unique and rewarding engineering challenge. This report serves as a technical guide for the project lead and team members tasked with upgrading an existing 8KG battlebot. Building upon foundational experience with smaller 1.5KG bots, the focus here is on enhancing specific systems – namely, the drive motor mounts and the drum weapon's power source – while also addressing crucial aspects of project management, reliability, and safety pertinent to this larger weight class.

The journey outlined will encompass a systematic assessment of the current robot, strategic planning for the required upgrades, detailed guidance on designing and implementing robust drive motor mounts, selecting and integrating a high-revolutions-per-minute (RPM) brushless motor for the weapon, ensuring overall electrical and mechanical integrity, prioritizing safety protocols (particularly concerning Lithium Polymer (LiPo) batteries and high-energy spinning weapons), leveraging valuable community resources, and effectively managing the student team. Successfully navigating these steps will prepare the team for the demanding environment of combat robotics competition.

## **2\. Phase 1: Project Kick-off \- Assessment and Planning**

Before embarking on modifications, a thorough understanding of the existing platform and clear project goals are essential. This initial phase lays the groundwork for successful upgrades.

### **2.1 Evaluating the Current Bot**

A systematic inspection is the first critical step. This involves meticulously documenting the robot's current state to establish a baseline for upgrades.

* **Chassis and Structure:** Examine the main frame material (e.g., aluminum, steel, polymer 1), construction methods (welded, bolted), and identify any signs of stress, damage, or potential weak points from previous use. Note existing mounting provisions.  
* **Weapon System:** Document the current drum weapon's dimensions (diameter, length), material, estimated weight, the type and specifications (if known) of the existing 1000rpm motor, bearing types and condition, and how it's currently mounted to the chassis.  
* **Drive System:** Identify the existing drive motors (brushed/brushless, model if possible), associated gearboxes (type, ratio), wheel type and diameter, and critically, the design and condition of the current motor mounts that are slated for replacement.  
* **Electronics:** Determine the battery type (likely LiPo), voltage (e.g., 3S/11.1V, 4S/14.8V 2), capacity (mAh/Ah), the Electronic Speed Controllers (ESCs) for drive and weapon, the Radio Control (RC) receiver model, the quality and routing of existing wiring, and the type and location of the main power switch/disconnect.4  
* **Weight and Space Constraints:** Accurately weigh the fully assembled robot. Compare this to the 8KG competition limit (note: 8kg is approx. 17.6 lbs, falling between Hobbyweight (12lb) and Featherweight (30lb) classes, or near the 15lb BotsIQ class 6). Measure the available internal space for new components, considering the volume required for larger motors, ESCs, and potentially different battery configurations. This initial assessment prevents designing components that won't fit or will push the robot overweight.

### **2.2 Defining Success**

Translate the upgrade requirements into specific, measurable, achievable, relevant, and time-bound (SMART) objectives.

* **Clear Objectives:** Instead of "better mounts," aim for "Design and fabricate drive motor mounts using 7075-T6 aluminum capable of withstanding repeated shock loads without failure, integrating securely with the existing chassis mounting points." For the weapon, define a target like "Increase weapon tip speed by at least 100% by selecting, integrating, and testing a brushless motor system capable of achieving over 5000 RPM under load with a spin-up time under 2 seconds.8"  
* **Realistic Constraints:** Engineering operates within limits. Acknowledge the team's budget, which impacts material choices (e.g., Titanium is strong and light but expensive 9) and component selection.6 Assess the available tools and machining capabilities; complex designs or difficult-to-machine materials like Grade 5 Titanium 9 may require outsourcing 10 or simpler design approaches. Factor in the team's collective skill level and allocate sufficient time for design iterations, fabrication, assembly, troubleshooting, and thorough testing.12 Be aware of common project management challenges like scope creep (avoid adding unplanned features), managing technical complexity, and allocating resources effectively.13

### **2.3 Leading Your Team**

Managing a student team with mixed experience requires structure and clear communication.

* **Leverage Mixed Experience:** The combination of freshers and experienced seniors is an asset. Assign tasks strategically: pair newer members with seniors for mentorship on specific subsystems (e.g., a senior guides a fresher on wiring practices). Understand individual strengths, weaknesses, and interests to assign roles effectively.14 The project lead's role involves directing the right people to the right work.14  
* **Establish Structure & Communication:** While the project lead provides direction, foster a collaborative environment.15 Develop a team charter outlining expectations: meeting frequency and format (e.g., weekly stand-ups 16), communication channels (dedicated Slack, MS Teams, or Discord channels are effective 16), task ownership, decision-making processes, and expected contributions.15 Using agendas for meetings and recording minutes ensures clarity and accountability.15  
* **Project Management Tools:** Implement simple tools appropriate for a student team. Use shared documents (Google Docs, Confluence 16) for design notes and the team charter. Track tasks using work logs or a simple online board, noting responsibilities and deadlines.15 Visualizing the workflow, perhaps with a basic Value Stream Map (VSM) to identify potential bottlenecks in the build process, can be helpful.13  
* **Build Trust & Avoid Micromanagement:** Delegate tasks clearly, giving team members ownership and the freedom to work independently.14 Provide support, answer questions, and check in periodically, but resist the urge to control every detail. This fosters engagement and allows the lead to focus on overall project goals.14 Create an environment where asking questions and seeking clarification is encouraged and seen as positive.16

Establishing clear team structures and communication protocols from the outset is vital for student projects. These teams often face varying commitment levels and diverse skill sets. Without defined roles, goals, and communication methods 15, projects can suffer from confusion, duplicated efforts, or tasks being overlooked. Basic project management practices, such as a team charter, regular focused meetings, and clearly assigned responsibilities 14, provide the necessary framework. This structure minimizes ambiguity and helps integrate the contributions of both new and experienced members effectively, setting the stage for a more organized and successful project, especially under new leadership.

## **3\. Phase 2: Fortifying the Foundation \- Drive Motor Mounts**

The drive system is critical for mobility and control.18 The motor mounts must reliably secure the motors to the chassis despite the violent impacts inherent in combat robotics.7

### **3.1 Design Principles for Robust Mounts**

Effective mount design goes beyond simply holding the motor.

* **Material Selection:** The choice involves balancing strength, weight, cost, and machinability.  
  * **Aluminum Alloys:** 7075-T6 aluminum offers excellent strength-to-weight ratio, significantly stronger than common 6061-T6.9 It's machinable with appropriate tools and techniques.  
  * **Steel Alloys:** 4130 Chromoly steel is strong, tough, weldable, and relatively easy to machine, making it a good choice where weight permits.9 Abrasion-resistant steels like AR400/AR500 offer extreme toughness but are very difficult to machine 10 and typically used for waterjet or laser-cut parts.  
  * **Titanium:** Grade 5 (Ti-6Al-4V) offers strength comparable to some steels at significantly lower density.9 However, it is expensive and notoriously difficult to machine due to work hardening.10  
  * **Plastics:** While high-strength polymers like Carbon Fiber Nylon 7 or UHMW/HDPE 10 might be considered for lighter components, metal alloys are generally preferred for drive motor mounts in the 8KG class due to the high loads involved. The final choice depends on the weight budget remaining after accounting for other systems and the team's fabrication capabilities.6  
* **Stress Concentration:** Design geometry plays a critical role in durability. Avoid sharp internal corners where stresses can concentrate; use generous fillets instead. Ensure sufficient material thickness around mounting holes and load-bearing features. If CAD software with Finite Element Analysis (FEA) capabilities is available, performing even a basic stress analysis can help identify potential weak spots in the design under simulated loads.12  
* **Integration with Chassis:** The mounts must transfer forces effectively to the main robot structure. Design them to mate securely with existing chassis features or strong points. Ensure a large contact area and use multiple fastening points spread out to distribute the load. Consider how impact forces on the wheels will translate through the gearbox, motor, and mount into the chassis.

### **3.2 Mitigating Shock and Vibration**

While combat robots endure extreme conditions, specific vibration dampening for drive mounts can be complex.

* **Passive Dampening Approaches:** Specialized vibration mounts exist 19, often using rubber or springs. However, tuning these correctly is crucial; an improperly selected mount can resonate with the motor or impact frequencies and *amplify* vibrations rather than reducing them.20 A common guideline is that the forcing frequency should be at least three times the natural frequency of the mounted system for effective isolation.20 Incorporating a thin layer of compliant material like rubber or TPU 10 between a rigid metal mount and the chassis *might* offer minimal damping, but care must be taken not to compromise the mount's rigidity, which is essential for maintaining gear mesh and drive alignment under load. In many combat robots, achieving maximum rigidity in drive mounts is prioritized over attempting complex damping.  
* **Secure Mounting as Primary Defense:** The most effective way to combat vibration-induced failures in drive mounts is through extremely secure fastening. Motors must be clamped tightly within their mounts 21, and the mounts must be rigidly bolted to the chassis. Loosening is a primary failure mode.22

### **3.3 Fabrication and Secure Installation**

Proper fabrication and meticulous assembly are critical for mount longevity.

* **Manufacturing:** Select a fabrication method appropriate for the chosen material and design complexity. CNC machining is ideal for precise aluminum or steel mounts. If using advanced polymers, ensure robust printing parameters and consider material properties under impact. Metal remains the standard recommendation for this application in an 8KG bot.  
* **Fasteners:** Use high-strength bolts, such as Grade 8 (Imperial) or Class 10.9/12.9 (Metric). Ensure bolts are long enough for full thread engagement in the mating part or nut, but not so long they bottom out or interfere with other components.  
* **Locking Methods:** This is non-negotiable for combat robots. Apply thread-locking compound (e.g., Loctite Blue 242/243 for serviceability, Loctite Red 271/272 for higher strength/more permanent assembly 9) to all metal-to-metal threaded fasteners, particularly motor mounting screws and any setscrews used on drive hubs or gears.22 Use lock washers (split or tooth type) or nylon insert locknuts (Nylocs) as additional security where appropriate, especially on through-bolts. Proper torque is also essential; use a torque wrench if specifications are available, or tighten firmly by feel using good quality tools.9  
* **Wire Safety:** During installation, carefully route all motor wires. Ensure no wires are pinched between the motor and mount, or between the mount and chassis.21 Secure wires away from potential abrasion points or areas where they could be snagged or damaged by impacts or moving parts.

Drive motor mount failures often stem from issues beyond just the material choice. While a strong material is necessary, inadequate fastening is a frequent culprit.22 Combat robots subject components to intense, repeated shocks and vibrations.7 If fasteners work loose, even the strongest mount can fail, leading to motor misalignment, drive failure, or further damage. The use of thread-locking compounds and ensuring proper torque on high-quality fasteners are essential preventative steps.9 Furthermore, poor geometric design, such as sharp corners or insufficient material around bolt holes, creates stress risers. These points concentrate stress under load, leading to fatigue cracks and eventual failure, even if the bulk material is strong. Therefore, meticulous assembly practices and thoughtful geometric design that distributes loads smoothly are just as crucial, if not more so, than simply selecting the strongest possible material.

## **4\. Phase 3: Unleashing the Drum \- Weapon Motor Upgrade**

Replacing the 1000rpm weapon motor with a high-RPM brushless motor is key to increasing the drum weapon's destructive potential. This involves careful selection, mechanical integration, and electrical system considerations.

### **4.1 Selecting Your Brushless Powerhouse**

Brushless DC (BLDC) motors are the preferred choice for high-speed, high-power weapon systems in modern combat robots.

* **Brushed vs. Brushless:** While brushed DC motors are simple and can be robust, often favored for drive systems due to their resilience 23, brushless motors offer superior efficiency, higher speeds, better power-to-weight ratios, and longer lifespan, making them ideal for spinning weapons.1 The goal of achieving significantly higher RPM necessitates a brushless motor.  
* **Motor Specifications:** Understanding key parameters is vital for selection:  
  * **KV (RPM/Volt):** This constant relates the motor's no-load speed to the applied voltage. The approximate no-load RPM is calculated as RPM=KV×Voltage.2 A higher KV rating results in higher potential speed for a given battery voltage. For an 8KG drum weapon aiming for high energy, motors with KV ratings roughly between 1000KV and 3000KV are common targets, depending on the chosen battery voltage (e.g., 3S/11.1V, 4S/14.8V, or higher) and whether gearing will be used.2 Motors used in featherweight (30lb/13.6kg) bots 7 or powerful drones often fall in this range.24  
  * **Power (Watts, W) & Torque (Newton-meters, Nm or lbf\*ft):** Power indicates the motor's ability to do work over time. Higher power generally allows the motor to spin up a heavy weapon faster and maintain speed during impacts.8 Torque, the rotational force, is crucial for accelerating the drum. It can be calculated from power (P) and angular velocity (ω in radians/sec) using the formula τ=P/ω.8 (ω=RPM×(2π/60)).  
  * **Size & Weight:** The motor must physically fit within the allocated space in the robot and conform to the overall weight budget. Outrunner motors (where the outer case rotates) are common for weapon applications due to good torque characteristics.9 Check dimensions and weight specifications carefully.23  
  * **Shaft Diameter:** The motor shaft diameter (e.g., 5mm, 6mm, 8mm) must be compatible with the chosen pulley, gear, or direct coupling method.9  
* **Candidate Motors:** Explore motors commonly used in the featherweight (30lb/13.6kg) class 7 as a starting point, as the power requirements may be similar. Look at offerings from combat robotics suppliers like ITGresa Robotics 23, FingerTech Robotics 23, Repeat Robotics 23, and general RC/drone suppliers like RobotShop.24 Specific motor series like the D-series outrunners (e.g., D2822, D3536) 23, Propdrive series (e.g., 3536, 4238\) 9, or specialized combat motors (e.g., Just Cuz Robotics JCR-4935 "Cherry Bomb" 23) are often mentioned in build logs and forums.

### **4.2 Proposed Table: Brushless Weapon Motor Candidate Comparison**

To aid selection, comparing potential motors systematically is helpful:

| Motor Model | Supplier | KV Rating | Max Voltage (LiPo Cells) | Max Power (W) | Weight (g) | Shaft Dia. (mm) | Mounting Pattern (mm) | Est. Cost (USD) | Notes |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| *Example: D3536/X* | *Various* | *\~1450* | *3S-4S* | *\~500-700* | *\~100* | *5* | *19x25* | *$20-30* | Common budget choice, various KVs available 23 |
| *Example: Propdrive 4238* | *HobbyKing* | *\~600-800* | *4S-6S* | *\~1000+* | *\~150* | *5* | *25x25* | *$30-40* | Mentioned as featherweight option 9 |
| *Example: JCR Cherry Bomb* | *Just Cuz Robotics* | *Custom* | *6S+* | *High* | *\~200+* | *8* | *Custom?* | *$90+* | High-performance combat-specific motor 23 |
| *Example: Repeat DRIVE MAX* | *Repeat Robotics* | *Custom* | *4S-6S* | *High* | *\~130* | *8* | *25x25* | *$50* | Designed for drive but potentially adaptable, robust 23 |
| *(Add other candidates)* | *(Supplier)* | *(KV)* | *(Cells)* | *(Watts)* | *(grams)* | *(mm)* | *(Pattern)* | *(Price)* | *23* |

*Note: Specific values are illustrative examples; actual specs vary by exact model and supplier. Thoroughly research specific models before purchase.*

### **4.3 Integration Mechanics**

Connecting the motor to the drum requires careful mechanical design.

* **Drive Method:**  
  * **Direct Drive:** Simplest mechanically, but requires the motor to have the exact KV/torque profile for the desired speed and spin-up. Can transmit shock directly to the motor shaft/bearings.  
  * **Belt Drive:** Common method using pulleys and a timing belt (e.g., HTD profile). Allows flexibility in motor choice by using pulley ratios (e=Drum Pulley Teeth/Motor Pulley Teeth) to adjust speed and torque (ωoutput​=ωinput​/e, τoutput​=τinput​×e, assuming input values are at the motor shaft).8 Belts can offer slight shock absorption/slip under extreme load, potentially protecting the motor. Requires careful tensioning.  
  * **Gear Drive:** Can be compact and efficient but requires precise alignment and can transmit shock more directly than belts. Planetary gearboxes are sometimes integrated 9 but add complexity and potential failure points.  
* **Shaft Adaptation:** Brushless motor shafts often need modification. They may need to be cut to the correct length using a Dremel or similar tool.9 Grinding a wide, substantial flat (not just a small divot) onto the shaft is crucial for secure setscrew engagement.9  
* **Pinion/Pulley Mounting:** This connection is critical and prone to failure if not done correctly.  
  * **Press-fitting:** Requires precise tolerances and proper tools. Can be very secure if done correctly.9  
  * **Setscrews:** Most common method. Use at least two high-quality, flat-bottom setscrews (grind tip flat if necessary) tightened securely onto a wide flat on the shaft.9 Use Loctite (Blue or Red, depending on desired permanence) on the setscrew threads.9 Ensure the tool (hex key) is high quality to allow proper torque application.9  
  * **Keyways:** Offer a very secure connection but require a keyway slot on both the shaft and the pulley/gear hub.

### **4.4 Powering and Controlling the Spin**

The electrical system must safely deliver and control the high power required by the weapon motor.

* **ESC Selection:** The Electronic Speed Controller (ESC) is the interface between the battery, receiver, and brushless motor.  
  * **Rating:** Choose an ESC specifically designed for brushless motors. Its continuous current rating (Amps) must comfortably exceed the motor's maximum expected current draw, including startup spikes. A safety margin of 20-50% is recommended.25 The ESC must also be rated for the LiPo battery voltage (cell count/voltage) being used.25  
  * **Features:** Look for ESCs with good heat sinking, programmable parameters (timing, braking), and ideally, features suited for the harsh RC combat environment (e.g., robustness, potentially specific firmware). RC car ESCs (especially sensorless ones for high power) are often suitable.  
  * **BEC:** Some ESCs include a Battery Eliminator Circuit (BEC) to provide 5V power to the RC receiver. However, for critical systems, using a separate, dedicated BEC (sometimes called a UBEC) powered directly from the main battery can be more reliable, as weapon ESC failure won't cut power to the receiver.25  
* **Wiring:** Use appropriately sized wire for the high currents involved. For featherweight-scale power levels, 10 AWG or 12 AWG high-strand-count silicone wire is typically suitable.25 Keep high-current wire runs (battery-to-ESC, ESC-to-motor) as short as possible to minimize voltage drop and resistance. Ensure all connections are mechanically secure and electrically sound. Soldering is strongly preferred over connectors for these paths to minimize resistance and failure points.22 Insulate all connections thoroughly with heat shrink tubing.25

### **4.5 Taming the Spin**

A high-RPM weapon requires careful balancing and safe testing procedures.

* **Weapon Balancing:** An unbalanced spinning weapon is a major hazard. The intense vibration can destroy bearings, motor mounts, and potentially the entire robot structure. Balancing involves ensuring the weapon's Center of Mass (CoM) lies precisely on its axis of rotation.27 While Moment of Inertia (J) affects the stored kinetic energy (KE=0.5×J×ω2) and spin-up time 8, it's the CoM location that determines balance.27  
  * **Static Balancing:** Can be done by placing the weapon on low-friction bearings (e.g., knife edges or smooth bearings) and allowing it to settle. Material is then carefully removed from the heavy side or added to the light side until it shows no preference to rotate to a specific orientation.27 CAD software can often calculate the CoM and help design an inherently balanced weapon.27  
  * **Dynamic Balancing:** More complex, requiring specialized equipment to detect imbalances that only appear at speed. Usually not feasible for student teams but crucial for very high-speed industrial rotors. Good static balancing is typically sufficient for combat robots if done carefully.  
* **Safe Spin-up Testing:** Weapon testing must *always* be conducted in a designated safe environment, such as a sturdy test enclosure or the competition arena itself.  
  * **Procedure:** Ensure mandatory weapon locking devices 4 are in place until the robot is secured in the test area and personnel are clear. Start testing at a very low throttle setting. Listen carefully for any unusual vibrations, grinding noises, or signs of instability. Gradually increase the throttle, observing the weapon's behavior. If severe vibration occurs, stop immediately and re-check balance and mounting security.  
  * **Performance Check:** Time the spin-up to maximum RPM. Compare this to the theoretical spin-up time, which can be estimated (a simplified formula is t≈(J×ωfinal​)/τavg​, where τavg​ is the average torque during spin-up; a rougher estimate is given in 8). Aim for a quick spin-up, ideally under 1-2 seconds, to be effective in combat.8 Successful testing verifies the weapon system's stability and performance before competition.28

Successfully integrating a high-RPM weapon motor requires attention to multiple interconnected systems. Simply choosing a motor with a high KV rating is insufficient. The mechanical mounting of both the motor and its drive components (pulleys/pinions) must be exceptionally secure to handle the generated torque and potential impact shocks.9 Failure here can lead to stripped gears, thrown belts, or detached motors. Simultaneously, the electrical system, including the ESC and wiring, must be robust enough to handle the high current demands, particularly during the initial spin-up phase.25 An undersized ESC or poor wiring connections can lead to overheating, component failure, loss of power, and even fire hazards.22 Therefore, a comprehensive approach that considers the mechanical forces, electrical loads, thermal management, and meticulous assembly is essential for achieving a reliable and powerful weapon system.

## **5\. Phase 4: Building for Battle \- Reliability and Safety**

Combat robots operate in an extreme environment; designing for reliability and adhering to strict safety protocols are not optional, they are fundamental requirements.

### **5.1 Electrical Integrity**

Robust wiring is the nervous system of the robot.

* **Wiring Best Practices:** Select high-quality, flexible silicone-insulated wire. Use an appropriate gauge (thickness) for the expected current – 10 AWG or 12 AWG is common for main power circuits in bots of this size.25 Keep wire runs as short as practical to minimize resistance and voltage drop. Avoid sharp bends that can stress conductors. Route wires away from moving parts (weapon, wheels), potential pinch points, and areas likely to sustain direct hits. Secure wiring looms neatly using zip ties or other management methods. Crucially, insulate *all* exposed solder joints and connections thoroughly using heat shrink tubing.25  
* **Connectors vs. Soldering:** For high-current paths (battery to ESCs, ESCs to motors), direct soldering provides the most reliable, lowest-resistance connection and is strongly recommended.22 Connectors introduce potential points of failure due to vibration, impact, or high current stress.22 If connectors must be used (e.g., XT60, XT90 for battery connection), ensure they are genuine parts rated for the current. Secure the connection physically (e.g., with a zip tie 25) to prevent accidental disconnection during combat.22 Bolted ring terminals offer a very secure and serviceable alternative for power distribution points.25  
* **Preventing Short Circuits:** Shorts are a major cause of electrical failure and potential fires. Double-check polarity before connecting batteries – reverse polarity will instantly destroy most electronics.3 Ensure no stray wire strands, loose fasteners, or conductive debris can bridge contacts. Design the internal layout to physically separate high-power positive and negative terminals where possible. Consider adding non-conductive barriers (e.g., plastic sheets) if needed.

### **5.2 LiPo Battery Discipline**

Lithium Polymer (LiPo) batteries offer high energy density 30 but require strict handling procedures due to their potential fire hazard.3

* **Handling:** Treat LiPos with extreme respect. They store a large amount of chemical energy.29 Visually inspect batteries before each use for any signs of physical damage (dents, punctures, worn insulation). *Never* use a battery that is punctured, crushed, or otherwise physically compromised.30 A common sign of internal damage or failure is puffing or swelling – a swollen LiPo is extremely dangerous and indicates a high risk of fire or explosion.3 Such batteries must be immediately and safely removed from service, discharged (using a resistive load or specialized discharger in a safe area), and disposed of according to event organizer or local hazardous waste regulations. A bucket of sand is often used for temporary safe containment of damaged batteries.30  
* **Charging:** This is a high-risk activity.  
  * **Charger:** ALWAYS use a charger specifically designed for LiPo batteries that includes a balancing function.3 Balancing ensures all cells within the pack maintain equal voltage; imbalance can lead to instability and failure.30  
  * **Safety Container:** ALWAYS charge LiPos inside a fire-resistant LiPo bag or container.3 These bags help contain potential fires.  
  * **Supervision:** NEVER leave charging LiPos unattended.29  
  * **Settings:** Before charging, meticulously verify the charger settings match the battery: correct LiPo chemistry, correct cell count (e.g., 3S, 4S), and appropriate charge current (typically 1C or less, where C is the battery capacity in Ah; e.g., 1 Amp for a 1000mAh battery). Incorrect settings can cause catastrophic failure.29  
  * **Battery Condition:** Never charge a battery that is hot or warm from use; allow it to cool to room temperature first.29 Never attempt to charge a battery that is known to be damaged or swollen.29  
  * **Monitoring:** During charging, periodically check the battery temperature. If the battery begins to swell, smoke, hiss, or become excessively hot, immediately discontinue charging, disconnect the battery (if safe to do so), place it in a safe location (like the sand bucket or outdoors away from flammable materials), and observe it from a distance.29  
  * **Voltage Limits:** Never charge LiPo cells above 4.2 Volts per cell.30 Quality chargers automatically stop at this voltage.  
* **Storage:** Store LiPos at approximately 3.7-3.8V per cell (nominal or storage charge level), not fully charged or fully depleted.3 Store them inside a LiPo bag or fireproof container 3 at room temperature, away from flammable materials.30 Extreme temperatures can damage batteries.30  
* **Installation/Removal:** Connect batteries to the robot shortly before a match, after ensuring the master power switch is off.29 *Critically double-check polarity* during connection.29 Some protocols suggest waiting a short period (e.g., 10 minutes 29) after installation before closing up the robot, allowing time to detect immediate issues like short circuits. Remove batteries promptly after each match for inspection, charging, and safe storage.29 When working with battery wires or connectors, *never* cut or allow tools to simultaneously touch the positive and negative wires/terminals – this creates a direct short circuit leading to sparks, fire, or explosion.3

### **5.3 Proposed Table: LiPo Battery Safety Checklist**

This checklist summarizes critical safety practices:

| Category | Checklist Item | Reference(s) |
| :---- | :---- | :---- |
| **Handling** | Inspect battery for physical damage (dents, punctures) before every use? | 30 |
|  | Battery shows no signs of puffing or swelling? | 3 |
| **Charging** | Using a LiPo-specific balance charger? | 3 |
|  | Charging inside a designated LiPo-safe bag or container? | 3 |
|  | Charger settings (cell count, voltage, current) verified correct for battery? | 29 |
|  | Charging process supervised at all times (never unattended)? | 29 |
|  | Battery is at room temperature (not hot/warm) before charging? | 29 |
|  | Charging stopped immediately if battery puffs, smokes, or gets too hot? | 29 |
|  | Not attempting to charge a known damaged battery? | 29 |
|  | Not charging cells above 4.2V? | 30 |
| **Storage** | Storing battery at partial charge (approx. 3.7-3.8V/cell)? | 3 |
|  | Storing inside a LiPo bag or fireproof container? | 3 |
|  | Storing at room temperature, away from flammable materials? | 30 |
| **Usage** | Polarity double-checked before connecting battery to robot/ESC? | 3 |
|  | Battery securely mounted within the robot? |  |
|  | Battery removed promptly from robot after use? | 29 |
|  | Never cutting/shorting positive and negative terminals/wires simultaneously? | 3 |
| **Disposal** | Safely discharging damaged/puffy/end-of-life batteries before disposal? | 30 |
|  | Following event organizer / local hazardous waste disposal procedures? | 29 |

Adherence to these LiPo safety procedures is non-negotiable due to the significant fire risk they pose.3 Mishandling during charging, storage, or use can easily lead to thermal runaway, resulting in intense fires or explosions.3 This simple checklist serves as a constant reminder for the team, helping to internalize these critical practices and minimize the risk of accidents that could harm personnel or destroy equipment.

### **5.4 Essential Safety Mechanisms**

Competition rules mandate several safety features, which are critical for safe operation.

* **Master Power Switch/Disconnect:** All combat robots must have a method to completely cut power to both drive and weapon systems.4 This must be achievable in under 60 seconds, typically via an externally accessible, easily removable link (e.g., an XT90 loop key) or a high-current rated switch.4 This allows event staff to safely disable a robot if needed.  
* **Weapon Locks:** Any weapon capable of storing energy or causing injury (spinners, hammers, lifters) must have a physical locking device installed whenever the robot is outside the designated arena or testing area.4 The lock must be clearly visible (e.g., painted neon orange, using a "Remove Before Flight" tag 4) and robust enough to physically prevent accidental weapon activation. Weapon locks must be in place when the robot is powered on, even during initial checks.4  
* **Radio Failsafe:** This is a critical electronic safety feature. The robot's RC receiver must be configured so that if the signal from the transmitter is lost (e.g., transmitter turned off, out of range, interference), all motors (drive and weapon) stop immediately and automatically.4 This prevents runaway robots or spinning weapons if control is lost. This function must be tested rigorously before every match.30  
* **SPARC Rules Adherence:** The Standardized Procedures for the Advancement of Robot Combat (SPARC) provide a common ruleset used by many events.5 Teams must familiarize themselves with the general SPARC rules 4 and any specific modifications or rules enforced by the competition they plan to attend.26 These rules cover weight classes, dimensions, construction requirements, prohibited weapons (e.g., entanglements, liquids, EMPs, most fire weapons 4), and detailed safety procedures. Compliance is mandatory for participation.

### **5.5 Anticipating Failure**

Designing for reliability means anticipating potential failure points.

* **Common Failure Points:** Experience shows recurring issues in combat robots. Drive systems are prone to failure: motors burning out, gearboxes stripping, pinions coming loose, mounts breaking.22 Weapon systems suffer from belt breakages, bearing failures, motor issues, or weapon components fracturing.33 Electrical systems are vulnerable: wires breaking or disconnecting due to vibration, connectors failing 22, ESCs overheating and failing 22, battery problems (voltage sag, damage) 29, and receiver/radio link issues.  
* **Design for Reliability:** Incorporate robustness from the start. Use components rated for the stresses involved. Protect sensitive electronics and batteries within the main chassis structure, ideally shielded by armor.1 Consider leaving an "air gap" between external armor and internal components, allowing the armor to deform slightly upon impact without immediately crushing internals.25 Design the robot for relatively easy assembly and disassembly to facilitate rapid repairs between matches.25 Use CAD software not just for part design, but also to plan component layout, ensure adequate clearance, and map out clean, protected wiring routes.25 While redundancy is often difficult within weight limits, avoid single points of failure where possible.  
* **Damage Assessment Context:** Understanding how judges evaluate damage in competitions informs design priorities.33 Damage is assessed based on loss of functionality and reduced effectiveness.33 Critically, damage that impairs mobility (e.g., non-functional drive side causing crab-walking, wobbly wheels reducing traction) is weighed heavily, often more than damage to a weapon system.33 Even seemingly minor damage like a bent lifting arm or spinner tooth can significantly reduce weapon effectiveness.33 Visible smoke, especially white smoke, usually indicates severe damage to batteries or motor controllers, counting significantly against a bot even if it keeps moving.33 This highlights the paramount importance of protecting the drive train and core electronics.

Integrating safety effectively requires more than just checking boxes on a rules list; it necessitates a design philosophy adopted from the project's inception. Combat robots inherently contain significant stored energy, both kinetic in spinning weapons and chemical in high-discharge batteries.8 While regulations mandate essential safety devices like power disconnects and weapon locks 4, a truly safe design goes further. It involves proactively *engineering* systems to be inherently less prone to hazardous failure. This includes routing wires securely away from potential damage zones, physically protecting batteries from impact, rigorously testing radio failsafes to ensure they function reliably under all conditions, and selecting robust components that are less likely to fail catastrophically under stress.1 By considering potential failure modes 22 and designing mitigations early in the process, the resulting robot will be significantly more robust and safer than one where safety features are merely added as afterthoughts.

## **6\. Your Combat Robotics Toolkit: Essential Resources**

Building a successful combat robot, especially for a student team, benefits immensely from leveraging the knowledge and resources available within the vibrant combat robotics community.

### **6.1 Connecting with the Community**

Engaging with other builders is invaluable for troubleshooting, inspiration, and learning best practices.

* **Forums/Groups:**  
  * **Facebook Groups:** The "Combat Robotics" group is a major hub.17 Specific weight class groups like the "Featherweight Combat Robots" group 17 are highly relevant. Regional groups also exist.17 These are active platforms for asking technical questions, sharing build progress, and discussing event logistics. Joining requires a Facebook account.35  
  * **SPARC Forum:** The official forum for the Standardized Procedures for the Advancement of Robot Combat (sparc.tools/forum) is another key resource, particularly for rules discussion and connecting with US builders.32  
  * **Reddit:** Subreddits like r/battlebots primarily focus on the TV show but can sometimes offer build advice, especially between seasons.34 r/robotwars is another related community.34  
* **Q\&A Sites:** The "Ask Aaron" archive (runamok.tech/AskAaron) maintained by veteran builder Aaron Hill contains thousands of answered questions on materials, components, and techniques, making it an exceptional resource for technical queries.9  
* **Wikis:** The RobotCombatWiki 17 provides definitions, event information, and links. University team wikis, like the RoboJackets Wiki 8, often contain valuable build guides, component data, and material information.

### **6.2 Sourcing Components**

Finding the right parts requires knowing where to look.

* **Specialist Combat Robotics Retailers:** Stores like ITGresa Robotics 23, FingerTech Robotics 23, Repeat Robotics 23, and Team Just Cuz Robotics 17 cater specifically to combat robot builders, offering motors, ESCs, wheels, hardware, and materials often tested or designed for the sport. RobotShop also carries relevant motors and components.24  
* **General Electronics and Hobby Suppliers:** Retailers like SparkFun 7, Adafruit, and HobbyKing offer motors, ESCs, batteries, RC gear, and general electronic components. Be mindful of verifying specifications and quality, especially from overseas hobby suppliers.3  
* **Materials Suppliers:** Online metal and plastic suppliers like OnlineMetals 11, McMaster-Carr 10, Alro Steel 10, and TMS Titanium 10 provide raw stock. Local suppliers can also be cost-effective. For custom-cut parts from materials like AR500 steel or Titanium, services like SendCutSend 10 offer waterjet and laser cutting based on CAD files.

### **6.3 Knowledge Base**

Utilize existing guides and documentation.

* **Build Guides and Tutorials:** Websites like Instructables host general robot build guides.6 Organizations like Bristol Bot Builders offer specific guides for different weight classes.26 Numerous YouTube channels created by experienced builders (e.g., Robert Cowan, Team Just 'Cuz Robotics, Endbots, Team Panic, Team Orby listed in 17) provide invaluable build logs, tutorials, and technical tips.  
* **Rulesets:** Always refer to the official SPARC ruleset 4 and, critically, the specific rules document for the event the team plans to attend, as variations exist.26 Major leagues like the National Havoc Robot League (NHRL) also publish their rules.31  
* **Material Databases:** Resources like the RoboJackets Materials Database 10, MatWeb.com, and supplier technical datasheets provide essential mechanical and physical properties (strength, hardness, density, machinability) for comparing material options like various steels (AR500, 4130, S7), aluminum alloys (6061, 7075), Titanium (Grade 5), and plastics (UHMW, HDPE, Polycarbonate).10

Actively tapping into the collective experience of the combat robotics community offers a significant advantage, particularly for student teams. The field combines specialized knowledge from mechanical engineering, electrical engineering, materials science, and software.7 Attempting to independently discover solutions to common problems is inefficient and can lead to costly mistakes or dangerous failures.6 Online forums, Q\&A archives like Ask Aaron, and dedicated Facebook groups 9 provide direct lines to experienced builders who have likely encountered and solved similar challenges. Furthermore, studying existing build logs, tutorials, and wiki pages 6 reveals proven design patterns, component recommendations, fabrication techniques, and crucial safety considerations. Leveraging these resources effectively accelerates the learning curve, helps avoid common pitfalls, saves time and budget, and ultimately leads to a more competitive and reliable robot.

## **7\. Advanced Considerations and Final Preparations**

As the build nears completion, focus shifts towards optimizing performance and ensuring readiness for competition.

### **7.1 Mastering Maneuverability**

High-speed spinning weapons introduce significant dynamic effects that impact driving.

* **Gyroscopic Precession:** A rapidly spinning mass, like a drum weapon, behaves like a gyroscope.8 When the driver attempts to turn the robot, they apply a torque perpendicular to the weapon's axis of rotation. Due to gyroscopic precession, this torque results in a reaction 90 degrees away in the direction of the weapon's spin, causing the robot to tilt rather than turn flatly.37 For a typical vertical spinner or drum rotating upwards at the front, attempting to turn left (applying yaw torque to the left) will cause the right side of the robot to lift, while turning right will cause the left side to lift.37 This effect is more pronounced at higher weapon RPMs and can make sharp turns difficult or unstable.8  
* **Managing Gyro Effects:** There are several ways to deal with gyroscopic forces:  
  * **Reduce Weapon Speed:** Lowering the weapon RPM significantly reduces the gyroscopic effect, but also reduces the stored kinetic energy and potential damage output.8 This is a performance trade-off.  
  * **Driving Technique:** Experienced drivers learn to anticipate and compensate for precession. This might involve making wider, smoother turns, pulsing the throttle during turns, or even momentarily reversing one side of the drive to counteract the tilt. Practice is essential.  
  * **Robot Design:** A lower center of gravity and a wider wheelbase can make the robot inherently more stable and less prone to tipping over due to gyroscopic forces. However, weapon placement and chassis design often constrain these factors.

Ignoring or underestimating the impact of gyroscopic precession is a common mistake for teams new to powerful spinning weapons. The effect is a direct consequence of physics related to angular momentum.37 Drivers expecting the robot to handle like a simple RC car will find it behaves unpredictably, tilting severely during turns.8 This instability makes it difficult to accurately aim the weapon, hinders evasive maneuvers, compromises control 18, and can even cause the robot to flip itself over during aggressive driving. Therefore, understanding the principles of precession, dedicating significant practice time for the driver to adapt, and considering stability during the design phase are crucial for operating a drum-spinner robot effectively in combat.

### **7.2 Pre-Event Readiness Checklist**

Before heading to a competition, a thorough checklist ensures the robot and team are prepared.

* **Mechanical Systems:**  
  * Fasteners: Are ALL bolts and screws tight? Has thread locker been applied where needed and allowed to cure?9  
  * Weapon: Is the weapon securely mounted and properly balanced?27 Spin it up (safely\!) to check for vibration.  
  * Bearings: Are all weapon and drive bearings spinning freely without roughness or excessive play?  
  * Armor: Are all armor panels securely attached?  
  * Drive Train: Do wheels spin freely? Is drive alignment correct? Any unusual noises from motors/gearboxes?  
  * Weapon Lock: Does the mandatory weapon lock fit correctly and effectively immobilize the weapon?4  
* **Electrical Systems:**  
  * Batteries: Are primary and spare LiPo batteries fully charged and balanced?29 Are they physically secured in the bot?  
  * Wiring: Inspect all wiring for chafing, loose connections, or potential shorts. Ensure all solder joints and connectors are secure.22  
  * Master Switch: Does the master power switch/link function correctly and disconnect all power?4  
  * Radio System: Are transmitter batteries fully charged? Is the receiver securely mounted and antenna positioned correctly?  
  * Failsafe: **CRITICAL TEST:** Verify the radio failsafe works correctly. Turn the robot on (weapon lock installed\!), then turn off the transmitter. The robot's drive and weapon systems must immediately cease all activity.4 Repeat this test multiple times.  
  * Thermal Check: Run the drive and weapon systems (safely) for a duration similar to a match (e.g., 3 minutes 12) and check if motors or ESCs are overheating.  
* **Spares and Tools:**  
  * Spare Parts: Pack essential spares based on anticipated failures: drive motors, gearboxes, weapon motor, ESCs (drive and weapon), belts/chains, fasteners (various sizes), wheels/tires, spare battery packs, spare weapon lock.  
  * Tools: Bring all necessary tools for repair and maintenance: soldering iron and solder, wire strippers/cutters, hex keys, screwdrivers, wrenches/spanners, pliers, crimping tool (if using crimp terminals), multimeter, battery charger, LiPo-safe charging bags.26  
  * Safety Gear: Safety glasses for everyone working on the bot are mandatory.29 Work gloves are recommended. Fire extinguisher (suitable for electrical/LiPo fires) readily available in the pit area.  
* **Logistics:**  
  * Competition Rules: Has the team registered for the event? Is the final version of the event-specific rules document downloaded and understood by all members?32  
  * Travel: Plan for safe transport of the robot, tools, and batteries (check any specific transport regulations for LiPos).

## **8\. Conclusion: Ready for Combat**

Successfully upgrading the 8KG battlebot requires a blend of careful planning, sound engineering design, meticulous assembly, and rigorous safety practices. Key takeaways include the critical importance of thorough initial assessment and planning, designing robust mechanical systems (especially motor mounts and weapon attachments) that account for extreme shock and vibration, making informed decisions in selecting high-performance brushless motors and compatible ESCs, and implementing unwavering discipline in LiPo battery handling and overall safety procedures including functional failsafes and weapon locks.

Furthermore, actively engaging with the resources and collective knowledge of the combat robotics community can significantly accelerate learning and help avoid common pitfalls. Effective teamwork, clear communication, and structured project management are essential for coordinating the efforts of a student team with diverse experience levels.

Combat robotics is an iterative discipline.12 Teams should anticipate challenges, view failures not as setbacks but as learning opportunities 22, and embrace the entire process of design, fabrication, testing 28, refinement, and ultimately, competition. With careful preparation and adherence to the principles outlined in this guide, the team will be well-equipped to field a competitive and reliable 8KG battlebot. Good luck in the arena\!

#### **Works cited**

1. 7\. Design Considerations for a Combat Robot, accessed April 27, 2025, [https://mtsu.pressbooks.pub/robotics/chapter/chapter-7/](https://mtsu.pressbooks.pub/robotics/chapter/chapter-7/)  
2. ECE 445, accessed April 27, 2025, [https://courses.grainger.illinois.edu/ece445/getfile.asp?id=24253](https://courses.grainger.illinois.edu/ece445/getfile.asp?id=24253)  
3. Bot Battery Basics & LiPo Care/Safety \- Combat Robotics NZ, accessed April 27, 2025, [https://combatrobotics.co.nz/pages/bot-battery-basics-lipo-care-safety](https://combatrobotics.co.nz/pages/bot-battery-basics-lipo-care-safety)  
4. SPARC | Clubs & Organizations \- Oregon State University, accessed April 27, 2025, [https://clubs.oregonstate.edu/combat-robotics/sparc](https://clubs.oregonstate.edu/combat-robotics/sparc)  
5. Robot Rules | Plant Series \- Combat Robot Weight Classes, accessed April 27, 2025, [https://plants.cometrobotics.org/combat-robotics/robot-rules](https://plants.cometrobotics.org/combat-robotics/robot-rules)  
6. How to Design and Build a Combat Robot : 11 Steps (with Pictures) \- Instructables, accessed April 27, 2025, [https://www.instructables.com/How-to-design-and-build-a-combat-robot/](https://www.instructables.com/How-to-design-and-build-a-combat-robot/)  
7. How to Build a Combat Robot \- News \- SparkFun Electronics, accessed April 27, 2025, [https://news.sparkfun.com/2763](https://news.sparkfun.com/2763)  
8. 3lb Beginner's Guide \- RoboJackets Wiki, accessed April 27, 2025, [https://wiki.robojackets.org/3lb\_Beginner%27s\_Guide](https://wiki.robojackets.org/3lb_Beginner%27s_Guide)  
9. Combat Robot Parts and Materials \- The Ask Aaron Archives \- RunAmok.tech, accessed April 27, 2025, [http://runamok.tech/AskAaron/materials.html](http://runamok.tech/AskAaron/materials.html)  
10. Materials Database \- RoboJackets Wiki, accessed April 27, 2025, [https://wiki.robojackets.org/Materials\_Database](https://wiki.robojackets.org/Materials_Database)  
11. BattleBots & Choosing the Right Materials | OnlineMetals.com®, accessed April 27, 2025, [https://www.onlinemetals.com/en/battlebots-choosing-right-material](https://www.onlinemetals.com/en/battlebots-choosing-right-material)  
12. Design, Build, Test, Compete: A Battlebot \- Peer Asee, accessed April 27, 2025, [https://peer.asee.org/design-build-test-compete-a-battlebot.pdf](https://peer.asee.org/design-build-test-compete-a-battlebot.pdf)  
13. Engineering Project Management: The Essential Guide for 2025 | Epicflow, accessed April 27, 2025, [https://www.epicflow.com/blog/engineering-project-management-the-essential-guide/](https://www.epicflow.com/blog/engineering-project-management-the-essential-guide/)  
14. 7 Best Practices for Leading a Team of Engineers \- Florida Tech, accessed April 27, 2025, [https://www.fit.edu/lp/7-best-practices-for-leading-a-team-of-engineers/](https://www.fit.edu/lp/7-best-practices-for-leading-a-team-of-engineers/)  
15. 4.1 Team Project Management Tools and Strategies – Technical Writing Essentials, accessed April 27, 2025, [https://pressbooks.bccampus.ca/technicalwriting/chapter/teampmtools/](https://pressbooks.bccampus.ca/technicalwriting/chapter/teampmtools/)  
16. Top 10 Communication Techniques for Engineering Leaders to Enhance Team Collaboration \- MoldStud, accessed April 27, 2025, [https://moldstud.com/articles/p-top-10-communication-techniques-for-engineering-leaders-to-enhance-team-collaboration](https://moldstud.com/articles/p-top-10-communication-techniques-for-engineering-leaders-to-enhance-team-collaboration)  
17. RobotCommunity \- RobotCombatWiki, accessed April 27, 2025, [https://robotcombatwiki.com/wiki/RobotCommunity](https://robotcombatwiki.com/wiki/RobotCommunity)  
18. How to Build a BattleBot Like a Pro, Part One: Rules and Combat Styles \- Fictiv, accessed April 27, 2025, [https://www.fictiv.com/articles/build-a-battlebot-like-a-pro-rules-and-combat-styles](https://www.fictiv.com/articles/build-a-battlebot-like-a-pro-rules-and-combat-styles)  
19. What is a Vibration Mount? \- RPM Rubber Parts, accessed April 27, 2025, [https://www.rpmrubberparts.com/what-is-a-vibration-mount/](https://www.rpmrubberparts.com/what-is-a-vibration-mount/)  
20. Designing rubber mounts for vibration reduction \- YouTube, accessed April 27, 2025, [https://www.youtube.com/watch?v=rrUUs7uC8ag](https://www.youtube.com/watch?v=rrUUs7uC8ag)  
21. Mounting The Drive Motors (Build Book Ch 3\) // Camp Witch Doctor 4 of 24 \- YouTube, accessed April 27, 2025, [https://www.youtube.com/watch?v=XI0iZfoqac4](https://www.youtube.com/watch?v=XI0iZfoqac4)  
22. What are some common failure points? : r/battlebots \- Reddit, accessed April 27, 2025, [https://www.reddit.com/r/battlebots/comments/52y4ha/what\_are\_some\_common\_failure\_points/](https://www.reddit.com/r/battlebots/comments/52y4ha/what_are_some_common_failure_points/)  
23. Combat Robotics Motors \- ItGresa Robotics carries the best Fingertechs\!, accessed April 27, 2025, [https://itgresa.com/combat-robotics-motors/](https://itgresa.com/combat-robotics-motors/)  
24. Brushless DC Motors \- RobotShop, accessed April 27, 2025, [https://www.robotshop.com/collections/bldc-motors](https://www.robotshop.com/collections/bldc-motors)  
25. How to Build a Combat Robot \- STEM Learning, accessed April 27, 2025, [https://www.stem.org.uk/system/files/elibrary-resources/2019/07/How%20to%20build%20a%20combat%20robot%20V1.2.pdf](https://www.stem.org.uk/system/files/elibrary-resources/2019/07/How%20to%20build%20a%20combat%20robot%20V1.2.pdf)  
26. Guides, Parts & Rules \- Bristol Bot Builders, accessed April 27, 2025, [https://bristolbotbuilders.com/guides/](https://bristolbotbuilders.com/guides/)  
27. Spinning weapon balance question : r/battlebots \- Reddit, accessed April 27, 2025, [https://www.reddit.com/r/battlebots/comments/fhuugj/spinning\_weapon\_balance\_question/](https://www.reddit.com/r/battlebots/comments/fhuugj/spinning_weapon_balance_question/)  
28. Bloodsport Battlebot Destruction\! Full System Testing for Season 5 \- YouTube, accessed April 27, 2025, [https://www.youtube.com/watch?v=ASk7xTwLpEo](https://www.youtube.com/watch?v=ASk7xTwLpEo)  
29. safety hazard warnings & handling for all batteries \- BattleBots, accessed April 27, 2025, [https://battlebots.com/wp-content/uploads/2020/09/BATTLEBOTS-Battery-Rules-9-24-20.pdf](https://battlebots.com/wp-content/uploads/2020/09/BATTLEBOTS-Battery-Rules-9-24-20.pdf)  
30. Electronics Basics \- RoboJackets Wiki, accessed April 27, 2025, [https://wiki.robojackets.org/Electronics\_Basics](https://wiki.robojackets.org/Electronics_Basics)  
31. Robot combat \- Wikipedia, accessed April 27, 2025, [https://en.wikipedia.org/wiki/Robot\_combat](https://en.wikipedia.org/wiki/Robot_combat)  
32. SparkFun AVC 2016 Course Preview: Robot Combat Arena \- YouTube, accessed April 27, 2025, [https://www.youtube.com/watch?v=vvsw\_6t5cPQ](https://www.youtube.com/watch?v=vvsw_6t5cPQ)  
33. Judges' Guide | BattleBots, accessed April 27, 2025, [https://battlebots.com/wp-content/uploads/2021/06/Judges-Guide-Rev.2021.0.pdf](https://battlebots.com/wp-content/uploads/2021/06/Judges-Guide-Rev.2021.0.pdf)  
34. What's the best subreddits or forums to discuss building combat robots or battlebots?, accessed April 27, 2025, [https://www.reddit.com/r/battlebots/comments/8yem47/whats\_the\_best\_subreddits\_or\_forums\_to\_discuss/](https://www.reddit.com/r/battlebots/comments/8yem47/whats_the_best_subreddits_or_forums_to_discuss/)  
35. Forums and Subs Exclusively For Bot Building : r/battlebots \- Reddit, accessed April 27, 2025, [https://www.reddit.com/r/battlebots/comments/55kpwa/forums\_and\_subs\_exclusively\_for\_bot\_building/](https://www.reddit.com/r/battlebots/comments/55kpwa/forums_and_subs_exclusively_for_bot_building/)  
36. Robotics Teams/Competitions for Adults \- General Forum \- Chief Delphi, accessed April 27, 2025, [https://www.chiefdelphi.com/t/robotics-teams-competitions-for-adults/153590](https://www.chiefdelphi.com/t/robotics-teams-competitions-for-adults/153590)  
37. Is there a good explainer out there for the physics of vert spinners and gyro control? \- Reddit, accessed April 27, 2025, [https://www.reddit.com/r/battlebots/comments/1k5wxnb/is\_there\_a\_good\_explainer\_out\_there\_for\_the/](https://www.reddit.com/r/battlebots/comments/1k5wxnb/is_there_a_good_explainer_out_there_for_the/)