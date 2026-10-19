# A7 – FEA On Bracket

# Objective
The primary objective of this assignment is to understand how Finite Element Analysis (FEA) can be used as an engineering design tool to evaluate and improve a component. Rather than relying solely on theoretical calculations or assumptions, FEA allows the bracket's structural performance to be evaluated under specified loading and boundary conditions.

The assignment focuses on three main design goals:

* **Strength:** Keep stresses within acceptable limits for the assigned material and maintain an appropriate factor of safety.
* **Stiffness:** Minimize displacement under the applied load so the bracket maintains its intended shape and function.
* **Weight:** Reduce the bracket's mass while maintaining sufficient strength and stiffness.

To achieve these goals, the bracket will be analyzed through multiple design iterations. Each iteration involves evaluating the current design, identifying areas for structural improvement, and modifying the geometry to optimize performance.

Mesh convergence testing is also required to verify that the simulation results are consistent as the mesh is refined. This helps distinguish actual design improvements from numerical artifacts caused by mesh size.

By the end of the assignment, the goal is to develop a bracket with an improved balance of strength, stiffness, and weight while gaining a deeper understanding of FEA, mesh refinement, stress concentrations, displacement, and engineering design optimization.

# Analyze
I started this assignment by opening my CAD model from the previous assignment. Before running any FEA, I needed to define how this part would be fixtured. Because this part supports a hanging load, I chose to fix the overhangs bearing on the rail using a roller/slider fixture, combined with an axial restraint to prevent rigid-body translation along the rail length. This accurately simulates real-world conditions, as the part can move along the rail but cannot pass through it or drift unconstrained. I then applied the load as a downward force distributed along the lower cylindrical surface.

I made no geometry modifications for the initial baseline run, as I wanted to evaluate how my hand calculations performed in simulation. Below are the results.

<img width="1238" height="763" alt="Screenshot 2026-10-18 161859" src="https://github.com/user-attachments/assets/5b624488-fd77-44bd-8c76-97f497fc450e" />

<img width="1233" height="761" alt="Screenshot 2026-10-18 161851" src="https://github.com/user-attachments/assets/d61be0e8-acf7-49a8-affa-5c7a95324120" />

From this initial run, it is evident that the bracket failed. The maximum stress occurred on the cantilevered extension supporting the strap. This was a primary failure point due to the large bending moment imposed on a thin section. The Factor of Safety was below 1.0, indicating structural failure.

For the second iteration, I increased the wall thickness of the failed region and added fillets to mitigate stress concentrations at the sharp right-angle intersections.

<img width="1241" height="761" alt="Screenshot 2026-10-18 162055" src="https://github.com/user-attachments/assets/9986d03b-75ee-47e7-890e-3f363ee8604f" />

<img width="1235" height="760" alt="Screenshot 2026-10-18 162104" src="https://github.com/user-attachments/assets/fd96a376-01e4-45dc-b5f9-ae518821802b" />

This modification significantly improved both overall strength and stiffness, yielding lower deflection values. However, the critical location remained the cantilevered connection point due to the ongoing high bending moment. Peak stress occurred on the load-facing surface near the termination of the lower fillet. Despite these improvements, the mount still exceeded the yield strength.

Recognizing that the primary failure mode stemmed from the high bending moment of a single cantilever support, I added a second symmetrical connection on the opposing side to distribute the load evenly. I reduced the thickness of the original side by half and mirrored it. While this prevents sliding a closed-loop strap directly onto the mount from the side, a strap can easily be threaded through. Additionally, I applied fillets across all remaining sharp edges to eliminate stress concentrations and reduce unnecessary material mass.

<img width="1231" height="760" alt="Screenshot 2026-10-18 162654" src="https://github.com/user-attachments/assets/dcc43def-3d88-4a5f-abf3-f69456ded660" />

<img width="1237" height="764" alt="Screenshot 2026-10-18 162714" src="https://github.com/user-attachments/assets/4a57a427-b858-4f8b-9269-9de406ab2421" />

This dual-bridge design provided a substantial performance boost, achieving a passing Factor of Safety of approximately 1.36 and significantly reducing overall deflection. A detailed summary of all iterations is provided in the table below.

<img width="1187" height="350" alt="image" src="https://github.com/user-attachments/assets/25de0971-ddf0-49a9-bb76-638b42b4a5e9" />


# Reflection

My primary takeaway from this assignment is how significantly simplifying assumptions can alter analytical outcomes. While initial hand calculations indicated a sufficient factor of safety, FEA revealed that the baseline design would fail under the applied load. This discrepancy occurred because the hand calculations assumed the pin connection experienced pure tension, neglecting the substantial bending moment caused by the load offset. Eliminating that moment arm through structural redesign highlighted how easily incorrect loading assumptions can result in a severely under-designed component.


# Ring Part

The setup for this part followed a similar process to the bracket. Fixtures and loads were applied as follows: the downward force was applied to the inner cylindrical face of the lower hole, and a fixed constraint was applied to the inner cylindrical face of the upper hole.

I evaluated the baseline geometry first to establish a performance baseline.

<img width="1233" height="760" alt="Screenshot 2026-10-18 220416" src="https://github.com/user-attachments/assets/f4c25322-3c26-4341-bbfa-dddefb9724e9" />

<img width="1238" height="758" alt="Screenshot 2026-10-18 220407" src="https://github.com/user-attachments/assets/8fb2c0b1-d07c-47f2-a083-f4fb3b63b710" />

Unlike the original bracket, this part successfully carried the load without exceeding yield limits, though noticeable stress concentrations were visible around the perimeter.

Stress distribution plots showed that the central interior region of the component carried negligible stress. To reduce weight, I removed material from the central web by adding a slotted cutout.

<img width="1226" height="757" alt="Screenshot 2026-10-18 220717" src="https://github.com/user-attachments/assets/3f021983-5311-4108-b19b-16007cafe8ad" />

<img width="1227" height="752" alt="Screenshot 2026-10-18 220732" src="https://github.com/user-attachments/assets/6ea28eea-f608-4671-b6ff-e3661f5f4676" />

The peak von Mises stress remained nearly unchanged after introducing the slot, confirming that the removed material was not actively participating in load transfer. Encouraged by this result, I further optimized the component by isolating the primary load path down to the outer side webs and mounting rings.

<img width="1228" height="756" alt="Screenshot 2026-10-18 221351" src="https://github.com/user-attachments/assets/889f3463-9824-4ead-918b-af1d77c089fc" />

<img width="1228" height="757" alt="Screenshot 2026-10-18 221343" src="https://github.com/user-attachments/assets/c7166cb9-f203-4084-9935-d08693a93301" />

This skeletal iteration proved highly effective. Maximum stress levels remained stable while mass was substantially reduced. Fillets were added to internal transition corners to facilitate manufacturability and prevent stress raisers. This geometry closely resembles commercial rigging links, demonstrating the practical reasoning behind such industry designs. A complete data breakdown across all mesh densities and iterations is presented below.

<img width="1365" height="407" alt="image" src="https://github.com/user-attachments/assets/1c0640b5-e2ca-442c-980c-ae99ceb28550" />

## Reflection

This portion of the assignment effectively demonstrated load path optimization within structural members. The highest stress levels were concentrated along the outer lateral edges of the link, which support the tension path and possess the narrowest cross-sectional area. The center section was largely unstressed because the primary load transfer occurs via pure tension along the outer perimeter—analogous to a continuous cable wrapped around two pins. As long as the cross-sectional area of the outer webs remains adequate, the central material can be removed entirely with minimal impact on structural integrity.
