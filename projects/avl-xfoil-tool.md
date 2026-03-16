**AVL / XFOIL Python Interface for Dragonfly Autopilot#**

## Project Overview

This project used an existing **AVL / XFOIL Python interface** to generate aerodynamic data for a flight dynamics model of the *Dragonfly aircraft*. None of this data is from the dragonfly aircraft as that is propritary data this is example code I have made seperatly to show what I have done. 

The goal was to automate aerodynamic analysis across a wide range of flight conditions in order to generate a **lookup table used as the aerodynamic plant for an autopilot simulation**.

The base AVL/XFOIL interface was sourced from an open-source GitHub repository. My contribution was designing and implementing a **Python automation framework** that repeatedly ran aerodynamic analyses across many flight conditions and compiled the results into a structured dataset suitable for flight simulation and control development.

---

## Objective

Create an aerodynamic dataset that maps:

- Angle of Attack  
- Flight Velocity  
- Elevator Deflection  

to resulting aerodynamic forces and moments.

This dataset was then used as a **lookup table representing the aircraft plant** for an autopilot simulation.

---

## Approach

The project workflow consisted of:

1. Using an existing **AVL / XFOIL Python interface** to control aerodynamic simulations.
2. Writing a Python loop that iterated across:
   - Multiple angles of attack
   - Multiple flight velocities
   - Multiple elevator deflections
3. Running AVL/XFOIL for each condition.
4. Extracting aerodynamic outputs such as:
   - Lift coefficient
   - Drag coefficient
   - Pitching moment
5. Organizing the results into a **structured lookup table**.
6. Exporting the table for use in the **autopilot plant model**.

---

## Parameter Sweep

The aerodynamic model was evaluated across a multidimensional parameter space.

Example parameter ranges:

| Parameter | Range | Step |
|--------|--------|--------|
| Angle of Attack (aoa)| *-5:15* | 1 |
| Velocity (m/s)| *10:30* | 5 |
| Elevator Deflection (deg)| *0:10* | 1 |

This resulted in **over a thousand aerodynamic simulations** automatically executed through the Python interface.

---

## Workflow Diagram

*(Insert a workflow diagram showing simulation automation pipeline)*


---

## Example Aerodynamic Results

### Lift Curve

![Lift Curve](images/lift_curve_example.png)

*Lift coefficient vs angle of attack generated from automated simulations.*

---

### Pitching Moment

![Pitching Moment](images/pitch_moment_example.png)

*Pitching moment variation with elevator deflection.*

---

### Example Lookup Table Visualization

![Lookup Table](images/lookup_table_visualization.png)

*Visualization of the aerodynamic dataset used by the autopilot.*

---

## Example Automation Code

Below is a simplified example of the Python looping structure used to generate the aerodynamic dataset.

```python
for velocity in velocity_range:
    for aoa in aoa_range:
        for elevator in elevator_range:

            results = run_avl_simulation(
                velocity=velocity,
                angle_of_attack=aoa,
                elevator_deflection=elevator
            )

            lookup_table.append({
                "velocity": velocity,
                "aoa": aoa,
                "elevator": elevator,
                "CL": results.CL,
                "CD": results.CD,
                "Cm": results.Cm
            })


