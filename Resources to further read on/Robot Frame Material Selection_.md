# **Comparative Analysis of Aluminum Slab and Welded Steel Truss Construction for Lightweight Combat Robots**

## **Section 1: Introduction: The Combat Robot Chassis Dilemma**

### **1.1. The Unique Structural Demands of Small Combat Robots**

Small combat robots, particularly those in the 8kg (Beetleweight) and 13.6kg (Featherweight) classes, operate in an environment characterized by extreme structural demands. These machines endure high-energy impacts from opponent weapons such as spinners, crushers, and lifters, experience rapid acceleration and deceleration forces, and must maintain structural integrity within exceptionally strict weight limitations. The chassis, or frame, is the foundational element of the robot, tasked not only with protecting critical internal components like batteries, motors, and control electronics but also with providing robust mounting points for weapon systems and drivetrains. Its design and materialization are paramount to a robot's survival and competitive success.

### **1.2. Restatement of the Core Question and Competing Philosophies**

This report addresses the query: Why is aluminum slab construction generally preferred over a welded hollow square mild steel truss frame with a thinner aluminum skin for 8kg or 13.6kg combat robots, even when access to skilled welders and university-level machining capabilities is available? This question highlights a central debate in combat robot design, pitting two distinct construction philosophies against each other.

* **Aluminum Slab Construction:** This approach often involves a unibody or semi-monocoque design, where the chassis is machined from solid plates or blocks of aluminum alloy. It emphasizes material thickness and an integrated structure, where the chassis walls simultaneously serve as armor and the primary load-bearing elements.  
* **Steel Truss with Aluminum Skin:** This method draws inspiration from traditional aerospace and civil engineering, aiming for high specific strength through an optimized geometric arrangement of steel members (typically hollow tubes) that primarily carry axial loads (tension or compression). A thin aluminum skin is then added, primarily for component containment and potentially some shear stiffening, rather than as primary armor.

The tension between these approaches is not merely a choice between aluminum and steel, but a deeper divergence in design philosophy. This divergence is heavily influenced by the specific scale of these robots and the characteristic failure modes observed in combat. The aluminum slab philosophy leans towards a robust, relatively simple method of achieving strength by utilizing a greater volume of a lighter material, often in a monolithic or near-monolithic fashion. Conversely, the steel truss/skin philosophy pursues a more "finesse-driven" path, employing a stronger, denser material more sparingly in a geometrically optimized configuration. The observed prevalence of one over the other suggests that the unique conditions of small-scale combat robotics—such as the nature of impacts, repair constraints, and the value of rapid design iteration—favor one philosophy, even if the alternative holds theoretical advantages in other engineering domains.

### **1.3. Scope and Objectives of the Report**

This report will provide a comprehensive comparative analysis of these two construction methodologies. The analysis will encompass:

* A review of the fundamental mechanical properties of candidate aluminum alloys and mild steel relevant to combat robotics.  
* An examination of structural efficiency, considering strength-to-weight and stiffness-to-weight ratios.  
* A detailed comparison of fabrication processes, including complexity, time, and the impact of available resources (skilled welders and university machinery).  
* An assessment of impact resistance, durability, and common failure modes.  
* A discussion of repairability, particularly in the time-constrained environment of a competition.  
* An evaluation of design iteration speed and flexibility.

The objective is to furnish a clear, evidence-based rationale explaining the general preference for aluminum slab construction in the specified weight classes, while fully considering the enabling factor of access to advanced fabrication resources, which the user rightly suspects *should* make the steel truss option more viable. This highlights a potential disconnect between theoretical capability provided by such resources and the practical competitive advantages sought in this domain. The report aims to clarify why, even with these resources, the practicalities of combat robot design and competition often lead builders to favor aluminum slabs.

## **Section 2: Material Fundamentals: Aluminum vs. Mild Steel in a Weight-Critical Context**

### **2.1. Key Mechanical Properties for Combat Robotics**

The selection of materials for a combat robot chassis is governed by a range of mechanical properties, each playing a critical role in performance and survivability:

* **Density (ρ):** Mass per unit volume. Crucial for adhering to strict weight limits, as a lower density material allows for more volume (and thus potentially thicker sections or larger parts) for a given mass.  
* **Yield Strength (σy​):** The stress at which a material begins to deform plastically (permanently). A high yield strength is vital for resisting permanent deformation from impacts.  
* **Ultimate Tensile Strength (UTS):** The maximum stress a material can withstand while being stretched or pulled before necking or fracture.  
* **Young's Modulus (Modulus of Elasticity, E):** A measure of a material's stiffness, or resistance to elastic deformation. Higher stiffness means less deflection under a given load.  
* **Fracture Toughness (KIc​):** A material's resistance to fracture when a crack is present. Important for preventing catastrophic failure from impact-induced cracks.  
* **Ductility/Elongation at Break:** The extent to which a material can deform plastically before fracturing. Higher ductility often implies better energy absorption capacity during plastic deformation.  
* **Fatigue Resistance:** The ability to withstand repeated loading cycles without failure. Relevant due to vibrations and multiple impacts during a robot's operational life.

### **2.2. Comparative Analysis of Candidate Materials**

The primary materials under consideration are specific alloys of aluminum and common mild steel grades.

* **Aluminum Alloys:**  
  * **6061-T6:** A widely used alloy known for its good balance of strength, corrosion resistance, machinability, and weldability (though welding can reduce strength in the heat-affected zone). Its yield strength is typically around 276 MPa.  
  * **7075-T6:** A very high-strength aluminum alloy, significantly stronger than 6061-T6, with a typical yield strength around 503 MPa. It offers excellent machinability but is generally considered unweldable for structural applications due to susceptibility to cracking and significant loss of strength. Its fracture toughness is generally lower than 6061-T6.  
