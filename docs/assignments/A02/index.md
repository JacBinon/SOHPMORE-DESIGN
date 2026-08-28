# A2 – Truss Stress Analysis

## Assignment Objectives

This assignment is meant to provide experience in applying students' engineering knowledge. This is done through designing a truss to support a load with a safety factor while navigating geometric constraints.

Objectives given include:

- Creating a planar truss following geometric constraints
- Creating free body diagrams for the truss and all joints
- Calculating minimum cross-sectional area of all members with a safety factor
- Calculating minimum cross-sectional area of pins with a safety factor to withstand single shear
- Calculating the weight of the pins with given material properties
- Creating an accurate CAD model of the truss and pin connections
- Applying mass properties to the CAD model to predict the weight of the truss
- Fully documenting the design process, calculations, and reasoning in this document

The following are the constraints given for the assignment:

"Design a lightweight planar truss using A500 structural steel (Some software will not have this material, use another type of steel). There are four steps outlined below. Steps 1 through 2 require FBDs as well as calculations to determine the design. The third step requires a CAD model and verification of the analytical calculations in the previous steps.

- Design constraints are shown in Figure #1. (See Appendix for deeper explanation).
- The cross-sectional area of each element is to be identical.
- The pins are to be identical to each other and each element is to have the same cross-sectional geometry."

<p align="center">
<img width="702" height="302" alt="image" src="https://github.com/user-attachments/assets/81ce9513-0628-42cc-be1e-0f92ac6e1efe" />

# Design And Process

## Initial Truss Geometry Selection

The first thing I needed to do was decide what my truss was going to look like, including the number of members and joints. I started out by first drawing the geometric constraints that were given to me to better understand them. I defined my load "P" as 30KN. I chose this number because it was at the high end of the range, providing additional load capacity to my truss. I then researched some popular truss designs on the internet for some inspiration. After doing so, I drew out a few designs I felt could be good candidates. These general designs had to be adapted to have the 2 points in the span for my load as well as the 2 end points (A and B).

<p align="center">
<img width="505" height="353" alt="image" src="https://github.com/user-attachments/assets/277c5027-8157-49aa-89b8-d0dbeb875ec1" />

## Truss Type Decision

I chose Design B (Circled in the top right). Firstly, this design has the fewest members. Fewer members means fewer components, fewer failure points, and less time calculating loads in the members. In real-world applications, choosing a simpler design can often decrease cost in both manufacturing, assembly, and design. The second reason I chose this design is that it is symmetrical. Being symmetrical means the truss can be split, and only one side needs to be solved to calculate loads on the whole truss. This once more simplifies the design, as the same member design can be used on both sides, saving time and cost on the manufacturing front.

## Calculating Internal Forces

To solve this truss and find its internal loads, I first needed to create a free body diagram to model this truss design. I drew the diagram and completed all my calculations on engineering paper. I also employed the use of a straight edge to assist in maintaining neat and organized calculations to help avoid careless mistakes.

<p align="center">
<img width="507" height="312" alt="image" src="https://github.com/user-attachments/assets/79d2ef1d-35c3-4543-8f5c-52d2a29fc5ab" />

After my model was created, I started by calculating the external loads acting on the truss. All of my calculations were done symbolically, and numbers were later plugged in per the assignment directions. This was done by defining my equilibrium equations in the X, Y, and Mo (Moment) directions. Solving for these values allowed me to solve Joint B/A first, as there was now only 1 unknown remaining in the Y direction. It is likely you could have solved this truss without finding the external forces; however, solving for them allowed me to more easily use the method of joints, which is my preferred way of solving trusses.

As previously stated, I started by solving Joint B/A. Joint B and Joint A are, for my purposes, the same, as the truss is symmetrical and has symmetrical loading. Therefore, when a joint is referred to as Letter/Letter, note the reason. To start solving, I first created another free body diagram to model the forces and members present at this joint. Second, I defined what Sin(x) and Cos(x) were equivalent to for this truss. Next, I created my equilibrium equations and solved for my unknowns. I repeated this process for all the joints besides Joint C, as solving it would only prove the truss to have a net force of 0. In hindsight, I should have solved Joint C, as it would expose any errors in my math.

<p align="center">
<img width="446" height="576" alt="image" src="https://github.com/user-attachments/assets/09f31d69-5d45-4673-9998-d67067ef301b" />

To aid in organization, I compiled the symbolic solutions for the internal forces onto a new page and defined my known variables once again. I then solved these equations by inputting the expressions into my calculator. The magnitude and compression or tension of the force was then noted. I could have solved these equations by hand; however, using a calculator helps prevent any careless errors.

<p align="center">
<img width="467" height="177" alt="image" src="https://github.com/user-attachments/assets/2c467e7a-f510-4870-97c9-8d6207ca383c" />

## Calculating Cross-Sectional Area

The next step of the design process was to calculate the minimum cross-sectional area of the highest-force member. I knew that I needed to create an expression that combined yield strength, safety factor, area, and force, as this would use the 3 knowns I had and leave me with one unknown. My first thought was to start by multiplying the force by the safety factor. This may have gotten me the answer, but per the assignment instructions, I needed to solve symbolically first, so I crossed this work out. The equation I settled on is defined in the image below.

