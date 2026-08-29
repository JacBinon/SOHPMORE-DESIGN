[Sohpmpre design A2.zip](https://github.com/user-attachments/files/31603484/Sohpmpre.design.A2.zip)
# A2 – Truss Stress Analysis

## Assignment Objectives

This assignment is meant to provide experience in applying students' engineering knowledge. This is done through designing a truss to support a load with a safety factor while navigating geometric constraints.

Objectives given include:

- Creating a planar truss following geometric constraints
- Creating free body diagrams for the truss and all joints
- Calculating the minimum cross-sectional area of all members with a safety factor
- Calculating the minimum cross-sectional area of pins with a safety factor to withstand single shear
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

The first thing I needed to do was decide what my truss was going to look like, including the number of members and joints. I started out by first drawing the geometric constraints that were given to me to better understand them. I defined my load "P" as 30 kN. I chose this number because it was at the high end of the range, providing additional load capacity to my truss. I then researched some popular truss designs on the internet for some inspiration. After doing so, I drew out a few designs I felt could be good candidates. These general designs had to be adapted to have the 2 points in the span for my load as well as the 2 end points (A and B).

<p align="center">
<img width="505" height="353" alt="image" src="https://github.com/user-attachments/assets/277c5027-8157-49aa-89b8-d0dbeb875ec1" />



## Truss Type Decision

I chose Design B (circled in the top right). Firstly, this design has the fewest members. Fewer members means fewer components, fewer failure points, and less time calculating loads in the members. In real-world applications, choosing a simpler design can often decrease cost in both manufacturing, assembly, and design. The second reason I chose this design is that it is symmetrical. Being symmetrical means the truss can be split, and only one side needs to be solved to calculate loads on the whole truss. This once more simplifies the design, as the same member design can be used on both sides, saving time and cost on the manufacturing front.

## Calculating Internal Forces

To solve this truss and find its internal loads, I first needed to create a free body diagram to model this truss design. I drew the diagram and completed all my calculations on engineering paper. I also employed the use of a straight edge to assist in maintaining neat and organized calculations to help avoid careless mistakes.

<p align="center">
<img width="507" height="312" alt="image" src="https://github.com/user-attachments/assets/79d2ef1d-35c3-4543-8f5c-52d2a29fc5ab" />



After my model was created, I started by calculating the external loads acting on the truss. All of my calculations were done symbolically, and numbers were later plugged in per the assignment directions. This was done by defining my equilibrium equations in the X, Y, and Mo (moment) directions. Solving for these values allowed me to solve Joint B/A first, as there was now only 1 unknown remaining in the Y direction. It is likely that I could have solved this truss without finding the external forces; however, solving for them allowed me to more easily use the method of joints, which is my preferred way of solving trusses.

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



The assignment instructed me to use A500 Steel. Before I solved using that number, I wanted to ensure that my CAD system had this material defined. Unfortunately, SolidWorks did not. I substituted A500 with ASTM A36. This is another construction-grade steel with a lower yield strength. I chose a metal with a lower yield strength to ensure that if this truss was constructed with the A500 material, it would be stronger than designed, ensuring it would withstand the defined load. I used the properties defined by SolidWorks for my calculations and used the greatest internal force found during my previous calculations. I calculated that a minimum cross-sectional area of 437.5 mm^2 would be required.

## Pin Calculations

The next step in designing this truss is to calculate the shear loads of the pins that hold the members together. This shear loading can then be used to calculate the minimum cross-sectional area of the pins with a safety factor. Once more, this required finding an expression that combined the known values and left the area value as an unknown. The expression I derived is located in the picture below.

<p align="center">
<img width="466" height="260" alt="image" src="https://github.com/user-attachments/assets/da6f1fa3-a6f9-443c-8128-3569aba0eda5" />



Once the expression was created, I solved for the area using the safety factor of 4 and the shear strength provided in the assignment instructions. The shear strength and density values provided in the assignment directions were given in imperial units. I converted these values to metric units to maintain a cohesive unit system across my calculations. I used the value of 50 kN for my maximum shear force, as this was the largest force acting on any pin. This could be found at Pin A and Pin B. Completing these calculations gave me a value of 170.63 mm^2 that would be needed to safely support this truss. This value was then converted from an area value to a diameter value. The next step was to estimate the weight of all the pins in this truss. In order to get the pin lengths, I assumed that my truss members would be squares and the pin would need to be double the width of the truss members to fully connect. This was then used to find the volume and, therefore, weight of one pin. Multiplying this value by 5 gave a weight of 274.6 g for all 5 pins in the truss.

## Approximate Truss Weight

To approximate the weight of the truss, I first wanted to create an expression for the total amount of material in the truss. I came to the realization that this was simply the length of all the members added up and then multiplied by the cross-sectional area. I then redrew the truss to assign lengths to each member and to ensure I didn't forget a member. I used trigonometry to assign lengths to the diagonal members. Horizontal and vertical members could have their lengths taken from the given overall dimensions. I then summed these lengths, converted them to mm, and then multiplied by the cross-sectional area previously calculated to get the volume in cubic millimeters. The density of ASTM A36 was taken from SolidWorks and converted to grams per mm cubed by multiplying it by 10^-6. This was then multiplied by the volume to get an estimated mass without pins of 11402.125 g. The calculations can be seen in the image below. Adding the weight of the pins, this brings the weight of the truss to 11676.725 g.

<p align="center">
<img width="707" height="599" alt="image" src="https://github.com/user-attachments/assets/c391ba39-8f5b-4e9c-aa4c-b4cff7d9f431" />



## CAD Model

The last part of this assignment is to create a CAD model of the truss. As instructed, I modeled the whole truss as one component. The pins were then added in the assembly. In an effort to get a more accurate weight of the entire bridge, I increased the thickness at the intersections by the thickness of the truss multiplied by the number of members attaching at that point. The same was done for the pins. I did this because, in order to have a pin connection, there will be an overlap of material where each member has the "hoop" that the pin contacts. Additionally, around the hole for the pins, I used the offset tool to widen the surrounding area at an offset factor of 1/2 the width of the truss. This ensures that there is a consistent cross-sectional area even at the intersection point of the pin. If I were to build this bridge, I would want to create a more accurate model of this truss, including individual components for each member, accurate models of the pin joints, and proper tolerances for the pins. Below are images of the CAD model.

<p align="center">
<img width="1138" height="482" alt="image" src="https://github.com/user-attachments/assets/6b9c27c3-fe21-4080-88c9-f1c02bb848ac" />



<p align="center">
<img width="920" height="618" alt="image" src="https://github.com/user-attachments/assets/ed7e0247-deac-435a-9817-4200e2534139" />



<p align="center">
<img width="1917" height="1033" alt="image" src="https://github.com/user-attachments/assets/ee911e63-5e1f-4cf8-8cea-dbf565757500" />



As seen in the above image, the estimated weight of the entire assembly is 12867.77 g. This comes out to approximately a 9 percent difference. I attribute this difference mostly to my CAD model accounting for the extra material required for the pin connections and the longer pins. I came to the realization that representing the weight in grams may not be the proper unit to use, as grams are a unit of mass. Converting these units to newtons would be more accurate and would make it simpler to account for the weight of the truss itself in the load calculations. This is something I need to ensure I pay attention to in the future. Fortunately, the load on the truss was given in the correct unit; otherwise, a complete recalculation would be needed.

Below is a download link to the cad assembly:
https://github.com/JacBinon/SOHPMORE-DESIGN/blob/main/docs/assignments/A02/Sohpmpre%20design%20A2.zip

## Engineering Lessons

This assignment was a beneficial exercise in taking a design from start to finish. I had never applied yield strength and shear stress calculations throughout an entire design problem like this before, so it gave me a better understanding of how these calculations influence a design. Additionally, this exercise emphasized the advice from previous professors to keep an organized page and consistently double-check your work. A single mistake, such as using incorrect units or entering the wrong value into an equation, can derail an entire problem and lead to an inaccurate final design.

Overall, this assignment helped reinforce the importance of accuracy, organization, and careful verification in engineering. It also showed me that completing the calculations is only one part of the design process; being able to clearly document and defend the decisions made throughout the process is equally important. I learned how making too broad of assumptions can have profound impacts on your calculated values. The biggest example of this was when I just assumed the truss members were square without accounting for the holes the pins make or the overlap of material at the pin joints.

##Failure Modes of Truss Members

In this truss, we have three unique members that have forces on them: BD/AE, BC/CA, and DE. The members BD/AE and DE are both in tension. Members BC/CA are in compression. The members DC/CE are zero-force members and therefore will not be discussed in this section.

- Tension Members
  Members BD/AE are in tension. Because they are made of a low-carbon ASTM A36 steel, they will yield a large amount before fracturing. This steel has a low carbon content and will be in a soft, ductile state in a truss structure. If these members were made of a high-carbon steel and hardened, they would be more likely to fracture rather than undergo significant deformation. This failure mode is described almost verbatim on Baling Steel's webpage (https://baling-steel.com/a36-steel-composition/): "The modest percentage keeps the alloy soft enough to bend, hammer, or machine without expensive preparation. Because brittleness is all but ruled out, the plate absorbs fatigue and still stretches a bit before it finally breaks." To prevent this failure, the members in tension could be replaced by cables or another material that is better suited for tensile loading. Alternatively, increasing the safety factor would also decrease the chances of this failure occurring.

- Compression Members
  Members BC/CA are in compression. This means these members are governed by Euler's buckling equations and therefore will fail by buckling. These members' strength in compression and, ultimately, the point at which they will fail are affected by their geometry. An effective way to decrease the likelihood of buckling is to construct these members with a favorable geometry. A thin, wide member will fail before a more proportional, square-shaped member. Think about trying to support an object with a piece of paper standing on its edge as opposed to rolling that paper into a cylinder. I referenced the following webpage for this information: https://ficientdesign.com/column-buckling-euler-critical-load-effective-length/
  
## Failure Modes of Pins 

The pins in this design will fail in shear. This is because the forces from the truss members act on the pins and create a shear force across the pins. Since the members are connected to the pins, the applied loads are transferred through the pins at the joints. If the shear stress in the pin exceeds the allowable shear stress of the material, the pin will begin to fail. According to the Machinery's Handbook, page 211, when calculating shear, a pin in single shear will fail at half the load of a pin in double shear. A simple way to decrease the likelihood of a failure of the pin is to place it in double shear instead of the single shear configuration that I modeled this truss with. The page also contains a diagram explaining what a shear load looks like, which depicts the exact loading case of the pins in question, further reinforcing that the pins will fail in shear. It is possible that the material containing the pin could fail before the pin shears. Further analysis of the truss geometry, materials, and construction would be needed to determine which would fail first.

## Time Spent
I started a stopwatch each time I started working on this assignment and spent approximately 5:30 on this assignment. 