* **Mild Steel (e.g., 1018, A36):** These are low-carbon steels known for their excellent ductility, high fracture toughness, good weldability, and relatively low cost. Their yield strengths typically range from 250 MPa to 350 MPa.

The most striking difference is density: aluminum alloys have a density of approximately 2.7 g/cm3 (2700 kg/m3), while mild steel is around 7.85 g/cm3 (7850 kg/m3). Steel is thus approximately 2.9 times denser than aluminum. While the yield strength of 1018 mild steel might be comparable to or slightly exceed that of 6061-T6 aluminum, 7075-T6 aluminum significantly surpasses common mild steels in yield strength. Steel's Young's Modulus (approx. 200 GPa) is about three times that of aluminum (approx. 69 GPa), making steel significantly stiffer per unit volume.

The choice is not simply between generic "aluminum" and "steel," but between specific alloys with markedly different characteristics. For instance, the user's access to university machinery is a significant factor, as it facilitates the machining of harder, higher-performance alloys like 7075-T6. This capability directly enhances the potential of aluminum construction by allowing the use of materials that might be too challenging to process with more rudimentary workshop tools, thereby pushing aluminum's performance advantages further.

### **2.3. The Critical Role of Specific Strength and Specific Stiffness**

In weight-limited applications like combat robotics, absolute strength or stiffness is often less important than these properties relative to material density. This leads to the concepts of:

* **Specific Strength:** Yield Strength / Density (σy​/ρ)  
* **Specific Stiffness:** Young's Modulus / Density (E/ρ)

These ratios indicate how much strength or stiffness a material offers for a given mass. When these are calculated, aluminum alloys, particularly 7075-T6, demonstrate a significant advantage in specific strength over mild steel. While steel generally has a higher specific stiffness due to its much higher Young's Modulus, aluminum remains competitive. This superior specific strength is often more critical for resisting the initial onset of permanent deformation from impacts within a fixed weight budget. If an aluminum component can be made sufficiently thick (due to its low density) to withstand typical combat loads without yielding, it is often preferred over a thinner steel counterpart that might also resist yielding but offers less material volume or protective coverage for the same weight.

### **2.4. Implications for Overall Robot Weight Budget**

The chassis material choice has a profound and direct impact on the weight budget available for all other systems: weapons, motors, batteries, electronics, and any ablative armor. A heavier chassis inherently consumes a larger portion of the allowable weight, leaving less for these critical components. This can lead to a compounding effect: a heavier chassis might necessitate more powerful (and thus heavier) motors and larger batteries to achieve desired agility and endurance, further encroaching on the limited weight budget. Consequently, materials with high specific strength are highly prized.

An interesting consideration is aluminum's lower Young's Modulus. While often perceived as a disadvantage (implying lower stiffness), this property can be beneficial in specific impact scenarios. Lower stiffness allows for greater elastic deformation before yielding for a given load (Stress \= E× Strain). If a structure is designed to utilize this, it can absorb more impact energy elastically, effectively damping impacts and reducing peak forces transmitted to internal components or preventing localized stress concentrations. This characteristic is particularly relevant for slab-style designs, which can distribute impact loads over a larger volume of material, allowing the entire structure to participate more effectively in energy absorption. This contrasts with a truss structure where individual members might be very stiff, but the overall energy absorption capability is more dependent on the complex behavior of joints and the potential for localized buckling or yielding of slender members.

**Table 2.1: Comparative Mechanical Properties of Candidate Materials for Combat Robot Chassis**

| Material | Density (kg/m3) | Yield Strength (σy​, MPa) | Ultimate Tensile Strength (UTS, MPa) | Young's Modulus (E, GPa) | Fracture Toughness (KIc​, MPa$\\sqrt{\\text{m}}$)1 \\$ | Specific Yield Strength (\\text{kNm/kg}$) \\$ | Specific Stiffness (\\text{MNm/kg}$) |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 6061-T6 Aluminum | 2700 | 276 | 310 | 69 | \~29-35 | 102.2 | 25.6 |
| 7075-T6 Aluminum | 2810 | 503 | 572 | 71.7 | \~24-29 | 179.0 | 25.5 |
| 1018 Mild Steel | 7870 | 370 (typical)\<sup\>2\</sup\> | 440 (typical)\<sup\>2\</sup\> | 205 | \~50-100+ | 47.0 | 26.0 |
| A36 Mild Steel | 7850 | 250 (minimum) | 400-550 | 200 | \~50-100+ | 31.8 | 25.5 |

\<sup\>1\</sup\> Fracture toughness values can vary significantly with specific processing, orientation, and testing conditions. Values are approximate ranges.  
\<sup\>2\</sup\> Properties for 1018 steel can vary based on cold work and specific condition. Hot-rolled yield strength is lower (\~260 MPa).  
This table centralizes the quantitative data underpinning subsequent arguments. It allows for direct comparison, highlighting aluminum's density advantage and the superior specific strength of 7075-T6. This data informs the engineering trade-offs inherent in material selection and provides a foundation for understanding why, for a given weight, an aluminum structure can often be designed to be thicker, offering advantages in resisting local buckling or distributing impact energy more effectively.

## **Section 3: Aluminum Slab Construction: Simplicity, Robustness, and Machinability**

### **3.1. Principles of "Billet" or Slab Construction**

Aluminum slab construction, often referred to as "billet" construction, involves machining the primary structural components of the robot from solid plates or blocks of material, typically aluminum alloys such as 6061-T6 or, for higher performance, 7075-T6. This manufacturing approach frequently results in unibody or semi-monocoque designs where the outer shell of the robot is not merely a covering but constitutes the main load-bearing structure and simultaneously serves as its armor. A key characteristic of this method is the emphasis on part count reduction and the integration of features. Elements like bearing bores for shafts, mounting points for motors and electronics, and lightening pockets for weight optimization are often machined directly into the slab components.

