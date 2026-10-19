# A7 – FEA On Bracket

# Objective
The primary objective of this assignment is to understand how Finite Element Analysis can be used as an engineering design tool to evaluate and improve a component. Rather than relying solely on theoretical calculations or assumptions, FEA allows the bracket's structural performance to be evaluated under specified loading and boundary conditions.

The assignment focuses on three main design goals:

Strength: Keep stresses within acceptable limits for the assigned material and maintain an appropriate factor of safety.

Stiffness: Minimize displacement under the applied load so the bracket maintains its intended shape and function.

Weight: Reduce the bracket's mass while maintaining sufficient strength and stiffness.

To achieve these goals, the bracket will be analyzed through multiple design iterations. Each iteration will involve evaluating the current design, identifying areas for improvement, and modifying the geometry to improve its performance.

Mesh convergence testing is also required to verify that the simulation results are sufficiently consistent as the mesh is refined. This helps distinguish actual design improvements from changes in results caused by mesh size.

By the end of the assignment, the goal is to develop a bracket with an improved balance of strength, stiffness, and weight while gaining a better understanding of FEA, mesh refinement, stress concentrations, displacement, and engineering design optimization.

# Analyze
I started this assignment by opening my CAD from the precious assignment. Before running any FEA, I needed to define how this part would be fixtured. Because this part will hang a load I chose to fix the over hangs that bear on the rail with a roller/slider fixture. This best simulates the real world as the part can move along the rail but can't move through it. I then defined my load by placing it along the surface of the cylinder bearing downward. 

I decided to change noting about the design on this first run. I wanted to see how my choice of hand calculations resulted. Below are the results. 

<img width="1238" height="763" alt="Screenshot 2026-10-18 161859" src="https://github.com/user-attachments/assets/5b624488-fd77-44bd-8c76-97f497fc450e" />

<img width="1233" height="761" alt="Screenshot 2026-10-18 161851" src="https://github.com/user-attachments/assets/d61be0e8-acf7-49a8-affa-5c7a95324120" />

From this first run I can see that my bracket has failed. The max stress was located on the part holding the up the strap. This Is an obvious place for failure as there is a large moment on a thin part. There was no safety factor as it failed. 

For the second Run I made the part that failed thicker. and added fillets around it to help prevent the stress concentrations at the right angles. 

<img width="1241" height="761" alt="Screenshot 2026-10-18 162055" src="https://github.com/user-attachments/assets/9986d03b-75ee-47e7-890e-3f363ee8604f" />

<img width="1235" height="760" alt="Screenshot 2026-10-18 162104" src="https://github.com/user-attachments/assets/fd96a376-01e4-45dc-b5f9-ae518821802b" />

This made a huge improvement to both the strength and to the deflection. The weakest link is once again that connection part that has a very large moment on it. The stress was highest on the face facing the load were the bottom fillet ended. Despite the improvement the mount still failed. 

Seeing that most of my problems were caused by the large moment caused by cantilevering the load I decided to add a second connection at the other end to cancel out the load. I halved the thickness of the one side and added it the other. This does mean that strap can't be slid on however as it's a strap it could be fed through. Aditianaly I filleted all the rest of the edges to reduce mass and prevent stress concentarions. 

<img width="1231" height="760" alt="Screenshot 2026-10-18 162654" src="https://github.com/user-attachments/assets/dcc43def-3d88-4a5f-abf3-f69456ded660" />

<img width="1237" height="764" alt="Screenshot 2026-10-18 162714" src="https://github.com/user-attachments/assets/4a57a427-b858-4f8b-9269-9de406ab2421" />


This was a huge improvement and left the bracket with a safety factor of approximately 1.36 The deflection was also drastically reduced. Below Is a Table with more details.

<img width="1187" height="350" alt="image" src="https://github.com/user-attachments/assets/25de0971-ddf0-49a9-bb76-638b42b4a5e9" />


# Reflection

My biggest takeaway from this assignment is how drastically design assumptions can alter structural outcomes. While hand calculations suggested my mount had a sufficient factor of safety, FEA showed it could not support even the baseline load. This error occurred because I assumed the pin connection was purely in tension, completely ignoring the significant bending loads caused by the pin's moment arm. Even though I fixed the design by eliminating that moment, the exercise proved how easily flawed assumptions can cause a part to be severely under-designed. 


# Ring Part

I started this part the same as the previous. I defined the fixtures and loads as follows: The load was on the inside face of the bottom circle and the fixture was on the inside face of the top circel.

I once more started with my base part to see how it preformed. 

<img width="1233" height="760" alt="Screenshot 2026-10-18 220416" src="https://github.com/user-attachments/assets/f4c25322-3c26-4341-bbfa-dddefb9724e9" />

<img width="1238" height="758" alt="Screenshot 2026-10-18 220407" src="https://github.com/user-attachments/assets/8fb2c0b1-d07c-47f2-a083-f4fb3b63b710" />

Unlike my bracket this part does survive the base loading but is experiencing pretty significant stress concentrations. 

I noticed most of the inside of the part was very unstressed. To reduce weight and material I decided to remove the middle with a slot. 

<img width="1226" height="757" alt="Screenshot 2026-10-18 220717" src="https://github.com/user-attachments/assets/3f021983-5311-4108-b19b-16007cafe8ad" />

<img width="1227" height="752" alt="Screenshot 2026-10-18 220732" src="https://github.com/user-attachments/assets/6ea28eea-f608-4671-b6ff-e3661f5f4676" />

The yield strength did not change much making this a good choice. This proved that the material was not helping support the load. Seeing how well this worked I decided to take this even further and leave just the rings and the outermost material. 

<img width="1228" height="756" alt="Screenshot 2026-10-18 221351" src="https://github.com/user-attachments/assets/889f3463-9824-4ead-918b-af1d77c089fc" />

<img width="1228" height="757" alt="Screenshot 2026-10-18 221343" src="https://github.com/user-attachments/assets/c7166cb9-f203-4084-9935-d08693a93301" />

This worked very well. The yield strenght did not change and even more material was removed. I decided to add fillets to the corer to aid in ensuring this design could be manufactured and didn't have any zero radius corners. I have seen links similar to this before in the wild and it makes sense why they choose this design. Below is a table with more details on each run.

<img width="1162" height="350" alt="image" src="https://github.com/user-attachments/assets/a3c145fb-91d0-4495-a72d-7a31eddc44e9" />

## Reflection

In this part of the assignment, I learned the most about load paths within materials. The highest-stress area of the design was around the edges of the ring, which makes sense because it supports the most force and is the thinnest. The center part of the connector was mostly unstressed. Because it was in pure tension, I could think of it almost like a cable wrapped around both circles: as long as the narrowest part of the cable was large enough, the entire cable would be sufficient. This was clearly demonstrated when I removed the entire inside section and the yield strength barely changed.