<p align="center">
<img width="430" height="187" alt="image" src="https://github.com/user-attachments/assets/63f4b767-083b-41c3-a3c4-053d17353032" />

The assignment instructed me to use A500 Steel. Before I solved using that number, I wanted to ensure that my CAD system had this material defined. Unfortunately, SolidWorks did not. I substituted A500 with ASTM A36. This is another construction-grade steel with a lower yield strength. I chose a metal with a lower yield strength to ensure that if this truss was constructed with the A500 material, it would be stronger than designed, ensuring it would withstand the defined load. I used the properties defined by SolidWorks for my calculations and used the greatest internal force found during my previous calculations. I calculated that a minimum cross-sectional area of 437.5mm^2 would be required.

## Pin Calculations

The next step in designing this truss is to calculate the shear loads of the pins that hold the pins together. This shear loading can then be used to calculate the minimum cross-sectional area of the pins with a safety factor. Once more, this required finding an expression that combined the known values and left the area value as an unknown. The expression I derived is located in the picture below.

<p align="center">
<img width="466" height="260" alt="image" src="https://github.com/user-attachments/assets/da6f1fa3-a6f9-443c-8128-3569aba0eda5" />

Once the expression was created, I solved for the area using the safety factor of 4 and the shear strength provided in the assignment instructions. The shear strength and density values provided in the assignment directions were given in imperial units. I converted these values to metric units to maintain a cohesive unit system across my calculations. I used the value of 50KN for my maximum shear force, as this was the largest force acting on any pin. This could be found at Pin A and Pin B. Completing these calculations gave me a value of 170.63MM^2 that would be needed to safely support this truss. This value was then converted from an area value to a diameter value. The next step was to estimate the weight of all the pins in this truss. In order to get the pin lengths, I assumed that my truss members would be squares and the pin would need to be double the width of the truss members to fully connect. This was then used to find the volume and, therefore, weight of one pin. Multiplying this value by 5 gave a weight of 274.6G for all 5 pins in the truss.

## Aprocamate Truss Weight

To aproxamate the weight of the truss I first wanted to create an expresion for the total ammount of material in the truss. I came to the realization this was simply the lenght of all the memmers added up then multiplied by the cross sectional area. I then re drew the truss to assign lenghts to each member and to ensure I didnt forget a member. I used trigonomerty to assign enghts to the dagonal members, horosonatl and veriacla mebres could have their lenghs taken from the given over all dimentions. I then summed these lengths converted to mm and then multipled by the corss sectioanl area prevouls claculated to get the volume in cubic millimeters. The decnity of ASTM A36 was taken form slolifoeks and converted to grams per mm cubed by multiplying it by 10^-6. This was then multiplied by the volume to get a estemated mass without pins of 11402.125 g. The caulations can be seen in the immage below. Adding the weight of the pins this bring the weight of the truss to 11676.725.

<p align="center">
<img width="707" height="599" alt="image" src="https://github.com/user-attachments/assets/c391ba39-8f5b-4e9c-aa4c-b4cff7d9f431" />

## CAD Moddel

The last part of this assigment is to create a cad moddel of the truss. As instructed I moddeld the whole truss as one component. The pins were then added in the assembly. In an effort to get a more accurate weight of the entire bridge I increaded the thickenss at the intersection by the thickness of the truss multiplied by the number of members attatching at that point. The same was done for the pins. I did this becasue in order to have a pin conection there will be an over lap of material where each member has the "Hoop" that the pin contacts. Aditonaly arround the hole for the pins I used the offset tool to widen the sourounding are at an offfset factor of 1/2 the width of the truss. This ensure that there is a consestant cross sectional area even at the intersection point of the pin. If I were to build this bridge I would want to creat a more accurate moddel of this truss inclding individual componets for each member, accurate moddels of the pin joints, and take in to account proper tolerance for then pins. Below are immages of the cad moddel 

<p align="center">
<img width="1138" height="482" alt="image" src="https://github.com/user-attachments/assets/6b9c27c3-fe21-4080-88c9-f1c02bb848ac" />

<p align="center">
<img width="920" height="618" alt="image" src="https://github.com/user-attachments/assets/ed7e0247-deac-435a-9817-4200e2534139" />

<p align="center">
<img width="1917" height="1033" alt="image" src="https://github.com/user-attachments/assets/ee911e63-5e1f-4cf8-8cea-dbf565757500" />

As seen in the above immage the estemated weight of the entire assembly is 12867.77 G. This comes out to aporxamatly a 9 precetn difference. This divverence I atribute mostly to my cad moddel accounting for the extra material required for the pin conections and the longer pins. I came to the realization that representing the weight in grams may not be the proper unit to use as grams are a unit of mass. Converting these units to neutons would be more accurate and would make it simpler to account for the weight of the truss itslef in the load calulations. This is somehting I need to ensure I pay attention too in the future. Forrunalty the load on the truss was given in the correct unit otherwise a complte recaculation would be needed. 




## Engineering Lessons 