### **3.2. Advantages in the Combat Robot Context**

#### **3.2.1. Design and CAD/CAM Integration**

Aluminum slab designs are relatively straightforward to conceptualize and model in modern Computer-Aided Design (CAD) software. Complex 2.5D (profiles with depth) or even full 3D shapes can be readily designed. These digital designs translate efficiently to Computer-Aided Manufacturing (CAM) software, which generates the toolpaths for CNC (Computer Numerical Control) machining operations like milling or waterjet cutting. This streamlined workflow from design to fabrication is a significant advantage, allowing for the creation of intricate and precise geometries that would be exceedingly difficult, if not impossible, to achieve through manual fabrication methods or even with welded truss structures requiring many individually shaped parts.

#### **3.2.2. Rapid Fabrication with CNC Machinery**

The availability of university-level machinery, such as CNC mills, lathes, and waterjet cutters, makes the fabrication of aluminum slab components highly efficient. Once a design is finalized and CAM programming is complete, CNC machines can produce parts with high precision and repeatability. This capability is crucial for teams needing to produce spare parts or iterate on designs quickly. For a user with access to these tools, aluminum slabs become a very rapid manufacturing option. This ease of fabrication directly contributes to faster design iteration cycles. In a dynamic field like combat robotics, where designs evolve rapidly and counter-strategies emerge quickly, the ability to move from a concept in CAD to a physical, testable part in a short timeframe is invaluable. This speed can translate into multiple design improvements within a single build season or even between competition rounds.

#### **3.2.3. Impact Load Distribution and Energy Absorption**

