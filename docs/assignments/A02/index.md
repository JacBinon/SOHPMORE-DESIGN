# A2 – Truss Stress Analysis

## Assignment Objectives 
This assignment is meant to provide empierce in applying students engineering knowledge. This is doen through deaging a truss to support a load with saefty factor while naviagtong gemoetric contraints. 

Objective given include: 
  - Creating a planar truss following geometric constrings
  - Create free body diagrams for the truss and all joints
  - Calculate minmum cross ectioanl area of all memebers with saefty factor
  - Calcualte mimum cross sectioal area of pins with saefty factor to sithsand single shear.
  - Calcualte weight of the pins with given material prpoerties
  - Create an accurate Cad moddel of truss and pin concetipons
  - Apply mass porperties to the cad moddel to predict weight of truss.
  - Fully document the dein procss, calcaulations, and reasoning in this document. 

The following are the constraints given for the assignment:

"Design a light weight planar truss using A500 structural steel (Some software will not have this material, use another type of steel). There are four steps outlined below. Steps 1 through 2 require FBDs as well as calculations to determine the design. The third step requires a CAD model and verification of the analytical calculations in the previous steps.

- Design constraints are shown in Figure #1. (See Appendix for deeper explanation). 
- The cross sectional area of each element is to be identical.
- The pins are to be identical to each other and each element is to have the same cross-sectional geometry."
  
<p align="center">
<img width="702" height="302" alt="image" src="https://github.com/user-attachments/assets/81ce9513-0628-42cc-be1e-0f92ac6e1efe" />



# Design And Process
## Initial Truss Geometry Selection
THe first thing I needed to do was decide what my truss was going to look like inlcuding number of members and joints. I started out by first dawing the geometric contrains that were given to me to better underand them. I defined my load "P" as 30KN. I chose this number because it was at the high end of the range providing aditonla load capcacity to my truss. I then resarched some popular truss deigns on the internet for some insperation. After doing so I drew out a few of design I felt could be good candidates. These genreal design had to be adapted to have the 2 points in the span for my load as well as the 2 end points (A and B). 

<p align="center">
<img width="505" height="353" alt="image" src="https://github.com/user-attachments/assets/277c5027-8157-49aa-89b8-d0dbeb875ec1" />


## Truss Type Decision
I chose Design B (Circled in the top right). Firslty this design has the fewest members. Fewer mebers means fewer components, fewer failure points, and less time calcualting loads in the members. In a real world apliations chosing a simper design can often decreace cost in both manufactuing, assembly, and design. The Secong reason I chose this design is it is symetrical. Being symetriacl means the truss can be split and only one side needs to be solved to cacualte loads on the whole truss. This once more simplifies the design as the same member design can be used on both sides saving time and cost on a manufacturing front. 

## Calulating internal forces
To solve this truss and find its internal loads I first needed to create a free body diagrm to moddel this truss design. I drew the diagram and completed all my caculation on enginering paper. I also employed the use of a stright edge to assist in mainting neat and orgainzed caluations to helpa avoid careless mistakes. 

<p align="center">
<img width="507" height="312" alt="image" src="https://github.com/user-attachments/assets/79d2ef1d-35c3-4543-8f5c-52d2a29fc5ab" />

After my moddel was created I strted by caculating the extrenal loads acting on the truss. All of my caluatiosn were done symbolicaly and numbers later pluged in per the assigment directions. This was done by deifiing my euqwlibriam equations in the X, Y, and Mo (Moment). Solving for these values allowed me solve joint B/A first as there was now only 1 unknonw remiang in the Y direction. It is likley you could have solved this truss without finding the external forces however solving for them allowed me to more easily use meathod of joints withc is my preferd way of solving trusses. 

As preciously stated I started by solving Joint B/A. Joint B and Joint A are for my porupoises the same as the truss is symmetrical and has symetrical loading therefor when a joint is refered to as Letter/Letter note the reason. To Start solving I first created another free body diagam to model the forces and members present at this joint. Second I defined what Sin(x) and Cos(x) were equevlant to for this truss. Next I created my equilibiram equations and solved for my unknowns. I repeated this process for all the joints besides joint C as solving it would only prove the truss to have a net force of 0. In hind sight I shoudl have solved joint C as it would expose any errors in my math. 

<p align="center">
<img width="446" height="576" alt="image" src="https://github.com/user-attachments/assets/09f31d69-5d45-4673-9998-d67067ef301b" />

To aid in organization I complied the Symbolic solutions for the internal forces on to a new page and defined my knonw variables once again. I then solved these equaiong by imputing the expresion in to my calculator. The magnitiude and compresion or tension of the force was then noted. I coudl have solved these equaitons by hand howver using a calculator helps prevent any careless errors. 

<p align="center">
<img width="467" height="177" alt="image" src="https://github.com/user-attachments/assets/2c467e7a-f510-4870-97c9-8d6207ca383c" />






