# Finite Element Analysis of Isolation Transformer 

This repositry contains coursework material from my Electrical Machines Module in university 


## Assignment
The coursework explores the finite element modelling of an isolation transformer using COMSOL Multiphysics. The objective is to understand the effects of core design, mesh refinement, and 2D vs. 3D simulation approaches on transformer behavior and proide a detailed yet onise technical report presenting these ideas.

## ⚠️ Academic Integrity
This repository **does not** contain any original solution content, reports, or code, to comply with academic regulations. This repository contains my personal learning and modeling workflow based on coursework. It does not contain any graded solutions or content that would violate academic integrity

## Tools I Used
- COMSOL Multiphysics (FEA Simulation)
- MATLAB (optional for circuit analysis)
- Excel (data logging and curve fitting)

  ## What I did

  #### 1. Citique of Solid Core 2D Model
  - I built a 2D axisymmetric model of a transformer with a solid steel core using COMSOL.
  - The goal was to simulate magnetic flux density and analyze the performance of the transformer without lamination.
  -  I evaluated the results, noting potential issues like core saturation and eddy current losses.

<img width="374" height="346" alt="image" src="https://github.com/user-attachments/assets/730483a1-0345-4701-b7c6-4029dab59884" />

<img width="166" height="320" alt="image" src="https://github.com/user-attachments/assets/0337359b-691d-48a2-90c7-93bb3f95598a" />

  #### 2. Impact of Laminating the 2D Model Core
  - By adjusting the core material’s conductivity and permeability tensors, I simulated the effect of lamination.
  - Analysed the reduction of eddy current losses and improved performance, particularly in high-frequency applications.
  - These changes were implemented without modifying the geometry.

<img width="367" height="547" alt="image" src="https://github.com/user-attachments/assets/8376c7b0-525c-4029-8b04-775dc314d54f" />


  #### 3. Mesh Refinement Study
  - I performed a mesh convergence study to ensure simulation accuracy.
  - Refined the mesh in critical domains (like the core).
  - I ensured the calculated magnetic flux density values were accurate to within three significant figures.


  #### 4. Equivalent Circuit Parameters (2D & 3D)
  - Using simulation data, I manually calculated equivalent circuit parameters such as magnetizing reactance and leakage inductance.
  - I compared results from both 2D and 3D models, highlighting differences due to dimensional effects and geometry resolution.

**Equation List:**

$$
P = I^2 R'_m
$$

$$
\frac{V_p}{I_p} = |Z| = \sqrt{(R'_m)^2 + (X'_m)^2}
$$

$$
\frac{R_m X_m^2}{R_m + X_m} + j \frac{R_m^2 X_m}{R_m + X_m} = R'_m + j X'_m
$$


  #### 5. Reducing 3D Computational Cost
  - I implemented model symmetry and boundary conditions by splitting the model into octants divides the coil length in 4 and halves the coil area sector.
  - By exploiting symmetry scaling the model requires the coil length to be 4 and the coil area sector to be 2 to accommodate for the fact that you are not working with the full coil length and coil area sector. (e.g., perfect magnetic conductor) to reduce the number of solved domains.
  - This significantly decreased simulation time while maintaining accuracy.
  - Highlights how the same results can be accumulated without haing to use entire model to save costs.

<img width="471" height="347" alt="image" src="https://github.com/user-attachments/assets/c5cecc29-008f-496e-b0e7-17d4b3664d4e" />


  #### 6. Discussion on Model Assumptions
  - I discussed key simplifications such as linear material properties, lack of thermal effects, and idealized geometry.
  - Explored how these assumptions impact equivalent circuit accuracy and real-world validity.



  #### 7. Future Work
I proposed two extensions: high frequency transformer optimisation and advanced cooling and thermal management.

- **High-Frequency Transformer Optimization**: Future simulations can investigate transformer designs at high frequencies (100 kHz–2 MHz), focusing on winding strategies such as Litz wire to reduce AC losses, increase magnetizing inductance, and improve thermal performance while considering trade-offs like cost and complexity.

- **Advanced Cooling and Thermal Management**: Ensuring thermal regulation is critical for high-voltage power electronics; CFD can simulate coolant flow in transformers to optimize heat dissipation through improved coolant channel designs and construction.

## What I Learnt

Through this coursework, I gained practical experience in finite element analysis (FEA) and developed a deeper understanding of transformer modeling. Key takeaways include:

- **FEA Modeling Skills**: Built and analysed 2D and 3D transformer models using COMSOL Multiphysics, including solid and laminated core configurations. Learned how model assumptions and dimensional choices impact results.
- **Mesh Refinement & Accuracy**: Conducted mesh convergence studies to ensure accurate simulations while balancing computational efficiency. Learned to identify critical regions for refinement. Whilst initially I didn't do this correctly for my final submission, I was able to get feedback from my professor to understand where I went wrong.
- **Material and Core Effects**: Explored how lamination and material properties affect eddy currents, flux distribution, and transformer performance. Developed skills in simulating practical engineering considerations.
- **Equivalent Circuit Estimation**: Translated simulation results into equivalent circuit parameters (magnetizing reactance, leakage inductance) and compared 2D vs. 3D approaches, improving understanding of real-world transformer behavior.
- **Computational Optimization**: Implemented model symmetries and boundary conditions to reduce computational cost without compromising accuracy.
- **Critical Thinking & Assumptions**: Evaluated the impact of simplifications such as linear material properties and idealized geometry, gaining insight into how assumptions affect results.
- **Workflow & Documentation**: Practiced organizing simulations, recording observations, and summarizing findings in a clear, structured manner.

Overall, this project strengthened my problem-solving, simulation, and analytical skills while providing a foundation for more advanced studies in electrical machines, transformer design, and simulation-based engineering analysis.
  