Due to aluminum's lower density compared to steel, thicker sections can be employed for the same overall weight. These thicker sections inherently offer better distribution of impact forces, reducing localized stress concentrations. The monolithic or semi-monolithic nature of slab construction allows impact energy to be dissipated over a larger volume of material. This can leverage aluminum's capacity for elastic deformation (as discussed in Section 2.3 regarding its lower Young's Modulus) and, for more ductile alloys like 6061, significant plastic deformation before fracture. In some designs, the aluminum slab can act as ablative armor, where material is intentionally sacrificed (gouged or deformed) to absorb the kinetic energy of an opponent's weapon, protecting critical internal components.

#### **3.2.4. Inherent Stiffness and Part Count Reduction**

Well-designed aluminum slabs, especially those incorporating strategically machined internal ribbing or optimized cross-sectional shapes, can achieve very high stiffness. The reduction in part count compared to a complex assembly like a truss simplifies the overall assembly process. Fewer parts mean fewer fasteners or joints, which are often potential points of failure, sources of stress concentration, or pathways for fatigue crack initiation in dynamically loaded structures. This "joint minimization" inherent in monolithic slab construction can contribute significantly to overall structural integrity and reliability. While a major impact might deform a slab, it is less likely to suffer a catastrophic joint failure that could occur in a truss if a single critical weld or bolted connection fails. This characteristic, sometimes described as "graceful degradation" or a "bend-don't-break" tendency (particularly for more ductile aluminum alloys), can be preferable to the sudden, total failure of a joint.

#### **3.2.5. Integrated Armor and Structural Elements**

A significant advantage of slab construction is that the chassis *is* the armor. There is often no need for separate, add-on armor panels, which saves weight, complexity, and potential points of attachment failure. The thickness of the material can be varied across the structure, with more material allocated to areas facing high threat levels (e.g., the front or weapon-exposed sides) and less material (through pocketing) in less critical areas to save weight. This strategic thickening is straightforward to implement with CNC machining.

### **3.3. Disadvantages and Considerations**

#### **3.3.1. Structural Efficiency (Theoretical vs. Practical)**

From a purely theoretical structural engineering standpoint, focusing solely on axial loads, a slab structure might not be as "mass efficient" as an idealized, perfectly optimized truss structure. Trusses are designed to place material precisely where it is needed to handle specific load paths. However, combat robots face complex, multi-axial, and high-strain-rate impact loads that are difficult to predict and often deviate significantly from idealized load cases. In this context, the volumetric nature and load redistribution capabilities of a slab can offer superior practical performance. A critical design consideration for slabs is that large cutouts or pockets introduced for weight reduction can create stress concentrations if not carefully designed with appropriate fillets and smooth transitions.

#### **3.3.2. Repair Strategies**

Significant damage to a monolithic slab component, such as a major bend or fracture, might necessitate the replacement of the entire part. This can be a disadvantage if spares are not readily available. However, if spare components are pre-machined (which is feasible given CNC repeatability), replacement can be relatively quick. Field repairs, such as attempting to bend a damaged aluminum part back into shape, are possible for more ductile alloys like 6061-T6, but this process can work-harden the material, reduce its ductility, and potentially introduce micro-cracks, weakening it for subsequent impacts. Higher strength alloys like 7075-T6 are much less forgiving of such field repairs and are more prone to cracking if bent.

#### **3.3.3. Material Cost and Waste**

Starting with large billets or thick plates of aluminum can lead to a significant portion of the material being machined away as swarf (chips). This increases the effective material cost, as the builder pays for the initial bulk material, much of which becomes waste. This issue can be mitigated to some extent by using near-net shape starting materials (e.g., custom extrusions or castings, though less common at this scale) or by using waterjet cutting to create profiled blanks that are closer to the final part shape before intricate milling operations commence.

The user's access to university CNC machinery fundamentally alters the fabrication cost-benefit analysis for aluminum slabs. Operations that might be prohibitively expensive or time-consuming if outsourced to commercial machine shops become highly accessible and rapid for students or affiliated builders. This resource availability removes a major barrier and makes sophisticated slab designs, featuring extensive pocketing, 3D contouring, and integrated features, highly practical. This access directly amplifies the inherent benefits of slab construction.

## **Section 4: Welded Steel Truss with Aluminum Skin: The Theoretical Ideal vs. Practical Realities**

### **4.1. Principles of Truss Design for Optimal Strength-to-Weight**

A truss is a structural framework composed of members (typically straight bars or tubes) connected at joints to form a series of triangles. This geometry is inherently stable and efficient because, under ideal conditions (pin-jointed connections and loads applied only at joints), the members are subjected primarily to axial tension or compression, minimizing bending loads. Bending stresses are generally less efficient uses of material than axial stresses. For combat robot chassis, hollow square or round steel tubing is often chosen for truss members because hollow sections offer a higher moment of inertia for a given cross-sectional area (and thus weight) compared to solid sections, providing greater resistance to buckling under compression and better stiffness.

The aluminum skin typically applied over a steel truss frame in this context serves several purposes: it protects internal components from debris and incidental contact, can contribute to the robot's aesthetics, and, if properly designed and attached, may provide some shear stiffness to the overall structure, helping to resist racking or twisting. However, in the lightweight classes under discussion, this skin is usually kept very thin (e.g., 1-2 mm aluminum sheet) to conserve weight and is therefore not intended to act as primary impact armor against dedicated weapons.

### **4.2. Theoretical Advantages**

#### **4.2.1. High Structural Efficiency**

The primary allure of a truss structure is its potential for exceptionally high structural efficiency, meaning a high strength-to-weight and stiffness-to-weight ratio. If designed and executed perfectly, and if loads are applied in a predictable manner consistent with the truss's design assumptions, a steel truss can theoretically offer a lighter frame for a given strength requirement compared to many other structural forms. This is the core appeal that draws designers to consider this approach, especially in weight-critical applications.

#### **4.2.2. Steel's Material Properties**

Mild steel itself brings desirable properties to a structural frame. It possesses high absolute strength, excellent ductility (allowing for significant plastic deformation before fracture, which can absorb energy), and very good fracture toughness, making it resistant to catastrophic crack propagation. Furthermore, its good weldability allows for the creation of strong, permanent joints between members, assuming appropriate welding techniques are employed.

### **4.3. Disadvantages and Challenges in Small Combat Robots (8-13.6kg)**

Despite the theoretical advantages, implementing an effective and reliable welded steel truss with an aluminum skin for small combat robots presents significant practical challenges.

#### **4.3.1. Fabrication Complexity and Precision**

Constructing a steel truss is a labor-intensive and skill-intensive process. It requires the precise cutting of numerous small tube sections, often with complex angled ends (coping or notching) to ensure proper fit-up at the joints. Elaborate jigging is absolutely essential during welding to maintain the correct geometry and alignment of all members; even minor misalignments can induce undesirable internal stresses or significantly alter the intended load paths, compromising the truss's efficiency and strength. While the availability of "skilled welders" and "university machinery" (which might include precise tube cutters or benders) can mitigate some of these fabrication barriers by improving the quality of cuts and welds, they do not eliminate the *inherent time cost and meticulous precision requirements* of truss construction. This extended fabrication time directly impacts design iteration speed and the ability to quickly produce replacements or repairs compared to CNC-driven slab manufacturing methods.

#### **4.3.2. Welding Thin-Walled Hollow Sections**

Welding the thin-walled (e.g., 1-2 mm wall thickness) steel tubing commonly used to save weight in these robot classes is particularly challenging.

* **Distortion (Warping):** The localized heat input from welding can easily cause thin sections to warp or distort, making it difficult to maintain the frame's intended geometry. Careful weld sequencing and robust jigging are needed to manage this.  
* **Burn-Through vs. Penetration:** Achieving full penetration welds, which are critical for joint strength, without burning through the thin tube walls requires considerable skill and precise control of welding parameters.  
* **Heat-Affected Zone (HAZ):** Welding inevitably alters the microstructure of the steel in the region adjacent to the weld, known as the HAZ. This alteration can reduce the material's strength, toughness, or ductility compared to the parent material. While mild steel is generally forgiving, the HAZ is still a critical consideration. In the small, thin-walled tubes used in lightweight robots, the HAZ can represent a proportionally larger and more critical region of compromised material properties than in larger, thicker-walled structures. For example, in a 1.5 mm wall tube, a HAZ extending even 0.5 mm into the material affects a significant percentage of the load-bearing cross-section at the most critical locations—the joints. This proportionally larger HAZ can create weak points more susceptible to fatigue or failure under high-strain-rate impacts, potentially undermining the perceived strength advantage of steel.

#### **4.3.3. Vulnerability of Thin Aluminum Skin**

This is arguably the Achilles' heel of the steel truss/aluminum skin approach in the context of combat robotics. To save weight, the aluminum skin is typically very thin (e.g., 1-1.5 mm). Such a skin offers minimal resistance to direct impacts from modern combat robot weapons, especially kinetic energy spinners or powerful piercing weapons. Penetration of this skin directly exposes internal components—batteries, speed controllers, motors, wiring—to damage. Even if the steel frame itself remains structurally intact, the robot can be quickly disabled by damage to these vulnerable internals, resulting in a functional kill. The frame might survive an encounter, but if the robot is rendered inoperable, the frame's integrity becomes a moot point from a competitive standpoint. This highlights a critical disconnect between theoretical structural efficiency of the frame and the practical combat effectiveness of the entire system.

#### **4.3.4. Repair Complexity and Time**

Repairing a damaged welded steel truss is a complex and time-consuming endeavor, especially under the pressure of a competition. Identifying the precise location and extent of damage within a complex latticework of tubes can be difficult. Cutting out a bent or broken tube section and welding in a replacement while maintaining the overall frame alignment is extremely challenging and often requires re-jigging the entire frame, which is rarely feasible in a pit environment. Field repairs, if attempted, are often crude (e.g., bending members back approximately) and can further compromise structural integrity or introduce new stresses.

#### **4.3.5. Stress Concentrations at Joints**

Even with high-quality welding, the joints in a truss are natural points of stress concentration. Imperfect welds (e.g., with undercuts, porosity, or insufficient penetration) or poorly designed joint geometries can exacerbate these stress concentrations, leading to premature failure under impact loading or fatigue. The transition from a relatively stiff tube member to a potentially less stiff (or differently stiff) weld bead, and then back to a tube, can itself be a point of weakness if not managed carefully through design and weld profiling.

#### **4.3.6. Scale Effects**

The benefits of a truss structure are often more pronounced at larger physical scales, where member sizes are more substantial relative to the practical limitations of joint fabrication, such as minimum weld bead size. In small robots, the minimum practical size of a strong weld bead can be disproportionately large relative to the thin tube walls. This can add more weight than theoretically calculated for an "ideal" joint and can also increase the risk of distortion due to the proportionally larger heat input.

Furthermore, the "ideal" truss often assumes that members are loaded purely axially. However, impacts in combat robotics are chaotic, multi-axial, and frequently involve significant bending or torsional loads being applied to frame members and joints. Simple truss designs, optimized for specific axial load cases, are not inherently well-suited to handle these complex, dynamic, off-axis loads efficiently without becoming much more complex themselves (e.g., requiring extensive additional triangulation, gusseting at joints, or larger-section members to resist local buckling or bending). Such additions inevitably increase complexity and weight, eroding the truss's primary theoretical advantage. Volumetric slab designs, by contrast, can often inherently handle these off-axis and torsional loads more robustly due to their continuous material paths and greater bulk, albeit with their own set of trade-offs.

## **Section 5: Comparative Analysis: Why Aluminum Slabs Often Win in Practice**

The preference for aluminum slab construction in 8kg and 13.6kg combat robots, even with access to skilled welders and university machinery, stems from a pragmatic assessment of how each construction method performs across a range of critical factors in the unique context of competitive robotics.

### **5.1. Weight Management and Distribution – The Deciding Factor?**

* **Aluminum Slab:** The lower density of aluminum (approximately 1/3 that of steel) is a fundamental advantage. It allows designers to use significantly more *volume* of material for the same weight. This volume can be strategically allocated: thicker sections can be used in areas requiring robust armor or high strength (e.g., front-facing surfaces, weapon mounts), while other areas can be extensively pocketed or thinned to save weight without compromising essential stiffness. This ability to tailor material distribution for both protection and structural integrity within the weight limit is a key benefit. The "volume advantage" isn't solely about thicker armor; it also translates to more internal space for components or allows for more robust, integrated mounting solutions for the same structural weight, contributing to overall system reliability and easier packaging.  
* **Steel Truss/Skin:** While a perfectly optimized steel truss frame itself might be very lightweight, the necessary aluminum skin adds parasitic weight that does not contribute significantly to impact resistance. The challenge lies in balancing the frame mass against the skin mass and the mass of internal components. Often, to make the steel frame truly damage-tolerant against the types of loads seen in combat (which include bending and torsion, not just pure axial loads), tube wall thicknesses need to be increased, or more members and gussets must be added. These additions quickly increase the frame's weight, diminishing its theoretical efficiency and consuming precious weight budget that could otherwise be allocated to weapons or armor.

In practice, aluminum slabs often provide a more favorable overall weight distribution for achieving a robust combination of structural integrity *and* effective component protection within the stringent weight classes.

### **5.2. Impact Resistance and Durability – Beyond Material Strength**

* **Aluminum Slab (e.g., using 7075-T6):**  
  * **Energy Absorption:** Slabs can absorb impact energy through the deformation (elastic and plastic) of a significant volume of material. The high yield strength of alloys like 7075-T6 means they can withstand considerable force before permanent deformation occurs.  
  * **Failure Mode:** Damage often manifests as localized deformation, denting, or gouging. Well-designed slabs can be "ablative," sacrificing outer material to protect internals.  
  * **Localized Impact Resistance:** The inherent thickness achievable with aluminum slabs provides good resistance to penetration or significant damage from localized impacts, such as those from spinner teeth or pointed weapons.  
* **Steel Truss/Skin (Mild Steel Frame, Aluminum Skin):**  
  * **Frame Resilience:** A well-constructed steel truss is very resilient to overall frame deformation or catastrophic structural failure due to steel's high toughness and ductility.  
  * **Skin Vulnerability:** As highlighted previously (Insight 4.B), the thin aluminum skin is the critical weak point. It is easily punctured or torn by weapon impacts, leading to direct damage to internal components. This is often the primary failure pathway, rendering the robot non-functional even if the frame itself is largely undamaged.  
  * **Truss Member Failure:** Under extreme or off-axis impacts, individual thin-walled truss members can buckle (especially if optimized for minimum weight) or welds can crack. This is particularly true if the HAZ has significantly compromised material properties or if bending loads on members are substantial.

The *mode* of damage and its consequences are crucial. A robot with a dented aluminum slab chassis might still be fully functional. A steel truss robot with a punctured skin and a damaged battery or speed controller is typically out of the fight.

### **5.3. Fabrication Time, Cost, and Design Iteration Speed**

* **Aluminum Slab:**  
  * **Design Iteration:** Extremely fast with modern CAD/CAM workflows. Design modifications can be made in software, and new parts can be re-machined relatively quickly, often within hours or a day.  
  * **Fabrication Time (Initial Build):** Once the CAD model is complete and CAM toolpaths are generated, CNC machining can be rapid for individual components. Assembly is often simpler due to a lower part count and reliance on bolting rather than welding.  
  * **Cost:** Material cost for high-strength aluminum (especially 7075-T6) can be significant, and commercial CNC machining time is expensive. However, access to university machinery drastically reduces the effective cost for the builder, making this route highly attractive.  
* **Steel Truss/Skin:**  
  * **Design Iteration:** Significantly slower. Changes to truss geometry often require re-evaluating numerous tube lengths and angles, creating new coping profiles, and potentially modifying or rebuilding complex welding jigs.  
  * **Fabrication Time (Initial Build):** Considerably longer due to the many manual or semi-manual steps involved: precise cutting of many tubes, notching/coping ends, meticulous jig setup, careful tack welding, sequential full welding to manage distortion, grinding welds, and finally, fitting and attaching the skin. Even with skilled labor, it is a time-intensive process.  
  * **Cost:** While mild steel tubing is relatively inexpensive, the labor component (even if "free" student labor, it represents an opportunity cost of time) is very high. Welding consumables also add to the cost.

Key metrics like "time to first fight" and, more importantly, "time to iterate and improve" are often drastically lower for teams using aluminum slab construction, especially when they have ready access to CNC machining. This rapid iteration capability is a powerful competitive advantage. The competitive combat robotics environment heavily favors designs that minimize "pit time" for repairs and maximize "iteration speed" between events or even between fights. Aluminum slab construction, particularly with CNC access, excels in both these practical aspects, often outweighing the theoretical mass efficiency of a perfect steel truss.

### **5.4. Repairability and Maintenance (Critical During Competitions)**

* **Aluminum Slab:**  
  * **Damage Repair:** Moderately damaged sections of 6061-T6 aluminum can sometimes be bent back into approximate shape, though this can compromise material properties. 7075-T6 is less forgiving and prone to cracking if bent.  
  * **Modular Replacement:** The most effective repair strategy for slabs is often part replacement. If the design incorporates modularity (e.g., bolt-on side panels or armor sections), damaged components can be quickly swapped out if spares are available. Even for unibody designs, having a spare machined chassis ready for a quick swap is a common strategy.  
  * **Component Access:** Access to internal components for repair or replacement is usually good if the design incorporates removable covers or panels, which are easily integrated into machined slabs.  
* **Steel Truss/Skin:**  
  * **Frame Damage:** Repairing a bent or broken welded truss joint or member accurately in a competition pit environment is exceptionally difficult and time-consuming. It typically requires cutting, grinding, re-welding, and careful checking of alignment, often without the benefit of the original jig. Such repairs are rarely feasible between matches.  
  * **Skin Damage:** The aluminum skin can be patched or replaced relatively easily, but if the underlying truss frame is damaged, this is a more significant issue.  
  * **Component Access:** Accessing components can be more complex if they are intricately woven into the truss structure or if many members obstruct direct access.

Competition pit time is minimal and precious. Designs that allow for quick swaps of pre-made assemblies or simple, rapid fixes are strongly favored. Complex welding repairs are generally not a viable option during the heat of an event.

### **5.5. Design Flexibility and Component Integration**

* **Aluminum Slab:** This method offers excellent flexibility for integrating various features directly into the machined parts. Precision bearing bores, complex gearbox housings, channels for wiring, secure mounting bosses for electronics, and contoured surfaces for armor optimization can all be directly machined. This allows for compact, robust, and efficient packaging of internal components. The ability to create true 3D shapes easily is a significant advantage.  
* **Steel Truss/Skin:** Mounting components to a truss frame often requires additional brackets, tabs, or plates to be designed, fabricated, and then welded or bolted onto the truss members. Each such addition adds complexity, weight, fabrication time, and potential failure points. Integrating complex curved surfaces or smoothly varying thicknesses is much harder with a tubular truss structure than with a machined slab.

The presence of "skilled welders" for steel trusses finds an equivalent in "skilled CAD/CAM operators and CNC machinists" for aluminum slabs. Given access to university machinery, the latter skill set can be leveraged to produce highly complex and optimized parts with remarkable speed and repeatability. In terms of output speed, achievable complexity, and consistency, the CAD/CAM/CNC route for aluminum often outpaces the manual/welded route for steel in this application, even with highly skilled welders.

**Table 5.1: Summary Comparison: Aluminum Slab vs. Steel Truss/Skin for Combat Robots (8-13.6kg)**

| Feature | Aluminum Slab (e.g., 7075-T6) | Steel Truss/Skin (Mild Steel Tubes, Thin Al Skin) |
| :---- | :---- | :---- |
| **Theoretical Structural Efficiency (Weight-Specific)** | Medium to High (depends on alloy and design optimization) | High to Very High (if perfectly designed for axial loads) |
| **Practical Overall Weight (Chassis \+ Effective Armor)** | Medium (can be optimized for good protection at weight) | Medium to High (skin adds weight; frame may need beefing) |
| **Impact Resistance (Frame Integrity)** | Good to Excellent (especially with 7075; resists deformation) | Excellent (steel toughness resists frame fracture) |
| **Impact Resistance (Component Protection / Skin)** | Good to Excellent (thick sections act as armor) | Poor to Fair (thin skin easily penetrated, exposing internals) |
| **Fabrication Time (Initial Build)** | Low to Medium (with CNC access; design time upfront) | High (many manual steps: cutting, coping, jigging, welding) |
| **Design Iteration Speed** | High (CAD changes easily translated to new CNC parts) | Low (changes require significant re-work and re-jigging) |
| **Repair Time (Competition Pit)** | Low to Medium (part swaps if modular/spares available) | High to Very High (weld repairs are complex and slow) |
| **Repair Complexity** | Low to Medium (bending 6061; replacing 7075 parts) | High (requires cutting, welding, alignment) |
| **Ease of Component Integration** | Excellent (features machined directly into structure) | Fair to Medium (requires added brackets/tabs) |
| **Requirement for Specialized Skills** | CAD/CAM proficiency, CNC operation | Precision cutting/coping, skilled welding, jig design |
| **Leverage of University CNC Machinery** | Very High (enables complex parts, fast iteration, use of 7075\) | Medium (tube cutting, jig making; less transformative) |
| **Leverage of Skilled Welders** | N/A (typically bolted or not welded structurally) | High (essential for quality joints in thin tubing) |

This table provides a side-by-side summary, illustrating that while neither method is universally superior in all aspects, the balance of trade-offs within the specific context of small combat robots—particularly regarding practical impact protection, fabrication speed, iteration capability, and repairability—tends to favor aluminum slab construction.

## **Section 6: The Role of Available Resources: Skilled Welders and University Machinery**

The user's access to skilled welders and university-level machining capabilities is a critical aspect of the query, as these resources significantly influence fabrication possibilities.

### **6.1. Skilled Welders: Enabling, Not Deciding, for Steel Trusses**

The availability of skilled welders is undoubtedly beneficial if pursuing a steel truss design. Proficient welders can:

* Produce higher quality, more reliable welds in thin steel tubing, minimizing defects such as burn-through, lack of penetration, or porosity.  
* Better manage heat input and weld sequencing to reduce distortion and warping.  
* Achieve stronger joints that more closely realize the theoretical strength of the truss design.  
* Potentially implement more advanced welding techniques or joint preparations that improve performance.

However, while skilled welding raises the *quality ceiling* and reliability of a steel truss, it does not fundamentally alter or eliminate several core practical disadvantages inherent to the truss/skin approach in the small combat robot context. These include:

* The significant time consumption involved in cutting, coping, jigging, and welding numerous joints.  
* The inherent vulnerability of the necessarily thin aluminum skin to weapon impacts, leading to internal component damage.  
* The difficulty and time required to perform accurate and robust repairs to a damaged truss structure in a competitive environment.  
* The challenges associated with the Heat Affected Zone (HAZ), which, even if better controlled by a skilled welder, still represents a region of altered material properties at critical joints.

Thus, skilled welders enable a *better* steel truss but do not necessarily make it the *better overall choice* when compared against a well-executed aluminum slab, given the other constraints and failure modes prevalent in combat robotics.

### **6.2. University Machinery: A Greater Enabler for Advanced Aluminum Slabs**

Access to university machinery—typically including CNC milling machines, lathes, waterjet cutters, and potentially advanced 3D printers—provides a more transformative advantage for aluminum slab construction. This is because:

* **Dramatically Reduced Fabrication Time and Cost (to the builder):** CNC automation allows complex aluminum parts to be produced rapidly and with high precision once the design and CAM programming are complete. What would be prohibitively expensive or slow if outsourced becomes feasible and efficient.  
* **Enabling Use of Advanced Alloys:** High-strength aluminum alloys like 7075-T6, which are harder to machine manually, can be readily processed using robust CNC equipment. This allows builders to leverage the superior specific strength of these advanced materials, significantly enhancing the performance of their slab designs.  
* **Facilitation of Complex Geometries and Integrated Features:** CNC machining excels at creating:  
  * Precision bearing bores and integrated gearbox housings.  
  * Complex 3D contoured surfaces for optimized armor profiles and impact deflection.  
  * Intricate internal pocketing and ribbing for maximal weight reduction while maintaining or enhancing stiffness.  
  * Highly repeatable parts, crucial for producing spares or iterating on designs.  
* **Rapid Prototyping and Design Iteration:** The speed of CNC machining allows teams to quickly translate CAD modifications into physical parts, test them, identify areas for improvement, and remanufacture. This accelerates the design evolution process immensely.

While university machinery could also be used to create more precise jigs or cut tubes more accurately for steel truss construction, its impact on the overall viability, sophistication, and competitive potential of aluminum slab designs is arguably far more significant and transformative. The availability of such CNC machinery disproportionately benefits aluminum slab construction by enabling complex geometries and the use of advanced alloys at low effective cost and high speed. This advantage often outweighs the benefits skilled welders bring to steel truss construction in this specific application.

### **6.3. The Intersection: When Resources Might Tip the Balance (or Not)**

Even when a team possesses *both* skilled welders and access to comprehensive university machinery, the choice of construction methodology is not automatically tipped towards steel trusses. The fundamental issues of skin vulnerability to direct weapon hits and the extended time required for fabrication and, crucially, for competition repairs of truss structures often remain the overriding concerns.

The speed, integrated protection, and design flexibility offered by CNC-machined aluminum slabs frequently provide a more competitively viable pathway. The "opportunity cost" of fabrication time, even with "free" university resources or student labor, becomes a critical hidden factor. The many hours spent on meticulous truss fabrication and jigging could potentially be reallocated to other critical areas of robot development, such as weapon system optimization, software development for autonomous functions, or extensive drive testing and strategy refinement. These activities might yield a greater competitive edge than a marginally lighter frame achieved through a time-consuming truss construction. The faster fabrication cycle of aluminum slabs frees up this valuable human resource for other tasks.

Furthermore, university machinery often implies access to advanced engineering software, such as Finite Element Analysis (FEA) tools, and potentially material testing labs. These resources can be used to highly optimize *either* type of design. However, the ease of translating an FEA-optimized design, often featuring complex surfaces, variable thicknesses, and internal structural details, into a manufacturable part is generally higher with CNC machining of a solid aluminum slab than with the intricate forming, coping, and welding required to realize a similarly optimized tubular truss structure.

In essence, while the resources can produce an excellent steel truss, they *also* enable the creation of truly top-tier aluminum slab robots. The decision then hinges on which construction method *best leverages these advanced resources to overcome the specific challenges and exploit the opportunities presented by small combat robots*. In most cases, for the reasons detailed throughout this report, that method tends to be aluminum slab construction.

## **Section 7: Conclusion: The Pragmatic Preference for Aluminum Slabs**

The general preference for aluminum slab construction over welded hollow square mild steel truss frames with thinner aluminum skins in 8kg and 13.6kg combat robots, even with access to skilled welders and university machinery, is rooted in a complex interplay of material properties, fabrication practicalities, impact dynamics, and the specific demands of the competitive environment.

### **7.1. Recapitulation of Key Differentiating Factors**

The analysis consistently points to several factors that drive this preference:

* **Weight Efficiency in Practice:** Aluminum's significantly lower density allows for the creation of thicker, more voluminous structures for a given weight. This translates directly into the ability to integrate robust armor as part of the primary structure, offering superior protection against common weapon types compared to a thin-skinned truss.  
* **Impact Management and Component Protection:** Aluminum slabs, particularly those made from high-strength alloys like 7075-T6, offer good energy absorption capabilities and can resist localized penetration effectively. The primary vulnerability of the steel truss/skin design lies in the ease with which its thin skin can be breached, exposing critical internal components to disabling damage, even if the frame itself remains intact.  
* **Fabrication Speed and Design Iteration:** The synergy between CAD/CAM software and CNC machining makes the design, fabrication, and iteration of aluminum slab components significantly faster and more flexible than the multi-stage, labor-intensive process of building a welded steel truss. This speed is a crucial competitive advantage.  
* **Repairability in Competitive Settings:** Repairing damage to an aluminum slab, especially if designed with modularity or if spares are readily available, is generally quicker and simpler in the high-pressure environment of a competition pit than attempting to accurately repair bent or broken members of a welded steel truss.  
* **Optimal Leverage of Available Resources:** University-grade CNC machinery provides a more transformative advantage to aluminum slab construction, enabling the use of advanced alloys and complex, optimized geometries with speed and precision. While skilled welders improve steel trusses, they do not overcome the inherent speed and repairability advantages of CNC-machined slabs in this context.

This "general preference" is not arbitrary. It is largely the result of collective experience and a form of convergent evolution within the competitive combat robot community. Builders continuously experiment, and successful design paradigms are emulated and refined. The prevalence of robust machined chassis (from aluminum or sometimes engineering plastics like HDPE/UHMW, which share some "machined-from-solid" characteristics) in these weight classes is empirical evidence born from countless competitions, where pragmatic factors related to build time, repairability, and overall effectiveness against common weapon archetypes have consistently favored these approaches.

### **7.2. Contextualizing the Choice: When a Steel Truss *Might* Still Be Considered**

Despite the general preference for aluminum slabs, there might be niche scenarios or specific design philosophies where a welded steel truss could still be a viable, or even preferred, option:

* **Extreme Stiffness Requirements:** For designs where exceptional frame stiffness is the absolute paramount concern, and impact protection can be adequately addressed through other means (e.g., certain types of control-oriented robots, or if a very robust, thick skin can somehow be afforded within the weight budget – though this is rare).  
* **Specialized Expertise and Resources:** Teams possessing exceptionally deep expertise, dedicated tooling, and refined processes specifically for micro-scale steel truss fabrication and rapid repair, who have perhaps developed unique solutions to mitigate common pitfalls like skin vulnerability or slow repair times.  
* **Frame-as-Weapon Designs:** In robots where the frame itself is an integral part of the weapon system (e.g., some types of full-body crushers or powerful clamping/grappling mechanisms), the extreme toughness and high yield strength of specific steel members might be indispensable.  
* **Specific Loading Conditions:** If a robot's design subjects its chassis to highly predictable and primarily axial load paths, a truss could theoretically offer the lightest solution, assuming the other vulnerabilities can be managed.

However, it must be reiterated that these are generally exceptions rather than the rule for the typical spinner-dominant, high-impact environments of Beetleweight and Featherweight combat robotics.

### **7.3. Final Recommendations for the User**

Based on the comprehensive analysis presented, and particularly considering the stated access to university CNC machinery, the following recommendations are offered:

1. **Prioritize Aluminum Slab Construction:** For 8kg or 13.6kg combat robots, focusing on aluminum slab construction offers a higher probability of achieving competitive success. This approach generally provides a better balance of integrated protection, structural robustness, manageable fabrication time, and rapid design iteration.  
2. **Leverage University Resources for Advanced Slabs:** Fully utilize the available CNC machinery to:  
   * Explore the use of high-strength aluminum alloys, primarily 7075-T6, for critical structural components.  
   * Employ advanced CAD and FEA tools to optimize slab designs for weight, stiffness, and impact resistance, incorporating features like strategic pocketing, integrated ribbing, and contoured armor surfaces.  
   * Design for modularity where feasible (e.g., bolt-on armor panels or sections) to facilitate rapid repairs and replacements.  
   * Produce spare parts efficiently to minimize downtime during competitions.  
3. **Strategic Skill Development:** While developing welding skills is a valuable engineering asset, its application to the primary chassis of small, competitive combat robots is generally a less optimal path compared to mastering CAD/CAM software and CNC machining techniques for aluminum. The latter skill set will likely yield greater returns in terms of competitive robot performance in these weight classes.

The user's access to both skilled welders and university machinery creates a scenario where excellent examples of *either* construction type *could* theoretically be produced. However, the crucial decision hinges on which method best leverages these advanced resources to address the specific, harsh realities of small-scale combat robotics. The evidence strongly suggests that these resources, particularly CNC machinery, amplify the inherent advantages of aluminum slab construction more effectively, leading to robots that are generally more robust, quicker to build and iterate, and easier to repair under competitive pressures.