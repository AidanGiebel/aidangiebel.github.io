**Homeland Defense Interceptor (HDI)**

![Final HDI Aircraft Render](assets/images/hdi/final_aircraft_render.png)

*Final HDI aircraft configuration*

---

## Aircraft Specifications

| Parameter | Value |
|----------|------|
| Maximum Speed | Mach 1.74 |
| Climb Rate | 770 ft/s |
| Endurance | 10 hours |
| Payload | 4 × AIM-120 AMRAAM |
| Wing Loading | 81.2 lb/ft² |
| Thrust-to-Weight Ratio | 1.0 |
| Estimated Unit Cost | $20.5M |
| Maximum Takeoff Weight | ~20,000 lb |

---

# Project Overview

The **Homeland Defense Interceptor (HDI)** is a conceptual aircraft designed to defend U.S. airspace against hijacked aircraft, hostile fighters, and cruise missile threats.

The project focused on **aircraft conceptual design**, translating mission requirements into a feasible aircraft configuration through **trade studies, performance analysis, and aircraft sizing methods**.

Primary design objectives included:

- Rapid response intercept capability
- Long endurance defensive patrol
- Integration with NATO air defense networks
- Low acquisition cost relative to modern fighters

---

# Engineering Work

This project demonstrates experience in several core areas of **aircraft design engineering**:

- Mission profile development  
- Aircraft **constraint analysis and sizing**
- Aerodynamic modeling using **OpenVSP**
- Payload and propulsion **trade studies**
- Center-of-gravity stability analysis
- Performance optimization
- Cost estimation using **DAPCA IV**

---

# Mission Profiles

Three operational missions drove the aircraft design.

---

## Defensive Counter-Air Patrol

Mission sequence:

1. Takeoff and climb  
2. Transit **300 nautical miles**  
3. **4 hour loiter at 35,000 ft**  
4. Intercept hostile aircraft if required  
5. **400 nautical mile return**  
6. **30 minute fuel reserve**

![DCA Mission Profile](assets/images/hdi/dca_mission_profile.png)

---

## Point Defense Intercept

Mission sequence:

1. Maximum thrust climb  
2. **200 nm supersonic dash**  
3. Engagement at **Mach 1.2 – Mach 0.9**  
4. Target neutralization  
5. Return to base

![Point Defense Mission](assets/images/hdi/point_defense_profile.png)

---

## Escort Mission

Mission sequence:

1. Rapid intercept  
2. Close escort (~300 nm)  
3. Monitoring and compliance enforcement  
4. Return to base

![Escort Mission Profile](assets/images/hdi/escort_mission_profile.png)

---

# Concept Development

Two candidate aircraft configurations were developed during early design.

---

## Concept 1

![Concept 1 Sketch](assets/images/hdi/concept1_sketch.png)

Characteristics:

- Swept wing interceptor layout
- Compact fuselage for reduced drag
- Possible **leading edge root extensions (LERX)**

### OpenVSP Model

![Concept 1 OpenVSP Model](assets/images/hdi/concept1_vsp.png)

---

## Concept 2

![Concept 2 Sketch](assets/images/hdi/concept2_sketch.png)

Concept 2 explored alternative wing geometry and fuselage configuration.

### OpenVSP Model

![Concept 2 OpenVSP Model](assets/images/hdi/concept2_vsp.png)

---

# Trade Studies

## Payload Trade Study

Missile payload significantly affects aircraft weight and aerodynamic drag.

The study evaluated how **AIM-120 AMRAAM payload count** affected aircraft performance.

![Missile Payload vs Weight](assets/images/hdi/missile_weight_trade.png)

### Drag Analysis

![Missile Drag Polar](assets/images/hdi/drag_polar.png)

These studies led to the selection of a **4 × AIM-120 AMRAAM payload configuration**.

---

# Aircraft Constraint Analysis

Aircraft performance constraints were used to determine feasible combinations of **wing loading and thrust-to-weight ratio**.

![Constraint Diagram Concept 1](assets/images/hdi/constraint_concept1.png)

![Constraint Diagram Concept 2](assets/images/hdi/constraint_concept2.png)

### Optimal Design Point

| Parameter | Value |
|----------|------|
| Wing Loading | 81.2 lb/ft² |
| Thrust-to-Weight | 1.0 |

This design point balances **interceptor acceleration, maneuverability, and mission endurance**.

---

# Aircraft Sizing

Final aircraft dimensions were determined using an **iterative sizing code** based on mission fuel fractions and aerodynamic performance.

![Aircraft Sizing Logic](assets/images/hdi/sizing_logic.png)

Inputs included:

- mission fuel fractions
- payload weight
- aerodynamic efficiency
- propulsion performance

Outputs included:

- takeoff weight
- required thrust
- wing area
- fuel fraction

---

# Stability and CG Analysis

Center-of-gravity travel was analyzed across all mission profiles to ensure stable aircraft operation.

### Defensive Counter-Air Mission

![CG DCA](assets/images/hdi/cg_dca.png)

### Point Defense Mission

![CG Point Defense](assets/images/hdi/cg_point_defense.png)

### Escort Mission

![CG Escort](assets/images/hdi/cg_escort.png)

---

# Final Aircraft Configuration

The final design is a **single-engine swept-wing interceptor** optimized for homeland defense missions.

### Structural Materials

| Material | Percentage |
|---------|------------|
| Aluminum | 85% |
| Steel | 10% |
| Composites | 5% |

This configuration balances:

- structural strength
- manufacturability
- cost efficiency

---

# Engineering Takeaways

This project demonstrates experience in:

- **Aircraft conceptual design**
- Mission-driven performance analysis
- **Constraint analysis and aircraft sizing**
- Aerodynamic modeling using **OpenVSP**
- Payload and propulsion **trade studies**
- Center-of-gravity stability analysis
- Cost modeling using **RAND DAPCA IV**

The final HDI design achieves **fighter-class interception capability while maintaining significantly lower procurement cost**, making it a scalable platform for homeland air defense.