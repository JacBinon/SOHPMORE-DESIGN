# A8 – Gears

# Objective

The main goal of this assignment was to walk through the full mechanical design process for a functional 24:9 gear ratio gearbox. The project focused on testing the structural strength of both the input and output shafts by creating free-body diagrams and running stress calculations using equations from lecture and the Machinery's Handbook. Beyond shaft sizing, the work covered calculating pressure-velocity (PV) ratings to select appropriate off-the-shelf plain journal bearings from McMaster-Carr, as well as designing a custom two-piece housing with proper running sliding fits, clearances, and hardware. Using parametric CAD software, the final step was building the complete assembly and generating a full set of ASME Y14.5-compliant engineering drawings, while documenting the entire workflow, including all calculations, CAD files, mistakes, and key lessons learned along the way.

# Analyze

I started this project by defining the problem and laying out my primary criteria and constraints. Here I selected my shaft material, listed my variables, and justified my constants. I then calculated the required input torque and rpm and solved for both the input and output shafts. Both shafts were strong enough to withstand the forces they would see.

<img width="758" height="1011" alt="image" src="https://github.com/user-attachments/assets/deeb2898-9039-4593-b489-8009923d19df" />

With the shafts sorted out, I moved on to the journal bearings. I started by listing the knowns and unknowns, drawing a free-body diagram, and referencing my Machinery's Handbook for the necessary calculations. After solving symbolically, I solved numerically for both the input and output bearings. Using these values, I referenced the table on page 2442 of the handbook to determine the required bearing material. The input bearing needed to be bronze, while the output bearing could be acetal because of its lower surface speed.

Next, I needed to determine the bearing wall thickness. The handbook gives an approximation stating that the wall thickness should be 0.5 times the shaft diameter when the diameter is less than 0.125 in. For the thicker shaft, the wall thickness should be 0.25 times the diameter. This allowed me to solve for the overall OD of each bearing. I determined the bearing length in a similar way: it should fall between 0.3 and 2 times the shaft diameter, and I chose 1x for both. The bearing part numbers are noted on the page.

<img width="790" height="1022" alt="image" src="https://github.com/user-attachments/assets/25529a71-5329-4f79-8299-57e36d72664d" />

<img width="757" height="986" alt="image" src="https://github.com/user-attachments/assets/c5c6789e-126f-41d4-955b-70ad6ea2958b" />

# Design

With the design parameters finalized, I needed to sketch a concept and design the gearbox. I chose to close the housing with bolts and to use two bearings per shaft for added rigidity. I made sure to note where I would need to incorporate tolerances into the design to prevent the gears from rubbing and the shafts from pinching when the bolts holding the housing together were tightened.

<img width="688" height="892" alt="image" src="https://github.com/user-attachments/assets/cec08718-e171-4ca1-999d-deb6dd068869" />

Once I had a concept, I jumped into CAD to start designing. I began by defining my key known geometry with global variables.

<img width="2145" height="838" alt="Screenshot 2026-10-27 022005" src="https://github.com/user-attachments/assets/857b3822-a4e9-4785-a7c0-d13f7ed4db26" />

Next, I imported all of the gears and bearings and modeled the shafts. I mated these parts together to give myself a reference to design from. The gear center-to-center spacing was then defined with a sketch.

<img width="1326" height="786" alt="Screenshot 2026-10-27 014938" src="https://github.com/user-attachments/assets/345ab5fa-3a74-43f0-8081-7db1fb767aff" />

Tolerance added to prevent binding:

<img width="1660" height="1107" alt="Screenshot 2026-10-27 014455" src="https://github.com/user-attachments/assets/abf3069b-6284-4567-9f86-f581a69c252c" />

I then created the bottom half of the housing by drawing sketches and extruding them. I used the same process for the top half.

<img width="2531" height="1181" alt="Screenshot 2026-10-27 015358" src="https://github.com/user-attachments/assets/8620ab19-18b0-4deb-a3ab-d051a14bb881" />

<img width="1145" height="842" alt="Screenshot 2026-10-27 020702" src="https://github.com/user-attachments/assets/300e289f-fabb-4e0e-bdc7-e43d1270579c" />

<img width="1457" height="941" alt="Screenshot 2026-10-27 021246" src="https://github.com/user-attachments/assets/a2b604f7-4b8a-4cf9-8d52-255781e43f08" />

Bosses were added for the bolts, and the holes were cut through them with the Hole Wizard.

<img width="552" height="476" alt="Screenshot 2026-10-27 020920" src="https://github.com/user-attachments/assets/5d4d3c4f-4f85-4577-a2f7-dfe2f7ef1828" />

Finally, I imported the bolts from McMaster-Carr and mated them in place, completing the CAD model.

<img width="1161" height="632" alt="Screenshot 2026-10-27 021550" src="https://github.com/user-attachments/assets/b62b4a5a-7487-4b8e-80da-04387e8563bc" />

# Drawings

With the CAD finished, I created drawings for all of the parts. I toleranced the bearing fits into the housing as light press fits, using parameters from the Machinery's Handbook.

<img width="1487" height="1157" alt="image" src="https://github.com/user-attachments/assets/6c3d447e-fe8e-4745-9554-b442000d4ecd" />

<img width="1463" height="1131" alt="image" src="https://github.com/user-attachments/assets/f0f5054d-2cff-4b57-b933-4fdef7af70e4" />

<img width="1736" height="1342" alt="image" src="https://github.com/user-attachments/assets/14babf60-b4c8-4c54-aa5c-a3c8b09f62f0" />

<img width="1616" height="1250" alt="image" src="https://github.com/user-attachments/assets/b5475d29-3cdd-4780-9738-827fe5a86d04" />

<img width="1755" height="1246" alt="image" src="https://github.com/user-attachments/assets/3b2c8592-9cc9-4df3-b08b-1bcdf5fb500a" />

<img width="1481" height="1147" alt="image" src="https://github.com/user-attachments/assets/12cf81c5-7897-4b1a-afae-b6d2c39a9b52" />

<img width="1123" height="870" alt="image" src="https://github.com/user-attachments/assets/316fd6bb-a4f7-4192-9fb7-9e762458e161" />

Overall, this was an enjoyable project. I spent about 5 hours on it.

Link to CAD (https://github.com/JacBinon/SOHPMORE-DESIGN/blob/main/docs/assignments/A08/A8.zip)





