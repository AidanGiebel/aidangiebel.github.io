**One Page Project Summary**

## A Convex Analysis of a Soft Capture Problem

### Objective
Develop a method for computing safe, fuel-efficient soft capture trajectories for spacecraft docking. Research how different constraints can affect the docking procedure and problem. Enforce realistic constraints such as control limits, velocity limits, collision, and field-of-view (FOV) constraints using convex optimization.

### Motivation
As autonomous spacecraft operations become more common, robust and reliable docking methods are critical. Soft capture allows for safe initial contact without damage or excessive force. Optimization provides a good framework for managing tradeoffs between performance and safety.

### Methodology
Formulate the problem using a discrete-time Clohessy-Wiltshire-Hill (CWH) model for relative motion. Use convex optimization (CVX) to minimize control effort while satisfying key constraints.

- Boundary conditions on initial/final position and velocity  
- Control magnitude constraints  
- Velocity limits  
- Collision constraints  
- Relaxed second-order cone constraints for FOV limits  

This was done by convexification and introducing a slack variable to soften hard constraints and improve feasibility.

### Results

#### Relative Position Trajectory
![Relative Position](/assets/images/relative_position.png)

#### Optimal Variables Over Time
![Optimal Variables](/assets/images/optimal_graphs_all.png)

### Discussion
The generated trajectories demonstrate that soft capture maneuvers can be planned within realistic mission constraints using convex optimization. The inclusion of thrust and velocity bounds ensures the solution remains safe for low-thrust docking objectives at close ranges. The relaxed collision-avoidance constraint allows for flexible enforcement of collision avoidance while maintaining convexity.

This trajectory shows the feasibility of using these constraints on a docking maneuver while maintaining safe operating conditions. These constraints were also deconstructed and could all be used separately. It is important to note that this does not mean all situations can be satisfied with this method.

### Conclusion
This project has been extremely insightful into some of the important work that is done in these fields. Reading research papers and attempting to replicate some of those results while adapting them for this project was extremely difficult but rewarding.

A key takeaway is the importance of carefully balancing constraint tightness and trajectory smoothness. Overly aggressive constraints can induce oscillations or infeasibility. Another takeaway is that some constraints cannot be applied alone and must be combined with others to create a robust formulation. While solutions may exist, they are often much harder to find without solving the full problem.