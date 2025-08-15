# Finite Element Analysis of Iolation Transfromer 

This repositry contains coursework material from my Electrical Machines Module in university 


## Assignment
The coursework explores the finite element modelling of an isolation transformer using COMSOL Multiphysics. The objective is to understand the effects of core design, mesh refinement, and 2D vs. 3D simulation approaches on transformer behavior and proide a detailed yet onise technical report presenting these ideas.

## ⚠️ Academic Integrity
This repository **does not** contain any original solution content, reports, or code, to comply with academic regulations.

## Tools I Used
- COMSOL Multiphysics (FEA Simulation)
- MATLAB (optional for circuit analysis)
- Excel (data logging and curve fitting)

  ## What I did

  #### 1. Citique of Solid Ore 2D Model
  - I built a 2D axisymmetric model of a transformer with a solid steel core using COMSOL.
  - The goal was to simulate magnetic flux density and analyze the performance of the transformer without lamination.
  -  I evaluated the results, noting potential issues like core saturation and eddy current losses.



  #### 2. Impact of Laminating the 2D Model Core
  - By adjusting the core material’s conductivity and permeability tensors, I simulated the effect of lamination.
  - Analysed the reduction of eddy current losses and improved performance, particularly in high-frequency applications.
  - These changes were implemented without modifying the geometry.



  #### 3. Mesh Refinement Study
  - I performed a mesh convergence study to ensure simulation accuracy.
  - Refined the mesh in critical domains (like the core).
  - I ensured the calculated magnetic flux density values were accurate to within three significant figures.



  #### 4. Equivalent Circuit Parameters (2D & 3D)
  - Using simulation data, I manually calculated equivalent circuit parameters such as magnetizing reactance and leakage inductance.
  - I compared results from both 2D and 3D models, highlighting differences due to dimensional effects and geometry resolution.



  #### 5. Reducing 3D Computational Cost
  - I implemented model symmetry and boundary conditions (e.g., perfect magnetic conductor) to reduce the number of solved domains.
  - This significantly decreased simulation time while maintaining accuracy.
  - Highlights how the same results can be accumulated without haing to use entire model to save costs.



  #### 6. Discussion on Model Assumptions
  - I discussed key simplifications such as linear material properties, lack of thermal effects, and idealized geometry.
  - Explored how these assumptions impact equivalent circuit accuracy and real-world validity.



  #### 7. Future Work
  - I proposed two extensions: simulating core saturation under overload and including frequency-dependent losses.
  - These would provide deeper insight into performance under extreme conditions and harmonics.

## What I Learnt
Overall, I learnt a range of skills
  
