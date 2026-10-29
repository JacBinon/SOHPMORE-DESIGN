# A8 – Gears

# Objective
For this assignment, the main goal is to walk through the full mechanical design process for a functional 24:9 gear ratio gearbox. The project focuses on testing the structural strength of both the input and output shafts by creating free-body diagrams and running stress calculations using equations from lecture and the Machinery’s Handbook. Along with shaft sizing, the work covers calculating pressure-velocity (PV) ratings to select appropriate off-the-shelf plain journal bearings from McMaster-Carr, as well as designing a custom two-piece housing with proper running sliding fits, clearances, and hardware. Using parametric CAD software, the final step involves building the complete assembly and generating a full set of ASME Y14.5-compliant engineering drawings, while documenting the entire step-by-step workflow—including all calculations, CAD files, mistakes, and key lessons learned along the way.

# Analyze
I started this project by first defining the problem and laying out my primary criteria and constraints. It is here I defined my shaft material, listed variables, and rationalized constants. I then Calculated the input torque and rpm required and solved the input shaft and output shaft. Both shafts were storing enough to withstand the forces they would see. 
<img width="758" height="1011" alt="image" src="https://github.com/user-attachments/assets/deeb2898-9039-4593-b489-8009923d19df" />

Now that the safts were sorted out I moved on the the jpurnal bearings. I started by listing knowns and unknonws for this, making a FBD and refrencing my macheneries handbook for the needed caculations. Once Solved for symbolicaly I then solved numericaly for both imput and the output. With the values I Obtinaed I refrecned the table on page 2442 of my handbook and deduced the required bering material. The IMput bering needed to be Bronze, and the output could get away with Acetal because of the lower surface speed. Next I needed to find the thickness of the bearins. I found a aproxamation in my handbook that stated that the wall thickenss shoudl be 0.5 the diameter when d is less than .125. For the thicker shaft the wall thickness sould be .25 the diameter. This then allowd me to solve for the over all OD of the bearings. Likewise I solved the length of the Bearings though a simmilar means. The length shoudl be between 0.3 - 2 x the sahft diameter. I chose 1x for both. The Bearing Part Numbers are noted on the page.

<img width="790" height="1022" alt="image" src="https://github.com/user-attachments/assets/25529a71-5329-4f79-8299-57e36d72664d" />

<img width="757" height="986" alt="image" src="https://github.com/user-attachments/assets/c5c6789e-126f-41d4-955b-70ad6ea2958b" />

# Design
Now that the Parameter of my design have been finalized, I needed to make a sketch and design the gearbox. I chose to go with Bolts to close it and use 2 bearings per shaft to help with rigidity. I ensured to note places where I would need to incorperate tolerances in to my design to prevent the gears from rubbing and getting pincehd when the bolts holding then housing togheter were tightened.

<img width="688" height="892" alt="image" src="https://github.com/user-attachments/assets/cec08718-e171-4ca1-999d-deb6dd068869" />

Now that I had a Concept I hopped in to Cad to start designing. I started by defining som og my key knonw gemoety with global variables. 

<img width="2145" height="838" alt="Screenshot 2026-10-27 022005" src="https://github.com/user-attachments/assets/857b3822-a4e9-4785-a7c0-d13f7ed4db26" />

I then Imported all the gears bearings and moddles the shafts. I mated these parts toghether to give me a a refrence to design off of. Then Gear center to center spacgin was defined my a scetch.

<img width="1326" height="786" alt="Screenshot 2026-10-27 014938" src="https://github.com/user-attachments/assets/345ab5fa-3a74-43f0-8081-7db1fb767aff" />

Tolerance Added to prevent binding

<img width="1660" height="1107" alt="Screenshot 2026-10-27 014455" src="https://github.com/user-attachments/assets/abf3069b-6284-4567-9f86-f581a69c252c" />

I then Created the bottom of the housing by creating some scetches and extrusing them The same process was used for the top of the housing

<img width="2531" height="1181" alt="Screenshot 2026-10-27 015358" src="https://github.com/user-attachments/assets/8620ab19-18b0-4deb-a3ab-d051a14bb881" />

<img width="1145" height="842" alt="Screenshot 2026-10-27 020702" src="https://github.com/user-attachments/assets/300e289f-fabb-4e0e-bdc7-e43d1270579c" />

<img width="1457" height="941" alt="Screenshot 2026-10-27 021246" src="https://github.com/user-attachments/assets/a2b604f7-4b8a-4cf9-8d52-255781e43f08" />

Bosses were added for the bolts and holes cut through them with the hole wizard.

<img width="552" height="476" alt="Screenshot 2026-10-27 020920" src="https://github.com/user-attachments/assets/5d4d3c4f-4f85-4577-a2f7-dfe2f7ef1828" />

Bolts where them imported form Micmaster and mated in place finishign the cad.  

<img width="1161" height="632" alt="Screenshot 2026-10-27 021550" src="https://github.com/user-attachments/assets/b62b4a5a-7487-4b8e-80da-04387e8563bc" />

# Drawings

Now that I had my Cad finished I needed to create all of the drawings for the parts. I chose to Toleracne the Bearing fits into the housing as a light press fit, parameters taken from machereries handbook.

<img width="1487" height="1157" alt="image" src="https://github.com/user-attachments/assets/6c3d447e-fe8e-4745-9554-b442000d4ecd" />

<img width="1463" height="1131" alt="image" src="https://github.com/user-attachments/assets/f0f5054d-2cff-4b57-b933-4fdef7af70e4" />

<img width="1736" height="1342" alt="image" src="https://github.com/user-attachments/assets/14babf60-b4c8-4c54-aa5c-a3c8b09f62f0" />

<img width="1616" height="1250" alt="image" src="https://github.com/user-attachments/assets/b5475d29-3cdd-4780-9738-827fe5a86d04" />

<img width="1755" height="1246" alt="image" src="https://github.com/user-attachments/assets/3b2c8592-9cc9-4df3-b08b-1bcdf5fb500a" />

<img width="1481" height="1147" alt="image" src="https://github.com/user-attachments/assets/12cf81c5-7897-4b1a-afae-b6d2c39a9b52" />

<img width="1123" height="870" alt="image" src="https://github.com/user-attachments/assets/316fd6bb-a4f7-4192-9fb7-9e762458e161" />


Over all this was an enjoyable project I spent 5 hours on it. 





